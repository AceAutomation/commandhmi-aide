# Visualizzazione dati storici

<span id="OLE_LINK279"></span><span id="OLE_LINK278"></span>         Nell'uso reale, i dati prodotti dal PLC o da altri dispositivi collegati, come gli allarmi, si aggiornano in continuazione. Per consultare i dati storici si usa la raccolta dati storici di CommandHMI.

CommandHMI offre la funzione di raccolta dati storici, accessibile da Gestione progetto. In un nuovo progetto, fare clic con il tasto destro su "Historical data collector" per aggiungerne una, quindi fare doppio clic su "Historical Data Collector 0" per aprire la finestra delle impostazioni. Per i dettagli vedere le proprietà della "[Raccolta dati storici](../../setting/history-data.md)" nel capitolo 6.

Fare clic sul pulsante di visualizzazione dati storici<img src="../../../configuration-guide/extended-controls/history-record.files/history-record687.png" width="32" /> nella barra degli strumenti: compare la finestra seguente:

<img src="../../../configuration-guide/extended-controls/history-record.files/history-record747.png" width="579" />

Figura 4-65 Finestra Historical Data Display

**Generale (General):**

• Colore primo piano (Foreground Color): fare clic sul colore nel riquadro per cambiare il colore di primo piano della visualizzazione.

• Colore bordo (Border Color): fare clic sul colore nel riquadro per cambiare il colore del bordo della visualizzazione.

• Titolo (Title): dimensione e stile del carattere, colore di sfondo, colore del testo e visualizzazione di data e ora. Per le impostazioni della lingua, vedere "Visualizzazione allarmi".

• Dati (Data): dimensione e colore del carattere e numero massimo di righe visualizzate.

Indirizzo di controllo:

Scrivere 1 nel registro con offset 0 (intero a 16 bit, come per gli offset da 1 a 12), l'ora di inizio nei registri con offset da 1 a 6, l'ora di fine nei registri con offset da 7 a 12 e infine 1 nel registro con offset 13: la visualizzazione dati storici mostrerà i dati del periodo corrispondente. Il registro con offset 13 si azzera automaticamente. Per visualizzare tutti i dati storici, scrivere 0 nel registro con offset 0.

Questo indirizzo occupa 40 offset consecutivi, con il significato seguente:

|                |                                                                                                                                                                          |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Offset | Funzione del registro di controllo |
| 0 | 1 = visualizza i dati tra l'ora di inizio e l'ora di fine; 0 = visualizza tutti i dati. |
| 1 | Ora di inizio (anno); una word |
| 2 | Ora di inizio (mese); una word |
| 3 | Ora di inizio (giorno); una word |
| 4 | Ora di inizio (ora); una word |
| 5 | Ora di inizio (minuti); una word |
| 6 | Ora di inizio (secondi); una word |
| 7 | Ora di fine (anno); una word |
| 8 | Ora di fine (mese); una word |
| 9 | Ora di fine (giorno); una word |
| 10 | Ora di fine (ora); una word |
| 11 | Ora di fine (minuti); una word |
| 12 | Ora di fine (secondi); una word |
| 13 | Passaggio da 0 a 1 con offset 0 = 1: visualizza i dati del periodo indicato; si azzera automaticamente; <span id="OLE_LINK339"></span>una word |
| 14 | Numero di dati storici tra l'ora di inizio e l'ora di fine; double word |

Dati:

<img src="../../../configuration-guide/extended-controls/history-record.files/history-record2617.png" width="581" />

Numero di gruppo: CommandHMI permette di scegliere tra più gruppi di dati storici.

Visualizzazione dei dati storici tramite indirizzi di controllo: la configurazione è quella della Figura 4-65-1:

<img src="../../../configuration-guide/extended-controls/history-record.files/001.png" width="797" />

Figura 4-65-1

In questo esempio, inserendo 1 in "Display all data" e 1 in "Inquire", la visualizzazione mostra tutti i dati storici del periodo compreso tra l'ora di inizio e l'ora di fine, come mostrato nella Figura 4-65-2

<img src="../../../configuration-guide/extended-controls/history-record.files/002.png" width="795" />

Figura 4-65-2

Inserendo 1 in "Display all data", ora di inizio 2016-7-11 3:30:4 e ora di fine 2016-7-11 14:39:4, quando "Inquire" vale 1 vengono visualizzati solo i dati di questo periodo.

<img src="../../../configuration-guide/extended-controls/history-record.files/history-record3263.png" width="130" />

Per la scheda "Visibility", vedere l'oggetto "Pulsante di bit".
