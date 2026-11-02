# Pilote d'équipements Keyence

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Ce pilote permet aux IHM de la série HM de lire et d'écrire les données ou l'état des registres des automates Keyence séries KV/VisualKV. La liaison série est établie entre le port série de l'écran tactile et celui de l'automate Keyence. Avant d'utiliser ce pilote, lisez attentivement ce chapitre et les spécifications techniques de l'automate Keyence KV/VisualKV.</p></td>
</tr>
<tr class="even">
<td><p>Établir la connexion avec un automate Keyence KV/VisualKV</p>
<p><strong>1. Raccordement matériel</strong></p>
<p>Câble de liaison :</p>
<p>RS232 (port série, protocole RS232)</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>IHM série HM COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Keyence séries KV/VisualKV</strong></p></td>
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
</table></td>
</tr>
</tbody>
</table>

<img src="../../drivers/keyence.files/image002.gif" width="130" /><img src="../../drivers/keyence.files/image003.gif" width="90" /><img src="../../drivers/keyence.files/image004.gif" width="278" />

Le connecteur de l'IHM est un DB9F ; celui de l'automate Keyence KV/VisualKV est une prise modulaire 6 broches.

**2. Paramétrage logiciel**

Choisissez Keyence Corporation dans le service d'équipement de la connexion.

Choisissez l'élément correspondant au modèle d'automate connecté ou au protocole pris en charge dans le service d'équipement de la connexion.

Vérifiez que les paramètres de communication de l'écran tactile et le numéro de station correspondent à ceux de l'automate connecté.

Pour le paramétrage de l'automate, voir la documentation technique des automates Keyence séries KV/VisualKV.

Paramètres de connexion par défaut de l'IHM série HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Paramètre**               | **Valeur par défaut**       | **Plage de réglage**                         |
| **Type d'automate**         | KV-1000/700 KV-L20(R)       | KV-1000/700 KV-L20(R)/ KV-/40 KV-P16         |
| **Type de port**            | RS232                       | RS232/RS422/RS485                            |
| **Vitesse (baud)**          | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bits de données**         | 8                           | 7/8                                          |
| **Parité**                  | EVEN                        | EVEN/ODD/NONE                                |
| **Bits de stop**            | 1                           | 1/2                                          |
| **N° de station automate**  | 0                           | 0~255                                        |
| **N° de station IHM**       | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Fonction**            | **Prise en charge**         |
| **Simulation hors ligne** | Oui                       |
| **Simulation en ligne**  | Oui                        |
| **Mode étendu**         | Non                         |

**3. Registres utilisables et plages d'adresses**

l  KV-1000/700 KV-L20(R)

|                   |                    |                 |                                |
|-------------------|--------------------|-----------------|--------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**                  |
| **R**             | dddDD              | 0~99915         | Bit : relais d'entrée/sortie   |
| **MR**            | dddDD              | 0~3915          | Bit : relais auxiliaire interne |
| **LR**            | dddDD              | 0~3999          | Bit : relais à verrouillage    |
| **CR**            | ddDD               | 0~3999          | Bit : relais de contrôle       |
| **T**             | dddd               | 0~65534         | Bit : temporisation            |
| **C**             | dddd               | 0~65534         | Bit : compteur                 |
| **DM**            | ddddd              | 0~32766         | Mot : mémoire de données       |
| **EM**            | ddddd              | 0~511           | Mot : mémoire de données étendue |
| **FM**            | ddddd              | 0~11998         | Mot : registre de fichier      |
| **TM**            | ddd                | 0~3999          | Mot : mémoire de données temporaire |
| **CM**            | ddddd              | 0~3999          | Mot : mémoire de contrôle      |
| **TV**            | dddd               | 0~99915         | Mot : valeur courante de temporisation |
| **CV**            | dddd               | 0~3915          | Mot : valeur courante de compteur |

l  KV-10/16/24/40 KV-P16

|                   |                    |                 |                                           |
|-------------------|--------------------|-----------------|-------------------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**                         |
| RLY               | dddDD              | 0~99915         | Bit : relais                              |
| T                 | dddd               | 0~999           | Bit : temporisation                       |
| C                 | dddd               | 0~999           | Bit : compteur                            |
| DM                | ddddd              | 0~9999          | Mot : mémoire de données                  |
| TM                | ddd                | 0~99            | Mot : mémoire de données temporaire       |
| TV_c              | dddd               | 0~999           | Mot : valeur courante de temporisation    |
| TV_p              | dddd               | 0~999           | Mot : présélection de temporisation       |
| CV_c              | dddd               | 0~999           | Mot : valeur courante de compteur         |
| CV_p              | dddd               | 0~999           | Mot : présélection de compteur            |
| CTH               | dddd               | 0~9             | Mot : valeur courante du compteur rapide  |

l  KV-Nano

|                   |                    |                 |                                      |
|-------------------|--------------------|-----------------|--------------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**                    |
| **R**             | ddddd              | 0~59915         | Bit : relais                         |
| **B**             | DDDD               | 0~1FFF          | Relais de liaison                    |
| **MR**            | ddddd              | 0~59915         | Relais auxiliaire interne            |
| **LR**            | ddddd              | 0~19915         | Relais à verrouillage                |
| **CR**            | dddd               | 0~8915          | Relais de contrôle                   |
| **VB**            | DDDD               | 0~1FFF          | Relais de travail                    |
| **T**             | ddd                | 0~511           | Bit : temporisation                  |
| **C**             | ddd                | 0~255           | Bit : compteur                       |
| **DM**            | dddd               | 0~32767         | Mémoire de données                   |
| **W**             | DDDD               | 0~3FFF          | Registre de liaison                  |
| **TM**            | dddd               | 0~511           | Mémoire de données temporaire        |
| **Z**             | dddd               | 1~12            | Registre d'index                     |
| **TC**            | dddd               | 0~511           | Double mot : temporisation (valeur courante) |
| **TS**            | dddd               | 0~511           | Double mot : temporisation (consigne) |
| **CC**            | ddd                | 0~255           | Double mot : compteur (valeur courante) |
| **CS**            | ddd                | 0~255           | Double mot : compteur (consigne)     |
| **CTH**           | d                  | 0~3             | Compteur rapide                      |
| **CTC**           | d                  | 0~7             | Double mot : comparateur rapide      |
| **CM**            | dddd               | 0~8999          | Mémoire de contrôle                  |
| **VM**            | dddd               | 0~9999          | Mémoire de travail                   |

<img src="../../drivers/keyence.files/image005.gif" width="595" />

Remarque :

d : décimal, plage de saisie 0-9 ;

DD : 16 bits, plage de saisie 0-15 ;

Bit dans les remarques : le registre ne s'utilise que comme bit ;

Mot dans les remarques : le registre ne s'utilise que comme mot ;

Les noms et plages des registres peuvent varier selon le modèle d'équipement.

Pour le détail des noms et plages, consultez la documentation technique de l'équipement connecté.

<img src="../../drivers/keyence.files/image005.gif" width="595" />
