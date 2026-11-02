# Pilote d'équipements Fuji

Ce pilote permet aux IHM de la série HM de lire et d'écrire les données ou l'état des registres des automates Fuji série NB. La liaison série est établie entre le port série de l'IHM et celui de l'automate Fuji NB. Avant d'utiliser ce pilote, lisez attentivement ce chapitre et les spécifications techniques de l'automate Fuji NB.

**Établir la connexion avec un équipement Fuji**

**1. Raccordement matériel**

Câble de liaison :

RS422<span id="OLE_LINK1"></span><span id="OLE_LINK2"></span> (port série, protocole RS422)

|                         |     |                |     |
|-------------------------|-----|----------------|-----|
| IHM série HM COM1/COM2 |     | Fuji série NB |     |
| 6                       | RX- | 4              | TX- |
| 7                       | RX+ | 3              | TX+ |
| 8                       | TX- | 6              | RX- |
| 9                       | TX+ | 5              | RX+ |

|     |                                                   |     |                                                   |     |                                                  |
|-----|---------------------------------------------------|-----|---------------------------------------------------|-----|--------------------------------------------------|
|     |                                                   |     |                                                   |     |                                                  |
|     |                                                   |     |                                                   |     | <img src="../../drivers/fuji.files/image002.gif" width="95" /> |
|     | <img src="../../drivers/fuji.files/image003.gif" width="130" /> |     |                                                   |     |                                                  |
|     |                                                   |     | <img src="../../drivers/fuji.files/image004.gif" width="278" /> |     |                                                  |
|     |                                                   |     |                                                   |     |                                                  |
|     |                                                   |     |                                                   |     |                                                  |

Le connecteur de l'IHM série HM est un DB9F ; celui de l'automate Fuji NB est un RJ45.

**2. Paramétrage logiciel**

Choisissez Fuji Electric Corporation dans le service d'équipement de la connexion.

Choisissez l'élément correspondant au modèle d'automate connecté ou au protocole pris en charge dans le service d'équipement de la connexion.

Vérifiez que les paramètres de communication de l'écran tactile et le numéro de station correspondent à ceux de l'automate connecté.

Pour le paramétrage de l'automate, voir la documentation technique des automates Fuji série NB.

Paramètres de connexion par défaut de l'IHM série HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Paramètre**               | **Valeur par défaut**       | **Plage de réglage**                         |
| **Type d'automate**         | Fuji NB Series              | Fuji NB Series                               |
| **Type de port**            | RS422                       | RS422                                        |
| **Vitesse (baud)**          | 19200                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bits de données**         | 8                           | 7/8                                          |
| **Parité**                  | ODD                         | EVEN/ODD/NONE                                |
| **Bits de stop**            | 1                           | 1/2                                          |
| **N° de station automate**  | 0                           | 0~255                                        |
| **N° de station IHM**       | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Fonction**            | **Prise en charge**         |
| **Simulation hors ligne** | Oui                       |
| **Simulation en ligne**  | Oui                        |
| **Mode étendu**         | Oui                         |

**3. Registres utilisables et plages d'adresses**

|                   |                    |                 |                                        |
|-------------------|--------------------|-----------------|----------------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**                      |
| **X**             | hhh                | 0~7ff           | Bit : entrée, lecture seule            |
| **Y**             | hhh                | 0~7ff           | Bit : sortie                           |
| **M**             | hhhh               | 0~7fff          | Bit : relais interne                   |
| **SM**            | hhhh               | 8000~81ff       | Bit : relais interne                   |
| **L**             | hhh                | 0~5ff           | Bit : relais à verrouillage            |
| **S**             | hh                 | 0~ff            | Bit : relais d'étape                   |
| **T**             | hhh                | 0~1ff           | Bit : état de temporisation            |
| **C**             | hh                 | 0~ff            | Bit : état de compteur                 |
| **D**             | hhhh               | 0~7fff          | Mot : registre de données              |
| **SD**            | hhhh               | 8000~80ff       | Mot : registre de données              |
| **TV**            | hhh                | 0~1ff           | Mot : valeur courante de temporisation |
| **CV**            | hh                 | 0~ff            | Mot : valeur courante de compteur      |

<img src="../../drivers/fuji.files/image005.gif" width="595" />

Remarque :

h : hexadécimal, plage de saisie 0-9, a-f ;

Bit dans les remarques : le registre ne s'utilise que comme bit ;

Mot dans les remarques : le registre ne s'utilise que comme mot ;

Lecture seule dans les remarques : le registre peut être lu mais pas écrit ;

Les noms et plages des registres peuvent varier selon le modèle d'équipement.

Pour le détail des noms et plages, consultez la documentation technique de l'équipement connecté.

<img src="../../drivers/fuji.files/image005.gif" width="595" />
