# Blocco di flusso ad angolo

Il blocco di flusso ad angolo funziona come il blocco di flusso, ma aggiunge la possibilità di disegnare angoli ed è quindi più flessibile.

 Fare clic sull'icona <img src="../../../configuration-guide/new_add_control/corner-flow-block.files/image001.jpg" width="74" alt="ScreenShot00054.jpg" /> nella casella degli strumenti e spostare il mouse nell'area della pagina: il cursore diventa una croce. Fare clic nel punto iniziale del blocco, spostare il mouse (compare una linea tra il punto iniziale e il cursore) e fare clic nel punto finale per ottenere il primo tratto. Il punto finale è anche il punto iniziale del tratto successivo, con rotazione di 90°: si possono così ottenere blocchi di flusso a più tratti. Fare clic con il tasto destro per terminare il disegno. Il risultato è mostrato nella Figura 4-134.

<img src="../../../configuration-guide/new_add_control/corner-flow-block.files/corner-flow-block1511.png" width="405" />

Figura 4-134  Blocco di flusso ad angolo

Al termine del disegno, fare doppio clic sul blocco oppure fare clic con il tasto destro e scegliere le proprietà: compare la finestra del blocco di flusso ad angolo, come mostrato nella Figura 4-135.

<img src="../../../configuration-guide/new_add_control/corner-flow-block.files/corner-flow-block1691.png" width="661" />

Figura 4-135 Finestra del blocco di flusso ad angolo

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

<img src="../../../configuration-guide/new_add_control/corner-flow-block.files/corner-flow-block3818.png" width="130" />

Per la scheda "Visibility", vedere l'oggetto "Pulsante di bit".
