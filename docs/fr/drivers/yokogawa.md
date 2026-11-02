# Pilote d'équipements Yokogawa

Ce pilote permet aux IHM de la série HM de lire et d'écrire les données ou l'état des registres des automates Yokogawa série FA-M3. La liaison série est établie entre le port série de l'écran tactile et celui de l'automate Yokogawa FA-M3. Avant d'utiliser ce pilote, lisez attentivement ce chapitre et les spécifications techniques de l'automate Yokogawa FA-M3.

Établir la connexion avec un automate Yokogawa série FA-M3

**1. Raccordement matériel**

Câble de liaison :

RS232 <span id="OLE_LINK2"></span><span id="OLE_LINK3"></span>

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
<td colspan="2"><p>Série HM COM1/COM2</p></td>
<td colspan="3"><p><strong>Yokogawa série FA-M3</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>5</strong></p></td>
<td><p>GND</p></td>
<td><p>5</p></td>
<td><p>SG</p></td>
<td rowspan="2"><p>4-5 court-circuitées</p>
<p>résistance de 220 Ω en série</p></td>
</tr>
<tr class="odd">
<td><p><strong>6</strong></p></td>
<td><p>RX-</p></td>
<td><p>4</p></td>
<td><p>SDB</p></td>
</tr>
<tr class="even">
<td><p><strong>7</strong></p></td>
<td><p>RX+</p></td>
<td><p>3</p></td>
<td><p>SDA</p></td>
<td rowspan="2"><p>2-3 court-circuitées</p>
<p>résistance de 220 Ω en série</p></td>
</tr>
<tr class="odd">
<td><p><strong>8</strong></p></td>
<td><p>TX-</p></td>
<td><p>2</p></td>
<td><p>RDB</p></td>
</tr>
<tr class="even">
<td><p><strong>9</strong></p></td>
<td><p>TX+</p></td>
<td><p>1</p></td>
<td colspan="2"><p>RDA</p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td><p>6</p></td>
<td><p>CSA</p></td>
<td rowspan="2"><p>6-7 court-circuitées</p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td><p>7</p></td>
<td><p>ERA</p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td><p>8</p></td>
<td><p>CSB</p></td>
<td rowspan="2"><p>8-9 court-circuitées</p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td><p>9</p></td>
<td><p>ERB</p></td>
</tr>
</tbody>
</table>

Le connecteur de l'IHM est un DB9F ; celui de l'automate Yokogawa FA-M3 est un SIO.

**2. Paramétrage logiciel**

Choisissez Yokogawa Electric Corp. dans le service d'équipement de la connexion.

Choisissez l'élément correspondant au modèle d'automate connecté ou au protocole pris en charge dans le service d'équipement de la connexion.

Vérifiez que les paramètres de communication de l'écran tactile et le numéro de station correspondent à ceux de l'automate connecté.

Pour le paramétrage de l'automate, consultez la documentation technique des automates Yokogawa série FA-M3.

Paramètres de connexion par défaut de l'IHM série HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Paramètre**               | **Valeur par défaut**       | **Plage de réglage**                         |
| **Type d'automate**         | Yokogawa FA-M3              | Yokogawa FA-M3                               |
| **Type de port**            | RS422                       | RS232/RS422/RS485                            |
| **Vitesse (baud)**          | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bits de données**         | 8                           | 7/8                                          |
| **Parité**                  | EVEN                        | EVEN/ODD/NONE                                |
| **Bits de stop**            | 1                           | 1/2                                          |
| **N° de station automate**  | 1                           | 0 à 255                                      |
| **N° de station IHM**       | 0                           | 0 à 255                                      |

|                         |                             |
|-------------------------|-----------------------------|
| **Fonction**            | **Prise en charge**         |
| **Simulation hors ligne** | Oui                       |
| **Simulation en ligne**   | Oui                       |
| **Mode étendu**         | Non                         |

**3. Registres utilisables et plages d'adresses**

|                   |                    |                 |                                                           |
|-------------------|--------------------|-----------------|-----------------------------------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**                                         |
| **X**             | ddddd              | 0 à 71664       | Bit : entrée, non continue, dépend du numéro d'emplacement  |
| **Y**             | ddddd              | 0 à 71664       | Bit : sortie, non continue, dépend du numéro d'emplacement  |
| **M**             | ddddd              | 0 à 16384       | Bit : relais spécial                                      |
| **I**             | ddddd              | 0 à 71024       | Bit : relais interne                                      |
| **L**             | ddddd              | 0 à 9984        | Bit : relais de liaison, non continu                      |
| **D**             | ddddd              | 0 à 8192        | Mot : registre de données                                 |
| **B**             | ddddd              | 0 à 32768       | Mot : registre de fichier                                 |
| **V**             | ddddd              | 0 à 64          | Mot : sortie TOR externe                                  |
| **W**             | ddddd              | 0 à 71024       | Mot : registre de liaison, non continu                    |
| **Z**             | ddddd              | 0 à 512         | Mot : registre spécial                                    |

<img src="../../drivers/yokogawa.files/image002.gif" width="595" />

Remarque :

d : décimal, plage de saisie 0-9 ;

Mot dans les remarques : le registre ne s'utilise que comme mot ;

Bit dans les remarques : le registre ne s'utilise que comme bit ;

Lecture seule dans les remarques : le registre peut être lu mais pas écrit ;

Les noms et plages des registres peuvent varier selon le modèle d'équipement.

Pour le détail des noms et plages, consultez la documentation technique de l'équipement connecté

<img src="../../drivers/yokogawa.files/image002.gif" width="595" />
