# Tubazione

L'oggetto permette di impostare il diametro della linea in base alla posizione definita per l'oggetto

<img src="../../../configuration-guide/new_add_control/conduit.files/image004.jpg" width="488" alt="ScreenShot00831.jpg" />

Finestra generale della tubazione

Ø  Stile (Style): stile di visualizzazione della linea; gli effetti disponibili sono quelli illustrati in "[stile](#style)"

Ø Sfumatura (Gradual layer): effetto di visualizzazione della tubazione; gli effetti disponibili sono quelli illustrati in "[sfumatura](#Graduallayer)"

Ø Diametro (Diameter): diametro della tubazione, vedere "[diametro](#diameter)".

Ø Spessore (Thickness): spessore della parete, che si aggiunge al diametro della tubazione. L'effetto è illustrato in "[spessore](#thickness)"

Ø Bordo (Edge): colore dello spessore della tubazione; con spessore 0 è il colore del bordo della tubazione

Ø  Parete/contenuto (Pipe wall/content): colore principale della linea

Ø Colore variabile di parete/contenuto

<img src="../../../configuration-guide/new_add_control/conduit.files/image005.jpg" width="451" alt="ScreenShot00832.jpg" />

l  Colore visualizzato: con la funzione di colore variabile attiva, la linea mostra un colore scelto tra parete/contenuto, colore parete/contenuto \# 2 e colore parete/contenuto \# 3; questo vale solo nel software di configurazione, mentre durante l'esecuzione il colore è determinato dal bit corrispondente della word di controllo

l  Colore parete/contenuto \# 2, colore parete/contenuto \# 3: colori alternativi della linea

l  Controllo lampeggio: fa lampeggiare la linea

Ø  Controllo del flusso:

l  Word di controllo: word, double word

l  Effetto di flusso: (nota: i tipi seguenti si applicano solo ai tubi per cui è stato abilitato l'effetto di flusso nella scheda dei tubi).

Tipo predefinito: effetto di flusso del tubo

Colore predefinito: colore del flusso nel tubo

Rapporto di lunghezza predefinito (7): rapporto di lunghezza del tubo

Usa tipo, colore e lunghezza predefiniti per tutti: applica il tipo scelto a tutti i tubi con effetto di flusso abilitato nella scheda dei tubi

Ø Word di controllo:

<img src="../../../configuration-guide/new_add_control/conduit.files/image006.jpg" width="450" alt="ScreenShot00833.jpg" />

Quando l'utente abilita il colore variabile di parete/contenuto e il controllo dell'effetto di flusso, i singoli bit del registro selezionato comandano effetti di visualizzazione diversi. Prendiamo come esempio LW0

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
<td><p><strong>Registro</strong></p></td>
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
<p><strong>(bit corrispondente a ON)</strong></p></td>
<td><p>Imposta il colore della parete</p>
<p>Colore parete/contenuto #3</p></td>
<td><p>Imposta il colore della parete</p>
<p>Colore parete/contenuto #3</p></td>
<td><p>Lampeggio della linea</p>
<p>Se i due bit precedenti sono entrambi a ON o a OFF, il colore è quello di parete/contenuto impostato</p>
<p>Se solo uno dei due bit precedenti è a ON, il colore della linea alterna tra il contenuto della tubazione e il contenuto #</p></td>
<td><p>Flusso nella tubazione</p></td>
<td><p>riservato</p></td>
<td><p>riservato</p></td>
<td><p>riservato</p></td>
<td><p>riservato</p></td>
</tr>
</tbody>
</table>

Interfaccia di impostazione dei tubi:

<img src="../../../configuration-guide/new_add_control/conduit.files/image007.jpg" width="488" alt="ScreenShot00834.jpg" />

Ø  Interfaccia di impostazione dei tubi

l  X1，Y1，X2，Y2：

Coordinate del tubo: coordinata sinistra (x1,y1), coordinata destra (x2, y2).

L'utente può modificare le coordinate del tubo, tenendo presente che per un tubo orizzontale si può modificare solo la coordinata x, per un tubo verticale solo la coordinata y; le coordinate degli angoli non sono modificabili, ma lo è lo stile dell'angolo.

l  Effetto di flusso: per ogni tubo l'utente può impostare un tipo di effetto di flusso, il colore, il rapporto di lunghezza, ecc.

Se l'utente usa lo stesso tipo di effetto per tutti, può abilitare qui solo l'effetto di flusso e usare le impostazioni predefinite dell'interfaccia generale, che vengono applicate a tutti i tubi dell'oggetto con effetto di flusso abilitato.

La scheda di visualizzazione è uguale a quella degli altri oggetti: vedere la scheda di visualizzazione del "bit switch".

<span id="style"></span>Stile:

stile 1<img src="../../../configuration-guide/new_add_control/conduit.files/image008.jpg" width="172" alt="ScreenShot00835.jpg" /> stile 2<img src="../../../configuration-guide/new_add_control/conduit.files/image009.jpg" width="178" alt="ScreenShot00836.jpg" /> stile 3<img src="../../../configuration-guide/new_add_control/conduit.files/image008.jpg" width="179" alt="ScreenShot00495.jpg" /> stile 4<img src="../../../configuration-guide/new_add_control/conduit.files/image009.jpg" width="177" alt="ScreenShot00496.jpg" /> stile 5<img src="../../../configuration-guide/new_add_control/conduit.files/image011.jpg" width="187" alt="2019_7_30_11_37_36.jpg" />

<span id="Graduallayer"></span>Sfumatura:

Colore pieno <img src="../../../configuration-guide/new_add_control/conduit.files/image011.jpg" width="182" alt="ScreenShot00498.jpg" /> Stile tridimensionale 1<img src="../../../configuration-guide/new_add_control/conduit.files/image012.jpg" width="180" alt="ScreenShot00499.jpg" /> Stile tridimensionale 2<img src="../../../configuration-guide/new_add_control/conduit.files/image013.jpg" width="180" alt="ScreenShot00500.jpg" /> Stile tridimensionale 3<img src="../../../configuration-guide/new_add_control/conduit.files/image014.jpg" width="179" alt="ScreenShot00501.jpg" />

<span id="diameter"></span>Diametro:

diametro 10<img src="../../../configuration-guide/new_add_control/conduit.files/image015.jpg" width="157" alt="ScreenShot00506.jpg" /> diametro 20<img src="../../../configuration-guide/new_add_control/conduit.files/image016.jpg" width="188" alt="ScreenShot00507.jpg" /> diametro 30<img src="../../../configuration-guide/new_add_control/conduit.files/image017.jpg" width="220" alt="ScreenShot00508.jpg" />

<span id="thickness"></span>Spessore:

spessore 0<img src="../../../configuration-guide/new_add_control/conduit.files/image018.jpg" width="183" alt="ScreenShot00502.jpg" /> spessore 1<img src="../../../configuration-guide/new_add_control/conduit.files/image019.jpg" width="174" alt="ScreenShot00505.jpg" /> spessore 4<img src="../../../configuration-guide/new_add_control/conduit.files/image020.jpg" width="178" alt="ScreenShot00503.jpg" /> spessore 8<img src="../../../configuration-guide/new_add_control/conduit.files/image021.jpg" width="187" alt="ScreenShot00504.jpg" />
