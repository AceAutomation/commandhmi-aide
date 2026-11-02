# Leiding

Dit object tekent een leiding met de ingestelde diameter op de opgegeven positie

<img src="../../../configuration-guide/new_add_control/conduit.files/image004.jpg" width="488" alt="ScreenShot00831.jpg" />

Algemeen dialoogvenster leiding

Ø  Stijl: weergavestijl van de leiding; voor de beschikbare effecten zie “[stijl](#style)”

Ø Verloop: weergave-effect van de leiding; voor de beschikbare effecten zie “[verloop](#Graduallayer)”

Ø Diameter: diameter van de leiding, zie “[diameter](#diameter)”.

Ø Dikte: dikte van de leiding, opgeteld bij de diameter. Zie “[dikte](#thickness)”

Ø Rand: kleur van de leidingdikte; dit is de randkleur van de leiding als de dikte 0 is

Ø  Wand/inhoud: hoofdkleur van de leiding

Ø Variabele kleur wand/inhoud

<img src="../../../configuration-guide/new_add_control/conduit.files/image005.jpg" width="451" alt="ScreenShot00832.jpg" />

l  Voorbeeldkleur: met de functie variabele kleur wand/inhoud ingeschakeld de kleur van de leiding, te kiezen uit wand/inhoud, kleur wand/inhoud \# 2 en kleur wand/inhoud \# 3; alleen zichtbaar in de configuratiesoftware; tijdens de werking wordt de kleur bepaald door de bits van het besturingswoord

l  Kleur wand/inhoud \# 2, kleur wand/inhoud \# 3: andere kleuren van de leiding

l  Knipperbesturing: laat de leiding knipperen

Ø  Stromingsbesturing:

l  Besturingswoord: woord, dubbelwoord

l  Stromingseffect: (let op: alleen als op de pagina “Leiding” het stromingseffect is ingeschakeld, kunnen de volgende typen worden toegepast op leidingen met stromingseffect).

Voorinstelling type: stromingseffect van de leiding

Standaardkleur: stromingskleur van de leiding

Voorinstelling lengteverhouding (7): lengteverhouding van de leiding

Voorinstelling type, kleur en lengte voor alle: past een type toe op alle leidingen waarvoor op de pagina “Leiding” het stromingseffect is ingeschakeld

Ø Besturingswoord:

<img src="../../../configuration-guide/new_add_control/conduit.files/image006.jpg" width="450" alt="ScreenShot00833.jpg" />

Heeft de gebruiker de besturing van de variabele kleur wand/inhoud en van het stromingseffect ingeschakeld, dan sturen de bits van het gekozen register verschillende weergave-effecten. Voorbeeld met LW0

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
<td><p><strong>Nr. 0</strong></p></td>
<td><p><strong>Nr. 1</strong></p></td>
<td><p><strong>Nr. 2</strong></p></td>
<td><p><strong>Nr. 3</strong></p></td>
<td><p><strong>Nr. 4</strong></p></td>
<td><p><strong>Nr. 5</strong></p></td>
<td><p><strong>Nr. 6</strong></p></td>
<td><p><strong>Nr. 7</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>LW0</strong></p>
<p><strong>(bijbehorende bit op ON)</strong></p></td>
<td><p>Wandkleur instellen</p>
<p>Kleur wand/inhoud #3</p></td>
<td><p>Wandkleur instellen</p>
<p>Kleur wand/inhoud #3</p></td>
<td><p>Leiding knippert</p>
<p>Zijn beide vorige bits aan of uit, dan is de kleur de ingestelde wand-/inhoudskleur</p>
<p>Is slechts één van beide gezet, dan wisselt de leidingkleur tussen de inhoudskleur en inhoudskleur #</p></td>
<td><p>Stroming in de leiding</p></td>
<td><p>gereserveerd</p></td>
<td><p>gereserveerd</p></td>
<td><p>gereserveerd</p></td>
<td><p>gereserveerd</p></td>
</tr>
</tbody>
</table>

Instellingenpagina leiding:

<img src="../../../configuration-guide/new_add_control/conduit.files/image007.jpg" width="488" alt="ScreenShot00834.jpg" />

Ø  Instellingenpagina leiding

l  X1，Y1，X2，Y2：

Coördinaten van de leiding: linkerpunt (x1,y1), rechterpunt (x2, y2).

De gebruiker kan de coördinaten wijzigen, maar let op: bij een horizontale leiding alleen de x-coördinaat, bij een verticale alleen de y-coördinaat; de coördinaat van een hoek kan niet worden gewijzigd, de stijl van de hoek wel.

l  Stromingseffect: per leiding kan een ander stromingseffect, een andere kleur, lengteverhouding enz. worden ingesteld.

Gebruikt u hetzelfde weergave-effect, dan schakelt u hier alleen het stromingseffect in en gebruikt u de voorinstellingen van de pagina “Algemeen”, die op alle leidingen met stromingseffect van het huidige object kunnen worden toegepast.

De pagina “Zichtbaarheid” is gelijk aan die van andere objecten; zie de pagina “Zichtbaarheid” van de “Bit-knop”.

<span id="style"></span>Stijl:

Stijl 1<img src="../../../configuration-guide/new_add_control/conduit.files/image008.jpg" width="172" alt="ScreenShot00835.jpg" /> Stijl 2<img src="../../../configuration-guide/new_add_control/conduit.files/image009.jpg" width="178" alt="ScreenShot00836.jpg" /> Stijl 3<img src="../../../configuration-guide/new_add_control/conduit.files/image008.jpg" width="179" alt="ScreenShot00495.jpg" /> Stijl 4<img src="../../../configuration-guide/new_add_control/conduit.files/image009.jpg" width="177" alt="ScreenShot00496.jpg" /> Stijl 5<img src="../../../configuration-guide/new_add_control/conduit.files/image011.jpg" width="187" alt="2019_7_30_11_37_36.jpg" />

<span id="Graduallayer"></span>Verloop:

Effen kleur <img src="../../../configuration-guide/new_add_control/conduit.files/image011.jpg" width="182" alt="ScreenShot00498.jpg" /> 3D-stijl 1<img src="../../../configuration-guide/new_add_control/conduit.files/image012.jpg" width="180" alt="ScreenShot00499.jpg" /> 3D-stijl 2<img src="../../../configuration-guide/new_add_control/conduit.files/image013.jpg" width="180" alt="ScreenShot00500.jpg" /> 3D-stijl 3<img src="../../../configuration-guide/new_add_control/conduit.files/image014.jpg" width="179" alt="ScreenShot00501.jpg" />

<span id="diameter"></span>Diameter:

Diameter 10<img src="../../../configuration-guide/new_add_control/conduit.files/image015.jpg" width="157" alt="ScreenShot00506.jpg" /> Diameter 20<img src="../../../configuration-guide/new_add_control/conduit.files/image016.jpg" width="188" alt="ScreenShot00507.jpg" /> Diameter 30<img src="../../../configuration-guide/new_add_control/conduit.files/image017.jpg" width="220" alt="ScreenShot00508.jpg" />

<span id="thickness"></span>Dikte:

Dikte 0<img src="../../../configuration-guide/new_add_control/conduit.files/image018.jpg" width="183" alt="ScreenShot00502.jpg" /> Dikte 1<img src="../../../configuration-guide/new_add_control/conduit.files/image019.jpg" width="174" alt="ScreenShot00505.jpg" /> Dikte 4<img src="../../../configuration-guide/new_add_control/conduit.files/image020.jpg" width="178" alt="ScreenShot00503.jpg" /> Dikte 8<img src="../../../configuration-guide/new_add_control/conduit.files/image021.jpg" width="187" alt="ScreenShot00504.jpg" />
