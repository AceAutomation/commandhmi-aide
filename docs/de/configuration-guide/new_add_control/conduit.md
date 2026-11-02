# Rohrleitung

Dieses Objekt zeichnet eine Rohrleitung mit festgelegtem Durchmesser entlang der eingestellten Punkte

<img src="../../../configuration-guide/new_add_control/conduit.files/image004.jpg" width="488" alt="ScreenShot00831.jpg" />

Dialogfeld Rohrleitung, Seite „Allgemein“

Ø  Stil: Darstellungsstil der Leitung; folgende Stile sind möglich, siehe „[Stil](#style)“

Ø Verlauf: Darstellung der Leitung mit Farbverlauf; folgende Varianten sind möglich, siehe „[Verlauf](#Graduallayer)“

Ø Durchmesser: Durchmesser der Rohrleitung, siehe „[Durchmesser](#diameter)“.

Ø Wandstärke: Wandstärke der Rohrleitung, die zum Durchmesser hinzukommt. Siehe „[Wandstärke](#thickness)“

Ø Rand: Farbe der Wandstärke; bei Wandstärke 0 ist dies die Randfarbe der Leitung

Ø  Rohrwand/Inhalt: Hauptfarbe der Leitung

Ø Variable Farbe von Rohrwand/Inhalt

<img src="../../../configuration-guide/new_add_control/conduit.files/image005.jpg" width="451" alt="ScreenShot00832.jpg" />

l  Vorschaufarbe: Ist die variable Farbe von Rohrwand/Inhalt aktiviert, zeigt die Leitung diese Farbe an; sie wird aus „Rohrwand/Inhalt“, „Rohrwand/Inhalt Farbe \# 2“ und „Rohrwand/Inhalt Farbe \# 3“ gewählt. Dies gilt nur in der Projektierungssoftware; im Betrieb bestimmt das Steuerwort die Farbe

l  Rohrwand/Inhalt Farbe \# 2, Rohrwand/Inhalt Farbe \# 3: weitere Farben der Leitung

l  Blinksteuerung: Lässt die Leitung blinken

Ø  Flusssteuerung:

l  Steuerwort: Wort, Doppelwort

l  Flusseffekt: (Hinweis: Die folgenden Typen gelten nur für Rohre, für die auf der Seite „Rohre“ der Flusseffekt aktiviert ist.)

Vorgabetyp: Art des Flusseffekts

Vorgabefarbe: Farbe des Flusses

Vorgabe-Längenverhältnis (7): Längenverhältnis des Flusses

Vorgabetyp, -farbe und -länge für alle verwenden: Wendet die Vorgabe auf alle Rohre an, für die auf der Seite „Rohre“ der Flusseffekt aktiviert ist

Ø Steuerwort:

<img src="../../../configuration-guide/new_add_control/conduit.files/image006.jpg" width="450" alt="ScreenShot00833.jpg" />

Hat der Benutzer die variable Farbe von Rohrwand/Inhalt und die Effektsteuerung aktiviert, steuern die einzelnen Bits des gewählten Registers die verschiedenen Darstellungen. Beispiel mit lw0:

<table>
<colgroup>
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Register</strong></p></td>
<td><p><strong>Bit 0</strong></p></td>
<td><p><strong>Bit 1</strong></p></td>
<td><p><strong>Bit 2</strong></p></td>
<td><p><strong>Bit 3</strong></p></td>
<td><p><strong>Bit 4</strong></p></td>
<td><p><strong>Bit 5</strong></p></td>
<td><p><strong>Bit 6</strong></p></td>
<td><p><strong>Bit 7</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>LW0</strong></p>
<p><strong>(entsprechendes Bit auf ON)</strong></p></td>
<td><p>Farbe der Rohrwand setzen</p>
<p>Rohrwand/Inhalt Farbe #3</p></td>
<td><p>Farbe der Rohrwand setzen</p>
<p>Rohrwand/Inhalt Farbe #3</p></td>
<td><p>Leitung blinkt</p>
<p>Sind die beiden vorigen Bits beide an oder beide aus, ist die Farbe die eingestellte Farbe von Rohrwand/Inhalt</p>
<p>Ist nur eines der beiden gesetzt, wechselt die Leitungsfarbe zwischen den Inhaltsfarben</p></td>
<td><p>Fluss in der Leitung</p></td>
<td><p>reserviert</p></td>
<td><p>reserviert</p></td>
<td><p>reserviert</p></td>
<td><p>reserviert</p></td>
</tr>
</tbody>
</table>

Seite „Rohre“:

<img src="../../../configuration-guide/new_add_control/conduit.files/image007.jpg" width="488" alt="ScreenShot00834.jpg" />

Ø  Seite „Rohre“

l  X1，Y1，X2，Y2：

Koordinatenpunkte des Rohrs: linke Koordinate (x1,y1), rechte Koordinate (x2, y2).

Der Benutzer kann die Rohrkoordinaten ändern. Achtung: Bei waagerechten Rohren ist nur die X-Koordinate änderbar, bei senkrechten nur die Y-Koordinate; die Eckkoordinaten sind nicht änderbar, wohl aber der Eckstil.

l  Flusseffekt: Für jedes Rohr können Art des Flusseffekts, Farbe, Längenverhältnis usw. festgelegt werden.

Soll überall derselbe Effekt verwendet werden, genügt es, hier den Flusseffekt zu aktivieren und auf der Seite „Allgemein“ die Vorgaben zu nutzen; sie gelten dann für alle Rohre des Objekts mit aktiviertem Flusseffekt.

Die Seite „Anzeige“ entspricht der anderer Objekte; siehe Seite „Anzeige“ der Bit-Taste.

<span id="style"></span>Stil:

Stil 1<img src="../../../configuration-guide/new_add_control/conduit.files/image008.jpg" width="172" alt="ScreenShot00835.jpg" /> Stil 2<img src="../../../configuration-guide/new_add_control/conduit.files/image009.jpg" width="178" alt="ScreenShot00836.jpg" /> Stil 3<img src="../../../configuration-guide/new_add_control/conduit.files/image008.jpg" width="179" alt="ScreenShot00495.jpg" /> Stil 4<img src="../../../configuration-guide/new_add_control/conduit.files/image009.jpg" width="177" alt="ScreenShot00496.jpg" /> Stil 5<img src="../../../configuration-guide/new_add_control/conduit.files/image011.jpg" width="187" alt="2019_7_30_11_37_36.jpg" />

<span id="Graduallayer"></span>Verlauf:

Einfarbig <img src="../../../configuration-guide/new_add_control/conduit.files/image011.jpg" width="182" alt="ScreenShot00498.jpg" /> 3D-Stil 1<img src="../../../configuration-guide/new_add_control/conduit.files/image012.jpg" width="180" alt="ScreenShot00499.jpg" /> 3D-Stil 2<img src="../../../configuration-guide/new_add_control/conduit.files/image013.jpg" width="180" alt="ScreenShot00500.jpg" /> 3D-Stil 3<img src="../../../configuration-guide/new_add_control/conduit.files/image014.jpg" width="179" alt="ScreenShot00501.jpg" />

<span id="diameter"></span>Durchmesser:

Durchmesser 10<img src="../../../configuration-guide/new_add_control/conduit.files/image015.jpg" width="157" alt="ScreenShot00506.jpg" /> Durchmesser 20<img src="../../../configuration-guide/new_add_control/conduit.files/image016.jpg" width="188" alt="ScreenShot00507.jpg" /> Durchmesser 30<img src="../../../configuration-guide/new_add_control/conduit.files/image017.jpg" width="220" alt="ScreenShot00508.jpg" />

<span id="thickness"></span>Wandstärke:

Wandstärke 0<img src="../../../configuration-guide/new_add_control/conduit.files/image018.jpg" width="183" alt="ScreenShot00502.jpg" /> Wandstärke 1<img src="../../../configuration-guide/new_add_control/conduit.files/image019.jpg" width="174" alt="ScreenShot00505.jpg" /> Wandstärke 4<img src="../../../configuration-guide/new_add_control/conduit.files/image020.jpg" width="178" alt="ScreenShot00503.jpg" /> Wandstärke 8<img src="../../../configuration-guide/new_add_control/conduit.files/image021.jpg" width="187" alt="ScreenShot00504.jpg" />
