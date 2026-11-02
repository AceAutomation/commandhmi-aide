# Pilote d'équipements Fatek

Ce pilote permet aux IHM de la série HM de lire et d'écrire les données ou l'état des registres des automates <span id="OLE_LINK158"></span><span id="OLE_LINK159"></span>Fatek série FB. La liaison série est établie entre le port série de l'écran tactile et celui de l'automate Fatek FB. Avant d'utiliser ce pilote, lisez attentivement ce chapitre et les spécifications techniques de l'automate Fatek FB.

**Établir la connexion avec un équipement Fatek**

**1. Raccordement matériel**

Câble de liaison :

RS232<span id="OLE_LINK1"></span><span id="OLE_LINK2"></span> (port série, protocole RS232)

|                         |     |                 |     |
|-------------------------|-----|-----------------|-----|
| IHM série HM COM1/COM2 |     | Fatek série FB |     |
| 2                       | RX  | 1               | TX  |
| 3                       | TX  | 2               | RX  |
| 5                       | GND | 4               | GND |

|     |                                                    |     |                                                    |     |                                                    |
|-----|----------------------------------------------------|-----|----------------------------------------------------|-----|----------------------------------------------------|
|     |                                                    |     |                                                    |     |                                                    |
|     |                                                    |     |                                                    |     | <img src="../../drivers/fatek.files/image006.gif" width="146" /> |
|     | <img src="../../drivers/fatek.files/image007.gif" width="129" /> |     |                                                    |     |                                                    |
|     |                                                    |     | <img src="../../drivers/fatek.files/image008.gif" width="280" /> |     |                                                    |
|     |                                                    |     |                                                    |     |                                                    |
|     |                                                    |     |                                                    |     |                                                    |

Le connecteur de l'IHM série HM est un DB9F ; celui de l'automate Fatek FB est un MD4M.

**2. Paramétrage logiciel**

Choisissez Fatek Automation Corp. dans le service d'équipement de la connexion.

Choisissez l'élément correspondant au modèle d'automate connecté ou au protocole pris en charge dans le service d'équipement de la connexion.

Vérifiez que les paramètres de communication de l'écran tactile et le numéro de station correspondent à ceux de l'automate connecté.

Pour le paramétrage de l'automate, voir la documentation technique des automates Fatek série FB.

Paramètres de connexion par défaut de l'écran tactile

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Paramètre**               | **Valeur par défaut**       | **Plage de réglage**                         |
| **Type d'automate**         | Fatek FB Series             | Fatek FB Series                              |
| **Type de port**            | RS232                       | RS232                                        |
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

**3. Registres utilisables et plages d'adresses**

|                   |                    |                 |                                                   |
|-------------------|--------------------|-----------------|---------------------------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**                                 |
| X                 | dddd               | 0~9999          | Bit : entrée, lecture seule                       |
| Y                 | dddd               | 0~9999          | Bit : relais de sortie                            |
| M                 | dddd               | 0~9999          | Bit : relais interne                              |
| S                 | dddd               | 0~9999          | Bit : relais d'étape                              |
| T                 | dddd               | 0~9999          | Bit : état de temporisation                       |
| C                 | dddd               | 0~9999          | Bit : état de compteur                            |
| R                 | dddd               | 0~9999          | <span id="OLE_LINK198"></span>Mot : registre de données |
| D                 | dddd               | 0~9999          | Mot : registre de données                         |
| TR                | dddd               | 0~9999          | Mot : valeur courante de temporisation            |
| CR                | dddd               | 0~9999          | Mot : valeur courante de compteur                 |
| F                 | dddd               | 0~9999          | Mot : registre de fichier                         |
| DRC               | ddd                | 200~255         | Double mot : valeur courante de compteur 32 bits  |

<img src="../../drivers/fatek.files/image009.gif" width="600" />

Remarque :

d : décimal, plage de saisie 0-9 ;

o : octal, plage de saisie 0-7 ;

Bit dans les remarques : le registre ne s'utilise que comme bit ;

Mot dans les remarques : le registre ne s'utilise que comme mot ;

Double mot dans les remarques : le type de données du registre dans la configuration doit être 32 bits ;

Lecture seule dans les remarques : le registre peut être lu mais pas écrit ;

Les noms et plages des registres peuvent varier selon le modèle d'équipement.

Pour le détail des noms et plages, consultez la documentation technique de l'équipement connecté

<img src="../../drivers/fatek.files/image009.gif" width="600" />
