# Équipements Invt

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Ce pilote permet aux IHM de la série HM de lire et d'écrire les données ou l'état des registres des automates <span id="OLE_LINK121"></span>Invt. La liaison série est établie entre le port série de l'IHM et celui de l'automate Invt. Avant d'utiliser ce pilote, lisez attentivement ce chapitre et les spécifications techniques de l'automate Invt.</p></td>
</tr>
<tr class="even">
<td><p>Établir la connexion avec un automate Invt</p>
<p>1.  Raccordement matériel</p>
<p>Câble de liaison :</p>
<p>RS232</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>IHM série HM COM1/COM2</strong></p></td>
<td colspan="2"><p>Invt</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>5</p></td>
<td><p>TX</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>TX</p></td>
<td><p>4</p></td>
<td><p>RX</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>3</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table>
<p><img src="../../drivers/invt.files/image005.gif" width="145" /><img src="../../drivers/invt.files/image006.gif" width="281" /><img src="../../drivers/invt.files/image007.gif" width="130" /></p></td>
</tr>
</tbody>
</table>

Le connecteur de l'IHM est un DB9F ; celui de l'automate Invt est un MD8M.

**2. Paramétrage logiciel**

Choisissez Invt dans le service d'équipement de la connexion.

Choisissez l'élément correspondant au modèle d'automate connecté ou au protocole pris en charge dans le service d'équipement de la connexion.

Vérifiez que les paramètres de communication de l'écran tactile et le numéro de station correspondent à ceux de l'automate connecté.

Pour le paramétrage de l'automate, voir la documentation technique des automates Invt.

Paramètres de connexion par défaut de l'écran tactile

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Paramètre**               | **Valeur par défaut**       | **Plage de réglage**                         |
| **PLC type**                | IVC1,IVC1L,IVCIS,IVC2L,IVC3 | IVC1,IVC1L,IVCIS,IVC2L,IVC3                  |
| **Type de port**            | RS232                       | RS232/RS422/RS485                            |
| **Vitesse (baud)**          | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bits de données**         | 7                           | 7/8                                          |
| **Parité**                  | EVEN                        | EVEN/ODD/NONE                                |
| **Bits de stop**            | 1                           | 1/2                                          |
| **N° de station automate**  | 1                           | 0~255                                        |
| **N° de station IHM**       | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Fonction**            | **Prise en charge**         |
| **Simulation hors ligne** | Oui                       |
| **Simulation en ligne**  | Oui                        |
| **Mode étendu**         | Oui                         |

**3. (IVC1,IVC1L,IVCIS,IVC2L,IVC3,IVC3 TCP) Registres utilisables et plages d'adresses**

|                   |                    |                 |                                             |
|-------------------|--------------------|-----------------|---------------------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**                           |
| X                 | ooo                | 0~377           | Bit : entrée, lecture seule                 |
| Y                 | ooo                | 0~377           | Bit : sortie                                |
| M                 | dddd               | 0~7999          | Bit : relais interne                        |
| SM                | ddd                | 0~255           | Bit : relais interne spécial                |
| S                 | ddd                | 0~999           | Bit : relais d'étape                        |
| T                 | ddd                | 0~255           | Bit : état de temporisation                 |
| C                 | ddd                | 0~255           | Bit : état de compteur                      |
| D                 | dddd               | 0~7999          | Mot : registre de données                   |
| SD                | ddd                | 0~255           | Mot : registre de données spécial           |
| TV                | ddd                | 0~255           | Mot : valeur courante de temporisation      |
| CV                | ddd                | 0~255           | Mot : valeur courante de compteur           |
| Z                 | dd                 | 0~15            | Mot : registre d'index                      |
| D_Double          | dddd               | 0~7999          | Double mot : registre de données            |
| CV_Double         | ddd                | 0~255           | Double mot : valeur courante de compteur    |
| SD_Double         | ddd                | 0~255           | Double mot : registre de données spécial    |
| R                 | ddd                | 0~32767         | Mot : registre 16 bits                      |
| RD                | ddd                | 32766           | Double mot : registre R 32 bits             |
|                   |                    |                 |                                             |
| D_Bit             | dddd.dd            | 0.0~7999.15     | Bit : bit de registre D                     |
| SD_Bit            | ddd.dd             | 0.0~255.15      | Bit : bit de registre SD                    |
| Z_Bit             | dd.dd              | 0.0~15.15       | Bit : bit de registre Z                     |
| R_Bit             | dddd.dd            | 0.0~32767.15    | Bit : bit de registre R                     |

AX70 RTU/AX70 TCP

|                   |                    |                 |                                                            |
|-------------------|--------------------|-----------------|------------------------------------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**                                          |
| **IX**            | ddd.o              | 0.0~511.7       | Bit : zone I en bits (lecture seule)                       |
| **QX**            | ddd.o              | 0.0~511.7       | Bit : zone Q en bits                                       |
| **MX**            | ddd.o              | 0.0~7566.7      | Bit : zone M en bits                                       |
| **IB**            | ddd                | 0~511           | Octet : zone I en octets (lecture seule)                   |
| **QB**            | ddd                | 0~511           | Octet : zone Q en octets                                   |
| **MB**            | dddd               | 0~7566          | Octet : zone M en octets                                   |
| **IW**            | ddd                | 0~511           | Mot : zone I en mots (lecture seule)                       |
| **QW**            | ddd                | 0~511           | Mot : zone Q en mots                                       |
| **MW**            | dddd               | 0~3783          | Mot : zone M en mots                                       |
| **ID**            | ddd                | 0~127           | Double mot : zone I en doubles mots (lecture seule)        |
| **QD**            | ddd                | 0~127           | Double mot : zone Q en doubles mots                        |
| **MD**            | dddd               | 0~1891          | Double mot : zone M en doubles mots                        |

<img src="../../drivers/invt.files/image004.gif" width="600" />

Remarque :

d : décimal, plage de saisie 0-9 ;

o : octal, plage de saisie 0-7 ;

Bit dans les remarques : le registre ne s'utilise que comme bit ;

Mot dans les remarques : le registre ne s'utilise que comme mot ;

Double mot dans les remarques : le type de données du registre dans la configuration doit être 32 bits ;

Lecture seule dans les remarques : le registre peut être lu mais pas écrit ;

Les noms et plages des registres peuvent varier selon le modèle d'équipement.

Pour le détail des noms et plages, consultez la documentation technique de l'équipement connecté.

<img src="../../drivers/invt.files/image004.gif" width="600" />
