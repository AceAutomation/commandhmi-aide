# Pilote d'équipements HaiWell

|                                                                                                                                                                                                                                                                                                                                                                                                                                                     |     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----|
| Ce pilote permet aux IHM de la série HM de lire et d'écrire les données ou l'état des registres des automates Haiwell séries E/S/H. La liaison série est établie entre le port série de l'écran tactile et celui de l'automate Haiwell. Avant d'utiliser ce pilote, lisez attentivement ce chapitre et les spécifications techniques de l'automate Haiwell E/S/H. |     |

<span id="OLE_LINK217"></span><span id="OLE_LINK218"></span><span id="OLE_LINK219"></span>Établir la connexion avec un équipement HAIWELL<span id="OLE_LINK221"></span>

<span id="OLE_LINK222"></span><span id="OLE_LINK223"></span><span id="OLE_LINK224"></span>**1. Raccordement matériel**

<span id="OLE_LINK225"></span><span id="OLE_LINK226"></span><span id="OLE_LINK227"></span>Câble de liaison :

RS232 (port série, protocole RS232)

|                                                                                                                       |     |                          |     |
|-----------------------------------------------------------------------------------------------------------------------|-----|--------------------------|-----|
| <span id="OLE_LINK228"></span><span id="OLE_LINK229"></span><span id="OLE_LINK230"></span>**IHM série HM COM1/COM2** |     | **HaiWell séries E/S/H** |     |
| 2                                                                                                                     | RX  | 2                        | TX  |
| 3                                                                                                                     | TX  | 1                        | RX  |
| 5                                                                                                                     | GND | 3                        | GND |

|     |                                                      |     |                                                      |     |                                                      |
|-----|------------------------------------------------------|-----|------------------------------------------------------|-----|------------------------------------------------------|
|     |                                                      |     |                                                      |     |                                                      |
|     | <img src="../../drivers/haiwell.files/image002.gif" width="129" /> |     |                                                      |     |                                                      |
|     |                                                      |     |                                                      |     | <img src="../../drivers/haiwell.files/image003.gif" width="140" /> |
|     |                                                      |     | <img src="../../drivers/haiwell.files/image004.gif" width="280" /> |     |                                                      |
|     |                                                      |     |                                                      |     |                                                      |
|     |                                                      |     |                                                      |     |                                                      |

<span id="OLE_LINK231"></span>Le connecteur de l'IHM série HM est un DB9F ; celui de l'automate Haiwell E/S/H est un MD4M.

<span id="OLE_LINK237"></span>**2. Paramétrage logiciel**

Choisissez Haiwell Technology Corp. dans le service d'équipement de la connexion.

Choisissez l'élément correspondant au modèle d'automate connecté ou au protocole pris en charge dans le service d'équipement de la connexion.

Vérifiez que les paramètres de communication de l'écran tactile et le numéro de station correspondent à ceux de l'automate connecté.

Pour le paramétrage de l'automate, voir la documentation technique des automates Haiwell séries E/S/H.

<span id="OLE_LINK242"></span>Paramètres de connexion par défaut de l'écran tactile

|                             |                             |                             |                                              |     |
|-----------------------------|-----------------------------|-----------------------------|----------------------------------------------|-----|
| **Paramètre**               | **Valeur par défaut**       |                             | **Plage de réglage**                         |     |
| **Type de port**            | RS232                       |                             | RS232/RS422/RS485                            |     |
| **Vitesse (baud)**          | 19200                       |                             | 1200/2400/4800/9600/19200/38400/57600/115200 |     |
| **Bits de données**         | 8                           |                             | 7/8                                          |     |
| **Parité**                  | NONE                        |                             | EVEN/ODD/NONE                                |     |
| **Bits de stop**            | 2                           |                             | 1/2                                          |     |
| **N° de station automate**  | 1                           |                             | 1~31                                         |     |
| **N° de station IHM**       | 0                           |                             | 0~255                                        |     |
| **Fonction**                |                             | **Prise en charge**         |                                              |     |
| **Simulation hors ligne**   |                             | Oui                         |                                              |     |
| **Simulation en ligne**     |                             | Oui                         |                                              |     |
| **Mode étendu**             |                             | Oui                         |                                              |     |
|                             |                             |                             |                                              |     |

3\. **Registres utilisables et plages d'adresses**

|                   |                    |                 |                                                            |
|-------------------|--------------------|-----------------|------------------------------------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**                                          |
| X                 | ddd                | 0~1023          | Bit : entrée TOR externe                                   |
| Y                 | ddd                | 0~1023          | Bit : sortie TOR externe                                   |
| M                 | ddd                | 0~12287         | Bit : relais interne                                       |
| SM                | ddd                | 0~215           | Bit :<span id="OLE_LINK153"></span> état système           |
| S                 | ddd                | 0~2047          | Bit : état d'étape                                         |
| T                 | ddd                | 0~1023          | Bit : état de temporisation                                |
| C                 | ddd                | 0~255           | Bit : état de compteur                                     |
| AI                | ddd                | 0~255           | Mot : registre d'entrée analogique                         |
| AQ                | ddd                | 0~255           | Mot : registre de sortie analogique                        |
| V                 | ddd                | 0~14847         | Mot : registre interne                                     |
| TCV               | ddd                | 0~1023          | Mot : <span id="OLE_LINK154"></span>valeur courante de temporisation |
| CCV               | ddd                | 0~47, 80~255    | Mot : valeur courante de compteur                          |
| SV                | ddd                | 0~154           | Mot : registre système                                     |
| CCV32             | ddd                | 0~31            | Double mot : valeur courante de compteur                   |

<img src="../../drivers/haiwell.files/image010.gif" width="595" />

Remarque :

d : décimal, plage de saisie 0-9 ;

Bit dans les remarques : le registre ne s'utilise que comme bit ;

Mot dans les remarques : le registre ne s'utilise que comme mot ;

Lecture seule dans les remarques : le registre peut être lu mais pas écrit ;

Les noms et plages des registres peuvent varier selon le modèle d'équipement.

Pour le détail des noms et plages, consultez la documentation technique de l'équipement connecté.

<img src="../../drivers/haiwell.files/image011.gif" width="595" />
