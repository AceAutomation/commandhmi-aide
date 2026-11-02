# Pilote d'équipements Xinje

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Ce pilote permet aux IHM de la série HM de lire et d'écrire les données ou l'état des registres des automates Thinget séries XC/XCM/XD. La liaison série est établie entre le port série de l'écran tactile et celui de l'automate Thinget. Avant d'utiliser ce pilote, lisez attentivement ce chapitre et les spécifications techniques de l'automate Thinget XC/XCM/XD.</p></td>
</tr>
<tr class="even">
<td><p>Établir la connexion avec un automate Thinget XC/XCM/XD</p>
<p><strong>1.  Raccordement matériel</strong></p>
<p>Câble de liaison :</p>
<p>RS232 <span id="OLE_LINK3"></span><span id="OLE_LINK2"></span></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>Écran tactile COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Thinget séries XC/XCM/XD</strong></p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>5</p></td>
<td><p>TX</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>TX</p></td>
<td><p>4</p></td>
<td><p>RX</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>8</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table>
<p><img src="../../drivers/xinje.files/image006.gif" width="130" /><img src="../../drivers/xinje.files/image007.gif" width="280" /><img src="../../drivers/xinje.files/image008.gif" width="146" /></p></td>
</tr>
</tbody>
</table>

Le connecteur de l'IHM est un DB9F ; celui de l'automate Thinget XC/XCM/XD est un MD8M.

**2. Paramétrage logiciel**

Choisissez Xinje Electronic dans le service d'équipement de la connexion.

Choisissez l'élément correspondant au modèle d'automate connecté ou au protocole pris en charge dans le service d'équipement de la connexion.

Vérifiez que les paramètres de communication de l'écran tactile et le numéro de station correspondent à ceux de l'automate connecté.

Pour le paramétrage de l'automate, consultez la documentation technique des automates Thinget séries XC/XCM/XD.

Paramètres de connexion par défaut de l'IHM série HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Paramètre**               | **Valeur par défaut**       | **Plage de réglage**                         |
| **Type d'automate**         | Thinget XC Series           | Thinget XC/XCM/XD Series                     |
| **Type de port**            | RS232                       | RS232/RS422/RS485                            |
| **Vitesse (baud)**          | 19200                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
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
| **Mode étendu**         | Oui                         |

**3. Registres utilisables et plages d'adresses**

Thinget séries XC/XCM

|                   |                    |                 |                                    |
|-------------------|--------------------|-----------------|------------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**                  |
| **X**             | dddd               | 0 à 1037        | Bit : bobine d'entrée              |
| **Y**             | dddd               | 0 à 1037        | Bit : bobine de sortie             |
| **M**             | dddd               | 0 à 8767        | Bit : bobine interne               |
| **S**             | dddd               | 0 à 1023        | Bit : étape                        |
| **T**             | ddd                | 0 à 639         | Bit : état de temporisation        |
| **C**             | ddd                | 0 à 639         | Bit : état de compteur             |
| **D**             | dddd               | 0 à 9023        | Mot : registre de données          |
| **TD**            | ddd                | 0 à 639         | Mot : valeur courante de temporisation |
| **CD**            | ddd                | 0 à 639         | Mot : valeur courante de compteur  |
| **FD**            | dddd               | 0 à 9023        | Mot : registre FlashROM            |
| **ED**            | ddddd              | 0 à 16383       | Mot : registre interne étendu      |

Thinget série XD2

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Registre</strong></p></td>
<td><p><strong>Format d'adresse</strong></p></td>
<td><p><strong>Plage de saisie</strong></p></td>
<td><p><strong>Remarques</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>X</strong></p></td>
<td><p>o</p></td>
<td><p>0~7</p></td>
<td><p>Bobine d'entrée</p></td>
</tr>
<tr class="odd">
<td><p><strong>Y</strong></p></td>
<td><p>o</p></td>
<td><p>0~7</p></td>
<td><p>Bobine de sortie</p></td>
</tr>
<tr class="even">
<td><p><strong>M</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~7999</p></td>
<td><p>Relais interne</p></td>
</tr>
<tr class="odd">
<td><p><strong>HM</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~959</p></td>
<td><p>Relais interne</p></td>
</tr>
<tr class="even">
<td><p><strong>SM</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~2047</p></td>
<td><p>Relais interne spécial</p></td>
</tr>
<tr class="odd">
<td><p><strong>S</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~1023</p></td>
<td><p>Étape</p></td>
</tr>
<tr class="even">
<td><p><strong>HS</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~127</p></td>
<td><p>Étape</p></td>
</tr>
<tr class="odd">
<td><p><strong>T</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~575</p></td>
<td><p>temporisation</p></td>
</tr>
<tr class="even">
<td><p><strong>TD</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~575</p></td>
<td><p>Valeur courante de temporisation</p></td>
</tr>
<tr class="odd">
<td><p><strong>HT</strong></p></td>
<td><p>dd</p></td>
<td><p>0~95</p></td>
<td><p>temporisation</p></td>
</tr>
<tr class="even">
<td><p><strong>ET</strong></p></td>
<td><p>dd</p></td>
<td><p>0~31</p></td>
<td><p>Temporisation de précision</p></td>
</tr>
<tr class="odd">
<td><p><strong>ETD</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~31</p></td>
<td><p>Registre interne étendu</p></td>
</tr>
<tr class="even">
<td><p><strong>C</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~575</p></td>
<td><p>Compteur</p></td>
</tr>
<tr class="odd">
<td><p><strong>CD</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~575</p></td>
<td><p>Valeur courante de compteur</p></td>
</tr>
<tr class="even">
<td><p><strong>HC</strong></p></td>
<td><p>dd</p></td>
<td><p>0~95</p></td>
<td><p>Compteur</p></td>
</tr>
<tr class="odd">
<td><p><strong> HSC</strong></p></td>
<td><p>dd</p></td>
<td><p>0~31</p></td>
<td><p>Compteur rapide</p></td>
</tr>
<tr class="even">
<td><p><strong>D</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~7999</p></td>
<td><p>Registre de données</p></td>
</tr>
<tr class="odd">
<td><p><strong>HD</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~999</p></td>
<td><p>Registre de données</p></td>
</tr>
<tr class="even">
<td><p><strong>SD</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~2047</p></td>
<td><p>Registre de données spécial</p></td>
</tr>
<tr class="odd">
<td><p><strong>HSD</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~499</p></td>
<td><p>Registre de données spécial</p></td>
</tr>
<tr class="even">
<td><p><strong>FD</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~4095</p></td>
<td><p>Registre FlashROM</p></td>
</tr>
<tr class="odd">
<td><p><strong>SFD</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~1999</p></td>
<td><p>Registre FlashROM</p></td>
</tr>
<tr class="even">
<td><p><strong>FS</strong></p></td>
<td><p>dd</p></td>
<td><p>0~47</p></td>
<td><p>Registre de sécurité spécial</p></td>
</tr>
<tr class="odd">
<td><p><strong>SEM</strong></p></td>
<td><p>dd</p></td>
<td><p>0~31</p></td>
<td><p>Bloc fonctionnel séquentiel WAIT<br />
Bobine de commande</p></td>
</tr>
</tbody>
</table>

Thinget série XD3

|                   |                    |                 |                                                                                                                  |
|-------------------|--------------------|-----------------|------------------------------------------------------------------------------------------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**                                                                                                |
| **X**             | ooooo              | 0~20077         | Bobine d'entrée (X10000~X11177 : module d'extension) (X20000~X20277 : module d'extension BD)                     |
| **Y**             | ooooo              | 0~20077         | Bobine de sortie (Y10000~Y11177 : module d'extension) (Y20000~Y20277 : module d'extension BD)                    |
| **M**             | dddd               | 0~7999          | Relais interne                                                                                                   |
| **HM**            | ddd                | 0~959           | Relais interne                                                                                                   |
| **SM**            | dddd               | 0~2047          | Relais interne spécial                                                                                           |
| **S**             | dddd               | 0~1023          | Étape                                                                                                            |
| **HS**            | ddd                | 0~127           | Étape                                                                                                            |
| **T**             | ddd                | 0~575           | temporisation                                                                                                    |
| **TD**            | ddd                | 0~575           | Valeur courante de temporisation                                                                                 |
| **HT**            | dd                 | 0~95            | temporisation                                                                                                    |
| **ET**            | dd                 | 0~31            | Temporisation de précision                                                                                       |
| **ETD**           | ddd                | 0~31            | Registre interne étendu                                                                                          |
| **C**             | ddd                | 0~575           | Compteur                                                                                                         |
| **CD**            | ddd                | 0~575           | Valeur courante de compteur                                                                                      |
| **HC**            | dd                 | 0~95            | Compteur                                                                                                         |
| **HSC**          | dd                 | 0~31            | Compteur rapide                                                                                                  |
| **D**             | dddd               | 0~7999          | Registre de données                                                                                              |
| **HD**            | ddd                | 0~999           | Registre de données                                                                                              |
| **SD**            | dddd               | 0~2047          | Registre de données spécial                                                                                      |
| **HSD**           | ddd                | 0~499           | Registre de données spécial                                                                                      |
| **FD**            | dddd               | 0~4095          | Registre FlashROM                                                                                                |
| **SFD**           | dddd               | 0~1999          | Registre FlashROM                                                                                                |
| **FS**            | dd                 | 0~47            | Registre de sécurité spécial                                                                                     |
| **ID**            | ddddd              | 0~20099         | Module de base (ID10000~ID10999 : module d'extension) (ID20000~20099 : module d'extension BD)                    |
| **QD**            | ddddd              | 0~20099         | Module de base (QD10000~QD10999 : module d'extension) (QD20000~QD20099 : module d'extension BD)                  |
| **SEM**           | dd                 | 0~31            | Bloc fonctionnel séquentiel WAIT, bobine de commande                                                             |

Thinget séries XD5/XDM

|                   |                    |                 |                                                                                                                  |
|-------------------|--------------------|-----------------|------------------------------------------------------------------------------------------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**                                                                                                |
| **X**             | ooooo              | 0~20077         | Bobine d'entrée (X10000~X11177 : module d'extension) (X20000~X20277 : module d'extension BD)                     |
| **Y**             | ooooo              | 0~20077         | Bobine de sortie (Y10000~Y11177 : module d'extension) (Y20000~Y20277 : module d'extension BD)                    |
| **M**             | ddddd              | 0~20479         | Relais interne                                                                                                   |
| **HM**            | ddddd              | 0~11999         | Relais interne                                                                                                   |
| **SM**            | dddd               | 0~4095          | Relais interne spécial                                                                                           |
| **S**             | dddd               | 0~7999          | Étape                                                                                                            |
| **HS**            | ddd                | 0~999           | Étape                                                                                                            |
| **T**             | dddd               | 0~4095          | temporisation                                                                                                    |
| **TD**            | ddd                | 0~575           | Valeur courante de temporisation                                                                                 |
| **HT**            | dddd               | 0~1023          | temporisation                                                                                                    |
| **ET**            | dd                 | 0~39            | Temporisation de précision                                                                                       |
| **ETD**           | ddd                | 0~39            | Registre interne étendu                                                                                          |
| **C**             | dddd               | 0~4095          | Compteur                                                                                                         |
| **CD**            | ddd                | 0~4095          | Valeur courante de compteur                                                                                      |
| **HC**            | dddd               | 0~1023          | Compteur                                                                                                         |
| **HSC**          | dd                 | 0~36            | Compteur rapide                                                                                                  |
| **D**             | ddddd              | 0~20479         | Registre de données                                                                                              |
| **HD**            | ddddd              | 0~6143          | Registre de données                                                                                              |
| **SD**            | dddd               | 0~4095          | Registre de données spécial                                                                                      |
| **HSD**           | dddd               | 0~1023          | Registre de données spécial                                                                                      |
| **FD**            | dddd               | 0~4095          | Registre FlashROM                                                                                                |
| **SFD**           | dddd               | 0~5999          | Registre FlashROM                                                                                                |
| **FS**            | dd                 | 0~47            | Registre de sécurité spécial                                                                                     |
| **ID**            | ddddd              | 0~20099         | Module de base (ID10000~ID10999 : module d'extension) (ID20000~20099 : module d'extension BD)                    |
| **QD**            | ddddd              | 0~20099         | Module de base (QD10000~QD10999 : module d'extension) (QD20000~QD20099 : module d'extension BD)                  |
| **SEM**           | ddd                | 0~127           | Bloc fonctionnel séquentiel WAIT, bobine de commande                                                             |

<img src="../../drivers/xinje.files/image009.gif" width="595" />

Remarque :

d : décimal, plage de saisie 0-9 ;

o : octal, plage de saisie 0-7 ;

Mot dans les remarques : le registre ne s'utilise que comme mot ;

Bit dans les remarques : le registre ne s'utilise que comme bit ;

Lecture seule dans les remarques : le registre peut être lu mais pas écrit ;

Les noms et plages des registres peuvent varier selon le modèle d'équipement.

Pour le détail des noms et plages, consultez la documentation technique de l'équipement connecté

<img src="../../drivers/xinje.files/image011.gif" width="595" />
