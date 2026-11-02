# Blocco di flusso

Il blocco di flusso è un elemento grafico animato che simula il flusso di un liquido in una tubazione. Il flusso dipende dallo stato dell'indirizzo di trigger: quando vale 1 il blocco è in movimento, quando vale 0 è fermo. La velocità è impostata dall'utente. Fare clic sul pulsante<img src="../../../configuration-guide/extended-controls/pipe.files/image002.jpg" width="28" /> nella barra degli strumenti: compare la finestra di dialogo seguente:

Colore (Color): proprietà di colore del blocco di flusso.

• Colore primo piano del blocco (Flow block foreground color): fare clic sul pulsante colore per impostarlo;

• Colore sfondo del blocco (Flow block background color): fare clic sul pulsante colore per impostarlo;

• Colore primo piano del tubo (Pipe foreground color): fare clic sul pulsante colore per impostarlo;

• Colore sfondo del tubo (Pipe background color): fare clic sul pulsante colore per impostarlo;

• Colore bordo (Border color): fare clic sul pulsante per impostare il colore del bordo dell'oggetto;

• Motivo (Pattern): motivo dell'oggetto; l'impostazione predefinita è "Solid".

• Indirizzo di trigger (Trigger Address): indirizzo che comanda il movimento del blocco; quando il suo valore è 1 il blocco scorre.

• Attributi (Attribute): proprietà del blocco di flusso, come direzione e velocità.

• Modalità di visualizzazione (Display Mode): "Horizontal" per un flusso orizzontale, "Vertical" per un flusso verticale.

• Direzione (Direction): con visualizzazione "Horizontal" si sceglie "Left" o "Right", altrimenti "Up" o "Down".

• Inversione della direzione tramite indirizzo di trigger: quando il valore dell'indirizzo di trigger è uguale allo stato attivo impostato, la direzione del flusso si inverte.

Per esempio, con direzione "Left", questa opzione selezionata, indirizzo di trigger LB2 e stato attivo 1: quando LB2 vale 1 il flusso va verso "Right", quando LB2 vale 0 torna verso "Left".

• Blocchi (Blocks): numero di elementi di flusso, da 1 a 30;

• Senza bordo (No Border): se selezionato, i bordi del blocco di flusso sono nascosti.

• Velocità di flusso (Flow rate): fissa o dinamica

• Velocità fissa: alta, media o bassa.

• Velocità dinamica: la velocità è data dal valore di un indirizzo word, compreso tra 1 e 10. Con valore 0 il blocco non scorre; con 1 scorre alla velocità minima; con 10 alla velocità massima.

<img src="../../../configuration-guide/extended-controls/pipe.files/image004.jpg" width="130" />

Per la scheda "Visibility", vedere l'oggetto "Pulsante di bit".
