# Pilote d'équipements Siemens

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Ce pilote permet aux IHM de la série HM de lire et d'écrire les données ou l'état des registres des automates Siemens S7-200/300/1200. La liaison est établie entre le port de l'écran tactile et celui de l'automate Siemens S7-200/300/1200tcp. Avant d'utiliser ce pilote, lisez attentivement ce chapitre et les spécifications techniques de l'automate Siemens S7-200/300/1200tcp.</p></td>
</tr>
<tr class="even">
<td><p> Établir la connexion avec un automate Siemens S7-200/300/1200tcp</p>
<p><strong>1. 1 Raccordement matériel</strong></p>
<p>Câble de liaison :</p>
<p>RS485-Siemens S7-200<span id="OLE_LINK1"></span><span id="OLE_LINK2"></span><span id="OLE_LINK3"></span></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>IHM série HM COM1/COM2</strong></p></td>
<td colspan="2"><p>Siemens série S7-200</p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p>TX-</p></td>
<td><p>8</p></td>
<td><p>TX-</p></td>
</tr>
<tr class="odd">
<td><p>9</p></td>
<td><p>TX+</p></td>
<td><p>3</p></td>
<td><p>TX+</p></td>
</tr>
</tbody>
</table>
<p><img src="../../drivers/siemens.files/image002.gif" width="130" /><img src="../../drivers/siemens.files/image003.gif" width="290" /><img src="../../drivers/siemens.files/image004.gif" width="130" /></p></td>
</tr>
</tbody>
</table>

  RS232-Siemens S7-300

|                             |     |                           |     |
|-----------------------------|-----|---------------------------|-----|
| **IHM série HM COM1/COM2** |     | **Siemens série S7-300** |     |
| **2**                       | RX  | 3                         | TX  |
| **3**                       | TX  | 2                         | RX  |
| **5**                       | GND | 5                         | GND |

|     |                                                      |     |                                                      |
|-----|------------------------------------------------------|-----|------------------------------------------------------|
|     |                                                      |     |                                                      |
|     | <img src="../../drivers/siemens.files/image005.gif" width="408" /> |     | <img src="../../drivers/siemens.files/image006.gif" width="129" /> |

Le connecteur de l'IHM est un DB9F ; celui du port MPI de l'automate Siemens S7-300 est un DB9M.

Établir la connexion avec un automate Siemens S7-200/300/1200

**1. 2 Raccordement matériel**

Câble de liaison :

  Câble RJ45 ;

  Brochage du RJ45 :

**<img src="../../drivers/siemens.files/image014.jpg" width="343" />**

1、 Réglage de l'IP et du numéro de port

Dans la page Général des propriétés du port de communication, choisissez « Port Ethernet » comme interface de connexion et « SIEMENS », « Siemens S7-200(TCP/IP)/Siemens S7-300(TCP/IP)/Siemens S7-1200(TCP) » comme service de connexion ;

Dans la page Paramètres des propriétés du port de communication, réglez l'IP et le numéro de port.

Attention :

L'adresse IP de l'automate doit être dans le même sous-réseau que l'IHM, c'est-à-dire qu'il suffit de régler le masque de sous-réseau à 255.255.255.0.

2、 Dans le paramétrage de l'automate Siemens 1200, vérifiez si la fonction de protection d'accès est active ; si nécessaire, cochez l'option correspondante, puis recompilez et chargez le programme dans l'automate.

Dans TIA Portal, chargez le programme de l'automate ou créez un nouveau projet Siemens 1200 ; faites un clic droit sur l'automate et choisissez « Propriétés » ; dans « Protection », cochez « Autoriser l'accès via la communication PUT/GET par le partenaire distant (API, HMI, OPC...) », comme sur la figure ci-dessous :

**<img src="../../drivers/siemens.files/image015.jpg" width="1152" />**

**2. Paramétrage logiciel**

Choisissez SIEMENS dans le service d'équipement de la connexion.

Choisissez l'élément correspondant au modèle d'automate connecté ou au protocole pris en charge dans le service d'équipement de la connexion.

Vérifiez que les paramètres de communication de l'écran tactile et le numéro de station correspondent à ceux de l'automate connecté.

Pour le paramétrage de l'automate, consultez la documentation technique des automates Siemens S7-200/300

Paramètres de connexion par défaut de l'IHM série HM

|                             |                         |                                    |                                              |
|-----------------------------|-------------------------|------------------------------------|----------------------------------------------|
| **Paramètre**               | Valeur par défaut       |                                    | Plage de réglage                             |
| **Type d'automate**         | S7-200(PPI)             |                                    | S7-200(PPI)/ S7-300(MPI)                     |
| **Type de port**            | RS485                   |                                    | RS232/RS422/RS485                            |
| **Vitesse (baud)**          | 19200                   |                                    | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bits de données**         | 8                       |                                    | 7/8                                          |
| **Parité**                  | EVEN                    |                                    | EVEN/ODD/NONE                                |
| **Bits de stop**            | 1                       |                                    | 1/2                                          |
| **N° de station automate**  | 2                       |                                    | 1 à 255                                      |
| **N° de station IHM**       | 0                       |                                    | 0 à 255                                      |
| **Fonction**                |                         | **Prise en charge**                |                                              |
| **Simulation hors ligne**   |                         | Oui                                |                                              |
| **Simulation en ligne**     |                         | Oui                                |                                              |
| **Mode étendu**             |                         | Oui : S7-200(PPI)/ Non : S7-300(MPI) |                                              |
|                             |                         |                                    |                                              |

**3. Registres utilisables et plages d'adresses**

Siemens S7-200

|                   |                    |                 |                                                                                                    |
|-------------------|--------------------|-----------------|----------------------------------------------------------------------------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**                                                                                  |
| **I**             | dd.o               | 0.0 à 4095.7    | Bit : image des entrées, lecture seule                                                             |
| **Q**             | dd.o               | 0.0 à 4095.7    | Bit : image des sorties                                                                            |
| **M**             | dd.o               | 0.0 à 4095.7    | Bit : mémentos                                                                                     |
| **S**             | dd.o               | 0.0 à 4095.7    | Bit : relais de commande séquentielle                                                              |
| **SM**            | ddd.o              | 0.0 à 4095.7    | Bit : mémentos spéciaux, SM0.0-SM29.7 en lecture seule                                             |
| **T**             | ddd                | 0 à 255         | Bit : état de temporisation, lecture seule                                                         |
| **C**             | ddd                | 0 à 255         | Bit : état de compteur, lecture seule                                                              |
| **VB_Bit**        | ddddd.o            | 0.0 à 10239.7   | Bit : bit de mémoire variable                                                                      |
| **IW**            | dd                 | 0 à 4095        | Mot : image des entrées, lecture seule, registre 8 bits, chaque mot occupe deux adresses           |
| **QW**            | dd                 | 0 à 4095        | Mot : image des sorties, registre 8 bits, chaque mot occupe deux adresses                          |
| **MW**            | dd                 | 0 à 4095        | Mot : mémentos, registre 8 bits, chaque mot occupe deux adresses                                   |
| **SW**            | dd                 | 0 à 4095        | Mot : relais de commande séquentielle, registre 8 bits, chaque mot occupe deux adresses            |
| **SMW**           | ddd                | 0 à 4095        | Mot : mémentos spéciaux, SMW0-SMW29 en lecture seule, registre 8 bits, chaque mot occupe deux adresses |
| **VB**            | ddddd              | 0 à 10239       | Mot : mémoire variable, registre 8 bits                                                            |
| **VW**            | ddddd              | 0 à 10238       | Mot : mémoire variable, registre 8 bits, chaque mot occupe deux adresses                           |
| **VD**            | ddddd              | 0 à 10236       | Double mot : mémoire variable, registre 8 bits, chaque double mot occupe quatre adresses           |
| **TV**            | ddd                | 0 à 255         | Mot : valeur courante de temporisation                                                             |
| **CV**            | ddd                | 0 à 255         | Mot : valeur courante de compteur                                                                  |
| **AIW**           | dd                 | 0 à 62          | Mot : entrée analogique, lecture seule, registre 8 bits, chaque mot occupe deux adresses           |
| **AQW**           | dd                 | 0 à 62          | Mot : sortie analogique, écriture seule, registre 8 bits, chaque mot occupe deux adresses          |

Siemens S7-300 / Siemens S7-300(MPI) / Siemens S7-300tcp

|                   |                    |                     |                                                                                                                                                            |
|-------------------|--------------------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**                                                                                                                                          |
| **I**             | dddd.o             | 0.0 à 4095.7        | Bit : image des entrées                                                                                                                                    |
| **Q**             | dddd.o             | 0.0 à 4095.7        | Bit : image des sorties                                                                                                                                    |
| **M**             | dddd.o             | 0.0 à 4095.7        | Bit : mémentos                                                                                                                                             |
| **DB_Bit**        | DDD:dddd.o         | 0:0.0 à 255:8192.7  | Bit : bit d'un mot de bloc de données DB ; n° de bloc DD 0 à 255, mot dddd 0 à 8192, bit o 0 à 7                                                          |
| **IW**            | dddd               | 0 à 4095            | Mot : image des entrées, registre 8 bits, chaque mot occupe deux adresses                                                                                  |
| **QW**            | dddd               | 0 à 4095            | Mot : image des sorties, registre 8 bits, chaque mot occupe deux adresses                                                                                  |
| **MW**            | dddd               | 0 à 4095            | Mot : mémentos, registre 8 bits, chaque mot occupe deux adresses                                                                                           |
| **DBW**           | DDD:dddd           | 0:0 à 255:8192      | Mot : bloc de données DB ; n° de bloc DD 0 à 255, mot dddd 0 à 8192, registre 8 bits, chaque mot occupe deux adresses                                     |
| **DBD**           | DDD:dddd           | 0:0 à 255:8192      | Double mot : bloc de données DB ; n° de bloc DD 0 à 255, mot dddd 0 à 8192, registre 8 bits, chaque double mot occupe quatre adresses                     |

Siemens S7-1200tcp

|                   |                    |                  |                                                                                                                                                            |
|-------------------|--------------------|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**                                                                                                                       |
| **I**             | dddd.o             | 0.0~1024.7       | Bit : image des entrées                                                                                                                                    |
| **Q**             | dddd.o             | 0.0~1024.7       | Bit : image des sorties                                                                                                                                    |
| **M**             | dddd.o             | 0.0~8191.7       | Bit : mémentos                                                                                                                                             |
| **DB_Bit**        | DDD:dddd.o         | 0:0.0~255:8192.7 | Bit : bit d'un mot de bloc de données DB ; n° de bloc DD 0 à 255, mot dddd 0 à 8192, bit o 0 à 7                                                          |
| **IW**            | dddd               | 0~1024           | Mot : image des entrées, registre 8 bits, chaque mot occupe deux adresses                                                                                  |
| **QW**            | dddd               | 0~1024           | Mot : image des sorties, registre 8 bits, chaque mot occupe deux adresses                                                                                  |
| **MW**            | dddd               | 0~8191           | Mot : mémentos, registre 8 bits, chaque mot occupe deux adresses                                                                                           |
| **DBW**           | DDD:dddd           | 0:0~255:8192     | Mot : bloc de données DB ; n° de bloc DD 0 à 255, mot dddd 0 à 8192, registre 8 bits, chaque mot occupe deux adresses                                     |
| **DBD**           | DDD:dddd           | 0:0~255:8192     | Double mot : bloc de données DB ; n° de bloc DD 0 à 255, mot dddd 0 à 8192, registre 8 bits, chaque double mot occupe quatre adresses                     |

LOGO_TCP

|                   |                    |                 |                                |
|-------------------|--------------------|-----------------|--------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques** |
| **I**             | dd                 | 1~64            | Bit : image des entrées        |
| **Q**             | dd                 | 1~64            | Bit : image des sorties        |
| **M**             | ddd                | 1~112           | Bit : mémentos                 |
| **VB**            | dddd.o             | 0.0~1023.7      | Bit                            |
| **AI**            | dd                 | 1~16            | Mot : image des entrées        |
| **AQ**            | dd                 | 1~16            | Mot : image des sorties        |
| **AM**            | dd                 | 1~64            | Mot : mémentos                 |
| **VW**            | dddd               | 0~511           | Mot                            |

<img src="../../drivers/siemens.files/image007.gif" width="595" />

Remarque :

d : décimal, plage de saisie 0-9 ;

o : octal, plage de saisie 0-7 ;

DDD : numéro de bloc, plage de saisie 0-255 ;

Mot dans les remarques : le registre ne s'utilise que comme mot ;

Double mot dans les remarques : le type de données du registre dans la configuration doit être 32 bits ;

Bit dans les remarques : le registre ne s'utilise que comme bit ;

Lecture seule dans les remarques : le registre peut être lu mais pas écrit ;

Les noms et plages des registres peuvent varier selon le modèle d'équipement.

Pour le détail des noms et plages, consultez la documentation technique de l'équipement connecté

<img src="../../drivers/siemens.files/image008.gif" width="595" />
