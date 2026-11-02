# Pilote d'équipements TaiAn

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Ce pilote permet aux IHM de la série HM de lire et d'écrire les données ou l'état des registres des automates TaiAn série TP03. La liaison série est établie entre le port série de l'écran tactile et celui de l'automate TaiAn TP03. Avant d'utiliser ce pilote, lisez attentivement ce chapitre et les spécifications techniques de l'automate TaiAn TP03.</p></td>
</tr>
<tr class="even">
<td><p>Établir la connexion avec un automate TaiAn série TP03</p>
<p><strong>1.  Raccordement matériel</strong></p>
<p>Câble de liaison :</p>
<p>RS232 <span id="OLE_LINK3"></span><span id="OLE_LINK2"></span></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>IHM série HM COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>TaiAn</strong> <strong>série TP03</strong></p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>3</p></td>
<td><p>TX</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>TX</p></td>
<td><p>2</p></td>
<td><p>RX</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>5</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table>
<p><img src="../../drivers/taian.files/image002.gif" width="130" /><img src="../../drivers/taian.files/image003.gif" width="291" /><img src="../../drivers/taian.files/image004.gif" width="130" /></p></td>
</tr>
</tbody>
</table>

Le connecteur de l'écran tactile est un DB9F ; celui de l'automate TaiAn TP03 est un DB9M.

**2. Paramétrage logiciel**

Choisissez TaiAn Technology dans le service d'équipement de la connexion.

Choisissez l'élément correspondant au modèle d'automate connecté ou au protocole pris en charge dans le service d'équipement de la connexion.

Vérifiez que les paramètres de communication de l'écran tactile et le numéro de station correspondent à ceux de l'automate connecté.

Pour le paramétrage de l'automate, consultez la documentation technique des automates TaiAn série TP03.

Paramètres de connexion par défaut de l'IHM série HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Paramètre**               | **Valeur par défaut**       | **Plage de réglage**                         |
| **Type d'automate**         | TP03 Series                 | TP03 Series                                  |
| **Type de port**            | RS232                       | RS232/RS422/RS485                            |
| **Vitesse (baud)**          | 19200                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bits de données**         | 8                           | 7/8                                          |
| **Parité**                  | NONE                        | EVEN/ODD/NONE                                |
| **Bits de stop**            | 2                           | 1/2                                          |
| **N° de station automate**  | 1                           | 0 à 255                                      |
| **N° de station IHM**       | 0                           | 0 à 255                                      |

|                         |                             |
|-------------------------|-----------------------------|
| **Fonction**            | **Prise en charge**         |
| **Simulation hors ligne** | Oui                       |
| **Simulation en ligne**   | Oui                       |
| **Mode étendu**         | Oui                         |

**3. Registres utilisables et plages d'adresses**

|                   |                    |                 |                                           |
|-------------------|--------------------|-----------------|-------------------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**                         |
| **X**             | ooo                | 0 à 377         | Bit : relais d'entrée, lecture seule      |
| **Y**             | ooo                | 0 à 377         | Bit : relais de sortie                    |
| **M**             | dddd               | 0 à 7999        | Bit : relais auxiliaire                   |
| **SM**            | dddd               | 8000 à 8511     | Bit : relais auxiliaire spécial           |
| **S**             | dddd               | 0 à 4095        | Bit : relais d'étape                      |
| **T**             | ddd                | 0 à 511         | Bit : temporisation                       |
| **C**             | ddd                | 0 à 255         | Bit : compteur                            |
| **D**             | dddd               | 0 à 7999        | Mot : registre de données                 |
| **SD**            | dddd               | 8000 à 8511     | Mot : registre de données spécial         |
| **TV**            | ddd                | 0 à 511         | Mot : valeur courante de temporisation    |
| **CV**            | ddd                | 0 à 199         | Mot : valeur courante de compteur         |
| **CV32**          | ddd                | 200 à 255       | Double mot : valeur courante de compteur  |

<img src="../../drivers/taian.files/image005.gif" width="595" />

Remarque :

d : décimal, plage de saisie 0-9 ;

o : octal, plage de saisie 0-7 ;

Mot dans les remarques : le registre ne s'utilise que comme mot ;

Double mot dans les remarques : le type de données du registre dans la configuration doit être 32 bits ;

Bit dans les remarques : le registre ne s'utilise que comme bit ;

Lecture seule dans les remarques : le registre peut être lu mais pas écrit ;

Les noms et plages des registres peuvent varier selon le modèle d'équipement ;

Pour le détail des noms et plages, consultez la documentation technique de l'équipement connecté.

<img src="../../drivers/taian.files/image005.gif" width="595" />
