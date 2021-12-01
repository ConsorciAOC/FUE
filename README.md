# Servei FUE Local
## Integració del catàleg de tràmits d’un ens amb solució pròpia cap a FUE (portal Canal Empresa)


FUE Local - Integració del catàleg de tràmits

# 1. Introducció

L’objectiu d’aquest document és descriure la implementació del mecanisme simplificat que permetrà distribuir el catàleg de tràmits d’un organisme cap a l’AOC i aquest cap a la Finestreta Única Empresarial (FUE) impulsada a Catalunya per la Oficina de Gestió Empresarial (OGE).

# 2. Implementació

La implementació que haureu de realitzar consisteix en la **publicació d’un fitxer XML estàtic a un servidor web** (Apache, IIS, etc...) que haurà de simular la resposta que s’obtindria des de un Web Service.

D’aquesta manera s’aconsegueix evitar tota tasca de programació i el manteniment 
únicament consistirà en modificar aquest fitxer estàtic per quan escaigui per mantenir les dades i informacions al dia. 

![1](captures/1.png)

## 2.1 Format del fitxer

A continuació es mostra el format que ha de tenir el fitxer XML a publicar al servidor web.

![2](captures/2.png)

La part d’XML en color verd correspon a la part del fitxer necessària que des de l’AOC utilitzem per a simular la resposta que donaria el nostre servei web intern, és una part fixa i no s’ha de modificar.

La part d’XML en color beige correspon a les dades del catàleg que cal personalitzar per cadascun dels tràmits i només està a mode d’exemple.

## 2.2 Relacions a incorporar a l’XML

A continuació es mostra l’equivalència i codificació dels diferents tràmits d’activitats per a què un ens amb solució de tramitació pròpia (que no sigui e-TRAM) pugui exposar el seu catàleg de tràmits a Canal Empresa, via el Consorci AOC.

### 2.2.1 Codificació dels tràmits potencials a incloure (node *fitxa XML*)

| **nomTramit** | **codiTramit** |
| --- | --- |
| Declaració responsable d&#39;oobertura | 8b4480882a1a497eea49a3d75f678323a |
| --- | --- |
| Comunicació prèvia d&#39;obertura | acbb09265b434fa779d0bc41124d2e400 |
| --- | --- |
| Comunicació prèvia ambiental municipal (Annex III) | dd0bdc022d1448d6687dde442c374efa4 |
| --- | --- |
| Llicència ambiental | 8372cb9e38c648f99ed1ccf1b16cf0c9 |
| --- | --- |
| Consulta prèvia de classificació de l&#39;activitat | a1094dd3554f410aaa0bae5fc7b0e4211 |
| --- | --- |
| Sol·licitud informe urbanístic associat a la tramitació | 1e9eeea3f3d142fabb12f0b2e3c8dc439 |
| --- | --- |
| d&#39;activitats |
 |
| Sol·licitud informe previ en matèria d&#39;incendis | 64b288428f6f46589947633dae04c3315 |
| --- | --- |
| Llicència per a espectaacles públics o activitats | 2c17d26b3f6549966b96b88c6129d082c |
| --- | --- |
| recreatives de caràcter extraordinari |
 |
| Comunicació prèvia d&#39;esstabliments no permanents | 125a702426264b300b7e6782ca8eed8f5 |
| --- | --- |
| desmuntables. |
 |
| Llicència municipal d&#39;estabbliments oberts al públic de | 4af40d89b08e471cc83035ca390158da8 |
| --- | --- |
| règim especial |
 |
| Comunicació prèvia d&#39;esstabliments fixos oberts al | aee81c1164374d355a3d7eedee8aca74f |
| --- | --- |
| públic d&#39;espectacles públiccs i activitats recreativ es |
 |
| ordinàries |
 |
| Llicència d&#39;establiments fixos oberts al públic | c349792547bf41d22a297073dfe8c05aa |
| --- | --- |

![](RackMultipart20211201-4-asf0r_html_e723e12813a5b5f0.gif) ![](RackMultipart20211201-4-asf0r_html_a3b96545f81d19ae.gif) ![](RackMultipart20211201-4-asf0r_html_e37606e6f7af4459.gif)

29/10/2015

![](RackMultipart20211201-4-asf0r_html_24552053b683ac41.gif) ![](RackMultipart20211201-4-asf0r_html_e7147a6d84cf436.gif)

FUE Local - Integració deel catàleg de tràmits

pàg 6/9

![](RackMultipart20211201-4-asf0r_html_a3a00f0ab5648d2a.gif) ![](RackMultipart20211201-4-asf0r_html_5dd11405cac18881.gif)

| d&#39;espectacles públics i activiitats recreatives ordi nàries |
 |
| --- | --- |
| Comunicació prèvia de modificació no substancia | f9b54450001d45b118bd608cab4a7551e |
| --- | --- |
| d&#39;una activitat amb efectes sobre les persones o el |
 |
| medi ambient |
 |
| Comunicació prèvia de moodificació no substancial d&#39;un | 672098d0ba4b41d0099d964c3eb486e40 |
| --- | --- |
| establiment i/o un espectacle o activitat recreativa |
 |
| Comunicació de transmissiió de llicència o dels efectes | ea8b8e37542e45033a3cbcf02496cf656 |
| --- | --- |
| d&#39;una comunicació prèvia |
 |
| Comunicació prèvia per a espectacles públics o | d41e3fc656e046fc99a3beb8390ce2df2 |
| --- | --- |
| activitats recreatives de caràcter extraordinari. |
 |
| Declaració responsable en matèria de salut alimentària | fe19dd38e1bc4a6aaaffbd8d654560c6f |
| --- | --- |

**2.2.2 Codificació de les seccions dels tràmits**** (node **_** seeccions XML **_** )**

| **nomSeccio** | **numIntSecccio** |
| --- | --- |
| Nom del tràmit | 3bc4204ddd414b29bb4350ada0854471 |
| Descripció | 5e09344b1cf64f7dadfcadbeef394b5e3 |
| Organisme competent / Reesponsable | d614d4b400c011e28ecd8b33e6188709b |
| Àrea que tramita | bef66d94f66541aaa9776d9307952853 |
| Classificació temàtica | 52e27c3b4d1946e6bdf3acbbd27453cde |
| Qui el pot demanar | 308e7a939a9b4c64a5f78f470b9d00bb |
| Canals de tramitació | ca07068df2504e97ac0f063ff7df455c7 |
| Període de l&#39;any en què ess pot demanar | 132b640120834580925665035590a2dd |
| Termini de la sol·licitud | 706f3e092522497184486855a1974f591 |
| Requisits previs | 456c15b8be8745a29086deb728561506 |
| Preu | cddf6a3371a6472281b33a005e0f584ef |
| Mitjans de pagament | 38a7df6244054c39aa049c99177f4d793 |
| Documentació a aportar | 8c8e9b4bc5a047509bf1c5ddade99a4fd |
| Impresos del tràmit | e9c41b04682b448d936ec9339222c9d9f |
| Normativa | d9577ab1cfa74465832a8022aade43a09 |
| Termini de resolució | c4172b500a474810b260f3cca736ed467 |
| Silenci administratiu | 39582558b476466bb83949698846f051 |
| Vies de reclamació | 68f0e84f063243f0bba247f6e1802a0d |
| Tràmits associats | 478f91f9140d47d490610f5118c55448e |

![](RackMultipart20211201-4-asf0r_html_e723e12813a5b5f0.gif) ![](RackMultipart20211201-4-asf0r_html_a3b96545f81d19ae.gif) ![](RackMultipart20211201-4-asf0r_html_e37606e6f7af4459.gif)

29/10/2015

![](RackMultipart20211201-4-asf0r_html_24552053b683ac41.gif) ![](RackMultipart20211201-4-asf0r_html_e7147a6d84cf436.gif)

FUE Local - Integració deel catàleg de tràmits

pàg 7/9

![](RackMultipart20211201-4-asf0r_html_a3a00f0ab5648d2a.gif) ![](RackMultipart20211201-4-asf0r_html_5dd11405cac18881.gif)

| Altra informació d&#39;interès | 461f7c55290c47fd9046e8744ff24015c |
| --- | --- |
| Normativa reguladora del silenci | b02f2f76396c47dd9d5d20f00e6c15e36 |
| --- | --- |
| administratiu |
 |
| Codificació del tràmit | e443b3ea426e4ef9bbeba3663019846e7 |
| --- | --- |
| Darrera actualització | ac37806b741241f6b6faeddf2296465b |
| --- | --- |
| Paraules claus de cerca | 6a3712d100a44a509a7a2b8b4eb040d5 |
| --- | --- |
| Procediment vinculat | 0d1b8d20a01243ae91359281a7f9a1dd |
| --- | --- |
| Peticions més comunes | 76bb9503c9854bf197bd73f143bb840b |
| --- | --- |
| Observacions internes | cd2e4d04f2fd4225870fed8fc9884713 |
| --- | --- |
| Passos a seguir per tramitació | 96c36afbe01048efb7efaa133f3fb9ff2 |
| --- | --- |

L&#39;XML no requereix infoormar obligatòriament totes les seccions anteriors, però per coherència amb la informmació es requerirà, com a mínim, mantenir el mateix nom a la secció, i informar obligatòriament les que estan **en verd** a la taula anterior.

![](RackMultipart20211201-4-asf0r_html_e723e12813a5b5f0.gif) ![](RackMultipart20211201-4-asf0r_html_a3b96545f81d19ae.gif) ![](RackMultipart20211201-4-asf0r_html_e37606e6f7af4459.gif)

29/10/2015

![](RackMultipart20211201-4-asf0r_html_24552053b683ac41.gif) ![](RackMultipart20211201-4-asf0r_html_e7147a6d84cf436.gif)

FUE Local - Integració deel catàleg de tràmits

pàg 8/9

![](RackMultipart20211201-4-asf0r_html_a3a00f0ab5648d2a.gif) ![](RackMultipart20211201-4-asf0r_html_5dd11405cac18881.gif)

**3. Definició dels camps per a preparaar l&#39;XML**

A continuació es mostra la descripció corresponent a cada camp del XML estàtic presentat pel vostre servei.

![](RackMultipart20211201-4-asf0r_html_ad71ebb38f556931.gif) ![](RackMultipart20211201-4-asf0r_html_af3112b1f248d562.gif)

**fitxa**

![](RackMultipart20211201-4-asf0r_html_3ef5aa24a5e2ad0.gif) ![](RackMultipart20211201-4-asf0r_html_b6e5b83bc52db1c7.gif) ![](RackMultipart20211201-4-asf0r_html_c0874d0d453f52b4.gif) ![](RackMultipart20211201-4-asf0r_html_3f8ba1577c71f7fe.gif) ![](RackMultipart20211201-4-asf0r_html_d728a0fbc2d17168.gif) ![](RackMultipart20211201-4-asf0r_html_9b59fac41c8932b5.gif) ![](RackMultipart20211201-4-asf0r_html_4b87ef604c3b99f0.gif) ![](RackMultipart20211201-4-asf0r_html_8db35431c739b330.gif) ![](RackMultipart20211201-4-asf0r_html_5b1158a29d1415f.gif) ![](RackMultipart20211201-4-asf0r_html_9cab79f602790b12.gif) ![](RackMultipart20211201-4-asf0r_html_a17c909e26159fc6.gif)

**Camp**** Tipuus ****Obligatori**** Descripció**

![](RackMultipart20211201-4-asf0r_html_a3c94fb355486b9b.gif) ![](RackMultipart20211201-4-asf0r_html_eb63802d5977f319.gif) ![](RackMultipart20211201-4-asf0r_html_38d92a042dda26f.gif) ![](RackMultipart20211201-4-asf0r_html_9aff138f8cd397cc.gif) ![](RackMultipart20211201-4-asf0r_html_33e2965c3e6ad24b.gif) ![](RackMultipart20211201-4-asf0r_html_7d64ce4f6131905.gif) ![](RackMultipart20211201-4-asf0r_html_306793993b692596.gif) ![](RackMultipart20211201-4-asf0r_html_f26b6d209961e079.gif) ![](RackMultipart20211201-4-asf0r_html_1ea0d5552d460f38.gif) ![](RackMultipart20211201-4-asf0r_html_be0440d06bb719ab.gif) ![](RackMultipart20211201-4-asf0r_html_594aa35581daf798.gif) ![](RackMultipart20211201-4-asf0r_html_6b25c6d87bb0a879.gif)

| codiTramit | Textt(32) | Si |
| --- | --- | --- |
| nomTramit | Textt(500) | Si |
| esTelematic | Boolleà | Si |

![](RackMultipart20211201-4-asf0r_html_9974ed8f57a63a18.gif) ![](RackMultipart20211201-4-asf0r_html_4d1e5fb7a40e05ea.gif) ![](RackMultipart20211201-4-asf0r_html_eb63802d5977f319.gif) ![](RackMultipart20211201-4-asf0r_html_571e840711bea240.gif) ![](RackMultipart20211201-4-asf0r_html_9aff138f8cd397cc.gif) ![](RackMultipart20211201-4-asf0r_html_4d1e5fb7a40e05ea.gif) ![](RackMultipart20211201-4-asf0r_html_eb63802d5977f319.gif) ![](RackMultipart20211201-4-asf0r_html_ab99a783a3b7c8e2.gif) ![](RackMultipart20211201-4-asf0r_html_9aff138f8cd397cc.gif) ![](RackMultipart20211201-4-asf0r_html_8483e5f60263f878.gif) ![](RackMultipart20211201-4-asf0r_html_f753a5c5b2cdc7de.gif) ![](RackMultipart20211201-4-asf0r_html_628381f95a9eb6cd.gif) ![](RackMultipart20211201-4-asf0r_html_88da542a60fa3247.gif) ![](RackMultipart20211201-4-asf0r_html_7d64ce4f6131905.gif) ![](RackMultipart20211201-4-asf0r_html_9d47354701843aae.gif) ![](RackMultipart20211201-4-asf0r_html_f26b6d209961e079.gif) ![](RackMultipart20211201-4-asf0r_html_ee62fe7afed11f05.gif) ![](RackMultipart20211201-4-asf0r_html_7d64ce4f6131905.gif) ![](RackMultipart20211201-4-asf0r_html_9d47354701843aae.gif) ![](RackMultipart20211201-4-asf0r_html_f26b6d209961e079.gif)

URLTramitAssociat Textt(8000) Si

![](RackMultipart20211201-4-asf0r_html_a3c94fb355486b9b.gif) ![](RackMultipart20211201-4-asf0r_html_eb63802d5977f319.gif) ![](RackMultipart20211201-4-asf0r_html_38d92a042dda26f.gif) ![](RackMultipart20211201-4-asf0r_html_9aff138f8cd397cc.gif) ![](RackMultipart20211201-4-asf0r_html_33e2965c3e6ad24b.gif) ![](RackMultipart20211201-4-asf0r_html_7d64ce4f6131905.gif) ![](RackMultipart20211201-4-asf0r_html_306793993b692596.gif) ![](RackMultipart20211201-4-asf0r_html_f26b6d209961e079.gif)

categoriaTextt(100)No

![](RackMultipart20211201-4-asf0r_html_a3c94fb355486b9b.gif) ![](RackMultipart20211201-4-asf0r_html_eb63802d5977f319.gif) ![](RackMultipart20211201-4-asf0r_html_38d92a042dda26f.gif) ![](RackMultipart20211201-4-asf0r_html_9aff138f8cd397cc.gif) ![](RackMultipart20211201-4-asf0r_html_33e2965c3e6ad24b.gif) ![](RackMultipart20211201-4-asf0r_html_7d64ce4f6131905.gif) ![](RackMultipart20211201-4-asf0r_html_306793993b692596.gif) ![](RackMultipart20211201-4-asf0r_html_f26b6d209961e079.gif)

seccionsTipuusSeccio Si

Número intern del tràmit (IT) . Codi de 32 caràcters alfanumèrics.

![](RackMultipart20211201-4-asf0r_html_92f51fdde9d1b997.gif) ![](RackMultipart20211201-4-asf0r_html_8f22bd63baaa386e.gif)

Nom concret del tràmit (IT) ![](RackMultipart20211201-4-asf0r_html_a4c06c635fa6c6d8.png)

![](RackMultipart20211201-4-asf0r_html_5372ef4da6a4ea48.gif) ![](RackMultipart20211201-4-asf0r_html_8ce2fd7c5f0a7d5e.gif) ![](RackMultipart20211201-4-asf0r_html_f54350a799e2c89a.gif) ![](RackMultipart20211201-4-asf0r_html_6b25c6d87bb0a879.gif)

Indica si la fitxa permet trammitació telemática

![](RackMultipart20211201-4-asf0r_html_5372ef4da6a4ea48.gif) ![](RackMultipart20211201-4-asf0r_html_8ce2fd7c5f0a7d5e.gif) ![](RackMultipart20211201-4-asf0r_html_5136ef60d98b5487.gif) ![](RackMultipart20211201-4-asf0r_html_6b25c6d87bb0a879.gif)

Link cap el tràmit associat a la fitxa (IT)

![](RackMultipart20211201-4-asf0r_html_1ea0d5552d460f38.gif) ![](RackMultipart20211201-4-asf0r_html_be0440d06bb719ab.gif) ![](RackMultipart20211201-4-asf0r_html_594aa35581daf798.gif)

Àmbit de la IT (Atenció a la ciutadania, Padró Habitants, Via Públicca, etc.)

![](RackMultipart20211201-4-asf0r_html_1ea0d5552d460f38.gif) ![](RackMultipart20211201-4-asf0r_html_be0440d06bb719ab.gif) ![](RackMultipart20211201-4-asf0r_html_594aa35581daf798.gif)

Tipus complex amb la llistta de seccions de la fitxa i els seus contingutss

![](RackMultipart20211201-4-asf0r_html_ad71ebb38f556931.gif) ![](RackMultipart20211201-4-asf0r_html_af3112b1f248d562.gif)

**seccions**

![](RackMultipart20211201-4-asf0r_html_d825fd994bd0c7c3.gif) ![](RackMultipart20211201-4-asf0r_html_99569378fc6d08b6.gif) ![](RackMultipart20211201-4-asf0r_html_7718ebc99e8d5dd5.gif) ![](RackMultipart20211201-4-asf0r_html_31d99d30b3e52489.gif) ![](RackMultipart20211201-4-asf0r_html_d17d09ebbd9888a4.gif) ![](RackMultipart20211201-4-asf0r_html_5eaa8bd0cbd020c0.gif) ![](RackMultipart20211201-4-asf0r_html_91197b0d701f57ba.gif) ![](RackMultipart20211201-4-asf0r_html_c0dffe287b69ae4e.gif) ![](RackMultipart20211201-4-asf0r_html_f3b78c1ffdd36db8.gif) ![](RackMultipart20211201-4-asf0r_html_9cab79f602790b12.gif) ![](RackMultipart20211201-4-asf0r_html_ddb8b487be9ef748.gif)

**Camp**** Tipuss ****Obligatori**** Descripció**

![](RackMultipart20211201-4-asf0r_html_c62e1e58598a6071.gif) ![](RackMultipart20211201-4-asf0r_html_51ba5bd1cdd6b86.gif) ![](RackMultipart20211201-4-asf0r_html_55625c202f10dbe9.gif) ![](RackMultipart20211201-4-asf0r_html_ec758be2d3e70601.gif) ![](RackMultipart20211201-4-asf0r_html_e7dae118638ecfa2.gif) ![](RackMultipart20211201-4-asf0r_html_8aaa0f31dd87a75a.gif) ![](RackMultipart20211201-4-asf0r_html_f5e769c2b32f476c.gif) ![](RackMultipart20211201-4-asf0r_html_97fccd69e44ea43a.gif) ![](RackMultipart20211201-4-asf0r_html_38f7cddd636311d7.gif) ![](RackMultipart20211201-4-asf0r_html_bf3919303c08d928.gif) ![](RackMultipart20211201-4-asf0r_html_594aa35581daf798.gif) ![](RackMultipart20211201-4-asf0r_html_6b25c6d87bb0a879.gif)

| numIntSeccio | Text(32) | Si |
| --- | --- | --- |
| nomSeccio | Text(256) | Si |
| idioma | idiomma | Si |
| contingutSeccio | Text(8000) | Si |

![](RackMultipart20211201-4-asf0r_html_e723e12813a5b5f0.gif) ![](RackMultipart20211201-4-asf0r_html_2ab102c1b4202060.gif) ![](RackMultipart20211201-4-asf0r_html_e74b9bb6363a816c.gif) ![](RackMultipart20211201-4-asf0r_html_51ba5bd1cdd6b86.gif) ![](RackMultipart20211201-4-asf0r_html_c62e1e58598a6071.gif) ![](RackMultipart20211201-4-asf0r_html_51ba5bd1cdd6b86.gif) ![](RackMultipart20211201-4-asf0r_html_f5e769c2b32f476c.gif) ![](RackMultipart20211201-4-asf0r_html_cc52027c21687ae0.gif) ![](RackMultipart20211201-4-asf0r_html_63e61996846c53fd.gif) ![](RackMultipart20211201-4-asf0r_html_e7ce54c8e831f8de.gif) ![](RackMultipart20211201-4-asf0r_html_80a4d4d18e316b6a.gif) ![](RackMultipart20211201-4-asf0r_html_ec758be2d3e70601.gif) ![](RackMultipart20211201-4-asf0r_html_53e485e7b9a38d52.gif) ![](RackMultipart20211201-4-asf0r_html_97fccd69e44ea43a.gif) ![](RackMultipart20211201-4-asf0r_html_a52b69779aefdb66.gif) ![](RackMultipart20211201-4-asf0r_html_bf3919303c08d928.gif) ![](RackMultipart20211201-4-asf0r_html_38f7cddd636311d7.gif) ![](RackMultipart20211201-4-asf0r_html_55625c202f10dbe9.gif) ![](RackMultipart20211201-4-asf0r_html_ec758be2d3e70601.gif)

Número inte rn de la secció (codi de 32 caràcters alfanumèrics).

![](RackMultipart20211201-4-asf0r_html_df30920334b079d8.gif) ![](RackMultipart20211201-4-asf0r_html_7acb41245253b2c0.gif)

Nom de la secció

![](RackMultipart20211201-4-asf0r_html_63e96a0052d1becd.gif) ![](RackMultipart20211201-4-asf0r_html_8aaa0f31dd87a75a.gif) ![](RackMultipart20211201-4-asf0r_html_fb46af308f152e31.gif) ![](RackMultipart20211201-4-asf0r_html_31ae1b1716351b62.gif) ![](RackMultipart20211201-4-asf0r_html_4bad827137c2b3c7.gif) ![](RackMultipart20211201-4-asf0r_html_4bad827137c2b3c7.gif) ![](RackMultipart20211201-4-asf0r_html_8aaa0f31dd87a75a.gif) ![](RackMultipart20211201-4-asf0r_html_c3f0969ec1bc838f.gif) ![](RackMultipart20211201-4-asf0r_html_6b25c6d87bb0a879.gif) ![](RackMultipart20211201-4-asf0r_html_df30920334b079d8.gif) ![](RackMultipart20211201-4-asf0r_html_47b3ff13adcabd23.gif) ![](RackMultipart20211201-4-asf0r_html_7e91e9e0e0be4017.gif)

Idioma del contingut de la secció.

![](RackMultipart20211201-4-asf0r_html_ebcc2f3eabd67da6.gif) ![](RackMultipart20211201-4-asf0r_html_e32f60ae9e15e4a8.gif) ![](RackMultipart20211201-4-asf0r_html_e32f60ae9e15e4a8.gif)

Catalàca\_ES

Castellàes\_ES

Aranèsoc\_ES

![](RackMultipart20211201-4-asf0r_html_a2dfb1176ed935f9.gif)

- Complir amb aquests valors respectant majúscules i minúscules i subguió Contingut de la secció

![](RackMultipart20211201-4-asf0r_html_a3b96545f81d19ae.gif) ![](RackMultipart20211201-4-asf0r_html_e37606e6f7af4459.gif) ![](RackMultipart20211201-4-asf0r_html_60da35a571d55c9b.gif) ![](RackMultipart20211201-4-asf0r_html_df30920334b079d8.gif)

29/10/2015

![](RackMultipart20211201-4-asf0r_html_24552053b683ac41.gif) ![](RackMultipart20211201-4-asf0r_html_e7147a6d84cf436.gif)

FUE Local - Integració deel catàleg de tràmits

pàg 9/9

![](RackMultipart20211201-4-asf0r_html_a3a00f0ab5648d2a.gif) ![](RackMultipart20211201-4-asf0r_html_5dd11405cac18881.gif)

**4. Fitxer estàtic d&#39;exemple**

\&lt;?xml version=&#39;1.0&#39; encoding=&#39;UUTF-8&#39;?\&gt;

\&lt;S:Envelope xmlns:S=&quot;http://schemas.xmlsoap.org/soap/envelope/&quot;\&gt;

\&lt;S:Body\&gt;

\&lt;ns4:transmissioResponse xmlnns=&quot;http://cat.aoc/etramsge/gateway/peticio&quot;

xmlns:ns2=&quot;http://cat.aoc/etrammsge/gateway/resposta&quot;

xmlns:ns3=&quot;http://cat.aoc/etrammsge/adapter/resposta&quot; xmlns:ns4=&quot;http://cat.aoc/etramssge/gateway/ops/&quot;

xmlns:ns5=&quot;http://cat.aoc/etrammsge/adapter/peticio&quot;\&gt;

\&lt;ns2:consultarCatalegResult\&gt;

\&lt;ns2:correcte\&gt;true\&lt;/ns2:correcte\&gt;

\&lt;ns2:missatgeError\&gt;OK\&lt;/ns2:missatgeError\&gt;

\&lt;ns2:ensPropietari\&gt;99999999999\&lt;/ns2:ensPropietari\&gt;

\&lt;ns2:dadesCataleg\&gt;

\&lt;ns2:fitxa\&gt;

\&lt;ns2:codiTramit\&gt;0123456789\&lt;/ns2:codiTramit\&gt;

\&lt;ns2:nomTramit\&gt;Tràmit 1\&lt;/ns2:nomTramit\&gt;

\&lt;ns2:esTelematic\&gt;true\&lt;/ns2:esTelematic\&gt;

\&lt;ns2:URLTramitAssociat\&gt;http://www.aoc.cat\&lt;/ns2:URLTrammitAssociat\&gt;

\&lt;ns2:categoria\&gt;Categoria\&lt;/ns2:categoria\&gt;

\&lt;ns2:seccions\&gt;

\&lt;ns2:seccio\&gt;

\&lt;ns2:numIntSeccio\&gt;00000000000001A\&lt;/ns2:numIntSeccio\&gt;

\&lt;ns2:nomSeccio\&gt;Secció 1\&lt;/ns2:nomSeccio\&gt;

\&lt;ns2:idioma\&gt;ca\_ES\&lt;/ns2:idioma\&gt;

\&lt;ns2:contingutSeccio\&gt;....\&lt;/ns2:contingutSeeccio\&gt;

\&lt;/ns2:seccio\&gt;

\&lt;ns2:seccio\&gt;

\&lt;ns2:numIntSeccio\&gt;00000000000001A\&lt;/ns2:numIntSeccio\&gt;

\&lt;ns2:nomSeccio\&gt;Secció 1\&lt;/ns2:nomSeccio\&gt;

\&lt;ns2:idioma\&gt;es\_ES\&lt;/ns2:idioma\&gt;

\&lt;ns2:contingutSeccio\&gt;.....\&lt;/ns2:contingutSeccio\&gt;

\&lt;/ns2:seccio\&gt;

\&lt;/ns2:seccions\&gt;

\&lt;/ns2:fitxa\&gt;

\&lt;ns2:fitxa\&gt;

\&lt;ns2:codiTramit\&gt;0ABCDEF1234\&lt;/ns2:codiTramit\&gt;

\&lt;ns2:nomTramit\&gt;Tràmit 2\&lt;/ns2:nomTramit\&gt;

\&lt;ns2:esTelematic\&gt;true\&lt;/ns2:esTelematic\&gt;

\&lt;ns2:URLTramitAssociat\&gt;http://www.aoc.cat\&lt;/ns2:URLTrammitAssociat\&gt;

\&lt;ns2:categoria\&gt;Categoria\&lt;/ns2:categoria\&gt;

\&lt;ns2:seccions\&gt;

\&lt;ns2:seccio\&gt;

\&lt;ns2:numIntSeccio\&gt;00000000000002A\&lt;/ns2:numIntSeccio\&gt;

\&lt;ns2:nomSeccio\&gt;Secció 2\&lt;/ns2:nomSeccio\&gt;

\&lt;ns2:idioma\&gt;ca\_ES\&lt;/ns2:idioma\&gt;

\&lt;ns2:contingutSeccio\&gt;....\&lt;/ns2:contingutSeeccio\&gt;

\&lt;/ns2:seccio\&gt;

\&lt;ns2:seccio\&gt;

\&lt;ns2:numIntSeccio\&gt;00000000000002A\&lt;/ns2:numIntSeccio\&gt;

\&lt;ns2:nomSeccio\&gt;Secció 2\&lt;/ns2:nomSeccio\&gt;

\&lt;ns2:idioma\&gt;es\_ES\&lt;/ns2:idioma\&gt;

\&lt;ns2:contingutSeccio\&gt;....\&lt;/ns2:contingutSeeccio\&gt;

\&lt;/ns2:seccio\&gt;

\&lt;/ns2:seccions\&gt;

\&lt;/ns2:fitxa\&gt;

\&lt;/ns2:dadesCataleg\&gt;

\&lt;ns2:idioma\&gt;ca\_ES\&lt;/ns2:idioma\&gt;

\&lt;/ns2:consultarCatalegResult\&gt;

\&lt;/ns4:transmissioResponse\&gt;

\&lt;/S:Body\&gt;

\&lt;/S:Envelope\&gt;

![](RackMultipart20211201-4-asf0r_html_e723e12813a5b5f0.gif) ![](RackMultipart20211201-4-asf0r_html_a3b96545f81d19ae.gif) ![](RackMultipart20211201-4-asf0r_html_e37606e6f7af4459.gif)

29/10/2015