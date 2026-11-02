# Pilote d'équipements Koyo

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Ce pilote permet aux IHM de la série HM de lire et d'écrire les données ou l'état des registres des automates Koyo série SN. La liaison série est établie entre le port série de l'écran tactile et celui de l'automate Koyo SN. Avant d'utiliser ce pilote, lisez attentivement ce chapitre et les spécifications techniques de l'automate Koyo SN.</p></td>
</tr>
<tr class="even">
<td><p> Établir la connexion avec un automate Koyo série SN</p>
<p><strong>1.</strong> <strong>Raccordement matériel</strong></p>
<p>Câble de liaison :</p>
<p>RS232 (port série, protocole RS232)</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p>IHM HM COM1/COM2</p></td>
<td colspan="2"><p>Koyo série SN</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>4</p></td>
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
<td><p>8</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table></td>
</tr>
</tbody>
</table>

<img src="../../drivers/koyo.files/image006.gif" width="278" /><img src="../../drivers/koyo.files/image007.gif" width="130" /><img src="../../drivers/koyo.files/image008.gif" width="90" />

Le connecteur de l'IHM est un DB9F ; celui de l'automate Koyo série SN est une prise modulaire 6 broches.

**2. Paramétrage logiciel**

Choisissez Koyo Electronics dans le service d'équipement de la connexion.

Choisissez l'élément correspondant au modèle d'automate connecté ou au protocole pris en charge dans le service d'équipement de la connexion.

Vérifiez que les paramètres de communication de l'écran tactile et le numéro de station correspondent à ceux de l'automate connecté.

Pour le paramétrage de l'automate, voir la documentation technique des automates Koyo série SN.

Paramètres de connexion par défaut de l'IHM série HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Paramètre**               | **Valeur par défaut**       | **Plage de réglage**                         |
| **Type d'automate**         | Koyo SN Series              | Koyo SN Series                               |
| **Type de port**            | RS232                       | RS232/RS422/RS485                            |
| **Vitesse (baud)**          | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bits de données**         | 8                           | 7/8                                          |
| **Parité**                  | ODD                         | EVEN/ODD/NONE                                |
| **Bits de stop**            | 1                           | 1/2                                          |
| **N° de station automate**  | 1                           | 0~255                                        |
| **N° de station IHM**       | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Fonction**            | **Prise en charge**         |
| **Simulation hors ligne** | Oui                       |
| **Simulation en ligne**  | Oui                        |
| **Mode étendu**         | Oui                         |

**3. Koyo série SN**

|                   |                    |                 |                                |
|-------------------|--------------------|-----------------|--------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**                  |
| **I**             | ooo                | 0~377           | Bit : relais d'entrée, lecture seule |
| **O**             | ooo                | 0~377           | Bit : relais de sortie         |
| **M**             | oooo               | 0~1177          | Bit : relais auxiliaire        |
| **SP**            | ooo                | 0~777           | Bit : relais auxiliaire spécial |
| **S**             | ooo                | 0~177           | Bit : relais d'étape           |
| **T**             | ooo                | 0~177           | Bit : temporisation            |
| **C**             | ooo                | 0~177           | Bit : compteur                 |
| **R**             | ooooo              | 0~13777         | Mot : registre de données      |
| **TR**            | ooooo              | 0~13777         | Mot : valeur courante de temporisation |
| **CR**            | ooooo              | 0~13777         | Mot : valeur courante de compteur |
| **SR**            | ooooo              | 0~13777         | Mot : registre de données spécial |

**4. Koyo série DIRECT**

|                   |                    |                 |                                |
|-------------------|--------------------|-----------------|--------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**                  |
| **X**             | ooo                | 0~3777          | Bit : relais d'entrée, lecture seule |
| **Y**             | ooo                | 0~3777          | Bit : relais de sortie         |
| **GX**            | oooo               | 0~7777          | Bit : relais d'entrée, lecture seule |
| **GY**            | oooo               | 0~7777          | Bit : relais de sortie         |
| **C**             | oooo               | 0~7777          | Bit : compteur                 |
| **S**             | oooo               | 0~1777          | Bit : relais d'étape           |
| **SP**            | oooo               | 0~1777          | Bit : relais auxiliaire spécial |
| **CT**            | ooo                | 0~777           | Bit : compteur                 |
| **T**             | ooo                | 0~777           | Bit : temporisation            |
| **V**             | oooo               | 0~77777         | Mot : registre de données spécial |
| **TV**            | ooo                | 0~777           | Mot : valeur courante de temporisation |
| **CV**            | ooo                | 0~777           | Mot : valeur courante de compteur |

KV-Nano

|                |              |              |                                            |
|----------------|--------------|--------------|--------------------------------------------|
| **Registre**   | **Format d'adresse** | **Plage de saisie** | **Remarques**                      |
| **R**          | ddddd        | 0~59915      | Bit : relais                               |
| **B**          | DDDD         | 0~1FFF       | Bit : relais de liaison                    |
| **MR**         | ddddd        | 0~59915      | Bit : relais auxiliaire interne            |
| **LR**         | ddddd        | 0~19915      | Bit : relais à verrouillage                |
| **CR**         | dddd         | 0~8915       | Bit : relais de contrôle                   |
| **VB**         | DDDD         | 0~1FFF       | Bit : relais de travail                    |
| **T**          | ddd          | 0~511        | Bit : temporisation                        |
| **C**          | ddd          | 0~255        | Bit : compteur                             |
| **DM**         | dddd         | 0~32767      | Mot : mémoire de données                   |
| **W**          | DDDD         | 0~3FFF       | Mot : registre de liaison                  |
| **TM**         | dddd         | 0~511        | Mot : mémoire de données temporaire        |
| **Z**          | dddd         | 1~12         | Mot : registre d'index                     |
| **TC**         | dddd         | 0~511        | Double mot : temporisation (valeur courante) |
| **TS**         | dddd         | 0~511        | Double mot : temporisation (consigne)      |
| **CC**         | ddd          | 0~255        | Double mot : compteur (valeur courante)    |
| **CS**         | ddd          | 0~255        | Double mot : compteur (consigne)           |
| **CTH**        | d            | 0~3          | Double mot : compteur rapide               |
| **CTC**        | d            | 0~7          | Double mot : comparateur de compteur rapide |
| **CM**         | dddd         | 0~8999       | Mot : mémoire de contrôle                  |
| **VM**         | dddd         | 0~9999       | Mot : mémoire de travail                   |

<img src="../../drivers/koyo.files/image009.gif" width="595" />

Remarque :

o : octal, plage de saisie 0-7 ;

Mot dans les remarques : le registre ne s'utilise que comme mot ;

Double mot dans les remarques : le type de données du registre dans la configuration doit être 32 bits ;

Bit dans les remarques : le registre ne s'utilise que comme bit ;

Lecture seule dans les remarques : le registre peut être lu mais pas écrit ;

Les noms et plages des registres peuvent varier selon le modèle d'équipement.

Pour le détail des noms et plages, consultez la documentation technique de l'équipement connecté

<img src="../../drivers/koyo.files/image010.gif" width="595" />
