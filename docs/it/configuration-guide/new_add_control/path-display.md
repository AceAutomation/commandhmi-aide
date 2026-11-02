# Visualizzazione percorso

L'oggetto disegna elementi grafici: punti, linee, archi, cerchi, ecc.

Gli indirizzi usati da questo oggetto sono tutti registri interni LB o LW

Finestra generale della visualizzazione percorso

• Per colore di primo piano, colore bordo, colore sfondo e stile della visibilità, vedere il "Pulsante di bit"

• Area di definizione del percorso: area che definisce gli elementi del percorso; il significato dei dati è descritto alla fine del capitolo, in "[Indirizzi dell'area di definizione del percorso](#路径定义区地址说明)"

• Bit di trigger disegno: quando il bit è a ON il disegno inizia; a OFF non disegna

• Bit di trigger cancellazione: quando il bit è a ON il disegno viene cancellato

• Funzione di selezione: seleziona un punto del disegno corrente per visualizzarne le informazioni

• Abilitazione tramite bit: abilita la funzione di selezione; con l'indirizzo a OFF (predefinito) la selezione è attiva, con l'indirizzo a ON la selezione è disattivata

• Tipo di dato del report di selezione: tipo di memorizzazione dei dati del report

• Area di ricezione del report di selezione: indirizzo di memorizzazione del report di selezione; il significato è descritto alla fine del capitolo, in "[Indirizzi dell'area di ricezione del report di selezione](#选点报告接收区地址)"

• Raggio di ricerca (pixel): raggio di ricerca

• Colore cursore: colore del cursore

• Notifica:

• Segnale:

Livello (Position): con la selezione dei punti abilitata, selezionando un punto del disegno corrente l'opzione si attiva e porta il bit di notifica allo stato specificato. Il bit di notifica deve essere azzerato manualmente per poter rilevare le notifiche successive

Impulso (Pulse): con la selezione dei punti abilitata, selezionando un punto del disegno corrente l'opzione si attiva e porta il bit di notifica a ON; il bit di notifica si azzera automaticamente

Bit di notifica: indirizzo da notificare all'attivazione della funzione

<span id="路径定义区地址说明"></span>**Indirizzi dell'area di definizione del percorso:**

Area di definizione del percorso: contiene i parametri di disegno della visualizzazione percorso, nel formato seguente. Prendendo come esempio l'indirizzo LW0, il significato dei dati è il seguente

|                     |                                                             |
|---------------------|-------------------------------------------------------------|
| Word | Descrizione |
| LW0 | Numero di elementi del percorso |
| LW1~LW8 | Informazioni sul primo elemento del percorso |
| LW9~LW16 | Informazioni sul secondo elemento del percorso |
| ...                 | ...                                                         |
| LW（8n-7）~LW（8n） | Informazioni sull'n-esimo elemento del percorso |

Indice degli elementi: [punto](#点), [linea](#线), [arco](#圆弧), [cerchio](#圆), [spessore](#厚度), [colore](#颜色)

<span id="点"></span>Punto:

|         |           |                       |
|---------|-----------|-----------------------|
| Word | Simbolo | Descrizione |
| LW1 | type | Codice del punto: 0 |
| LW2 | color | [colore](#颜色) |
| LW3 | x | Coordinata X del punto |
| LW4 | y | Coordinata Y del punto |
| LW5~LW8 | (riservato) | Attualmente 0 |

<span id="线"></span>Linea:

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Word</p></td>
<td><p>Simbolo</p></td>
<td><p>Descrizione</p></td>
</tr>
<tr class="even">
<td><p>LW1</p></td>
<td><p>type</p></td>
<td><p>Codice della linea: 1</p></td>
</tr>
<tr class="odd">
<td><p>LW2</p></td>
<td><p>color</p></td>
<td><p><a href="#颜色">colore</a></p></td>
</tr>
<tr class="even">
<td><p>LW3</p></td>
<td><p>X1</p></td>
<td><p>Coordinata X del punto iniziale</p></td>
</tr>
<tr class="odd">
<td><p>LW4</p></td>
<td><p>Y1</p></td>
<td><p>Coordinata Y del punto iniziale</p></td>
</tr>
<tr class="even">
<td><p>LW5</p></td>
<td><p>X2</p></td>
<td><p>Coordinata X del punto finale</p></td>
</tr>
<tr class="odd">
<td><p>LW6</p></td>
<td><p>Y2</p></td>
<td><p>Coordinata Y del punto finale</p></td>
</tr>
<tr class="even">
<td><p>LW7</p></td>
<td><p>style</p></td>
<td><p>Tipo di stile:</p>
<p>0: non visualizzata</p>
<p>1: <img src="../../../configuration-guide/new_add_control/path-display.files/image002.jpg" width="40" alt="ScreenShot00233.jpg" /> linea continua</p>
<p>2: <img src="../../../configuration-guide/new_add_control/path-display.files/image004.jpg" width="40" alt="ScreenShot00232.jpg" /> linea tratteggiata</p>
<p>3: <img src="../../../configuration-guide/new_add_control/path-display.files/image005.jpg" width="40" alt="ScreenShot00234.jpg" /> linea a punti</p>
<p>4: <img src="../../../configuration-guide/new_add_control/path-display.files/image006.jpg" width="40" alt="ScreenShot00235.jpg" /> linea tratto-punto</p>
<p>5: <img src="../../../configuration-guide/new_add_control/path-display.files/image007.jpg" width="40" alt="ScreenShot00236.jpg" /> linea tratto-punto-punto</p>
<p>6 o superiore: <img src="../../../configuration-guide/new_add_control/path-display.files/image002.jpg" width="40" alt="ScreenShot00233.jpg" /> linea continua</p></td>
</tr>
<tr class="odd">
<td><p>LW8</p></td>
<td><p>(riservato)</p></td>
<td><p>Attualmente 0</p></td>
</tr>
</tbody>
</table>

Arco (disegnato in senso antiorario dal punto iniziale al punto finale):

|      |           |                             |
|------|-----------|-----------------------------|
| Word | Simbolo | Descrizione |
| 0 | type | Codice dell'arco: 2 |
| 1 | color | [colore](#颜色) |
| 2 | X | Coordinata X del centro |
| 3 | Y | Coordinata Y del centro |
| 4 | X1 | Coordinata X del punto iniziale |
| 5 | Y1 | Coordinata Y del punto iniziale |
| 6 | X2 | Coordinata X del punto finale |
| 7 | Y2 | Coordinata Y del punto finale |

Cerchio:

|      |           |                      |
|------|-----------|----------------------|
| Word | Simbolo | Descrizione |
| 0 | type | Codice del cerchio: 3 |
| 1 | color | [colore](#颜色) |
| 2 | X | Coordinata X del centro |
| 3 | Y | Coordinata Y del centro |
| 4 | r | Raggio del cerchio |
| 5~7 | (riservato) | Attualmente 0 |

<span id="厚度"></span>Spessore (vale per gli elementi successivi, fino al successivo elemento di spessore):

|      |                      |                                 |
|------|----------------------|---------------------------------|
| Word | Simbolo | Descrizione |
| 0 | type | Codice dello spessore: 8 |
| 1 | (riservato) | Attualmente 0 |
| 2 | Spessore | Spessore del tratto, in pixel |
| 3~7 | (riservato) | Attualmente 0 |

<span id="颜色"></span>Valori dei colori più comuni:

|              |                                   |
|--------------|-----------------------------------|
| Colore | Valore (esadecimale) |
| nero | 0x0000 |
| blu | 0x0010 |
| verde | 0x0400 |
| ciano | 0x0410 |
| rosso | 0x8000 |
| magenta | 0x8010 |
| marrone | 0x8400 |
| grigio | 0xc618 |
| grigio scuro | 0x8410 |
| azzurro | 0x001f |
| verde chiaro | 0x07e0 |
| celeste | 0x07ff |
| rosa | 0xf800 |
| magenta chiaro | 0xf81f |
| giallo | 0xffe0 |
| bianco | 0xffff |

<span id="选点报告接收区地址"></span>**Indirizzi dell'area di ricezione del report di selezione**

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Word</p></td>
<td colspan="3"><p>Descrizione</p></td>
</tr>
<tr class="even">
<td><p>0</p></td>
<td colspan="3"><p>Coordinata X del punto selezionato</p></td>
</tr>
<tr class="odd">
<td><p>1</p></td>
<td colspan="3"><p>Coordinata Y del punto selezionato</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td colspan="3"><p>Numero d'ordine dell'elemento a cui appartiene il punto selezionato</p></td>
</tr>
<tr class="odd">
<td rowspan="3"><p>3</p></td>
<td colspan="2"><p>Valore</p></td>
<td><p>Descrizione</p></td>
</tr>
<tr class="even">
<td><p>0</p></td>
<td colspan="2"><p>Punto: il punto</p>
<p>Linea: il punto iniziale della linea</p>
<p>Cerchio: il centro del cerchio</p>
<p>Arco: il punto iniziale dell'arco</p></td>
</tr>
<tr class="odd">
<td><p>1</p></td>
<td colspan="2"><p>Linea: il punto finale della linea</p>
<p>Arco: il punto finale dell'arco</p></td>
</tr>
<tr class="even" height="0">
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>
