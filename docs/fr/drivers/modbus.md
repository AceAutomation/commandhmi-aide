# Pilote d'équipements Modbus

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Ce pilote permet aux IHM de la série HM de lire et d'écrire les données ou l'état des équipements <span id="OLE_LINK37"></span><span id="OLE_LINK38"></span>MODBUS. La liaison série est établie entre le port série de l'écran tactile et celui de l'équipement MODBUS. Avant d'utiliser ce pilote, lisez attentivement ce chapitre et les spécifications techniques de l'équipement MODBUS.</p></td>
</tr>
<tr class="even">
<td><p>Établir la connexion avec un équipement MODBUS</p>
<p><strong>1.</strong> <strong>Raccordement matériel</strong></p>
<p>Câble de liaison :</p>
<p>RS232<span id="OLE_LINK24"></span><span id="OLE_LINK25"></span><span id="OLE_LINK26"></span></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><span id="OLE_LINK62"></span><span id="OLE_LINK63"></span><span id="OLE_LINK64"></span><strong>IHM série HM COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Équipement Modbus</strong></p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>Broche définie par l'utilisateur</p></td>
<td><p>TX</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>TX</p></td>
<td><p>Broche définie par l'utilisateur</p></td>
<td><p>RX</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>Broche définie par l'utilisateur</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table></td>
</tr>
</tbody>
</table>

<img src="../../drivers/modbus.files/image002.gif" width="157" /><img src="../../drivers/modbus.files/image003.gif" width="130" />

Le connecteur de l'IHM est un DB9F. Le brochage de l'équipement Modbus dépend de l'équipement.

**RS422**

|                                                                                                                    |     |                   |     |
|--------------------------------------------------------------------------------------------------------------------|-----|-------------------|-----|
| <span id="OLE_LINK72"></span><span id="OLE_LINK73"></span><span id="OLE_LINK74"></span>**IHM série HM COM1/COM2** |     | **Équipement Modbus** |     |
| 6                                                                                                                  | RX- | Broche définie par l'utilisateur | TX- |
| 7                                                                                                                  | RX+ | Broche définie par l'utilisateur | TX+ |
| 8                                                                                                                  | TX- | Broche définie par l'utilisateur | RX- |
| 9                                                                                                                  | TX+ | Broche définie par l'utilisateur | RX+ |

<img src="../../drivers/modbus.files/image004.gif" width="157" /><img src="../../drivers/modbus.files/image005.gif" width="130" />

Le connecteur de l'IHM est un DB9F. Le brochage de l'équipement Modbus dépend de l'équipement.

**RS485**

|                                                                                       |     |                   |     |
|---------------------------------------------------------------------------------------|-----|-------------------|-----|
| <span id="OLE_LINK78"></span><span id="OLE_LINK79"></span>**IHM série HM COM1/COM2** |     | **Équipement Modbus** |     |
| 8                                                                                     | D-  | Broche définie par l'utilisateur | B   |
| 9                                                                                     | D+  | Broche définie par l'utilisateur | A   |

<img src="../../drivers/modbus.files/image006.gif" width="157" /><img src="../../drivers/modbus.files/image007.gif" width="130" />

Le port de l'IHM est un connecteur femelle 9 broches trapézoïdal. Le brochage de l'équipement Modbus dépend de l'équipement.

**TCP/IP (connexion directe RJ45)**

|                                                                                                                    |      |                   |      |
|--------------------------------------------------------------------------------------------------------------------|------|-------------------|------|
| <span id="OLE_LINK82"></span><span id="OLE_LINK83"></span><span id="OLE_LINK84"></span>**IHM série HM COM1/COM2** |      | **Équipement Modbus** |      |
| 1                                                                                                                  | TX+  | 3                 | RX+  |
| 2                                                                                                                  | TX-  | 6                 | RX-  |
| 3                                                                                                                  | RX+  | 1                 | TX+  |
| 4                                                                                                                  | BD4+ | 4                 | BD4+ |
| 5                                                                                                                  | BD4- | 5                 | BD4- |
| 6                                                                                                                  | RX-  | 2                 | TX-  |
| 7                                                                                                                  | BD3+ | 7                 | BD3+ |
| 8                                                                                                                  | BD3- | 8                 | BD3- |

|     |                                                    |     |                                                     |     |                                                    |
|-----|----------------------------------------------------|-----|-----------------------------------------------------|-----|----------------------------------------------------|
|     |                                                    |     |                                                     |     |                                                    |
|     | <img src="../../drivers/modbus.files/image008.gif" width="95" /> |     |                                                     |     |                                                    |
|     |                                                    |     |                                                     |     | <img src="../../drivers/modbus.files/image009.gif" width="95" /> |
|     |                                                    |     | <img src="../../drivers/modbus.files/image010.gif" width="267" /> |     |                                                    |
|     |                                                    |     |                                                     |     |                                                    |
|     |                                                    |     |                                                     |     |                                                    |

<span id="OLE_LINK68"></span><span id="OLE_LINK69"></span><span id="OLE_LINK70"></span>

Le connecteur de l'IHM est un RJ45, celui de l'équipement Modbus aussi.

**TCP/IP (connexion RJ45 via routeur)**

|                       |      |               |      |
|-----------------------|------|---------------|------|
| **IHM HM COM1/COM2** |      | Équipement Modbus |      |
| 1                     | TX+  | 3             | RX+  |
| 2                     | TX-  | 6             | RX-  |
| 3                     | RX+  | 1             | TX+  |
| 4                     | BD4+ | 4             | BD4+ |
| 5                     | BD4- | 5             | BD4- |
| 6                     | RX-  | 2             | TX-  |
| 7                     | BD3+ | 7             | BD3+ |
| 8                     | BD3- | 8             | BD3- |

<img src="../../drivers/modbus.files/image011.gif" width="95" />

|     |                                                     |     |                                                    |
|-----|-----------------------------------------------------|-----|----------------------------------------------------|
|     |                                                     |     |                                                    |
|     |                                                     |     | <img src="../../drivers/modbus.files/image012.gif" width="95" /> |
|     | <img src="../../drivers/modbus.files/image013.gif" width="267" /> |     |                                                    |
|     |                                                     |     |                                                    |

Le connecteur de l'IHM est un RJ45, celui de l'équipement Modbus aussi.

**2. Paramétrage logiciel**

Choisissez Modbus dans le service d'équipement de la connexion.

Choisissez l'élément correspondant au modèle d'automate connecté ou au protocole pris en charge dans le service d'équipement de la connexion.

Vérifiez que les paramètres de communication de l'écran tactile et le numéro de station correspondent à ceux de l'automate connecté.

Pour le paramétrage de l'équipement, voir sa documentation technique.

Paramètres de connexion par défaut de l'IHM série HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Paramètre**               | **Valeur par défaut**       | **Plage de réglage**                         |
| **Type d'automate**         | RTU Master                  | RTU/RTU_S/ASCII/ASCII_S Master               |
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
| **Simulation en ligne**  | Oui                        |
| **Mode étendu**         | Oui                         |

<img src="../../drivers/modbus.files/image014.gif" width="595" />

Remarque : en RTU_S et ASCII_S, le code fonction d'écriture est toujours 0x10 (quelle que soit la longueur des données écrites) ;

· Avec le numéro de station 0, le système est en mode diffusion (broadcast).

**3. Registres utilisables et plages d'adresses**

|                   |                    |                 |                                                                                                  |
|-------------------|--------------------|-----------------|--------------------------------------------------------------------------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**                                                                                |
| 0x                | ddddd              | 0~65535         | Bit : bobine                                                                                     |
| 1x                | ddddd              | 0~65536         | Bit : entrée TOR, lecture seule                                                                  |
| 3x_Bit            | ddddd.DD           | 0.00~65535.15   | Bit : <span id="OLE_LINK100"></span>bit d'un registre d'entrée 16 bits, lecture seule            |
| 4x_Bit            | ddddd.DD           | 0.00~65535.15   | Bit : bit d'un registre de maintien 16 bits                                                      |
| 3x                | ddddd              | 0~65535         | Mot : registre d'entrée 16 bits, lecture seule                                                   |
| 4x                | ddddd              | 0~65535         | Mot : registre de maintien 16 bits                                                               |
| 3x_D              | ddddd              | 0~65535         | Double mot : registre d'entrée, 16 bits hauts et bas inversés par rapport à 3x, lecture seule    |
| 4x_D              | ddddd              | 0~65535         | Double mot : registre de maintien, 16 bits hauts et bas inversés par rapport à 4x                |

Modbus Slave

|                       |                             |                 |                                                                |
|-----------------------|-----------------------------|-----------------|----------------------------------------------------------------|
| **Registre interne**  | **Codes fonction pris en charge** | **Plage de saisie** | **Remarque**                                       |
| LB                    | 01/02/05/15                 | 0~59999         | Bit : lecture et écriture des adresses internes LB de l'écran tactile |
| LW                    | 03/04/06/16                 | 0~59999         | Mot : lecture et écriture des adresses internes de l'écran tactile |

<img src="../../drivers/modbus.files/image015.gif" width="595" />

Remarque :

d : décimal, plage de saisie 0-9 ;

DD : 16 bits, plage de saisie 0-15 ;

Mot dans les remarques : le registre ne s'utilise que comme mot ;

Double mot dans les remarques : le type de données du registre dans la configuration doit être 32 bits ;

Bit dans les remarques : le registre ne s'utilise que comme bit ;

Lecture seule dans les remarques : le registre peut être lu mais pas écrit ;

Les noms et plages des registres peuvent varier selon le modèle d'équipement.

Pour le détail des noms et plages, consultez la documentation technique de l'équipement connecté

<img src="../../drivers/modbus.files/image016.gif" width="595" />
