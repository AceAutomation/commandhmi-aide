# FAQ e soluzioni

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>       <strong>Area</strong></p></td>
<td colspan="2"><p><strong>Sintomo</strong></p></td>
<td><p><strong>Causa</strong></p></td>
<td><p><strong>Soluzione</strong></p></td>
</tr>
<tr class="even">
<td rowspan="6"><p><strong>Display</strong></p></td>
<td rowspan="5"><p>Schermo nero</p></td>
<td rowspan="3"><p>Schermo nero all'accensione</p></td>
<td><p>Problema di alimentazione</p></td>
<td><p>1. Verificare il collegamento dell'alimentazione; 2. Verificare il tipo di alimentazione: deve essere un'alimentazione dedicata 24 VDC (±20%).</p></td>
</tr>
<tr class="odd">
<td><p>Errore nel progetto di configurazione, per esempio uso scorretto delle macro: puntatore nullo, puntatore non inizializzato, accesso fuori dai limiti di un array, divisione per 0.</p></td>
<td><p>Portare l'interruttore DIP 2 su ON e riscaricare un progetto semplice per il test; se la macro non funziona correttamente, eseguirne il debug e correggerne la programmazione.</p></td>
</tr>
<tr class="even">
<td><p>Guasto dell'unità: corrosione del cavo flat dell'LCD, problema dell'oscillatore al quarzo, ecc.</p></td>
<td><p>Contattare l'assistenza post-vendita per la riparazione in laboratorio.</p></td>
</tr>
<tr class="odd">
<td rowspan="2"><p>Schermo che diventa improvvisamente nero durante il funzionamento, oppure schermo nero e blocchi occasionali</p></td>
<td><p>Problema di alimentazione</p></td>
<td><p>Verificare il cavo di alimentazione e l'alimentatore.</p></td>
</tr>
<tr class="even">
<td><p>Guasto dell'unità</p></td>
<td><p>Contattare l'assistenza post-vendita per la riparazione in laboratorio.</p></td>
</tr>
<tr class="odd">
<td colspan="2"><p>Righe verticali o orizzontali sullo schermo</p></td>
<td><p>Guasto dell'LCD</p></td>
<td><p>Se le righe compaiono su tutte le pagine, contattare l'assistenza post-vendita per la riparazione in laboratorio.</p></td>
</tr>
<tr class="even">
<td rowspan="4"><p><strong>Touch</strong></p></td>
<td colspan="2" rowspan="2"><p>Risposta lenta al tocco, oggetti difficili da azionare</p></td>
<td><p>Problema di installazione</p></td>
<td><p>1. Verificare che il foro di montaggio non sia troppo piccolo e non schiacci l'HMI; in tal caso rispettare le dimensioni corrette del foro; 2. Verificare che le viti di fissaggio non siano troppo strette e che la pressione sui quattro angoli sia il più possibile uniforme.</p></td>
</tr>
<tr class="odd">
<td><p>Progetto di configurazione non adeguato</p></td>
<td><p>Troppe informazioni nel progetto, troppe macro in background, troppe variabili e oggetti nella pagina: modificare il programma di configurazione, distribuendo in modo ragionevole oggetti e pagine.</p></td>
</tr>
<tr class="even">
<td colspan="2"><p>Il touch non funziona</p></td>
<td><p>Calibrazione delle coordinate o pannello touch danneggiato</p></td>
<td><p>1. Portare l'interruttore DIP 1 su ON per eseguire la calibrazione delle coordinate;</p>
<p>2. <span id="OLE_LINK4"></span><span id="OLE_LINK3"></span>Se non basta, contattare l'assistenza post-vendita per la riparazione in laboratorio.</p></td>
</tr>
<tr class="odd">
<td colspan="2"><p>Tocco errato (sulla tastiera si preme A ma compare X o un altro carattere)</p></td>
<td><p>Guasto del pannello touch</p></td>
<td><p>Contattare l'assistenza post-vendita per la riparazione in laboratorio.</p></td>
</tr>
<tr class="even">
<td rowspan="9"><p><strong>Comunicazione</strong></p></td>
<td rowspan="6"><p>Interruzione della comunicazione tra HMI e controllore</p></td>
<td rowspan="3"><p>La comunicazione non funziona mai</p></td>
<td><p>Guasto del dispositivo comunicante (PLC, microcontrollore, ecc.)</p></td>
<td><p>Verificare lo stato della porta di comunicazione e la corrispondenza dei parametri di comunicazione.</p></td>
</tr>
<tr class="odd">
<td><p>Guasto della porta di comunicazione dell'HMI</p></td>
<td><p>Contattare l'assistenza post-vendita per la riparazione in laboratorio.</p></td>
</tr>
<tr class="even">
<td><p>Cavo di comunicazione interrotto</p></td>
<td><p>Usare per quanto possibile i cavi specifici CommandHMI.</p></td>
</tr>
<tr class="odd">
<td rowspan="3"><p>La comunicazione si interrompe dopo un periodo di funzionamento normale</p></td>
<td><p>Corrosione e ossidazione dei collegamenti del cavo dopo un lungo funzionamento.</p></td>
<td><p>Sostituire o risaldare il cavo di comunicazione.</p></td>
</tr>
<tr class="even">
<td><p>Disturbi ambientali</p></td>
<td><p>Schermare adeguatamente la sorgente di disturbo, usare cavi schermati e un corretto collegamento a terra</p></td>
</tr>
<tr class="odd">
<td><p>Guasto dell'HMI (dovuto a forti campi magnetici, correnti o fulmini sul posto)</p></td>
<td><p>Contattare l'assistenza post-vendita per la riparazione in laboratorio.</p></td>
</tr>
<tr class="even">
<td colspan="2" rowspan="3"><p>L'HMI non si collega al PC e il download non è possibile.</p></td>
<td><p>Driver USB del PC installato in modo errato</p></td>
<td><p>Selezionare il driver corrispondente al sistema e reinstallare il driver USB.</p></td>
</tr>
<tr class="odd">
<td><p>Dimensioni e modello dell'HMI non corrispondono a quelli reali.</p></td>
<td><p>Selezionare il modello corretto di HMI nel software di configurazione.</p></td>
</tr>
<tr class="even">
<td><p>Porta di download dell'HMI danneggiata</p></td>
<td><p>Contattare l'assistenza post-vendita per la riparazione in laboratorio. (Verifica: collegare un altro HMI con lo stesso cavo USB e lo stesso PC; se il download funziona, il guasto è nella porta USB del primo HMI)</p></td>
</tr>
<tr class="odd">
<td rowspan="3"><p><strong>Applicazione</strong></p></td>
<td colspan="2"><p>Configurazione non utilizzabile</p></td>
<td><p>Oggetto o macro non validi nella configurazione</p></td>
<td><p>Correggere la configurazione</p></td>
</tr>
<tr class="even">
<td colspan="2"><p>Compilazione della macro non riuscita</p></td>
<td><p>Posizione della cartella di installazione di HM nelle variabili d'ambiente</p></td>
<td><p>Spostare all'inizio la cartella di installazione di CommandHMI nelle variabili d'ambiente.</p></td>
</tr>
<tr class="odd">
<td colspan="2"><p>La simulazione offline e online non funziona.</p></td>
<td><p>Software avviato senza diritti di amministratore</p></td>
<td><p>Avviare CommandHMI come amministratore</p></td>
</tr>
</tbody>
</table>
