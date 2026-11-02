# Pilote d'équipements TaiLing

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Ce pilote permet aux IHM de la série HM de lire et d'écrire les données ou l'état des registres des automates TaiLing série DX. La liaison série est établie entre le port série de l'écran tactile et celui de l'automate TaiLing DX. Avant d'utiliser ce pilote, lisez attentivement ce chapitre et les spécifications techniques de l'automate TaiLing DX.</p></td>
</tr>
<tr class="even">
<td><p>Établir la connexion avec un automate TaiLing série DX</p>
<p><strong>1.  Raccordement matériel</strong></p>
<p>Câble de liaison :</p>
<p>RS232 <span id="OLE_LINK1"></span><span id="OLE_LINK2"></span><span id="OLE_LINK3"></span>(port série, protocole RS232)</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>IHM série HM COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>TaiLing</strong> <strong>série DX</strong></p></td>
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
<p><img src="../../drivers/tailing.files/image002.gif" width="130" /><img src="../../drivers/tailing.files/image003.gif" width="290" /><img src="../../drivers/tailing.files/image004.gif" width="130" /></p></td>
</tr>
</tbody>
</table>

Le connecteur de l'IHM est un DB9F ; celui de l'automate TaiLing DX est un DB9M.

**2. Paramétrage logiciel**

Choisissez TaiLing Electric dans le service d'équipement de la connexion.

Choisissez l'élément correspondant au modèle d'automate connecté ou au protocole pris en charge dans le service d'équipement de la connexion.

Vérifiez que les paramètres de communication de l'écran tactile et le numéro de station correspondent à ceux de l'automate connecté.

Pour le paramétrage de l'automate, consultez la documentation technique des automates TaiLing série DX.

Paramètres de connexion par défaut de l'IHM série HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Paramètre**               | **Valeur par défaut**       | **Plage de réglage**                         |
| **Type d'automate**         | DX Series                   | DX Series                                    |
| **Type de port**            | RS232                       | RS232/RS422/RS485                            |
| **Vitesse (baud)**          | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bits de données**         | 8                           | 7/8                                          |
| **Parité**                  | NONE                        | EVEN/ODD/NONE                                |
| **Bits de stop**            | 1                           | 1/2                                          |
| **N° de station automate**  | 1                           | 1 à 31                                       |
| **N° de station IHM**       | 0                           | 0 à 255                                      |

|                         |                             |
|-------------------------|-----------------------------|
| **Fonction**            | **Prise en charge**         |
| **Simulation hors ligne** | Oui                       |
| **Simulation en ligne**   | Oui                       |
| **Mode étendu**         | Non                         |

**3. Registres utilisables et plages d'adresses**

|                   |                    |                 |                                              |
|-------------------|--------------------|-----------------|----------------------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**                            |
| **X**             | oooo               | 0 à 377         | Bit : bobine d'entrée, lecture seule         |
| **Y**             | oooo               | 0 à 377         | Bit : bobine de sortie                       |
| **M**             | dddd               | 0 à 7999        | Bit : relais intermédiaire                   |
| **SM**            | dddd               | 8000 à 8999     | Bit : relais intermédiaire spécial           |
| **S**             | dddd               | 0 à 999         | Bit : bit d'état                             |
| **T**             | dddd               | 0 à 256         | Bit : état de temporisation                  |
| **C**             | dddd               | 0 à 256         | Bit : état de compteur                       |
| **D**             | dddd               | 0 à 7999        | Mot : registre                               |
| **SD**            | dddd               | 8000 à 8999     | Mot : registre spécial                       |
| **TV**            | dddd               | 0 à 255         | Mot : valeur courante de temporisation       |
| **CV**            | dddd               | 0 à 199         | Mot : valeur courante de compteur            |
| **CV32**          | dddd               | 200 à 255       | Double mot : valeur courante de compteur 32 bits |

<img src="../../drivers/tailing.files/image005.gif" width="595" />

Remarque :

d : décimal, plage de saisie 0-9 ;

o : octal, plage de saisie 0-7 ;

Mot dans les remarques : le registre ne s'utilise que comme mot ;

Double mot dans les remarques : le type de données du registre dans la configuration doit être 32 bits ;

Bit dans les remarques : le registre ne s'utilise que comme bit ;

Lecture seule dans les remarques : le registre peut être lu mais pas écrit ;

Les noms et plages des registres peuvent varier selon le modèle d'équipement ;

Pour le détail des noms et plages, consultez la documentation technique de l'équipement connecté.

<img src="../../drivers/tailing.files/image005.gif" width="595" />
