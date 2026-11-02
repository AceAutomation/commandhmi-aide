# Pilote d'équipements Mitsubishi

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Ce pilote permet aux IHM de la série HM de lire et d'écrire les données ou l'état des registres des automates Melsec FXxn/Q00J/C24N. La liaison série est établie entre le port série de l'écran tactile et celui de l'automate Melsec. Avant d'utiliser ce pilote, lisez attentivement ce chapitre et les spécifications techniques de l'automate Melsec FXxn/Q00J/C24N.</p></td>
</tr>
<tr class="even">
<td><p>Établir la connexion avec un automate Melsec FXxn/Q00J/Q00U/C24N</p>
<p><strong>1.  Raccordement matériel</strong></p>
<p>Câble de liaison :</p>
<p>RS422- Melsec-FXxn/FX3U/3G<span id="OLE_LINK1"></span><span id="OLE_LINK3"></span><span id="OLE_LINK2"></span> <span id="OLE_LINK24"></span><span id="OLE_LINK26"></span><span id="OLE_LINK25"></span>(port série, protocole RS232)</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><span id="OLE_LINK60"></span><span id="OLE_LINK30"></span><span id="OLE_LINK27"></span><span id="OLE_LINK62"></span><span id="OLE_LINK61"></span><strong>IHM série HM COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Melsec-FXxn</strong></p></td>
</tr>
<tr class="even">
<td><p>6</p></td>
<td><p>RX-</p></td>
<td><p>4</p></td>
<td><p>TX-</p></td>
</tr>
<tr class="odd">
<td><p>7</p></td>
<td><p>RX+</p></td>
<td><p>7</p></td>
<td><p>TX+</p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p>TX-</p></td>
<td><p>1</p></td>
<td><p>RX-</p></td>
</tr>
<tr class="odd">
<td><p>9</p></td>
<td><p>TX+</p></td>
<td><p>2</p></td>
<td><p>RX+</p></td>
</tr>
</tbody>
</table></td>
</tr>
</tbody>
</table>

<img src="../../drivers/mitsubishi.files/image002.gif" width="145" /><img src="../../drivers/mitsubishi.files/image003.gif" width="280" /><img src="../../drivers/mitsubishi.files/image004.gif" width="130" />

Le connecteur de l'écran tactile est un DB9F ; celui de l'automate Melsec FXxn est un MD8M.

**RS232- Melsec-Q00J/Q00U**

|                                                                                       |     |              |     |
|---------------------------------------------------------------------------------------|-----|--------------|-----|
| <span id="OLE_LINK32"></span><span id="OLE_LINK33"></span>**IHM série HM COM1/COM2** |     | **Q00J CPU** |     |
| **2**                                                                                 | RX  | 2            | TX  |
| **3**                                                                                 | TX  | 1            | RX  |
| **5**                                                                                 | GND | 3            | GND |

<img src="../../drivers/mitsubishi.files/image005.gif" width="146" /><img src="../../drivers/mitsubishi.files/image006.gif" width="280" /><img src="../../drivers/mitsubishi.files/image007.gif" width="130" />

Le connecteur de l'écran tactile est un DB9F ; celui de l'automate Melsec FXxn est un MD8M.

Remarque : raccordement du Q00U

Q00U : broches 5 et 6 reliées (6 broches)

Logiciel de programmation MITSUBISHI : paramètres &gt; paramètres de l'automate -- &gt; paramètres de communication série

Cochez l'utilisation de la communication série, choisissez la vitesse 115200, cochez le contrôle et l'écriture en RUN

Utilisez le câble de communication MITSUBISHI, en liaison directe avec l'IHM

**RS232 - module Melsec-QC24N**

|                             |     |              |     |
|-----------------------------|-----|--------------|-----|
| **IHM série HM COM1/COM2** |     | **Q00J CPU** |     |
| **2**                       | RX  | 3            | TX  |
| **3**                       | TX  | 2            | RX  |
| **5**                       | GND | 5            | GND |

<img src="../../drivers/mitsubishi.files/image008.gif" width="130" /><img src="../../drivers/mitsubishi.files/image009.gif" width="290" /><img src="../../drivers/mitsubishi.files/image010.gif" width="130" />

Le connecteur de l'écran tactile est un DB9F ; celui du module Melsec QC24N est un MB9M.

**2. Paramétrage logiciel**

Choisissez MITSUBISHI dans le service d'équipement de la connexion.

Choisissez l'élément correspondant au modèle d'automate connecté ou au protocole pris en charge dans le service d'équipement de la connexion.

Vérifiez que les paramètres de communication de l'écran tactile et le numéro de station correspondent à ceux de l'automate connecté.

Pour le paramétrage de l'automate, voir la documentation technique des automates Melsec FXxn/Q00J/C24N.

Paramètres de connexion par défaut de l'IHM série HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Paramètre**               | **Valeur par défaut**       | **Plage de réglage**                         |
| **Type d'automate**         | Melsec-FX2N                 | Melsec-FX/ FX2N/ FX3U/3G /Q_C24N Q00J        |
| **Type de port**            | RS232                       | RS232/RS422/RS485                            |
| **Vitesse (baud)**          | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
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
| **Mode étendu**         | Non                         |

**3. Registres utilisables et plages d'adresses**

Melsec-FXxn/FX3U/3G/ FX3U-Ethernet

|                   |                    |                 |                                              |
|-------------------|--------------------|-----------------|----------------------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**                            |
| **X**             | oooo               | 0~377           | Bit : bobine d'entrée, lecture seule         |
| **Y**             | oooo               | 0~377           | Bit : bobine de sortie                       |
| **M**             | dddd               | 0~7999          | Bit : relais intermédiaire                   |
| **SM**            | dddd               | 8000~8999       | Bit : relais intermédiaire spécial           |
| **S**             | dddd               | 0~999           | Bit : bit d'état                             |
| **T**             | dddd               | 0~256           | Bit : état de temporisation                  |
| **C**             | dddd               | 0~256           | Bit : état de temporisation                  |
| **D_Bit**         | dddd.dd            | 0.00~7999.15    | Bit : bit d'un registre 16 bits              |
| **D**             | dddd               | 0~7999          | Mot : registre                               |
| **SD**            | dddd               | 8000~8999       | Mot : registre spécial                       |
| **TV**            | dddd               | 0~255           | Mot : valeur courante de temporisation       |
| **CV**            | dddd               | 0~199           | Mot : valeur courante de compteur            |
| **CV32**          | dddd               | 200~255         | Double mot : valeur courante de compteur 32 bits |

FX5U/FX5U-Ethernet

|                   |                    |                               |                                         |
|-------------------|--------------------|-------------------------------|-----------------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie**           | **Remarques**                       |
| **X**             | oooo               | 0~1777                        | Bit : bobine d'entrée, lecture seule    |
| **Y**             | oooo               | 0~1777                        | Bit : bobine de sortie                  |
| **M**             | dddd               | 0~7679                        | Bit : relais interne                    |
| **L**             | dddd               | 0~7679                        | Bit : relais à verrouillage             |
| **F**             | ddd                | 0~127                         | Bit : relais d'alarme                   |
| **TS**            | ddd                | 0~511                         | Bit : contact de temporisation          |
| **CS**            | ddd                | 0~255                         | Bit : contact de compteur               |
| **S**             | dddd               | 0~4095                        | Bit : relais d'étape                    |
| **SM**            | dddd               | 0~9999                        | Bit : relais spécial                    |
| **B**             | hh                 | 0-ff（notation hexadécimale）  | Bit : relais de liaison                 |
| **D_Bit**         | dddd.dd            | 0.0~7999.15                   | Bit : bit d'un registre 16 bits         |
| **D**             | dddd               | 0~7999                        | Mot : registre                          |
| **R**             | ddddd              | 0~32767                       | Mot : valeur courante cumulée de temporisation |
| **W**             | hhh                | 0-1ff（notation hexadécimale） | Mot : registre de liaison               |
| **CN**            | ddd                | 0~255                         | Mot : valeur courante du registre       |
| **TN**            | ddd                | 0~511                         | Mot : valeur courante de temporisation  |
| **SD**            | ddddd              | 0~11999                       | Mot : registre spécial                  |

  Melsec-Q00J/QC24N

|                   |                    |                 |                                |
|-------------------|--------------------|-----------------|--------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**                  |
| **X**             | hhh                | 0~7ff           | Bit : relais d'entrée, lecture seule |
| **Y**             | hhh                | 0~7ff           | Bit : relais de sortie         |
| **M**             | dddd               | 0~8191          | Bit : relais interne           |
| **L**             | dddd               | 0~2047          | Bit : relais à verrouillage    |
| **F**             | dddd               | 0~2047          | Bit : alarme                   |
| **V**             | dddd               | 0~2047          | Bit : relais d'index           |
| **S**             | dddd               | 0~2047          | Bit : relais d'étape           |
| **B**             | hhh                | 0~7ff           | Bit : relais de liaison        |
| **SB**            | hhh                | 0~3ff           | Bit : relais de liaison spécial |
| **T**             | ddd                | 0~511           | Bit : état de temporisation    |
| **C**             | ddd                | 0~511           | Bit : état de compteur         |
| **D**             | ddddd              | 0~11135         | Mot : registre de données      |
| **W**             | hhh                | 0~7ff           | Mot : registre de liaison      |
| **SW**            | hhh                | 0~3ff           | Mot : registre de liaison spécial |
| Z                 | d                  | 0~9             | Mot : registre d'index         |
| TV                | ddd                | 0~511           | Mot : valeur courante de temporisation |
| CV                | ddd                | 0~511           | Mot : valeur courante de compteur |

Q00U

|                   |                    |                 |                                |
|-------------------|--------------------|-----------------|--------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**                  |
| **X**             | hhhh               | 0~1fff          | Bit : relais d'entrée, lecture seule |
| **Y**             | hhhh               | 0~1fff          | Bit : relais de sortie         |
| **M**             | dddd               | 0~8191          | Bit : relais interne           |
| **L**             | dddd               | 0~8191          | Bit : relais à verrouillage    |
| **F**             | dddd               | 0~2047          | Bit : relais d'alarme          |
| **V**             | dddd               | 0~2047          | Bit : relais d'index           |
| **B**             | ffff               | 0~1fff          | Bit : relais de liaison        |
| **T**             | ddd                | 0~2047          | Bit : état de temporisation    |
| **C**             | dddd               | 0~1023          | Bit : état de compteur         |
| **SB**            | hhh                | 0~7ff           | Bit : relais de liaison spécial |
| **SM**            | ddd                | 0~2047          | Bit : relais spécial           |
| **D_Bit**         | Dddd.h             | 0.0~12287.f     | Bit : bit d'un registre 16 bits |
| **D**             | Dddd               | 0~12287         | Mot : registre de données      |
| **W**             | Hhhh               | 0~1fff          | Mot : registre de liaison      |
| **TV**            | Dddd               | 0~2047          | Mot : valeur courante de temporisation |
| **CV**            | Dddd               | 0~1023          | Mot : valeur courante de compteur |
| **SW**            | Hhh                | 0~7ff           | Mot : registre de liaison spécial |
| **SD**            | Dddd               | 0~2047          | Mot : registre spécial         |
| **Z**             | Dd                 | 0~19            | Mot : registre d'index         |

Melsec-E71

|                   |                    |                 |                                |
|-------------------|--------------------|-----------------|--------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**                  |
| **X**             | hhhh               | 0~1fff          | Bit : relais d'entrée, lecture seule |
| **Y**             | hhhh               | 0~1fff          | Bit : relais de sortie         |
| **M**             | dddd               | 0~8191          | Bit : relais interne           |
| **L**             | dddd               | 0~8191          | Bit : relais à verrouillage    |
| **F**             | dddd               | 0~2047          | Bit : relais d'alarme          |
| **V**             | dddd               | 0~2047          | Bit : relais d'index           |
| **S**             | dddd               | 0~8191          | Bit : relais d'étape           |
| **B**             | ffff               | 0~1fff          | Bit : relais de liaison        |
| **T**             | ddd                | 0~2047          | Bit : état de temporisation    |
| **C**             | dddd               | 0~1023          | Bit : état de compteur         |
| **SB**            | hhh                | 0~7ff           | Bit : relais de liaison spécial |
| **SM**            | ddd                | 0~2047          | Bit : relais spécial           |
| **D_Bit**         | Dddd.h             | 0.0~12287.f     | Bit : bit d'un registre 16 bits |
| **D**             | Dddd               | 0~12287         | Mot : registre de données      |
| **W**             | Hhhh               | 0~1fff          | Mot : registre de liaison      |
| **TV**            | Dddd               | 0~2047          | Mot : valeur courante de temporisation |
| **CV**            | Dddd               | 0~1023          | Mot : valeur courante de compteur |
| **SW**            | Hhh                | 0~7ff           | Mot : registre de liaison spécial |
| **SD**            | Dddd               | 0~2047          | Mot : registre spécial         |
| **Z**             | Dd                 | 0~19            | Mot : registre d'index         |

Melsec-LCPU

|                |              |              |                                |
|----------------|--------------|--------------|--------------------------------|
| **Registre**   | **Format d'adresse** | **Plage de saisie** | **Remarques**          |
| **X**          | hhhh         | 0~1fff       | Bit : relais d'entrée, lecture seule |
| **Y**          | hhhh         | 0~1fff       | Bit : relais de sortie         |
| **M**          | dddd         | 0~8191       | Bit : relais interne           |
| **L**          | dddd         | 0~8191       | Bit : relais à verrouillage    |
| **F**          | dddd         | 0~2047       | Bit : relais d'alarme          |
| **V**          | dddd         | 0~2047       | Bit : relais d'index           |
| **S**          | dddd         | 0~8191       | Bit : relais d'étape           |
| **B**          | hhhh         | 0~1fff       | Bit : relais de liaison        |
| **SB**         | hhh          | 0~7ff        | Bit : relais de liaison spécial |
| **T**          | dddd         | 0~2047       | Bit : état de temporisation    |
| **C**          | dddd         | 0~1023       | Bit : état de compteur         |
| **D-bit**      | ddddd.dd     | 0~45055.15   | Bit : bit d'un registre 16 bits |
| **D**          | ddddd        | 0~45055      | Mot : registre de données      |
| **TV**         | dddd         | 0~2047       | Mot : valeur courante de temporisation |
| **CV**         | dddd         | 0~1023       | Mot : valeur courante de compteur |
| **W**          | hhhh         | 0~1fff       | Mot : registre de liaison      |
| **SW**         | hhh          | 0~7ff        | Mot : registre de liaison spécial |
| **SD**         | hhhh         | 0~2047       | Mot : registre spécial         |
| **Z**          | hh           | 0~19         | Mot : registre d'index         |

<img src="../../drivers/mitsubishi.files/image011.gif" width="595" />

Remarque :

d : décimal, plage de saisie 0-9 ;

o : octal, plage de saisie 0-7 ;

h : hexadécimal, plage de saisie 0-9, a-f ;

Mot dans les remarques : le registre ne s'utilise que comme mot ;

Double mot dans les remarques : le type de données du registre dans la configuration doit être 32 bits ;

Bit dans les remarques : le registre ne s'utilise que comme bit ;

Lecture seule dans les remarques : le registre peut être lu mais pas écrit ;

Les noms et plages des registres peuvent varier selon le modèle d'équipement.

Pour le détail des noms et plages, consultez la documentation technique de l'équipement connecté

<img src="../../drivers/mitsubishi.files/image011.gif" width="595" />

**4. Connexion des IHM série HM à un automate Mitsubishi FX5U**

Ouvrez GX Works3 - Nouveau fichier - Série FX5CPU - Type FX5U

<img src="../../drivers/mitsubishi.files/image012.gif" width="384" />

Navigation - Paramètres - Paramètres du module - Ethernet

<img src="../../drivers/mitsubishi.files/image013.gif" width="1092" />

Liaison - Réglages spécifiques

<img src="../../drivers/mitsubishi.files/image014.gif" width="1024" />

CommandHMI - Général

<img src="../../drivers/mitsubishi.files/image015.gif" width="532" />

Liaison - Paramètres

<img src="../../drivers/mitsubishi.files/image016.gif" width="532" />
