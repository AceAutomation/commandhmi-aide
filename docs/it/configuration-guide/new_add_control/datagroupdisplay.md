# Visualizzazione gruppo dati

Visualizzazione gruppo dati: un gruppo (o blocco) di dati è un insieme di dati in indirizzi consecutivi, per esempio LW12, LW13, LW14, LW15, ecc. L'oggetto può visualizzare contemporaneamente il contenuto di più gruppi di dati, per esempio LW12-LW15 e RWI12-RWI15, per osservare e confrontare i dati dei registri. Può inoltre tracciare curve di riferimento per più gruppi, con il numero di punti sull'asse orizzontale e il valore di ciascun dato sull'asse verticale, per valutare in modo preciso e intuitivo l'andamento di un valore in un periodo di tempo. Possono essere visualizzate fino a 8 linee spezzate (grafico a linee).

L'icona dell'oggetto nella barra degli strumenti è: <img src="../../../configuration-guide/new_add_control/datagroupdisplay.files/datagroupdisplay756.png" width="31" />; facendo clic si apre la finestra di dialogo mostrata nella Figura 4-122:

<img src="../../../configuration-guide/new_add_control/datagroupdisplay.files/datagroupdisplay838.png" width="741" />

Figura 4-122 Scheda General della visualizzazione gruppo dati

• Colore sfondo (Background color): colore di sfondo del grafico.

• Tipo di dato (Data type): sono disponibili 7 tipi di dato.

• Bit di trigger lettura (Read trigger bit): la curva avanza solo quando il valore dell'indirizzo del bit di trigger lettura è 1.

• Reset automatico (Automatic Reset): quando l'indirizzo del bit di trigger lettura vale 1, viene riportato automaticamente a 0 al rilascio del pulsante del mouse.

• Numero di canali (Channel number): numero di gruppi di dati, cioè di linee.

• Canale corrente (Current Channel): selezionare il canale di cui impostare \[Control Address\].

• Indirizzo di controllo (Control Address): indirizzo di lettura; ogni canale ha il proprio indirizzo di controllo.

L'indirizzo iniziale può essere diverso per ogni canale; la lunghezza dell'indirizzo = Len \* numero di punti visualizzati (Len = 1 per dati a 16 bit, Len = 2 per dati a 32 bit).

Per esempio, con indirizzo iniziale del canale 1 LW1, tipo di dato intero a 32 bit e 4 punti visualizzati, il canale 1 occupa LW1 LW3 LW5 LW7;

• Punti visualizzati (Display points): numero di indirizzi letti per ogni canale.

• Linea di rilevamento (Detection)

• Abilitata (Enabled): abilita la linea di rilevamento (linea di riferimento).

• Colore (Color): colore della linea di rilevamento.

• Indirizzo di rilevamento (Detection address): il valore corrispondente alla linea di rilevamento viene scritto in questo registro.

• Esempio

16 bit, 4 canali, 10 punti visualizzati, LW1 come \[Control Address\] del canale 1, LW100 per il canale 2, LW200 per il canale 3 e RWI1 per il canale 4. Si ottiene:

Linea 1: da LW1 a LW10

Linea 2: da LW100 a LW109

Linea 3: da LW200 a LW209

Linea 4: da RWI1 a RWI10

Con tipo di dato a 32 bit e le altre impostazioni invariate:

Linea 1: da LW1 a LW20

Linea 2: da LW100 a LW119

Linea 3: da LW200 a LW219

Linea 4: da RWI1 a RWI20

Quindi, con dati a 32 bit e N gruppi di dati, i valori vengono letti a intervalli di 2 indirizzi secondo le regole di indirizzamento del modello di PLC.

• Colore sfondo (Background color): colore dell'area delle linee.

• Bit di cancellazione (Clear Trigger Bit): cancella tutte le linee quando il valore dell'indirizzo passa da 0 a 1 (fronte di salita); le linee restano invariate quando il valore passa da 1 a 0 (fronte di discesa) o non cambia.

• Marcatori a punti (Data Point marker): ogni linea è composta da punti

• Marcatori a linee (Draw line markers): ogni linea è composta da segmenti.

<img src="../../../configuration-guide/new_add_control/datagroupdisplay.files/datagroupdisplay3263.png" width="130" />

Per l'uso della scheda "Visibility", vedere il "Pulsante di bit".
