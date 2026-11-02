# Pilote d'équipements Omron

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Ce pilote permet aux IHM de la série HM de lire et d'écrire les données ou l'état des registres des automates SYSMAC C/CPM/CS/CJ. La liaison série est établie entre le port série de l'écran tactile et celui de l'automate SYSMAC. Avant d'utiliser ce pilote, lisez attentivement ce chapitre et les spécifications techniques de l'automate SYSMAC C/CPM/CS/CJ.</p></td>
</tr>
<tr class="even">
<td><p>Établir la connexion avec un automate SYSMAC C/CPM/CS/CJ</p>
<p>1.  Raccordement matériel</p>
<p>Câble de liaison :</p>
<p>RS232<span id="OLE_LINK1"></span><span id="OLE_LINK2"></span><span id="OLE_LINK3"></span> <span id="OLE_LINK25"></span><span id="OLE_LINK26"></span></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><span id="OLE_LINK60"></span><span id="OLE_LINK61"></span><span id="OLE_LINK62"></span><span id="OLE_LINK27"></span><span id="OLE_LINK30"></span><strong>Écran tactile COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>SYSMAC CS/CJ</strong></p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>2</p></td>
<td><p>TX</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>TX</p></td>
<td><p>3</p></td>
<td><p>RX</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>9</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table>
<p><img src="../../drivers/omron.files/image002.gif" width="130" /><img src="../../drivers/omron.files/image003.gif" width="290" /><img src="../../drivers/omron.files/image004.gif" width="130" /></p></td>
</tr>
</tbody>
</table>

Le connecteur de l'IHM est un DB9F ; celui de l'automate SYSMAC C/CPM/CS/CJ est un DB9M.

**2. Paramétrage logiciel**

Choisissez OMRON dans le service d'équipement de la connexion.

Choisissez l'élément correspondant au modèle d'automate connecté ou au protocole pris en charge dans le service d'équipement de la connexion.

Vérifiez que les paramètres de communication de l'écran tactile et le numéro de station correspondent à ceux de l'automate connecté.

Pour le paramétrage de l'automate, voir la documentation technique des automates SYSMAC C/CPM/CS/CJ.

Paramètres de connexion par défaut de l'IHM série HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Paramètre**               | **Valeur par défaut**       | **Plage de réglage**                         |
| **Type d'automate**         | SYSMAC C/CPM Series         | SYSMAC C/CPM/CS/CJ Series                    |
| **Type de port**            | RS232                       | RS232/RS422/RS485                            |
| **Vitesse (baud)**          | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bits de données**         | 7                           | 7/8                                          |
| **Parité**                  | EVEN                        | EVEN/ODD/NONE                                |
| **Bits de stop**            | 2                           | 1/2                                          |
| **N° de station automate**  | 0                           | 0~255                                        |
| **N° de station IHM**       | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Fonction**            | **Prise en charge**         |
| **Simulation hors ligne** | Oui                       |
| **Simulation en ligne**  | Oui                        |
| **Mode étendu**         | Non                         |

**3. Registres utilisables et plages d'adresses**

Série SYSMAC C/CPM

|                   |                    |                 |                                                                                                                  |
|-------------------|--------------------|-----------------|------------------------------------------------------------------------------------------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**                                                                                                |
| **IR_Bit**        | dddd.DD            | 0.0~4095.15     | Bit : relais d'entrée/sortie                                                                                     |
| **HR_Bit**        | dddd.DD            | 0.0~4095.15     | Bit : relais de maintien                                                                                         |
| **LR_Bit**        | dddd.DD            | 0.0~4095.15     | Bit : relais de liaison                                                                                          |
| **AR_Bit**        | dddd.DD            | 0.0~4095.15     | Bit : relais de mémoire auxiliaire                                                                               |
| **T**             | ddd                | 0~255           | Bit : état de temporisation                                                                                      |
| **C**             | ddd                | 0~255           | Bit : état de compteur                                                                                           |
| **IR**            | dddd               | 0~4095          | Mot : relais d'entrée/sortie                                                                                     |
| **HR**            | dddd               | 0~4095          | Mot : relais de maintien                                                                                         |
| **LR**            | dddd               | 0~4095          | Mot : relais de liaison                                                                                          |
| **AR**            | dddd               | 0~4095          | Mot : relais de mémoire auxiliaire                                                                               |
| **TC**            | ddd                | 0~255           | <span id="OLE_LINK234"></span>Mot : valeur de temporisation                                                      |
| **DM**            | dddd               | 0~9999          | Mot : <span id="OLE_LINK235"></span><span id="OLE_LINK236"></span><span id="OLE_LINK237"></span>zone de données |

Série SYSMAC CS/CJ

|                   |                    |                 |                                                                                         |
|-------------------|--------------------|-----------------|-----------------------------------------------------------------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**                                                                       |
| **CIO_Bit**       | dddd.DD            | 0.0~3189.15     | Bit : <span id="OLE_LINK238"></span>zone d'E/S                                          |
| **W_Bit**         | dddd.DD            | 0.0~6143.15     | Bit :<span id="OLE_LINK239"></span> zone de travail                                     |
| **H_Bit**         | dddd.DD            | 0.0~511.15      | Bit :<span id="OLE_LINK240"></span> zone de maintien                                    |
| **A_Bit**         | dddd.DD            | 0.0~959.15      | Bit : <span id="OLE_LINK241"></span>zone auxiliaire, lecture seule : 7 168 bits : A00000～A447.15 |
| **D_Bit**         | dddd.DD            | 0.0~32767.15    | Bit :<span id="OLE_LINK242"></span> zone de données                                     |
| **T**             | dddd               | 0~4095          | Bit : état de temporisation                                                             |
| **C**             | dddd               | 0~4095          | Bit : état de compteur                                                                  |
| **CIO**           | dddd               | 0~3189          | Mot : zone d'E/S                                                                        |
| **W**             | dddd               | 0~6143          | Mot : zone de travail                                                                   |
| **H**             | dddd               | 0~511           | Mot : zone de maintien                                                                  |
| **A**             | dddd               | 0~959           | Mot : zone auxiliaire, lecture seule : 448 mots : A000～A447                            |
| **D**             | dddd               | 0~32767         | Mot : zone de données                                                                   |
| **TV**            | dddd               | 0~4095          | Mot : valeur courante de temporisation                                                  |
| **CV**            | dddd               | 0~4095          | Mot : valeur courante de compteur                                                       |

CP1L Tcp/Ip       / Fins-udp

|                   |                    |                 |                                                           |
|-------------------|--------------------|-----------------|-----------------------------------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**                                         |
| **CIO_Bit**       | dddd.DD            | 0.0~3189.15     | Bit : zone d'E/S                                          |
| **W_Bit**         | dddd.DD            | 0.0~6143.15     | Bit : zone de travail                                     |
| **H_Bit**         | dddd.DD            | 0.0~511.15      | Bit : zone de maintien                                    |
| **A_Bit**         | dddd.DD            | 0.0~959.15      | Bit : zone auxiliaire, lecture seule : 7 168 bits : A00000～A447.15 |
| **D_Bit**         | dddd.DD            | 0.0~32767.15    | Bit : zone de données                                     |
| **T**             | dddd               | 0~4095          | Bit : état de temporisation                               |
| **C**             | dddd               | 0~4095          | Bit : état de compteur                                    |
| **CIO**           | dddd               | 0~3189          | Mot : zone d'E/S                                          |
| **W**             | dddd               | 0~6143          | Mot : zone de travail                                     |
| **H**             | dddd               | 0~511           | Mot : zone de maintien                                    |
| **A**             | dddd               | 0~959           | Mot : zone auxiliaire, lecture seule : 448 mots : A000～A447 |
| **D**             | dddd               | 0~32767         | Mot : zone de données                                     |
| **TV**            | dddd               | 0~4095          | Mot : valeur courante de temporisation                    |
| **CV**            | dddd               | 0~4095          | Mot : valeur courante de compteur                         |

<img src="../../drivers/omron.files/image010.gif" width="595" />

Remarque :

d : décimal, plage de saisie 0-9 ;

DD : 16 bits, plage de saisie 0-15 ;

Mot dans les remarques : le registre ne s'utilise que comme mot ;

Bit dans les remarques : le registre ne s'utilise que comme bit ;

Lecture seule dans les remarques : le registre peut être lu mais pas écrit ;

Les noms et plages des registres peuvent varier selon le modèle d'équipement.

Pour le détail des noms et plages, consultez la documentation technique de l'équipement connecté

<img src="../../drivers/omron.files/image011.gif" width="595" />

 Paramétrage de la connexion TCP/IP du CP1L : réglez

-&gt; Ethernet intégré -&gt; IP et numéro de port. Remarque :

il est conseillé d'utiliser la communication fins-udp, qui permet de connecter plusieurs écrans tactiles au même automate ; une connexion préalable (handshake) est nécessaire avant la communication normale, ce qui demande un certain temps

Instructions de connexion Fins-udp :

Réglez -&gt; Ethernet intégré -&gt; IP et numéro de port

Le numéro de nœud de la configuration fins-udp doit correspondre au numéro de nœud défini dans les paramètres Ethernet de l'automate Omron

<img src="../../drivers/omron.files/image008.jpg" width="500" alt="image009.jpg" />
