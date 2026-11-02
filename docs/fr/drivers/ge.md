# Pilote d'équipements GE

Ce pilote permet aux IHM de la série HM de lire et d'écrire les données ou l'état des registres des automates GE Fanuc. La liaison série est établie entre le port série de l'IHM et celui de l'automate GE Fanuc. Avant d'utiliser ce pilote, lisez attentivement ce chapitre et les spécifications techniques de l'automate GE Fanuc.

**1. Raccordement matériel**

Câble de liaison :

RS232 (port série, protocole RS232)

|                             |     |                     |     |
|-----------------------------|-----|---------------------|-----|
| **IHM série HM COM1/COM2** |     | **GE Fanuc** |     |
| 2                           | RX  | 4                   | TX  |
| 3                           | TX  | 3                   | RX  |
| 5                           | GND | 8                   | GND |

|     |                                                 |     |                                                 |     |                                                |
|-----|-------------------------------------------------|-----|-------------------------------------------------|-----|------------------------------------------------|
|     |                                                 |     |                                                 |     |                                                |
|     |                                                 |     |                                                 |     | <img src="../../drivers/ge.files/image002.gif" width="97" /> |
|     | <img src="../../drivers/ge.files/image003.gif" width="130" /> |     |                                                 |     |                                                |
|     |                                                 |     | <img src="../../drivers/ge.files/image004.gif" width="278" /> |     |                                                |
|     |                                                 |     |                                                 |     |                                                |
|     |                                                 |     |                                                 |     |                                                |

Le connecteur de l'IHM série HM est un DB9F ; celui de l'automate GE Fanuc est un RJ45.

**2. Paramétrage logiciel**

Choisissez GE Corporation dans le service d'équipement de la connexion.

Choisissez l'élément correspondant au modèle d'automate connecté ou au protocole pris en charge dans le service d'équipement de la connexion.

Vérifiez que les paramètres de communication de l'écran tactile et le numéro de station correspondent à ceux de l'automate connecté.

Pour le paramétrage de l'automate, voir la documentation technique des automates GE Fanuc.

Paramètres de connexion par défaut de l'IHM série HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Paramètre**               | **Valeur par défaut**       | **Plage de réglage**                         |
| **Type d'automate**         | GE Fanuc SNP-X              | GE Fanuc SNP-X/ GE Fanuc CCM                 |
| **Type de port**            | RS232                       | RS232/RS422/RS485                            |
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
| **Mode étendu**         | Non                         |

**3. Registres utilisables et plages d'adresses**

|                   |                    |                 |                            |
|-------------------|--------------------|-----------------|----------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**          |
| **%I**            | ddddd              | 1~10000         | Bit : entrée TOR           |
| **%Q**            | ddddd              | 1~10000         | Bit : sortie TOR           |
| **%M**            | ddddd              | 1~10000         | Bit : usage interne        |
| **%S**            | ddd                | 1~128           | Bit : usage système, lecture seule |
| **%SA**           | ddd                | 1~128           | Bit : usage système, lecture seule |
| **%SB**           | ddd                | 1~128           | Bit : usage système, lecture seule |
| **%SC**           | ddd                | 1~128           | Bit : usage système, lecture seule |
| **%T**            | ddd                | 1~256           | Bit : état temporaire      |
| **%G**            | dddd               | 1~7680          | Bit : global Genius        |
| **%AI**           | ddddd              | 1~10000         | Mot : entrée analogique    |
| **%AQ**           | ddddd              | 1~10000         | Mot : sortie analogique    |
| **%R**            | ddddd              | 1~32640         | Mot : mémoire registres    |

 <img src="../../drivers/ge.files/image005.gif" width="595" />

Remarque :

d : décimal, plage de saisie 0-9 ;

o : octal, plage de saisie 0-7 ;

Bit dans les remarques : le registre ne s'utilise que comme bit ;

Mot dans les remarques : le registre ne s'utilise que comme mot ;

Lecture seule dans les remarques : le registre peut être lu mais pas écrit ;

Les noms et plages des registres peuvent varier selon le modèle d'équipement.

Pour le détail des noms et plages, consultez la documentation technique de l'équipement connecté.

<img src="../../drivers/ge.files/image005.gif" width="595" />
