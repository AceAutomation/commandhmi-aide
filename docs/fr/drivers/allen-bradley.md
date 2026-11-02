# Pilote d'équipements Allen-Bradley

Ce pilote permet aux IHM de la série HM de lire et d'écrire les données ou l'état d'un équipement AIBUS via le protocole AIBUS. La liaison série est établie entre le port série de l'IHM et celui de l'équipement AIBUS. Avant d'utiliser ce pilote, lisez attentivement ce chapitre et les spécifications techniques de l'équipement AIBUS.

**Établir la connexion avec l'équipement**

**1. Raccordement matériel**

Câble de liaison :

RS232 (port série, protocole RS232)

|                             |     |                   |     |
|-----------------------------|-----|-------------------|-----|
| **IHM série HM COM1/COM2** |     | **Équipement AIBUS**  |     |
| 2                           | RX  | Broche définie par l'utilisateur | TX  |
| 3                           | TX  | Broche définie par l'utilisateur | RX  |
| 5                           | GND | Broche définie par l'utilisateur | GND |

<img src="../../drivers/allen-bradley.files/image002.gif" width="130" /><img src="../../drivers/allen-bradley.files/image003.gif" width="280" /><img src="../../drivers/allen-bradley.files/image004.gif" width="145" />

ControlLogix/CompactLogix:

|                             |     |                         |     |
|-----------------------------|-----|-------------------------|-----|
| **IHM série HM COM1/COM2** |     | **Allen-Bradley（AB）** |     |
| 2                           | RX  | 3                       | TX  |
| 3                           | TX  | 2                       | RX  |
| 5                           | GND | 5                       | GND |

<img src="../../drivers/allen-bradley.files/image005.gif" width="129" /><img src="../../drivers/allen-bradley.files/image006.gif" width="290" /><img src="../../drivers/allen-bradley.files/image007.gif" width="130" />

Le port de l'IHM série HM est un DB9F, celui de l'équipement AB un MD8M.

**2. Paramétrage logiciel**

ü Choisissez Allen-Bradley dans le service d'équipement de la connexion.

ü Choisissez l'élément correspondant au modèle d'automate connecté ou au protocole pris en charge.

ü Vérifiez que les paramètres de communication de l'écran tactile et le numéro de station correspondent à ceux de l'automate connecté.

ü Pour le paramétrage de l'automate, voir la documentation technique de l'automate Allen-Bradley.

Paramètres de connexion par défaut de l'IHM série HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Paramètre**               | **Valeur par défaut**       | **Plage de réglage**                         |
| **Type d'automate**         | MicroLogix DF1_CRC          | MicroLogix DF1_CRC/MicroLogix DF1_BCC        |
| **Type de port**            | RS232                       | RS232/RS422/RS485                            |
| **Vitesse (baud)**          | 19200                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bits de données**         | 8                           | 7/8                                          |
| **Parité**                  | NONE                        | EVEN/ODD/NONE                                |
| **Bits de stop**            | 1                           | 1/2                                          |
| **N° de station automate**  | 1                           | 1~31                                         |
| **N° de station IHM**       | 0                           | 0~255                                        |
| **Contrôle**                | CRC                         | BCC                                          |

|                         |                             |
|-------------------------|-----------------------------|
| **Fonction**            | **Prise en charge**         |
| **Simulation hors ligne** | Oui                       |
| **Simulation en ligne**  | Oui                        |
| **Mode étendu**         | Non                         |

**3. Registres utilisables et plages d'adresses**

Série SLC / MicroLogix :

|                   |                    |                        |                                |
|-------------------|--------------------|------------------------|--------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie**    | **Remarques**                  |
| **I**             | 1:ddd/o            | 1:0/0~1:255/15         | Bit : image des entrées        |
| **O**             | 0:ddd/o            | 0:0/0~0:255/15         | Bit : image des sorties        |
| **B**             | ddd:ddd/o          | 3:0/0~255:255/15       | Bit : mémoire bit              |
| **S_Bit**         | 2:ddd/o            | 2:0/0~2:255/15         | Bit : bit d'état système       |
| **N_Bit**         | ddd:ddd/o          | 7:0、10:0/0~255:255/15 | Bit : bit d'un mot de registre de données |
| **S**             | 2:ddd              | 2:0~2:255              | Mot : mot d'état système       |
| **ST**            | ddd:ddd.dd         | 0:0.0~255:255.40       | Mot : mot d'état système       |
| **N**             | ddd:ddd            | 7:0、10:0~255:255      | Mot : registre de données      |
| **F**             | ddd:ddd            | 8:0~255:255            | Mot : registre flottant        |
| **T_ACC**         | ddd:ddd            | 4:0~255:255            | Mot : valeur ACC de temporisation |
| **T_PRE**         | ddd:ddd            | 4:0~255:255            | Mot : valeur PRE de temporisation |
| **C_ACC**         | ddd:ddd            | 5:0~255:255            | Mot : valeur ACC de compteur   |
| **C_PRE**         | ddd:ddd            | 5:0~255:255            | Mot : valeur PRE de compteur   |

ControlLogix/CompactLogix:

|                   |                    |                  |                                |
|-------------------|--------------------|------------------|--------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**                  |
| **B-Bit**         | ddd:ddd/dd         | 3~225:0~255/0~15 | Bit : bit d'un mot de registre de données |
| **N_Bit**         | ddd:ddd/dd         | 7~225:0~255/0~15 | Bit : bit d'un mot de registre de données |
| **N_Bit**         | ddd:ddd/o          | 7:0/0~255:255/7  | Bit : bit d'un mot de registre de données |
| **S**             | 2:ddd              | 2:0~2:255        | Mot : mot d'état système       |
| **N**             | ddd:ddd            | 7:0~255:255      | Mot : registre de données      |
| **F**             | ddd:ddd            | 8:0~255:255      | Mot : registre flottant        |

CompactLogix_L16ER_TCP (port : 44818)

|               |                    |                 |                                        |
|---------------|--------------------|-----------------|----------------------------------------|
| Registre      | **Format d'adresse** | **Plage de saisie** | **Remarques**                      |
| **B**         | ddd.ddd            | 0.0~255.255     | Bit : adresse de type bool             |
| **I**         | Ddd.ddd            | 0.0~255.255     | Mot : registre int 16 bits             |
| **F**         | ddd.ddd            | 0.0~255.99      | Double mot : registre float 32 bits    |

MicroLogix DF1_TCP            (port : 44818)

|               |                    |                  |                                                    |
|---------------|--------------------|------------------|----------------------------------------------------|
| Registre      | **Format d'adresse** | **Plage de saisie** | **Remarques**                                  |
| **I**         | ddd.ddd/dd         | 0.0/0~255.255/15 | Bit : image des entrées, lecture seule            |
| **O**         | ddd.ddd/dd         | 0.0/0~255.255/15 | Bit : image des sorties                           |
| **B**         | ddd.ddd/dd         | 0.0/0~255.255/15 | Bit : mémoire bit                                 |
| **T**         | ddd.ddd            | 0.0~255.255      | Bit : état de temporisation                       |
| **C**         | ddd.ddd            | 0.0~255.255      | Bit : état de compteur                            |
| **S_Bit**     | ddd.ddd/dd         | 0.0/0~255.255/15 | Bit : bit du registre système                     |
| **N_Bit**     | ddd.ddd/dd         | 0.0/0~255.255/15 | Bit : bit d'un registre de données                |
| **S**         | ddd.ddd            | 0.0~255.255      | Mot : registre système                            |
| **N**         | ddd.ddd            | 0.0~255.255      | Mot : registre entier 16 bits                     |
| **F**         | ddd.ddd            | 0.0~255.255      | Double mot : registre flottant 32 bits            |
| **TV**        | ddd.ddd            | 0.0~255.255      | Mot : valeur courante de temporisation            |
| **CV**        | ddd.ddd            | 0.0~255.255      | Mot : valeur courante de compteur                 |
| **TS**        | ddd.ddd            | 0.0~255.255      | Mot : consigne de temporisation                   |
| **CS**        | ddd.ddd            | 0.0~255.255      | Mot : consigne de compteur                        |

**4. Connexion des IHM série HM aux automates ControlLogix et CompactLogix d'Allen-Bradley**

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td></td>
<td><p>Ouvrez RSLinx et configurez le pilote de communication de l'automate</p>
<p><img src="../../drivers/allen-bradley.files/image008.gif" width="349" /></p>
<p>Créez un pilote ; choisissez la connexion série et les équipements RS-232 DF1</p>
<p><img src="../../drivers/allen-bradley.files/image009.gif" width="425" /></p>
<p>Une fois réglé, et si un câble relie le PC à l'automate, l'automate apparaît dans RSLinx</p>
<p><img src="../../drivers/allen-bradley.files/image010.gif" width="430" /></p>
<p>Ouvrez le logiciel de programmation RSLogix 5000 ; créez votre projet et de nouvelles étiquettes (tags)</p>
<p><img src="../../drivers/allen-bradley.files/image011.gif" width="282" /></p>
<p>Créez les tags B003, N007 et F008</p>
<p><img src="../../drivers/allen-bradley.files/image012.gif" width="390" /></p>
<p>Liste des tags après création :</p>
<p><img src="../../drivers/allen-bradley.files/image013.gif" width="633" /></p>
<p>Créez le <a href="javascript:;">mappage d'adresses</a></p>
<p><img src="../../drivers/allen-bradley.files/image014.gif" width="428" /><strong></strong></p>
<p><img src="../../drivers/allen-bradley.files/image015.gif" width="410" /><strong></strong></p>
<p><strong>Réglez les paramètres de l'automate</strong></p>
<p><img src="../../drivers/allen-bradley.files/image016.gif" width="807" /><strong></strong></p>
<p><img src="../../drivers/allen-bradley.files/image017.gif" width="552" /><strong></strong></p>
<p>·d : décimal, plage de saisie 0-9 ;</p>
<p>·o : octal, plage de saisie 0-7 ;</p>
<p>·Bit dans les remarques : le registre ne s'utilise que comme bit ;</p>
<p>·Mot dans les remarques : le registre ne s'utilise que comme mot ;</p>
<p>·Lecture seule dans les remarques : le registre peut être lu mais pas écrit ;</p>
<p>·Les noms et plages des registres peuvent varier selon le modèle d'équipement.</p>
<p>Pour le détail des noms et plages, consultez la documentation technique de l'équipement connecté </p></td>
</tr>
</tbody>
</table>

Connexion d'un automate CompactLogix série 1769

Nouvelles étiquettes d'adresse dans l'automate

Correspondance des étiquettes d'adresse

Registre            type d'étiquette  taille du tableau

B                          bool             255

I                           int                 255

F                          real               100

Le nom d'étiquette doit comporter 3 caractères, par exemple B003, I004 et F005

<img src="../../drivers/allen-bradley.files/image018.jpg" width="314" alt="ab_guanli.jpg" />

<img src="../../drivers/allen-bradley.files/image019.jpg" width="390" alt="ab_guanli2.jpg" />

Connexion d'un MicroLogix série 1766 en DF1_TCP

Hormis les registres d'E/S dont la taille n'est pas réglable, la taille des tableaux des autres registres est 256. Le premier nombre du format d'adresse est le numéro de fichier : par exemple, le numéro de fichier de F8 est 8, celui de I1 est 1, etc.
