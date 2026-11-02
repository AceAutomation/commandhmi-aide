# Casella combinata

La casella combinata visualizza un elenco di voci che l'utente può consultare e selezionare. Selezionando una voce, il valore corrispondente viene scritto nell'indirizzo di controllo del registro.

L'icona dell'oggetto nella barra degli strumenti è<img src="../../../configuration-guide/new_add_control/combobox.files/combobox771.png" width="35" />: facendo clic si apre la finestra di dialogo mostrata nella Figura 4-115:

<img src="../../../configuration-guide/new_add_control/combobox.files/combobox1012.png" width="677" />

Figura 4-115   Scheda General della casella combinata

• Numero totale di stati (Total Number of States): numero di stati dell'oggetto. Ogni voce rappresenta uno stato ed è visualizzata nell'elenco; il suo valore può essere scritto in \[Control Address\].

• Colore sfondo (Background Color): colore di sfondo della voce selezionata

• Colore testo (Text Color): colore del testo della voce selezionata

• Indirizzo di controllo (Control Address): indirizzo di scrittura

• Usa macro (Use macro): esegue la macro selezionata quando l'oggetto è utilizzabile.

Impostazione stati: fare clic sulla scheda "Status Set"; compare la figura seguente (Figura 4-116):

<img src="../../../configuration-guide/new_add_control/combobox.files/combobox1554.png" width="675" />

Figura 4-116   Scheda Status Set della casella combinata

• Lingua (Language): stesso "carattere" e stessa "dimensione" per tutti gli stati, ma carattere e dimensione diversi per lingue diverse.

• Valore (Value): valore di ciascuna voce, secondo le due regole seguenti:

a\. \[Lettura\]: se il sistema rileva una variazione del contenuto di \[Control Address\], l'oggetto confronta il contenuto con i valori delle voci e seleziona la prima corrispondente. Se nessuna voce corrisponde, passa allo stato di errore e attiva il bit di notifica errore (se impostato).

b\. \[Scrittura\]: quando si seleziona una voce, il sistema ne scrive il valore in \[Control Address\].

• Etichetta (Label): testo di ciascuna voce. Il menu mostra i testi di tutte le voci dell'elenco, da cui l'utente può scegliere.

• Notifica errore

a\. Per esempio, con \[Number of status\] impostato a 8, lo stato 8 è lo stato di errore; analogamente, con 11 lo stato di errore è 11.

b\. In caso di errore, la casella combinata visualizza il testo dello stato di errore.

In caso di errore, il sistema porta a ON / OFF un bit specifico (scritto in \[Error notification address\]). Questo bit di notifica può essere usato per attivare un'operazione di correzione dell'errore.

Per l'uso delle schede "Advanced" e "Visibility", vedere il "Pulsante di bit".
