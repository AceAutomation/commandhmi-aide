# Animazione

Animazione: permette di definire in anticipo il percorso di un elemento e di controllarne la posizione lungo il percorso tramite i dati di due registri: uno controlla lo stato, l'altro la posizione.

L'icona dell'oggetto nella barra degli strumenti è: <img src="../../../configuration-guide/new_add_control/dymicbutton.files/image002.jpg" width="28" />. Disegnare i punti del percorso nell'area della pagina (al massimo 64 punti) e fare clic con il tasto destro per terminare.

Fare doppio clic sull'oggetto per aprire la finestra di dialogo mostrata nella Figura 4-118:

Figura 4-118   Scheda General dell'animazione

Numero totale di stati (Total status): numero di stati dell'elemento

Posizione (Location):

Registro (Register): con "Register" selezionato, stato e posizione dell'elemento sono controllati dai dati del registro.

Indirizzo di lettura (Read Address): se stato e posizione dipendono dai dati del registro, occorre impostare correttamente l'indirizzo di lettura, il cui formato è indicato nella tabella seguente.

|           |                            |                              |
|-----------|----------------------------|------------------------------|
| Tipo di dato | Indirizzo di controllo dello stato | Indirizzo di controllo della posizione |
| 16-Bit    | Address                    | Address + 1                  |
| 32-Bit    | Address                    | Address + 2                  |

Per esempio, con registro \[LW100\] e formato "intero positivo a 16 bit", \[LW100\] contiene lo stato dell'elemento e \[LW101\] la sua posizione. Nella Figura 4-119, per esempio, \[LW100\] = 2 e \[LW101\] = 1: l'elemento mostra lo stato 2 e si trova nella posizione 1.

<img src="../../../configuration-guide/new_add_control/dymicbutton.files/image004.gif" width="520" />

Figura 4-119

• Orologio (Clock): con l'opzione "Clock" l'elemento cambia automaticamente stato e posizione; la voce "Automatic position control" imposta la modalità di cambio di stato e posizione.

• Velocità (Speed): velocità di cambio di posizione, in decimi di secondo. Per esempio, 10 significa che l'elemento si sposta di una posizione al secondo.

• Ritorno (Back): supponiamo che l'elemento abbia quattro posizioni: 0, 1, 2 e 3. Se l'opzione non è selezionata, arrivato all'ultima posizione (3) l'elemento torna alla posizione iniziale (0) e ripete la sequenza:

Posizione 0-&gt; posizione 1-&gt; posizione 2-&gt; posizione 3-&gt; posizione 0-&gt; posizione 1-&gt; posizione 2...

Se l'opzione è selezionata, arrivato all'ultima posizione l'elemento ripercorre il percorso a ritroso fino alla posizione iniziale, e così via. La sequenza delle posizioni è la seguente:

Posizione 0-&gt; posizione 1-&gt; posizione 2-&gt; posizione 3-&gt; posizione 2-&gt; posizione 1-&gt; posizione 0...

Cambio di stato (Status transition): modalità di cambio dello stato

Si può scegliere Position-Based o Time-Based. Con "Position-based" lo stato cambia al cambiare della posizione.

Con "Time-Based" posizione e stato cambiano secondo i punti definiti nella pagina.

<img src="../../../configuration-guide/new_add_control/dymicbutton.files/image005.jpg" width="484" />

Figura 4-120   Controllo automatico della posizione

**Scheda Profile:**

<img src="../../../configuration-guide/new_add_control/dymicbutton.files/image006.jpg" width="484" />

Dimensioni del disegno vettoriale:

• Larghezza (Width): larghezza dell'<span id="OLE_LINK520"></span><span id="OLE_LINK521"></span>oggetto grafico nella scheda General.

• Altezza (Height): altezza dell'oggetto grafico nella scheda General.

• Percorso (Orbit): selezionare i punti del percorso per regolarne la posizione.

Per le impostazioni delle schede "Text" e "Picture", vedere la "Spia multistato".

<span id="OLE_LINK676"></span><span id="OLE_LINK677"></span>Per l'uso della scheda "Visibility", vedere il "Pulsante di bit".
