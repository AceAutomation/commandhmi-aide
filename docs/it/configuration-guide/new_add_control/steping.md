# Pulsante a passi

Questo comando crea nella pagina corrente un pulsante a passi, che fa scorrere ciclicamente gli stati. Fare clic sull'icona<img src="../../../configuration-guide/new_add_control/steping.files/image002.jpg" width="31" /> per aprire la finestra di dialogo mostrata nella Figura 4-113:

<img src="../../../configuration-guide/new_add_control/steping.files/image004.jpg" width="675" />

Figura 4-113   Finestra del pulsante a passi

Ordine degli stati (State sequence): direzione dei testi sull'oggetto

Per esempio, con 3 stati in totale, i testi degli stati 0, 1 e 2 sono rispettivamente 0, 1, 2.

• Da sinistra a destra (Left to Right): oggetto orizzontale, testi da sinistra a destra: 0, 1, 2

• Da destra a sinistra (Right to Left): oggetto orizzontale, testi da destra a sinistra: 2, 1, 0

• Dall'alto in basso (Up to Down): oggetto verticale, testi dall'alto in basso: 0, 1, 2

• Dal basso in alto (Down to Up): oggetto verticale, testi dal basso in alto: 2, 1, 0

Tipo di stato (State Type): vedere la "Spia multistato".

Stato corrente (Current state): colore di sfondo e colore del testo dello stato corrente.

Per i parametri delle schede Text e Picture, vedere la "Spia multistato".

Per l'uso della scheda "Advanced" e dei tasti di scelta rapida, vedere il Pulsante di bit.

Per esempio, con tipo di stato "Value", indirizzo di scrittura LW1, 3 stati in totale e testi degli stati 0, 1 e 2 rispettivamente 0, 1 e 2: dopo il download del progetto nell'HMI, a ogni clic sull'oggetto lo stato passa ciclicamente da 0 a 2 e il valore corrispondente viene scritto in LW1.
