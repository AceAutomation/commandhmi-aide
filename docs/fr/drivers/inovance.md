# Pilote d'équipements Inovance

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Ce pilote permet aux IHM de la série HM de lire et d'écrire les données ou l'état des registres des automates Inovance séries H1u/H2u. La liaison série est établie entre le port série de l'IHM et celui de l'automate Inovance. Avant d'utiliser ce pilote, lisez attentivement ce chapitre et les spécifications techniques de l'automate Inovance H1u/H2u.</p></td>
</tr>
<tr class="even">
<td><p>Établir la connexion avec un automate Inovance H1u/H2u</p>
<p><strong>1.  Raccordement matériel</strong></p>
<p>Câble de liaison :</p>
<p>RS232 (port série, protocole RS232)</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p>IHM HM COM1/COM2</p></td>
<td colspan="2"><p>Inovance séries H1u/H2u</p></td>
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

<img src="../../drivers/inovance.files/image002.gif" width="281" /><img src="../../drivers/inovance.files/image003.gif" width="130" /><img src="../../drivers/inovance.files/image004.gif" width="145" />

Le connecteur de l'IHM est un DB9F ; celui de l'automate Inovance H1u/H2u est un DB9M.

**2. Paramétrage logiciel**

Choisissez Inovance Technology Corp. dans le service d'équipement de la connexion.

Choisissez l'élément correspondant au modèle d'automate connecté ou au protocole pris en charge dans le service d'équipement de la connexion.

Vérifiez que les paramètres de communication de l'écran tactile et le numéro de station correspondent à ceux de l'automate connecté.

Pour le paramétrage de l'automate, voir la documentation technique des automates Inovance séries H1u/H2u.

Paramètres de connexion par défaut de l'IHM série HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Paramètre**               | **Valeur par défaut**       | **Plage de réglage**                         |
| **Type d'automate**         | H1u/H2u                     | H1u/H2u                                      |
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

|                   |                    |                 |                                              |
|-------------------|--------------------|-----------------|----------------------------------------------|
| **Registre**      | **Format d'adresse** | **Plage de saisie** | **Remarques**                            |
| **X**             | oooo               | 0~377           | Bit : bobine d'entrée, lecture seule         |
| **Y**             | oooo               | 0~377           | Bit : bobine de sortie                       |
| **M**             | dddd               | 0~7999          | Bit : relais intermédiaire                   |
| **SM**            | dddd               | 8000~8999       | Bit : relais intermédiaire spécial           |
| **S**             | dddd               | 0~999           | Bit : bit d'état                             |
| **T**             | dddd               | 0~256           | Bit : état de temporisation                  |
| **C**             | dddd               | 0~256           | Bit : état de compteur                       |
| **D**             | dddd               | 0~7999          | Mot : registre                               |
| **SD**            | dddd               | 8000~8999       | Mot : registre spécial                       |
| **TV**            | dddd               | 0~255           | Mot : valeur courante de temporisation       |
| **CV**            | dddd               | 0~199           | Mot : valeur courante de compteur            |
| **CV32**          | dddd               | 200~255         | Double mot : valeur courante de compteur 32 bits |

<img src="../../drivers/inovance.files/image005.gif" width="595" />

Remarque :

d : décimal, plage de saisie 0-9 ;

o : octal, plage de saisie 0-7 ;

Mot dans les remarques : le registre ne s'utilise que comme mot ;

Double mot dans les remarques : le type de données du registre dans la configuration doit être 32 bits ;

Bit dans les remarques : le registre ne s'utilise que comme bit ;

Lecture seule dans les remarques : le registre peut être lu mais pas écrit ;

Les noms et plages des registres peuvent varier selon le modèle d'équipement.

Pour le détail des noms et plages, consultez la documentation technique de l'équipement connecté

<img src="../../drivers/inovance.files/image006.gif" width="595" />
