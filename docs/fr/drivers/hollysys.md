# Pilote d'équipements HollySys

Ce pilote permet aux écrans tactiles de lire et d'écrire les données ou l'état des registres des automates HollySys série LM. La liaison série est établie entre le port série de l'écran tactile et celui de l'automate HollySys LM. Avant d'utiliser ce pilote, lisez attentivement ce chapitre et les spécifications techniques de l'automate HollySys LM.

**Établir la connexion avec un automate HOLLYSYS**

**1.  Raccordement matériel**

Câble de liaison :

RS232 (port série, protocole RS232)

|                             |     |                        |     |
|-----------------------------|-----|------------------------|-----|
| **IHM série HM COM1/COM2** |     | **HollySys série LM** |     |
| 2                           | RX  | 3                      | TX  |
| 3                           | TX  | 2                      | RX  |
| 5                           | GND | 5                      | GND |

<img src="../../drivers/hollysys.files/image002.gif" width="130" /><img src="../../drivers/hollysys.files/image003.gif" width="290" /><img src="../../drivers/hollysys.files/image004.gif" width="130" />

Le connecteur de l'IHM série HM est un DB9F ; celui de l'automate HollySys LM est un DB9M.

**2. Paramétrage logiciel**

Choisissez HollySys Group dans le service d'équipement de la connexion.

Choisissez l'élément correspondant au modèle d'automate connecté ou au protocole pris en charge dans le service d'équipement de la connexion.

Vérifiez que les paramètres de communication de l'écran tactile et le numéro de station correspondent à ceux de l'automate connecté.

Pour le paramétrage de l'automate, voir la documentation technique des automates HollySys série LM.

Paramètres de connexion par défaut de l'IHM série HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Paramètre**               | **Valeur par défaut**       | **Plage de réglage**                         |
| **Type d'automate**         | HollySys LM Series          | HollySys LM Series                           |
| **Type de port**            | RS232                       | RS232/RS422/RS485                            |
| **Vitesse (baud)**          | 38400                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bits de données**         | 8                           | 7/8                                          |
| **Parité**                  | NONE                        | EVEN/ODD/NONE                                |
| **Bits de stop**            | 1                           | 1/2                                          |
| **N° de station automate**  | 51                          | 0~255                                        |
| **N° de station IHM**       | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Fonction**            | **Prise en charge**         |
| **Simulation hors ligne** | Oui                       |
| **Simulation en ligne**  | Oui                        |
| **Mode étendu**         | Non                         |

**3. Registres utilisables et plages d'adresses**

|                   |                    |                 |                                                                                                       |
|-------------------|--------------------|-----------------|-------------------------------------------------------------------------------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**                                                                                     |
| **IX**            | ddd.o              | 0.0~511.7       | Bit : zone I, lecture seule                                                                           |
| **QX**            | ddd.o              | 0.0~511.7       | Bit : zone Q                                                                                          |
| **MX**            | dddd.o             | 0.0~7816.7      | Bit : zone M                                                                                          |
| **IW**            | ddd                | 0~510           | Mot :<span id="OLE_LINK284"></span> zone I, registre 8 bits, chaque mot occupe deux adresses          |
| **QW**            | ddd                | 0~510           | Mot : <span id="OLE_LINK285"></span>zone Q, registre 8 bits, chaque mot occupe deux adresses          |
| **MW**            | dddd               | 0~8190          | Mot : zone M, registre 8 bits, chaque mot occupe deux adresses                                        |

<img src="../../drivers/hollysys.files/image005.gif" width="600" />

Remarque :

d : décimal, plage de saisie 0-9 ;

o : octal, plage de saisie 0-7 ;

Mot dans les remarques : le registre ne s'utilise que comme mot ;

Bit dans les remarques : le registre ne s'utilise que comme bit ;

Registre 8 bits dans les remarques : l'écart d'adresse entre deux mots consécutifs du registre est de 2 ;

Lecture seule dans les remarques : le registre peut être lu mais pas écrit ;

Les noms et plages des registres peuvent varier selon le modèle d'équipement.

Pour le détail des noms et plages, consultez la documentation technique de l'équipement connecté

<img src="../../drivers/hollysys.files/image005.gif" width="600" />
