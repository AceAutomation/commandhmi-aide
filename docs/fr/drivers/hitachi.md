# Pilote d'équipements Hitachi

Ce pilote permet aux IHM de la série HM de lire et d'écrire les données ou l'état des registres des automates Hitachi séries E/EH. La liaison série est établie entre le port série de l'IHM et celui de l'automate Hitachi E/EH. Avant d'utiliser ce pilote, lisez attentivement ce chapitre et les spécifications techniques de l'automate Hitachi E/EH.

**1. Raccordement matériel**

Câble de liaison :

RS232 (port série, protocole RS232)

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>IHM série HM COM1/COM2</strong></p></td>
<td colspan="3"><p><strong>Hitachi séries E/EH</strong></p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>5</p></td>
<td colspan="2"><p>SD</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>TX</p></td>
<td><p>6</p></td>
<td colspan="2"><p>RD</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>1</p></td>
<td colspan="2"><p>SG</p></td>
</tr>
<tr class="odd">
<td colspan="2" rowspan="2"></td>
<td><p>4</p></td>
<td><p>PHL</p></td>
<td rowspan="2"><p>4-7</p>
<p>Court-circuit</p></td>
</tr>
<tr class="even">
<td><p>7</p></td>
<td><p>DR</p></td>
</tr>
</tbody>
</table>

|     |                                                      |     |                                                      |     |                                                     |
|-----|------------------------------------------------------|-----|------------------------------------------------------|-----|-----------------------------------------------------|
|     |                                                      |     |                                                      |     |                                                     |
|     |                                                      |     |                                                      |     | <img src="../../drivers/hitachi.files/image002.gif" width="91" /> |
|     | <img src="../../drivers/hitachi.files/image003.gif" width="130" /> |     |                                                      |     |                                                     |
|     |                                                      |     | <img src="../../drivers/hitachi.files/image004.gif" width="278" /> |     |                                                     |
|     |                                                      |     |                                                      |     |                                                     |
|     |                                                      |     |                                                      |     |                                                     |

Le connecteur de l'IHM série HM est un DB9F ; celui de l'équipement est un RJ45.

**2. Paramétrage logiciel**

Choisissez Hitachi Industrial dans le service d'équipement de la connexion.

Choisissez l'élément correspondant au modèle d'automate connecté ou au protocole pris en charge dans le service d'équipement de la connexion.

Vérifiez que les paramètres de communication de l'écran tactile et le numéro de station correspondent à ceux de l'automate connecté.

Pour le paramétrage de l'automate, voir la documentation technique des automates Hitachi séries E/EH.

Paramètres de connexion par défaut de l'IHM série HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Paramètre**               | **Valeur par défaut**       | **Plage de réglage**                         |
| **Type d'automate**         | Hitachi E/EH Series         | Hitachi E/EH Series                          |
| **Type de port**            | RS232                       | RS232/RS422/RS485                            |
| **Vitesse (baud)**          | 19200                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bits de données**         | 7                           | 7/8                                          |
| **Parité**                  | EVEN                        | EVEN/ODD/NONE                                |
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

|                   |                    |                 |                                                                    |
|-------------------|--------------------|-----------------|--------------------------------------------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**                                                  |
| **X**             | hhhh               | 0~ffff          | Bit : entrée TOR externe, lecture seule                            |
| **Y**             | hhhh               | 0~ffff          | Bit : <span id="OLE_LINK247"></span>sortie TOR externe             |
| **M**             | hhhh               | 0~ffff          | Bit : relais interne                                               |
| **R**             | hhhh               | 0~ffff          | Bit : registre interne                                             |
| **T**             | hhhh               | 0~ffff          | Bit : état de temporisation                                        |
| **L**             | hhhh               | 0~ffff          | Bit : relais de liaison                                            |
| **WX**            | hhhh               | 0~ffff          | Mot : entrées TOR externes                                         |
| **WY**            | hhhh               | 0~ffff          | Mot : sorties TOR externes                                         |
| **WM**            | hhhh               | 0~ffff          | Mot : relais internes                                              |
| **WR**            | hhhh               | 0~ffff          | Mot : registre interne                                             |
| **WL**            | hhhh               | 0~ffff          | Mot : relais de liaison                                            |
| **TC**            | hhhh               | 0~ffff          | Mot : valeur courante de temporisation/compteur                    |

<img src="../../drivers/hitachi.files/image005.gif" width="595" />

Remarque :

h : hexadécimal, plage de saisie 0-9, a-f ;

Bit dans les remarques : le registre ne s'utilise que comme bit ;

Mot dans les remarques : le registre ne s'utilise que comme mot ;

Lecture seule dans les remarques : le registre peut être lu mais pas écrit ;

Les noms et plages des registres peuvent varier selon le modèle d'équipement.

Pour le détail des noms et plages, consultez la documentation technique de l'équipement connecté.

<img src="../../drivers/hitachi.files/image006.gif" width="595" />
