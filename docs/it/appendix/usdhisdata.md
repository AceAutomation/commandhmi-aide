# Esportare dati tramite chiavetta USB

Gli HMI della serie HM supportano l'esportazione di dati storici, ricette, allarmi storici e screenshot tramite chiavetta USB.

Poiché CommandHMI gestisce più gruppi di dati storici, per esportarli è necessario indicare il numero del gruppo. LW60408 contiene il numero del gruppo di dati storici selezionato. Per esempio, impostando LW60408 a 1, l'importazione e l'esportazione tramite chiavetta USB riguardano il gruppo di dati storici 0 e nessun altro.

Nota: se il valore inserito supera il numero massimo di gruppi meno 1, la funzione non è attiva.

**Come esportare i dati storici tramite chiavetta USB**

1\. Inserire la chiavetta USB

2\. Impostare nel registro LW60408 il numero del gruppo di dati storici da importare o esportare.

3\. Portare LB60127 a ON: l'HMI copia il file del gruppo di dati storici sulla chiavetta USB con il nome hisdatai.csv (hisdata1.csv se il numero del gruppo è 1).

Portare LB60128 a ON: l'HMI copia il file del gruppo di dati storici dalla chiavetta USB; per importare il gruppo 1, il file deve chiamarsi hisdata1.csv.

Al termine dell'esportazione questi trigger tornano automaticamente a OFF

Per l'esportazione dei dati locali si usano i registri LW: LW60359-LW60429

**Come esportare le ricette**

Poiché CommandHMI gestisce più gruppi di ricette, per l'esportazione è necessario impostare LW61143.

1\. Inserire la chiavetta USB.

2\. Impostare il numero del gruppo in LW61143.

3\. Portare LB60163 a ON: l'HMI copia il file del gruppo di ricette sulla chiavetta USB

4\. Al termine dell'esportazione questi trigger tornano automaticamente a OFF

Nota: i dati storici esportati non possono essere aperti direttamente sul computer: occorre lo strumento di conversione SK_SQL_CSV.exe, <img src="../../appendix/usdhisdata.files/image002.jpg" width="86" />che si trova nella cartella principale del software di configurazione HM.

Questo strumento converte il file esportato in un file CSV apribile direttamente. Fare doppio clic per aprire lo strumento.

Progress: avanzamento della conversione.

File name: selezionare il file da convertire.

Selezionare dati storici o allarmi a seconda del caso. La codifica predefinita è ANSI e non può essere modificata. Dopo le impostazioni, fare clic su "Generate CSV": quando la barra di avanzamento raggiunge il 100%, la conversione è completata.

**Come ottenere screenshot tramite chiavetta USB**

1\. Inserire la chiavetta USB

2\. In fase di configurazione, creare un Function Button -&gt; Screenshot e selezionare l'esportazione su chiavetta USB

3\. Premendo questo pulsante funzione, l'HMI salva la pagina corrente nella memoria corrispondente

<img src="../../appendix/usdhisdata.files/image004.gif" width="595" />

Nota:

 • Non scollegare la chiavetta USB durante l'esportazione;

• Mantenere l'alimentazione durante l'esportazione;

• Verificare che la chiavetta USB disponga di spazio sufficiente.

<img src="../../appendix/usdhisdata.files/image004.gif" width="595" />
