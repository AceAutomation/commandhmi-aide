# Grafico di tendenza

**Presentazione del grafico di tendenza:**

<span id="OLE_LINK525"></span><span id="OLE_LINK526"></span>Visualizzazione dinamica e continua dei valori delle variabili.

Traccia le curve di riferimento di più dati, con il tempo sull'asse orizzontale e il valore sull'asse verticale, per valutare in modo preciso e intuitivo l'andamento di un valore in un periodo di tempo.

Possono essere visualizzate fino a 8 linee spezzate (grafico a linee).

Aggiungere un grafico di tendenza e impostarne le proprietà:

1. Selezionare l'icona Trend Chart<img src="../../../configuration-guide/extended-controls/trend.files/image002.jpg" width="35" /> nella barra degli strumenti: compare la finestra delle proprietà, come mostrato nella Figura 4-50

Figura 4-50    Finestra generale del grafico di tendenza

• Colore sfondo (Background color): colore di sfondo del grafico di tendenza. La modifica è visibile solo dopo aver fatto clic su OK.

• Tipo di dato (Data type): sono disponibili 7 tipi di dato.

• Bit di trigger lettura (Read trigger bit): la curva avanza solo quando il valore dell'indirizzo del bit di trigger lettura è 1.

• Numero di curve (Curve number): numero di linee, al massimo 8.

• Reset automatico del bit di trigger lettura: quando l'indirizzo letto vale 1, viene riportato a 0.

• Numero di punti per gruppo (Number of data points per group): <span id="OLE_LINK492"></span><span id="OLE_LINK493"></span>numero di dati visualizzati sull'<span id="OLE_LINK494"></span><span id="OLE_LINK495"></span>asse X.

• Tempo di campionamento (Sampling time): frequenza di campionamento.

• Indirizzo di lettura (Read Address): il suo valore rappresenta il valore di ciascuna linea sull'asse Y. In base al numero di gruppi e al tipo di dato, gli indirizzi vengono letti in modo consecutivo (dati a 16 bit) o a intervalli (dati a 32 bit).

• Punti variabili (Variable data points): il "Numero di punti per gruppo" viene impostato dinamicamente dal valore di un indirizzo. Con questa opzione selezionata, il valore iniziale dell'indirizzo è il numero di punti per gruppo impostato.

**Linea di rilevamento**

• Abilitata (Enabled): abilita la linea di rilevamento (linea di riferimento).

• Colore (Color): colore della linea di rilevamento.

<span id="OLE_LINK527"></span><span id="OLE_LINK528"></span><span id="OLE_LINK543"></span>• Indirizzo di rilevamento (Detection address): il valore della linea di rilevamento (linea di riferimento) corrente viene scritto in questo indirizzo.

• Usa indirizzo di controllo: imposta dinamicamente il minimo e il massimo dell'asse Y in base al valore dell'indirizzo di controllo. L'indirizzo occupa cinque offset consecutivi e permette di modificare minimo e massimo della scala dell'asse Y e di ripristinare lo stato iniziale.

|                |                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Offset | Funzione del registro di controllo |
| 0 | 16 bit bassi del valore minimo |
| 1 | 16 bit alti del valore minimo |
| 2 | 16 bit bassi del valore massimo |
| 3 | 16 bit alti del valore massimo |
| 4 | Ripristino dei valori massimo e minimo: 1 = variazione dinamica, altrimenti vengono ripristinati i valori iniziali |

<img src="../../../configuration-guide/extended-controls/trend.files/image004.jpg" width="130" />

L'indirizzo di controllo può usare solo indirizzi interni; minimo e massimo occupano ciascuno due word consecutive.

E.g.:

Con tipo di dato a 16 bit e 8 gruppi di dati, se l'indirizzo inserito è LW3 vengono letti 8 indirizzi consecutivi:

LW3: valore della linea 1

LW4: <span id="OLE_LINK513"></span><span id="OLE_LINK514"></span>valore della linea 2

LW5: <span id="OLE_LINK515"></span><span id="OLE_LINK516"></span>valore della linea 3

LW6: valore della linea 4

LW7: valore della linea 5

LW8: valore della linea 6

LW9: valore della linea 7

LW10: valore della linea 8

Quindi, con dati a 16 bit e N gruppi di dati, vengono letti N indirizzi consecutivi secondo le regole di indirizzamento del modello di PLC.

Con tipo di dato a 32 bit e 5 gruppi di dati, se l'indirizzo inserito è LW3 vengono letti 5 valori consecutivi:

LW3: <span id="OLE_LINK517"></span><span id="OLE_LINK518"></span>valore della linea 1

LW5: valore della linea 2

LW7: valore della linea 3

LW9: valore della linea 4

LW11: valore della linea 5

Quindi, con dati a 32 bit e N gruppi di dati, vengono letti N valori a intervalli di 2 indirizzi secondo le regole di indirizzamento del modello di PLC.

• Direzione (Direction):

• Da sinistra a destra (Left to right): la linea avanza da sinistra.

• Da destra a sinistra (Right to left): la linea avanza da destra.

• Colore sfondo (Background color): colore dell'area delle linee

• Bit di cancellazione (Clear Trigger Bit): cancella tutte le linee quando il valore dell'indirizzo passa da 0 a 1 (fronte di salita). Le linee restano invariate quando il valore passa da 1 a 0 (fronte di discesa) o non cambia.

La scheda "Line" del grafico di tendenza è mostrata nella Figura 4-51: permette di impostare valore massimo, minimo, stile e colore di ciascuna linea.

<img src="../../../configuration-guide/extended-controls/trend.files/image005.jpg" width="774" />

Figura 4-51    Scheda Pen del grafico di tendenza

Il tipo di dato della scheda General determina quello dei valori massimo e minimo.

Per esempio, se il valore massimo o minimo è in virgola mobile, occorre prima selezionare virgola mobile a 32 bit come tipo di dato nella scheda General; altrimenti, facendo clic su "OK" si verifica un errore.

3\. La scheda "XY Axis" del grafico di tendenza è mostrata nella Figura 4-52:

<img src="../../../configuration-guide/extended-controls/trend.files/image006.jpg" width="774" />

Figura 4-52    Scheda XY Axis del grafico di tendenza

• Asse X

• Visualizza scala (Display scale): visualizza la scala dell'asse X.

• Mostra griglia asse Y (Show Y-axis grid): visualizza la griglia dell'asse Y.

• Colore asse / scala (Axis / Scale Color): colore dell'asse X / della scala.

• Colore griglia (Grid Color): colore della griglia dell'asse X.

• Divisioni principali (Main sub-scale): tacche principali dell'asse X.

• Divisioni secondarie (Sub-scale): tacche secondarie dell'asse X.

Display Scale: visualizza la scala dell'asse X.

• Asse Y

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

<img src="../../../configuration-guide/extended-controls/trend.files/image004.jpg" width="130" />

Per la scheda "Visibility", vedere l'oggetto "Pulsante di bit".
