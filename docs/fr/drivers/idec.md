# Pilote d'équipements IDEC

Ce pilote permet aux IHM de la série HM de lire et d'écrire les données ou l'état des registres des automates Macro Smart séries FC4A/FC5A/FC6A. La liaison série est établie entre le port série de l'IHM et celui de l'automate Macro Smart. Avant d'utiliser ce pilote, lisez attentivement ce chapitre et les spécifications techniques de l'automate Macro Smart FC4A/FC5A/FC6A.

**Établir la connexion avec un Macro Smart FC4A/FC5A**

1\. Raccordement matériel

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
<td colspan="3"><p><strong>Macro Smart FC4A/FC5A</strong></p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>3</p></td>
<td colspan="2"><p>TX</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>TX</p></td>
<td><p>4</p></td>
<td colspan="2"><p>RX</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>6</p></td>
<td><p>GND</p></td>
<td rowspan="2"><p>6-7</p>
<p>Court-circuit</p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td><p>7</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table>

|     |                                                   |     |                                                   |     |                                                   |
|-----|---------------------------------------------------|-----|---------------------------------------------------|-----|---------------------------------------------------|
|     |                                                   |     |                                                   |     |                                                   |
|     |                                                   |     |                                                   |     | <img src="../../drivers/idec.files/image002.gif" width="146" /> |
|     | <img src="../../drivers/idec.files/image003.gif" width="129" /> |     |                                                   |     |                                                   |
|     |                                                   |     | <img src="../../drivers/idec.files/image004.gif" width="280" /> |     |                                                   |
|     |                                                   |     |                                                   |     |                                                   |
|     |                                                   |     |                                                   |     |                                                   |

Le connecteur de l'IHM est un DB9F ; celui de l'automate Macro Smart FC4A/FC5A est un MD8M.

**2. Paramétrage logiciel**

Choisissez Allen-Bradley dans le service d'équipement de la connexion.

Choisissez l'élément correspondant au modèle d'automate connecté ou au protocole pris en charge dans le service d'équipement de la connexion.

Vérifiez que les paramètres de communication de l'écran tactile et le numéro de station correspondent à ceux de l'automate connecté.

Pour le paramétrage de l'automate, voir la documentation technique des automates Macro Smart séries FC4A/FC5A/FC6A.

Paramètres de connexion par défaut de l'IHM HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Paramètre**               | **Valeur par défaut**       | **Plage de réglage**                         |
| **Type d'automate**         | Macro Smart FC4A            | Macro Smart FC4A/ Macro Smart FC5A           |
| **Type de port**            | RS232                       | RS232/RS422/RS485                            |
| **Vitesse (baud)**          | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bits de données**         | 7                           | 7/8                                          |
| **Parité**                  | EVEN                        | EVEN/ODD/NONE                                |
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

Macro Smart FC4A

|                   |                    |                 |                                                |
|-------------------|--------------------|-----------------|------------------------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**                              |
| **I**             | ddd                | 0~255           | Bit : entrée TOR externe, lecture seule        |
| **Q**             | ddd                | 0~255           | Bit : sortie TOR externe                       |
| **M**             | dddd               | 0~1023          | Bit : relais interne                           |
| **SM**            | ddd                | 0~215           | Bit : registre interne                         |
| **R**             | ddd                | 0~255           | Mot : registre à décalage                      |
| **D**             | ddd                | 0~1299          | Mot : registre de données                      |
| **TV**            | ddd                | 0~127           | Mot : valeur courante de temporisation         |
| **CV**            | ddd                | 0~127           | Mot : valeur courante de compteur              |

Macro Smart FC5A

|                   |                    |                 |                                                |
|-------------------|--------------------|-----------------|------------------------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**                              |
| **I**             | ddd                | 0~255           | Bit : entrée TOR externe, lecture seule        |
| **Q**             | ddd                | 0~255           | Bit : sortie TOR externe                       |
| **M**             | dddd               | 0~2047          | Bit : relais interne                           |
| **SM**            | ddd                | 0~215           | Bit : registre interne                         |
| **R**             | ddd                | 0~255           | Mot : registre à décalage                      |
| **D**             | ddd                | 0~42000         | Mot : registre de données                      |
| **TV**            | ddd                | 0~255           | Mot : valeur courante de temporisation         |
| **CV**            | ddd                | 0~255           | Mot : valeur courante de compteur              |

Macro Smart FC6A Tcp/IP

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
<td><p><strong>I</strong></p></td>
<td><p>Ddo</p></td>
<td><p>0~627</p></td>
<td><p>Bit : entrée TOR externe, lecture seule</p></td>
</tr>
<tr class="odd">
<td><p><strong>Q</strong></p></td>
<td><p>Ddo</p></td>
<td><p>0~627</p></td>
<td><p>Bit : sortie TOR externe</p></td>
</tr>
<tr class="even">
<td><p><strong>M</strong></p></td>
<td><p>Dddo</p></td>
<td><p>0~7997</p>
<p>8000~8317</p>
<p>10000~17497</p></td>
<td><p>Bit : relais interne</p></td>
</tr>
<tr class="odd">
<td><p><strong>R</strong></p></td>
<td><p>Ddd</p></td>
<td><p>0~255</p></td>
<td><p>Bit : registre à décalage</p></td>
</tr>
<tr class="even">
<td><p><strong>T</strong></p></td>
<td><p>Dddd</p></td>
<td><p>0~1023</p></td>
<td><p>Bit : état de temporisation (lecture seule)</p></td>
</tr>
<tr class="odd">
<td><p><strong>C</strong></p></td>
<td><p>Dddd</p></td>
<td><p>0~511</p></td>
<td><p>Bit : état de compteur (lecture seule)</p></td>
</tr>
<tr class="even">
<td><p><strong>D</strong></p></td>
<td><p>ddddd</p></td>
<td><p>0~8499</p>
<p>10000~55999</p></td>
<td><p>Mot : registre</p></td>
</tr>
<tr class="odd">
<td><p><strong>TV</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~1023</p></td>
<td><p>Mot : valeur courante de temporisation (lecture seule)</p></td>
</tr>
<tr class="even">
<td><p><strong>CV</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~511</p></td>
<td><p>Mot : valeur courante de compteur (lecture seule)</p></td>
</tr>
<tr class="odd">
<td><p><strong>TS</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~1023</p></td>
<td><p>• Mot : consigne de temporisation (lecture seule)</p></td>
</tr>
<tr class="even">
<td><p><strong>CS</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~511</p></td>
<td><p>Mot : consigne de compteur (lecture seule)</p></td>
</tr>
</tbody>
</table>

<img src="../../drivers/idec.files/image009.gif" width="595" />

Remarque :

d : décimal, plage de saisie 0-9 ;

Bit dans les remarques : le registre ne s'utilise que comme bit ;

Mot dans les remarques : le registre ne s'utilise que comme mot ;

Lecture seule dans les remarques : le registre peut être lu mais pas écrit ;

Les noms et plages des registres peuvent varier selon le modèle d'équipement.

Pour le détail des noms et plages, consultez la documentation technique de l'équipement connecté.

<img src="../../drivers/idec.files/image010.gif" width="595" />
