# Pilote d'équipements Delta

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Ce pilote permet aux IHM de la série HM de lire et d'écrire les données ou l'état des registres des automates <span id="OLE_LINK42"></span><span id="OLE_LINK43"></span>Delta série DVP. La liaison série est établie entre le port série de l'IHM et celui de l'automate Delta DVP. Avant d'utiliser ce pilote, lisez attentivement ce chapitre et les spécifications techniques de l'automate Delta DVP.</p></td>
</tr>
<tr class="even">
<td><p>Établir la connexion avec un automate Delta série DVP</p>
<p><strong>1.  Raccordement matériel</strong></p>
<p>Câble de liaison :</p>
<p>RS232<span id="OLE_LINK1"></span><span id="OLE_LINK53"></span><span id="OLE_LINK2"></span> (port série, protocole RS232)</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p>IHM série HM COM1/COM2</p></td>
<td colspan="2"><p>Delta série DVP</p></td>
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
<p><img src="../../drivers/delta.files/image008.gif" width="281" /><img src="../../drivers/delta.files/image009.gif" width="146" /><img src="../../drivers/delta.files/image010.gif" width="130" />  </p>
<p><span id="OLE_LINK54"></span>Le connecteur de l'IHM série HM est un DB9F ; celui de l'automate Delta DVP est un MD8M.</p>
<p>RS485 (port série, protocole RS485)</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p>IHM série HM COM1/COM2</p></td>
<td><p>Delta série DVP</p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p>TX-</p></td>
<td><p>B</p></td>
</tr>
<tr class="odd">
<td><p>9</p></td>
<td><p>TX+</p></td>
<td><p>A</p></td>
</tr>
</tbody>
</table>
<p><img src="../../drivers/delta.files/image011.gif" width="130" /><img src="../../drivers/delta.files/image012.gif" width="156" /></p>
<p>Le connecteur de l'IHM série HM est un DB9F ; celui de l'automate Delta DVP est un bornier deux fils.</p></td>
</tr>
</tbody>
</table>

**2. Paramétrage logiciel**

ü Choisissez Delta Corporation dans le service d'équipement de la connexion.

ü Choisissez l'élément correspondant au modèle d'automate connecté ou au protocole pris en charge.

ü Vérifiez que les paramètres de communication de l'écran tactile et le numéro de station correspondent à ceux de l'automate connecté.

ü Pour le paramétrage de l'automate, voir la documentation technique des automates Delta série DVP.

Paramètres de connexion par défaut de l'IHM série HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Paramètre**               | **Valeur par défaut**       | **Plage de réglage**                         |
| **Type d'automate**         | Delta DVP Series            | Delta DVP Series                             |
| **Type de port**            | RS232                       | RS232/RS422/RS485                            |
| **Vitesse (baud)**          | 19200                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
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

**3. Registres utilisables et plages d'adresses**

|                   |                    |                 |                                               |
|-------------------|--------------------|-----------------|-----------------------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**                             |
| **X**             | ooo                | 0~377           | Bit : entrée, lecture seule                   |
| **Y**             | ooo                | 0~377           | Bit : sortie                                  |
| **M**             | dddd               | 0~4095          | Bit : relais auxiliaire                       |
| **S**             | dddd               | 0~1023          | Bit : relais interne                          |
| **T**             | ddd                | 0~255           | Bit : état de temporisation                   |
| **C**             | ddd                | 0~255           | Bit : état de compteur                        |
| **D**             | dddd               | 0~9999          | Mot : registre de données                     |
| **TV**            | ddd                | 0~255           | Mot : valeur courante de temporisation        |
| **CV**            | ddd                | 0~199           | Mot : valeur courante de compteur             |
| **CV32**          | ddd                | 200~255         | Double mot : valeur courante de compteur 32 bits |

<img src="../../drivers/delta.files/image013.gif" width="595" />

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td></td>
<td><p>Remarque :</p>
<p>d : décimal, plage de saisie 0-9 ;</p>
<p>o : octal, plage de saisie 0-7 ;</p>
<p>Bit dans les remarques : le registre ne s'utilise que comme bit ;</p>
<p>Mot dans les remarques : le registre ne s'utilise que comme mot ;</p>
<p>Double mot dans les remarques : le type de données du registre dans la configuration doit être 32 bits ;</p>
<p>Lecture seule dans les remarques : le registre peut être lu mais pas écrit ;</p>
<p>Les noms et plages des registres peuvent varier selon le modèle d'équipement.</p>
<p>Pour le détail des noms et plages, consultez la documentation technique de l'équipement connecté.</p></td>
</tr>
</tbody>
</table>
