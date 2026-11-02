# Visualizzazione storico allarmi

La visualizzazione storico allarmi serve principalmente a mostrare gli allarmi passati; il funzionamento è lo stesso della visualizzazione allarmi, a cui si rimanda. Fare clic sul pulsante Historical Alarm <img src="../../../configuration-guide/extended-controls/alarm-dialog.files/alarm-dialog791.png" width="32" /> nella barra degli strumenti per aprire la finestra seguente:

<img src="../../../configuration-guide/extended-controls/alarm-dialog.files/alarm-dialog1031.png" width="650" />

Indirizzo di controllo (Control address): scrivere 1 nel registro con offset 0 (intero a 16 bit, come per gli offset da 1 a 12), l'ora di inizio nei registri con offset da 1 a 6 e l'ora di fine nei registri con offset da 7 a 12: lo storico allarmi mostrerà i dati del periodo corrispondente. Per visualizzare tutto lo storico allarmi, scrivere 0 nel registro con offset 0. Il registro con offset 13 al momento non è utilizzato.

Questo indirizzo occupa 12 offset consecutivi, con il significato seguente:

|                |                                                                                              |
|----------------|----------------------------------------------------------------------------------------------|
| Offset | Funzione del registro di controllo |
| 0 | 1 = visualizza i dati tra l'ora di inizio e l'ora di fine; 0 = visualizza tutti i dati. |
| 1 | Ora di inizio (anno) |
| 2 | Ora di inizio (mese) |
| 3 | Ora di inizio (giorno) |
| 4 | Ora di inizio (ora) |
| 5 | Ora di inizio (minuti) |
| 6 | Ora di inizio (secondi) |
| 7 | Ora di fine (anno) |
| 8 | Ora di fine (mese) |
| 9 | Ora di fine (giorno) |
| 10 | Ora di fine (ora) |
| 11 | Ora di fine (minuti) |
| 12 | Ora di fine (secondi) |

• Nascondi data allarme (Clear alarm date): non visualizza la data dell'allarme

• Nascondi ora allarme (Clear alarm time): non visualizza l'ora dell'allarme

• Allarme rientrato (Clear alarm): colore della riga di un allarme rientrato

• Conteggio allarmi (Statistics alarms): abilita il conteggio degli allarmi, visualizzato dopo il messaggio.

• Tempo cumulato (Cumulative time): abilita il tempo cumulato dell'allarme, visualizzato dopo il messaggio.

• OK: colore dell'allarme quando viene generato

<img src="../../../configuration-guide/extended-controls/alarm-dialog.files/alarm-dialog2576.png" width="130" />

Per il funzionamento di base, vedere l'oggetto "Visualizzazione allarmi".

Per la scheda "Visibility", vedere l'oggetto "Pulsante di bit".
