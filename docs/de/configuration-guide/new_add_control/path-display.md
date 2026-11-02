# Bahnanzeige

Dieses Objekt zeichnet grafische Elemente wie Punkte, Linien, Bögen und Kreise.

Alle von diesem Objekt verwendeten Adressen sind interne Register LB oder LW

Dialogfeld Bahnanzeige, Seite „Allgemein“

• Vordergrundfarbe, Rahmenfarbe, Hintergrundfarbe, Sichtbarkeit und Stil: siehe „Bit-Taste“

• Bahndefinitionsbereich: Bereich zur Definition der Bahnelemente; zur Bedeutung der Daten siehe am Ende dieses Kapitels „[Adressen des Bahndefinitionsbereichs](#路径定义区地址说明)“

• Zeichen-Triggerbit: Ist die Bitadresse ON, wird gezeichnet; sonst OFF

• Lösch-Triggerbit: Bei ON wird die Zeichnung gelöscht

• Punktauswahl: Wählt einen Punkt der aktuellen Zeichnung, um dessen Informationen anzuzeigen

• Bitgesteuert: Legt fest, ob die Punktauswahl aktiviert ist; ist die Adresse OFF (Standard), ist sie aktiviert, bei ON deaktiviert

• Datentyp des Auswahlberichts: Speichertyp der Berichtsdaten nach Bedarf

• Empfangsbereich des Auswahlberichts: Speicheradressen für den Bericht der Punktauswahl; Bedeutung siehe am Ende dieses Kapitels „[Adressen des Empfangsbereichs für den Auswahlbericht](#选点报告接收区地址)“

• Suchradius (Pixel): Suchradius

• Cursorfarbe: Farbe des Cursors

• Benachrichtigung:

• Signal:

Pegel: Bei aktivierter Punktauswahl löst die Auswahl eines Punkts in der Zeichnung diese Option aus und setzt das Benachrichtigungsbit auf den festgelegten Zustand. Das Bit muss manuell zurückgesetzt werden, um weitere Auswahlen zu überwachen

Impuls: Bei aktivierter Punktauswahl löst die Auswahl eines Punkts in der Zeichnung diese Option aus und setzt das Benachrichtigungsbit auf ON; es wird automatisch zurückgesetzt

Benachrichtigungsbit: Adresse, die bei Auslösung der Impulsfunktion benachrichtigt wird

<span id="路径定义区地址说明"></span>**Adressen des Bahndefinitionsbereichs:**

Bahndefinitionsbereich: enthält die Zeichenparameter der Bahnanzeige im folgenden Format. Beispiel mit Startadresse LW0; die Daten bedeuten:

|                     |                                                             |
|---------------------|-------------------------------------------------------------|
| Wortnummer         | Bedeutung                                                   |
| LW0                 | Anzahl der Bahnelemente                                     |
| LW1~LW8             | Angaben zum ersten Bahnelement                              |
| LW9~LW16            | Angaben zum zweiten Bahnelement                             |
| ...                 | ...                                                         |
| LW（8n-7）~LW（8n） | n-tes Bahnelement                                           |

Index der Elemente: [Punkt](#点), [Linie](#线), [Bogen](#圆弧), [Kreis](#圆), [Stärke](#厚度), [Farbe](#颜色)

<span id="点"></span>Punkt:

|         |           |                       |
|---------|-----------|-----------------------|
| Wort    | Kürzel    | Beschreibung          |
| LW1     | type      | Code des Punkts: 0    |
| LW2     | color     | [Farbe](#颜色)        |
| LW3     | x         | X-Koordinate des Punkts |
| LW4     | y         | Y-Koordinate des Punkts |
| LW5~LW8 | (reserviert) | derzeit null        |

<span id="线"></span>Linie:

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Wort</p></td>
<td><p>Kürzel</p></td>
<td><p>Beschreibung</p></td>
</tr>
<tr class="even">
<td><p>LW1</p></td>
<td><p>type</p></td>
<td><p>Code der Linie: 1</p></td>
</tr>
<tr class="odd">
<td><p>LW2</p></td>
<td><p>color</p></td>
<td><p><a href="#颜色">Farbe</a></p></td>
</tr>
<tr class="even">
<td><p>LW3</p></td>
<td><p>X1</p></td>
<td><p>X-Koordinate des Anfangspunkts</p></td>
</tr>
<tr class="odd">
<td><p>LW4</p></td>
<td><p>Y1</p></td>
<td><p>Y-Koordinate des Anfangspunkts</p></td>
</tr>
<tr class="even">
<td><p>LW5</p></td>
<td><p>X2</p></td>
<td><p>X-Koordinate des Endpunkts</p></td>
</tr>
<tr class="odd">
<td><p>LW6</p></td>
<td><p>Y2</p></td>
<td><p>Y-Koordinate des Endpunkts</p></td>
</tr>
<tr class="even">
<td><p>LW7</p></td>
<td><p>style</p></td>
<td><p>Linienart:</p>
<p>0: nicht anzeigen</p>
<p>1: <img src="../../../configuration-guide/new_add_control/path-display.files/image002.jpg" width="40" alt="ScreenShot00233.jpg" /> durchgezogen</p>
<p>2: <img src="../../../configuration-guide/new_add_control/path-display.files/image004.jpg" width="40" alt="ScreenShot00232.jpg" /> gestrichelt</p>
<p>3: <img src="../../../configuration-guide/new_add_control/path-display.files/image005.jpg" width="40" alt="ScreenShot00234.jpg" /> gepunktet</p>
<p>4: <img src="../../../configuration-guide/new_add_control/path-display.files/image006.jpg" width="40" alt="ScreenShot00235.jpg" /> Strich-Punkt</p>
<p>5: <img src="../../../configuration-guide/new_add_control/path-display.files/image007.jpg" width="40" alt="ScreenShot00236.jpg" /> Strich-Punkt-Punkt</p>
<p>6 oder höher: <img src="../../../configuration-guide/new_add_control/path-display.files/image002.jpg" width="40" alt="ScreenShot00233.jpg" /> durchgezogen</p></td>
</tr>
<tr class="odd">
<td><p>LW8</p></td>
<td><p>(reserviert)</p></td>
<td><p>derzeit 0</p></td>
</tr>
</tbody>
</table>

Bogen (gegen den Uhrzeigersinn vom Anfangs- zum Endpunkt gezeichnet):

|      |           |                             |
|------|-----------|-----------------------------|
| Wort | Kürzel    | Beschreibung                |
| 0    | type      | Code des Bogens: 2          |
| 1    | color     | [Farbe](#颜色)              |
| 2    | X         | X-Koordinate des Mittelpunkts |
| 3    | Y         | Y-Koordinate des Mittelpunkts |
| 4    | X1        | X-Koordinate des Anfangspunkts |
| 5    | Y1        | Y-Koordinate des Anfangspunkts |
| 6    | X2        | X-Koordinate des Endpunkts  |
| 7    | Y2        | Y-Koordinate des Endpunkts  |

Kreis:

|      |           |                      |
|------|-----------|----------------------|
| Wort | Kürzel    | Beschreibung         |
| 0    | type      | Code des Kreises: 3  |
| 1    | color     | [Farbe](#颜色)       |
| 2    | X         | X-Koordinate des Mittelpunkts |
| 3    | Y         | Y-Koordinate des Mittelpunkts |
| 4    | r         | Radius des Kreises   |
| 5~7  | (reserviert) | derzeit null      |

<span id="厚度"></span>Strichstärke (gilt für alle folgenden Elemente bis zur nächsten Stärkeangabe):

|      |                      |                                 |
|------|----------------------|---------------------------------|
| Wort | Kürzel               | Beschreibung                    |
| 0    | type                 | Code der Stärke: 8              |
| 1    | (reserviert)         | derzeit null                    |
| 2    | Stärke               | Strichstärke in Pixel           |
| 3~7  | (reserviert)         | derzeit null                    |

<span id="颜色"></span>Übliche Farbwerte:

|              |                                   |
|--------------|-----------------------------------|
| Farbe        | Wert (hexadezimal)                |
| Schwarz      | 0x0000                            |
| Blau         | 0x0010                            |
| Grün         | 0x0400                            |
| Cyan         | 0x0410                            |
| Rot          | 0x8000                            |
| Magenta      | 0x8010                            |
| Braun        | 0x8400                            |
| Grau         | 0xc618                            |
| Dunkelgrau   | 0x8410                            |
| Hellblau     | 0x001f                            |
| Hellgrün     | 0x07e0                            |
| Blassblau    | 0x07ff                            |
| Rosa         | 0xf800                            |
| Blassmagenta | 0xf81f                            |
| Gelb         | Oxffe0                            |
| Weiß         | 0xffff                            |

<span id="选点报告接收区地址"></span>**Adressen des Empfangsbereichs für den Auswahlbericht**

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Wortnummer</p></td>
<td colspan="3"><p>Bedeutung</p></td>
</tr>
<tr class="even">
<td><p>0</p></td>
<td colspan="3"><p>X-Koordinate des gewählten Punkts</p></td>
</tr>
<tr class="odd">
<td><p>1</p></td>
<td colspan="3"><p>Y-Koordinate des gewählten Punkts</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td colspan="3"><p>Nummer des angeklickten Elements, zu dem der gewählte Punkt gehört</p></td>
</tr>
<tr class="odd">
<td rowspan="3"><p>3</p></td>
<td colspan="2"><p>Wert</p></td>
<td><p>Beschreibung</p></td>
</tr>
<tr class="even">
<td><p>0</p></td>
<td colspan="2"><p>Punkt: der Punkt</p>
<p>Linie: Anfangspunkt der Linie</p>
<p>Kreis: Mittelpunkt des Kreises</p>
<p>Bogen: Anfangspunkt des Bogens</p></td>
</tr>
<tr class="odd">
<td><p>1</p></td>
<td colspan="2"><p>Linie: Endpunkt der Linie</p>
<p>Bogen: Endpunkt des Bogens</p></td>
</tr>
<tr class="even" height="0">
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>
