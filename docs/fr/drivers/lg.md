# Pilote d'équipements LG

Ce pilote permet aux IHM de la série HM de lire et d'écrire les données ou l'état des registres des automates LG série Master-K. La liaison série est établie entre le port série de l'écran tactile et celui de l'automate LG Master-K. Avant d'utiliser ce pilote, lisez attentivement ce chapitre et les spécifications techniques de l'automate LG Master-K.

Établir la connexion avec un automate LG série Master-K

**1. Raccordement matériel**

Câble de liaison :

RS232 avec protocole CNet<span id="OLE_LINK1"></span><span id="OLE_LINK2"></span><span id="OLE_LINK3"></span> (port série, protocole RS232)

|                                                                                                                    |     |                 |     |
|--------------------------------------------------------------------------------------------------------------------|-----|-----------------|-----|
| <span id="OLE_LINK60"></span><span id="OLE_LINK62"></span><span id="OLE_LINK61"></span>**IHM série HM COM1/COM2** |     | **LG Master-K** |     |
| 2                                                                                                                  | RX  | 7               | TX  |
| 3                                                                                                                  | TX  | 4               | RX  |
| 5                                                                                                                  | GND | 5               | GND |

<img src="../../drivers/lg.files/image002.gif" width="130" /><img src="../../drivers/lg.files/image003.gif" width="291" /><img src="../../drivers/lg.files/image004.gif" width="130" />

Le connecteur de l'IHM est un DB9F ; celui de l'automate LG Master-K est un DB9M.

RS232 avec protocole KLoader

|                                                                                       |     |                 |     |
|---------------------------------------------------------------------------------------|-----|-----------------|-----|
| <span id="OLE_LINK65"></span><span id="OLE_LINK66"></span>**IHM série HM COM1/COM2** |     | **LG Master-K** |     |
| 2                                                                                     | RX  | 3               | TX  |
| 3                                                                                     | TX  | 2               | RX  |
| 5                                                                                     | GND | 5               | GND |

<img src="../../drivers/lg.files/image005.gif" width="291" /><img src="../../drivers/lg.files/image006.gif" width="130" /><img src="../../drivers/lg.files/image007.gif" width="130" />

Le connecteur de l'IHM est un DB9F ; celui de l'automate LG Master-K est un DB9M.

RS<span id="OLE_LINK51"></span><span id="OLE_LINK52"></span>485

|                                                          |     |                 |
|----------------------------------------------------------|-----|-----------------|
| <span id="OLE_LINK67"></span>**IHM série HM COM1/COM2** |     | **LG Master-K** |
| 8                                                        | D-  | B               |
| 9                                                        | D+  | A               |

 <img src="../../drivers/lg.files/image008.gif" width="157" /><img src="../../drivers/lg.files/image009.gif" width="130" />

Le connecteur de l'IHM est un DB9F ; celui de l'automate LG Master-K est un bornier deux fils.

RS232-K10S1

|                             |     |                 |     |
|-----------------------------|-----|-----------------|-----|
| **IHM série HM COM1/COM2** |     | **LG Master-K** |     |
| 2                           | RX  | 4               | TX  |
| 3                           | TX  | 1               | RX  |
| 5                           | GND | 6               | GND |

Le connecteur de l'IHM est un DB9F ; celui de l'automate LG Master-K est un MD6M.

|     |                                                 |     |                                                 |
|-----|-------------------------------------------------|-----|-------------------------------------------------|
|     |                                                 |     |                                                 |
|     |                                                 |     | <img src="../../drivers/lg.files/image010.gif" width="146" /> |
|     | <img src="../../drivers/lg.files/image011.gif" width="401" /> |     |                                                 |
|     |                                                 |     |                                                 |

**2. Paramétrage logiciel**

Choisissez LG Industrial Systems dans le service d'équipement de la connexion.

Choisissez l'élément correspondant au modèle d'automate connecté ou au protocole pris en charge dans le service d'équipement de la connexion.

Vérifiez que les paramètres de communication de l'écran tactile et le numéro de station correspondent à ceux de l'automate connecté.

Pour le paramétrage de l'automate, voir la documentation technique des automates LG série Master-K.

Paramètres de connexion par défaut de l'IHM série HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Paramètre**               | **Valeur par défaut**       | **Plage de réglage**                         |
| **Type d'automate**         | LG Master-K Cnet            | LG Master-K Cnet/K Loader/K10s1              |
| **Type de port**            | RS232                       | RS232/RS422/RS485                            |
| **Vitesse (baud)**          | 19200                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bits de données**         | 8                           | 7/8                                          |
| **Parité**                  | NONE                        | EVEN/ODD/NONE                                |
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

Plage d'adresses utilisables des automates série Kxxx :

|               |                |             |                                |
|---------------|----------------|-------------|--------------------------------|
| Registre      | Format d'adresse | Plage de saisie | Remarques                  |
| P_Bit         | dddh           | 0~255f      | Bit : zone d'entrées/sorties   |
| M_Bit         | dddh           | 0~255f      | Bit : relais auxiliaire        |
| K_Bit         | dddh           | 0~255f      | Bit : relais de maintien       |
| L_Bit         | dddh           | 0~255f      | Bit : relais de liaison        |
| F_Bit         | dddh           | 0~255f      | Bit : relais spécial           |
| P             | dddh           | 0~255f      | Mot : zone d'entrées/sorties   |
| M             | dddh           | 0~255f      | Mot : relais auxiliaire        |
| K             | dddh           | 0~255f      | Mot : relais de maintien       |
| L             | dddh           | 0~255f      | Mot : relais de liaison        |
| F             | dddh           | 0~255f      | Mot : relais spécial           |
| T             | ddd            | 0~255       | Bit : relais de temporisation  |
| C             | ddd            | 0~255       | Bit : relais de compteur       |
| S             | dddd           | 0~9999      | Mot : registre d'étape         |
| D             | dddd           | 0~9999      | Mot : registre de données      |
| TV            | ddd            | 0~255       | Mot : valeur courante de temporisation |
| CV            | ddd            | 0~255       | Mot : valeur courante de compteur |

Plage d'adresses utilisables des automates série XGB CPU (communication via le port de téléchargement RS232 de l'automate) :

|                |              |              |                                   |
|----------------|--------------|--------------|-----------------------------------|
| **Registre**   | **Format d'adresse** | **Plage de saisie** | **Remarques**             |
| P_Bit          | ddddh        | 0-1023f      | Bit : zone d'entrées/sorties      |
| M_Bit          | ddddh        | 0-1023f      | Bit : relais auxiliaire           |
| F_Bit          | ddddh        | 0-1023f      | Bit : relais spécial              |
| L_Bit          | ddddh        | 0-2047f      | Bit : relais de liaison           |
| K_Bit          | ddddh        | 0-4095f      | Bit : relais de maintien          |
| D_Bit          | ddddh        | 0-10239f     |                                   |
| T              | dddd         | 0-1023       | Bit : relais de temporisation     |
| C              | dddd         | 0-1023       | Bit : relais de compteur          |
| TV             | dddd         | 0-1023       | Mot : valeur courante de temporisation |
| CV             | dddd         | 0-1023       | Mot : valeur courante de compteur |
| P              | dddd         | 0-1023       | Mot : zone d'entrées/sorties      |
| M              | dddd         | 0-1023       | Mot : relais auxiliaire           |
| F              | dddd         | 0-1023       | Mot : relais spécial （lecture seule） |
| L              | dddd         | 0-2047       | Mot : relais de liaison           |
| K              | dddd         | 0-4095       | Mot : relais de maintien          |
| D              | dddd         | 0-10239      | Mot : registre de données         |
| R              | dddd         | 0-10239      | Mot : registre d'étape            |
| ZR             | dddd         | 0-10239      | Mot :                             |
| S              | ddd          | 0-127        | Mot : registre d'étape            |
| Z              | ddd          | 0-127        | Mot :                             |
| U              | dd.dd        | 0.0-10.31    | Mot :（lecture seule）            |

Plage d'adresses utilisables des automates série XGB CNET :

|               |                |             |                         |
|---------------|----------------|-------------|-------------------------|
| Registre      | Format d'adresse | Plage de saisie | Remarques           |
| P             | dddh           | 0~127f      | Mot : zone d'entrées/sorties |
| M             | dddh           | 0~255f      | Mot : relais auxiliaire |
| K             | dddh           | 0~2559f     | Mot : relais de maintien |
| L             | dddh           | 0~1279f     | Mot : relais de liaison |
| F             | dddh           | 0~255f      | Mot : relais spécial    |
| T             | ddd            | 0~255       | Bit : relais de temporisation |
| C             | ddd            | 0~255       | Bit : relais de compteur |
| S             | ddd            | 0~127.99    | Mot : registre d'étape  |
| D             | dddd           | 0~5119      | Mot : registre de données |
| N             | dddd           | 0~3935      |                         |
| Z             | ddd            | 0~127       |                         |
| ZR            | dddd           | 0~1023      |                         |
| U             | d              | 0~7.31      |                         |

XGB TCP/IP

|                |              |              |                                   |
|----------------|--------------|--------------|-----------------------------------|
| **Registre**   | **Format d'adresse** | **Plage de saisie** | **Remarques**             |
| P_Bit          | ddddh        | 0-2047f      | Bit : zone d'entrées/sorties      |
| M_Bit          | ddddh        | 0-2047f      | Bit : relais auxiliaire           |
| F_Bit          | ddddh        | 0-2047f      | Bit : relais spécial              |
| L_Bit          | ddddh        | 0-4095f      | Bit : relais de liaison           |
| K_Bit          | ddddh        | 0-8191f      | Bit : relais de maintien          |
| T              | dddd         | 0-2047       | Bit : relais de temporisation     |
| C              | dddd         | 0-2047       | Bit : relais de compteur          |
| TV             | dddd         | 0-2047       | Mot : valeur courante de temporisation |
| CV             | dddd         | 0-2047       | Mot : valeur courante de compteur |
| P              | dddd         | 0-2047       | Mot : zone d'entrées/sorties      |
| M              | dddd         | 0-2047       | Mot : relais auxiliaire           |
| F              | dddd         | 0-2047       | Mot : relais spécial （lecture seule） |
| L              | dddd         | 0-4095       | Mot : relais de liaison           |
| K              | dddd         | 0-8191       | Mot : relais de maintien          |
| D              | ddddd        | 0-19999      | Mot : registre de données         |
| R              | ddddd        | 0-16383      |                                   |
| S              | ddd          | 0-127        | Mot : registre d'étape            |
| Z              | ddd          | 0-127        |                                   |
| U              | dd.dd        | 0.0-11.31    |                                   |
| N              | ddddd        | 0-10239      | Mot :（lecture seule）            |

<img src="../../drivers/lg.files/image012.gif" width="595" />

Remarque :

d : décimal, plage de saisie 0-9 ;

h : hexadécimal, plage de saisie 0-9, a-f ;

Mot dans les remarques : le registre ne s'utilise que comme mot ;

Bit dans les remarques : le registre ne s'utilise que comme bit ;

Les noms et plages des registres peuvent varier selon le modèle d'équipement.

Pour le détail des noms et plages, consultez la documentation technique de l'équipement connecté

<img src="../../drivers/lg.files/image013.gif" width="595" />
