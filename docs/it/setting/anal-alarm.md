# Registrazione allarmi analogici

Aprire la finestra delle impostazioni degli allarmi analogici, come mostrato nella Figura 7-28:

Sono disponibili due tipi: Valore numerico e Confronto numerico.

<img src="../../setting/anal-alarm.files/image002.jpg" width="145" />

L'allarme a confronto numerico è mostrato di seguito:

<img src="../../setting/anal-alarm.files/image007.jpg" width="599" />

Figura 7-28    Finestra Registrazione allarmi analogici

Per usare gli allarmi analogici, procedere come segue:

• Inserire prima l'indirizzo da sorvegliare nella colonna "Indirizzo di lettura" (Read Address). In questo esempio si usa l'indirizzo interno LW1.

• Selezionare nell'opzione "Dimensione" (Size) il numero totale di allarmi, cioè il numero totale di indirizzi; il tipo di dati determina come viene letto l'indirizzo. Ogni indirizzo è impostato inizialmente come dato a 16 bit, con indirizzi consecutivi, ma il tipo può essere modificato. Come mostrato nella Figura 7-28, per LW1 è scelto un intero positivo a 32 bit, mentre LW3 e LW4 sono interi positivi a 16 bit. Quindi, se per un indirizzo si sceglie un dato a 32 bit, l'indirizzo successivo è quello precedente più 2; se si sceglie un dato a 16 bit, è quello precedente più 1.

• L'utente può impostare il "Tempo di scansione" (Scanning time) dell'allarme, cioè la frequenza di scansione.

• Fare clic su ogni voce per inserire un valore nel campo "Limite" (Limit) a destra, poi inserire il testo (contenuto dell'allarme) nel campo "Testo" (Text). Si supponga che i messaggi siano quelli della Figura 7-28: il valore di ogni indirizzo può ricadere in uno di quattro intervalli: Basso, Molto basso, Alto, Molto alto.

Come mostrato nella Figura 7-29:

<img src="../../setting/anal-alarm.files/image004.jpg" width="566" />

Figura 7-29    I quattro intervalli di valore per l'indirizzo LW1

• Molto basso (Low Low): quando il valore è inferiore al limite impostato e l'opzione "Usa" (Use) è selezionata, il messaggio di allarme viene mostrato nell'"Oggetto allarme" o nella "Barra allarmi dinamica";

• Basso (Low): quando il valore è maggiore o uguale al limite "Molto basso" ma inferiore al limite "Basso" e l'opzione "Usa" è selezionata, il messaggio di allarme viene mostrato nell'"Oggetto allarme" o nella "Barra allarmi dinamica";

• Alto (High): quando il valore è superiore al limite "Alto" ma non superiore al limite "Molto alto" e l'opzione "Usa" è selezionata, il messaggio di allarme viene mostrato nell'"Oggetto allarme" o nella "Barra allarmi dinamica".

• Molto alto (High High): quando il valore è superiore al limite impostato e l'opzione "Usa" è selezionata, il messaggio di allarme viene mostrato nell'"Oggetto allarme" o nella "Barra allarmi dinamica".

• Esporta U (U export): esporta le impostazioni degli allarmi

• Importa U (U import): importa le impostazioni degli allarmi

Per l'uso dell'opzione "Usa", vedere "Registrazione allarmi digitali".

L'allarme a valore numerico scatta quando il valore raggiunge il valore limite impostato.

Le impostazioni sono le seguenti: l'allarme scatta quando il valore raggiunge 1, 12, 30 e 40.

<img src="../../setting/anal-alarm.files/image006.jpg" width="130" />

Nota: gli HMI serie HM supportano fino a 10 allarmi analogici.
