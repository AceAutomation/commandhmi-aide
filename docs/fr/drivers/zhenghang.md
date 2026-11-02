# Pilote d'équipements ZhengHang

Ce pilote permet aux IHM de la série HM de lire et d'écrire les données ou l'état des registres des automates ZhengHang série A5. La liaison série est établie entre le port série de l'écran tactile et celui de l'automate ZhengHang A5. Avant d'utiliser ce pilote, lisez attentivement ce chapitre et les spécifications techniques de l'automate ZhengHang A5.

Établir la connexion avec un automate ZhengHang série A5

**1. Raccordement matériel**

Câble de liaison :

RS232 <span id="OLE_LINK2"></span><span id="OLE_LINK3"></span>

|                           |     |                    |     |
|---------------------------|-----|--------------------|-----|
| **HM　ＨＭＩ　COM1/COM2** |     | **ZhengHang A5　** |     |
| 2                         | RX  | 2                  | TX  |
| 3                         | TX  | 3                  | RX  |
| 5                         | GND | 5                  | GND |

<img src="../../drivers/zhenghang.files/image002.gif" width="130" /><img src="../../drivers/zhenghang.files/image003.gif" width="290" /><img src="../../drivers/zhenghang.files/image004.gif" width="130" />

Le connecteur de l'IHM est un DB9F ; celui de l'automate ZhengHang A5 est un DB9M.

**2. Paramétrage logiciel**

Choisissez ZhengHang Electronics dans le service d'équipement de la connexion.

Choisissez l'élément correspondant au modèle d'automate connecté ou au protocole pris en charge dans le service d'équipement de la connexion.

Vérifiez que les paramètres de communication de l'écran tactile et le numéro de station correspondent à ceux de l'automate connecté.

Pour le paramétrage de l'automate, consultez la documentation technique des automates ZhengHang série A5.

Paramètres de connexion par défaut de l'IHM série HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Paramètre**               | **Valeur par défaut**       | **Plage de réglage**                         |
| **Type d'automate**         | A5 Series                   | A5 Series                                    |
| **Type de port**            | RS232                       | RS232/RS422/RS485                            |
| **Vitesse (baud)**          | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bits de données**         | 8                           | 7/8                                          |
| **Parité**                  | NONE                        | EVEN/ODD/NONE                                |
| **Bits de stop**            | 1                           | 1/2                                          |
| **N° de station automate**  | 1                           | 0~255                                        |
| **N° de station IHM**       | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Fonction**            | **Prise en charge**         |
| **Simulation hors ligne** | Oui                       |
| **Simulation en ligne**   | Oui                       |
| **Mode étendu**         | Oui                         |

**3. Registres utilisables et plages d'adresses**

|                   |                    |                 |                                                                           |
|-------------------|--------------------|-----------------|---------------------------------------------------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**                                                         |
| **I**             | dd.o               | 0.0 à 15.7      | Bit : image des entrées, lecture seule                                    |
| **Q**             | dd.o               | 0.0 à 15.7      | Bit : image des sorties                                                   |
| **M**             | dddd.o             | 0.0 à 4095.7    | Bit : mémentos                                                            |
| **VW**            | dddd               | 0 à 1998        | Mot : mémoire variable, registre 8 bits, chaque mot occupe deux adresses  |
| **AIW**           | d                  | 0 à 9           | Mot : entrée analogique, lecture seule                                    |
| **AQW**           | d                  | 0 à 9           | Mot : sortie analogique, écriture seule                                   |

<img src="../../drivers/zhenghang.files/image005.gif" width="595" />

Remarque :

d : décimal, plage de saisie 0-9 ;

o : octal, plage de saisie 0-7 ;

Mot dans les remarques : le registre ne s'utilise que comme mot ;

Bit dans les remarques : le registre ne s'utilise que comme bit ;

Lecture seule dans les remarques : le registre peut être lu mais pas écrit ;

Les noms et plages des registres peuvent varier selon le modèle d'équipement.

Pour le détail des noms et plages, consultez la documentation technique de l'équipement connecté

<img src="../../drivers/zhenghang.files/image005.gif" width="595" />
