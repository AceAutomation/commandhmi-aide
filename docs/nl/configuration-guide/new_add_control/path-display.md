# Padweergave

Dit object tekent de bijbehorende grafische elementen: punt, lijn, boog, cirkel enz.

Alle adressen van dit object zijn interne registers LB of LW

Algemeen dialoogvenster padweergave

• Voorgrondkleur, randkleur, achtergrondkleur, zichtbaarheid: zie “Bit-knop”

• Padgebied: gebied met de definitie van de padelementen; zie voor de betekenis van de gegevens het einde van dit hoofdstuk “[Adressen van het padgebied](#路径定义区地址说明)”

• Tekentriggerbit: is de bit ON, dan begint het tekenen; anders niet

• Wistriggerbit: bij ON wordt de tekening gewist

• Selectiefunctie: selecteert een punt in de huidige tekening om de bijbehorende informatie te tonen

• Via bit: bepaalt of de selectiefunctie actief is. Standaard is de bit OFF en is de selectiefunctie actief; is de bit ON, dan is ze uitgeschakeld

• Gegevenstype rapport: kies het opslagtype van het rapport naar behoefte

• Ontvangstgebied rapport: opslagadres van het selectierapport; zie voor de betekenis het einde van dit hoofdstuk “[Adressen van het ontvangstgebied van het selectierapport](#选点报告接收区地址)”

• Zoekstraal (pixels): stelt de zoekstraal in

• Cursorkleur: stelt de kleur van de cursor in

• Melding:

• Signaal:

Niveau: met de selectiefunctie actief wordt deze optie geactiveerd zodra een punt in de huidige tekening wordt geselecteerd, en wordt de meldingsbit op de opgegeven status gezet. De meldingsbit moet handmatig worden gereset om volgende selecties te kunnen volgen

Puls: met de selectiefunctie actief wordt deze optie geactiveerd zodra een punt in de huidige tekening wordt geselecteerd; de meldingsbit wordt op ON gezet en automatisch gereset

Meldingsbit: stelt het adres in dat bij activering van de pulsfunctie wordt gemeld

<span id="路径定义区地址说明"></span>**Adressen van het padgebied:**

Padgebied: geeft de adressen van de tekenparameters van de padweergave in het volgende formaat. Voorbeeld met adres LW0; de gegevens betekenen:

|                     |                                                             |
|---------------------|-------------------------------------------------------------|
| Woordnummer         | Beschrijving                                                |
| LW0                 | Aantal padelementen in het pad                     |
| LW1~LW8             | Gegevens van het eerste padelement  |
| LW9~LW16            | Gegevens van het tweede padelement |
| ...                 | ...                                                         |
| LW（8n-7）~LW（8n） | N-de padelement                      |

Index van de elementen: [punt](#点), [lijn](#线), [boog](#圆弧), [cirkel](#圆), [dikte](#厚度), [kleur](#颜色)

<span id="点"></span>Punt:

|         |           |                       |
|---------|-----------|-----------------------|
| Woord    | Afkorting | Beschrijving              |
| LW1     | type      | De code van een punt is 0   |
| LW2     | kleur     | [kleur](#颜色)        |
| LW3     | x         | X-coördinaat van het punt |
| LW4     | y         | Y-coördinaat van het punt |
| LW5~LW8 | (gereserveerd)    | Momenteel nul           |

<span id="线"></span>Lijn:

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Woord</p></td>
<td><p>Afkorting</p></td>
<td><p>Beschrijving</p></td>
</tr>
<tr class="even">
<td><p>LW1</p></td>
<td><p>type</p></td>
<td><p>De code van een lijn is 1</p></td>
</tr>
<tr class="odd">
<td><p>LW2</p></td>
<td><p>kleur</p></td>
<td><p><a href="#颜色">kleur</a></p></td>
</tr>
<tr class="even">
<td><p>LW3</p></td>
<td><p>X1</p></td>
<td><p>X-coördinaat van het beginpunt</p></td>
</tr>
<tr class="odd">
<td><p>LW4</p></td>
<td><p>Y1</p></td>
<td><p>Y-coördinaat van het beginpunt</p></td>
</tr>
<tr class="even">
<td><p>LW5</p></td>
<td><p>X2</p></td>
<td><p>X-coördinaat van het eindpunt</p></td>
</tr>
<tr class="odd">
<td><p>LW6</p></td>
<td><p>Y2</p></td>
<td><p>Y-coördinaat van het eindpunt</p></td>
</tr>
<tr class="even">
<td><p>LW7</p></td>
<td><p>stijl</p></td>
<td><p>Type stijl:</p>
<p>0: niet tonen</p>
<p>1: <img src="../../../configuration-guide/new_add_control/path-display.files/image002.jpg" width="40" alt="ScreenShot00233.jpg" /> Doorgetrokken lijn</p>
<p>2: <img src="../../../configuration-guide/new_add_control/path-display.files/image004.jpg" width="40" alt="ScreenShot00232.jpg" /> Stippellijn</p>
<p>3: <img src="../../../configuration-guide/new_add_control/path-display.files/image005.jpg" width="40" alt="ScreenShot00234.jpg" /> Punt-streeplijn</p>
<p>4: <img src="../../../configuration-guide/new_add_control/path-display.files/image006.jpg" width="40" alt="ScreenShot00235.jpg" /> Streep-puntlijn</p>
<p>5: <img src="../../../configuration-guide/new_add_control/path-display.files/image007.jpg" width="40" alt="ScreenShot00236.jpg" /> Streep-punt-puntlijn</p>
<p>6 of hoger: <img src="../../../configuration-guide/new_add_control/path-display.files/image002.jpg" width="40" alt="ScreenShot00233.jpg" /> Doorgetrokken lijn</p></td>
</tr>
<tr class="odd">
<td><p>LW8</p></td>
<td><p>(gereserveerd)</p></td>
<td><p>Momenteel 0</p></td>
</tr>
</tbody>
</table>

Boog (getekend tegen de klok in van beginpunt naar eindpunt):

|      |           |                             |
|------|-----------|-----------------------------|
| Woord | Afkorting | Beschrijving                    |
| 0    | type      | De code van een boog is 2           |
| 1    | kleur     | [kleur](#颜色)              |
| 2    | X         | X-coördinaat van het middelpunt        |
| 3    | Y         | Y-coördinaat van het middelpunt         |
| 4    | X1        | X-coördinaat van het beginpunt |
| 5    | Y1        | Y-coördinaat van het beginpunt |
| 6    | X2        | X-coördinaat van het eindpunt      |
| 7    | Y2        | Y-coördinaat van het eindpunt      |

Cirkel:

|      |           |                      |
|------|-----------|----------------------|
| Woord | Afkorting | Beschrijving             |
| 0    | type      | De code van een cirkel is 3 |
| 1    | kleur     | [kleur](#颜色)       |
| 2    | X         | X-coördinaat van het middelpunt |
| 3    | Y         | Y-coördinaat van het middelpunt  |
| 4    | r         | Straal van de cirkel        |
| 5~7  | (gereserveerd)    | Momenteel nul          |

<span id="厚度"></span>Dikte (geldt voor de volgende elementen tot de volgende dikte):

|      |                      |                                 |
|------|----------------------|---------------------------------|
| Woord | Afkorting            | Beschrijving                        |
| 0    | type                 | Code van de dikte: 8                |
| 1    | (gereserveerd)               | Momenteel nul                     |
| 2    | dikte | Lijndikte, eenheid: pixel |
| 3~7  | (gereserveerd)               | Momenteel nul                     |

<span id="颜色"></span>Gangbare kleurwaarden:

|              |                                   |
|--------------|-----------------------------------|
| Kleur        | Waarde (hexadecimaal) |
| zwart        | 0x0000                            |
| blauw         | 0x0010                            |
| groen        | 0x0400                            |
| cyaan         | 0x0410                            |
| rood         | 0x8000                            |
| magenta      | 0x8010                            |
| bruin        | 0x8400                            |
| grijs         | 0xc618                            |
| Donkergrijs    | 0x8410                            |
| Lichtblauw   | 0x001f                            |
| Lichtgroen  | 0x07e0                            |
| Hemelsblauw    | 0x07ff                            |
| roze         | 0xf800                            |
| Lichtmagenta | 0xf81f                            |
| geel       | Oxffe0                            |
| wit        | 0xffff                            |

<span id="选点报告接收区地址"></span>**Adressen van het ontvangstgebied van het selectierapport**

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Woordnummer</p></td>
<td colspan="3"><p>Beschrijving</p></td>
</tr>
<tr class="even">
<td><p>0</p></td>
<td colspan="3"><p>X-coördinaat van het geselecteerde punt</p></td>
</tr>
<tr class="odd">
<td><p>1</p></td>
<td colspan="3"><p>Y-coördinaat van het geselecteerde punt</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td colspan="3"><p>Volgnummer van het element waartoe het geselecteerde punt behoort</p></td>
</tr>
<tr class="odd">
<td rowspan="3"><p>3</p></td>
<td colspan="2"><p>Waarde</p></td>
<td><p>Beschrijving</p></td>
</tr>
<tr class="even">
<td><p>0</p></td>
<td colspan="2"><p>Punt: een punt</p>
<p>Lijn: het beginpunt van een lijn</p>
<p>Cirkel: het middelpunt van een cirkel</p>
<p>Boog: het beginpunt van een boog</p></td>
</tr>
<tr class="odd">
<td><p>1</p></td>
<td colspan="2"><p>Lijn: het eindpunt van een lijn</p>
<p>Boog: het eindpunt van een boog</p></td>
</tr>
<tr class="even" height="0">
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>
