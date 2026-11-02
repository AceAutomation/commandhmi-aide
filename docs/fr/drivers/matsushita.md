# Pilote d'équipements Matsushita

Ce pilote permet aux IHM de la série HM de lire et d'écrire les données ou l'état des registres des automates Matsushita série FP. La liaison série est établie entre le port série de l'écran tactile et celui de l'automate Matsushita FP. Avant d'utiliser ce pilote, lisez attentivement ce chapitre et les spécifications techniques de l'automate Matsushita FP.

Établir la connexion avec un automate Matsushita série FP

**1.  Raccordement matériel**

Câble de liaison :

RS232-FP0/FP2/FP2SH/FPM

|                                                                                                                                                 |     |                          |     |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-----|--------------------------|-----|
| <span id="OLE_LINK60"></span><span id="OLE_LINK61"></span><span id="OLE_LINK62"></span><span id="OLE_LINK27"></span>**IHM série HM COM1/COM2** |     | **Matsushita série FP** |     |
| 2                                                                                                                                               | RX  | 3                        | TX  |
| 3                                                                                                                                               | TX  | 2                        | RX  |
| 5                                                                                                                                               | GND | 1                        | GND |

<img src="../../drivers/matsushita.files/image002.gif" width="280" /><img src="../../drivers/matsushita.files/image003.gif" width="129" /><img src="../../drivers/matsushita.files/image004.gif" width="145" />

Le connecteur de l'IHM est un DB9F ; celui de l'automate Matsushita FP est un MD5M.

RS422-FP1

|                             |     |                      |     |
|-----------------------------|-----|----------------------|-----|
| **IHM série HM COM1/COM2** |     | Matsushita série FP |     |
| 6                           | RX- | 2                    | TX- |
| 7                           | RX+ | 5                    | TX+ |
| 8                           | TX- | 3                    | RX- |
| 9                           | TX+ | 6                    | RX+ |

<img src="../../drivers/matsushita.files/image005.gif" width="140" /><img src="../../drivers/matsushita.files/image006.gif" width="129" /><img src="../../drivers/matsushita.files/image007.gif" width="280" />

Le connecteur de l'IHM est un DB9F ; celui de l'automate Matsushita FP est un MD8M.

**2. Paramétrage logiciel**

Choisissez MATSUSHITA dans le service d'équipement de la connexion.

Choisissez l'élément correspondant au modèle d'automate connecté ou au protocole pris en charge dans le service d'équipement de la connexion.

Vérifiez que les paramètres de communication de l'écran tactile et le numéro de station correspondent à ceux de l'automate connecté.

Pour le paramétrage de l'automate, voir la documentation technique des automates Matsushita série FP.

Paramètres de connexion par défaut de l'IHM série HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Paramètre**               | **Valeur par défaut**       | **Plage de réglage**                         |
| **Type d'automate**         | FP Series                   | FP Series                                    |
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
| **Mode étendu**         | Non                         |

**3. Registres utilisables et plages d'adresses**

|                   |                    |                 |                                        |
|-------------------|--------------------|-----------------|----------------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**                      |
| **X**             | ddddh              | 0~9999f         | Bit : entrée externe, lecture seule    |
| **Y**             | ddddh              | 0~9999f         | Bit : sortie externe                   |
| **R**             | ddddh              | 0~9999f         | Bit : relais interne                   |
| **L**             | ddddh              | 0~9999f         | Bit : relais de liaison                |
| **T**             | dddd               | 0~9999          | Bit : état de temporisation, lecture seule |
| **C**             | dddd               | 0~9999          | Bit : état de compteur, lecture seule  |
| **WX**            | dddd               | 0~9999          | Mot : entrée externe, lecture seule    |
| **WY**            | dddd               | 0~9999          | Mot : sortie externe                   |
| **WR**            | dddd               | 0~9999          | Mot : relais interne                   |
| **WL**            | dddd               | 0~9999          | Mot : relais de liaison                |
| **DT**            | ddddd              | 0~99999         | Mot : registre de données              |
| **LD**            | ddddd              | 0~99999         | Mot : registre de liaison              |
| **FL**            | ddddd              | 0~99999         | Mot : registre de fichier              |
| **SV**            | dddd               | 0~9999          | Mot : zone des consignes temporisation/compteur |
| **EV**            | dddd               | 0~9999          | Mot : zone des valeurs courantes temporisation/compteur |

<img src="../../drivers/matsushita.files/image008.gif" width="595" />

Remarque :

d : décimal, plage de saisie 0-9 ;

h : hexadécimal, plage de saisie 0-9, a-f ;

Mot dans les remarques : le registre ne s'utilise que comme mot ;

Bit dans les remarques : le registre ne s'utilise que comme bit ;

Lecture seule dans les remarques : le registre peut être lu mais pas écrit ;

Les noms et plages des registres peuvent varier selon le modèle d'équipement.

Pour le détail des noms et plages, consultez la documentation technique de l'équipement connecté

<img src="../../drivers/matsushita.files/image009.gif" width="595" />
