# Grafico di tendenza storico

• Presentazione del grafico di tendenza storico: questo grafico si usa insieme alla "[Raccolta dati storici](../../setting/history-data.md)" di Gestione progetto, di cui visualizza i valori.

• Presentazione del grafico di tendenza XY:

Visualizzazione dinamica e continua dei valori delle variabili.

Visualizza più curve di riferimento, con il tempo sull'asse X e il valore dell'indirizzo sull'asse Y, per valutare in modo preciso e intuitivo l'andamento di un valore in un periodo di tempo.

Possono essere visualizzate fino a 8 linee spezzate (grafico a linee).

• Aggiungere il grafico di tendenza e modificarne le proprietà:

1. Selezionare l'icona del grafico di tendenza<img src="../../../configuration-guide/extended-controls/histrendgraphics.files/image002.jpg" width="34" /> nella barra degli strumenti: compare la finestra delle proprietà del grafico di tendenza storico, come mostrato nella Figura 4-53:

Figura 4-53    Scheda General del grafico di tendenza storico

• Colore sfondo (Background color): colore di sfondo del grafico di tendenza. La modifica non è visibile subito: fare clic su "OK" per applicarla.

• Trasparenza (Transparency): trasparenza del colore di sfondo.

• Raccolta dati (Data Collection): per impostazione predefinita è la "Historical data collector" di Gestione progetto. Poiché CommandHMI gestisce più gruppi di dati storici, con questa opzione si sceglie il gruppo da usare, come mostrato di seguito:

<img src="../../../configuration-guide/extended-controls/histrendgraphics.files/image004.jpg" width="774" />

• Numero di curve (Number of curves): numero di linee visualizzate; al massimo 8.

• Colore (Background Color): colore della traccia (linea).

• Usa indirizzo di controllo (Use control address): abilita l'indirizzo di controllo, che occupa 28 offset e controlla la visualizzazione di ciascuna linea, valore massimo e minimo, ora di fine, periodo (minuti), massimo e minimo dell'asse Y, visualizzazione dell'asse Y e ritorno allo stato iniziale.

|                |                                                                                                         |
|----------------|---------------------------------------------------------------------------------------------------------|
| Offset | Funzione del registro di controllo |
| 0 | Numero totale di linee visualizzate |
| 1 | <span id="OLE_LINK534"></span><span id="OLE_LINK533"></span>Visualizza la linea 1 |
| 2 | Visualizza la linea 2 |
| 3 | Visualizza la linea 3 |
| 4 | Visualizza la linea 4 |
| 5 | Visualizza la linea 5 |
| 6 | Visualizza la linea 6 |
| 7 | Visualizza la linea 7 |
| 8 | Visualizza la linea 8 |
| 9 | Valore massimo dell'asse Y |
| 10             |                                                                                                         |
| 11 | Valore minimo dell'asse Y |
| 12             |                                                                                                         |
| 13 | 0 = usa i valori massimo e minimo predefiniti; 1 = usa i limiti impostati |
| 14 | Ora di inizio della ricerca |
| 15             |                                                                                                         |
| 16             |                                                                                                         |
| 17             |                                                                                                         |
| 18             |                                                                                                         |
| 19             |                                                                                                         |
| 20 | Ora di fine della ricerca |
| 21             |                                                                                                         |
| 22             |                                                                                                         |
| 23             |                                                                                                         |
| 24             |                                                                                                         |
| 25             |                                                                                                         |
| 26 | 1 = esegue la ricerca, poi torna automaticamente a 0 |
| 27 | 1 = ripristina lo stato iniziale, poi torna automaticamente a 0 |

Visualizzazione dell'indirizzo di controllo:

<img src="../../../configuration-guide/extended-controls/histrendgraphics.files/2020-03-23_091355.jpg" width="774" />

**Linea di rilevamento**

• Abilitata (Enabled): abilita la linea di rilevamento (linea di riferimento).

• Colore (Color): colore della linea di rilevamento.

• Indirizzo di rilevamento (Detection address): registro in cui viene scritto il valore corrispondente alla posizione della linea di rilevamento.

• Visualizza ora di rilevamento (Display the detection time): l'ora corrispondente alla posizione della linea di rilevamento viene scritta in questo registro, da visualizzare con un oggetto di visualizzazione ASCII di 19 caratteri.

• Differenza di tempo del punto di rilevamento: la differenza tra l'ora della posizione della linea di rilevamento e l'ora di inizio viene scritta in questo registro, da visualizzare con un oggetto di visualizzazione numerica, intero a 16 bit, in secondi.

2\. La scheda "Line" del grafico di tendenza storico è mostrata nella Figura 4-54.

<img src="../../../configuration-guide/extended-controls/histrendgraphics.files/image005.jpg" width="774" />

Figura 4-54    Scheda Pen del grafico di tendenza storico

Questa scheda permette di impostare valore massimo, minimo, stile e colore di ciascuna linea. La sorgente dati è la "[Raccolta dati storici](../../setting/history-data.md)" di Gestione progetto; ogni linea può corrispondere a una sorgente dati diversa.

3\. La scheda "XY Axis" del grafico di tendenza storico è mostrata nella Figura 4-55.

<img src="../../../configuration-guide/extended-controls/histrendgraphics.files/image006.jpg" width="774" />

Figura 4-55    Scheda XY Axis del grafico di tendenza storico

**Asse X**

• Visualizza scala (Display scale): visualizza la scala dell'asse X.

• Mostra griglia asse Y (Show Y-axis grid): visualizza la griglia dell'asse Y.

• Colore asse / scala (Axis / Scale Color): colore dell'asse X / della scala.

• Colore griglia (Grid Color): colore della griglia dell'asse X.

• Divisioni principali (Main sub-scale): tacche principali dell'asse X.

• Divisioni secondarie (Sub-scale): tacche secondarie dell'asse X.

• Visualizza ora (Display time): formato e dimensione del carattere dell'ora.

• Intervallo di tempo (Time Range): intervallo di tempo visualizzato nel grafico.

**Asse Y**

• Visualizza scala (Display Scale): visualizza la scala dell'asse Y.

• Mostra griglia asse X (Show X-axis grid): visualizza la griglia dell'asse X.

• Colore asse / scala (Axis / Scale Color): colore dell'asse Y / della scala.

• Colore griglia (Grid Color): colore della griglia dell'asse Y.

• Divisioni principali (Major scale division): numero di tacche principali dell'asse Y.

• Divisioni secondarie (Sub-scale division): numero di tacche secondarie dell'asse Y.

• Mostra etichette (Show Marks): visualizza le etichette della scala dell'asse Y.

• Dimensione carattere (Font Size): dimensione del carattere della scala dell'asse Y.

• Minimo (Minimum): valore minimo della scala dell'asse Y.

• Massimo (Max): valore massimo della scala dell'asse Y.

• Totale (Total): numero massimo di cifre visualizzate.

• Decimali (Decimal Place): numero massimo di cifre dopo il punto decimale.

• Visualizza più assi (Display the multi-axis): visualizza più assi.

<img src="../../../configuration-guide/extended-controls/histrendgraphics.files/image007.jpg" width="130" />

Per la scheda "Visibility", vedere l'oggetto "Pulsante di bit".
