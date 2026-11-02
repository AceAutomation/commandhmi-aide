# Pulsante di word

Il pulsante di word permette di eseguire sull'indirizzo del registro dati del dispositivo collegato le operazioni: costante, inserimento valore, incremento, decremento, inserimento password, somma e sottrazione.

Per aggiungere un pulsante di word:

• Selezionare l'icona Word Button<img src="../../../configuration-guide/basic-control/wordbutton.files/wordbutton222.png" width="29" /> nella barra degli strumenti: compare la finestra di dialogo mostrata nella Figura 4-76:

<img src="../../../configuration-guide/basic-control/wordbutton.files/wordbutton308.png" width="664" />

Figura 4-76 Finestra di dialogo Word Button

<img src="../../../configuration-guide/basic-control/wordbutton.files/wordbutton345.png" width="130" />

Per forma, colore bordo, colore primo piano, colore sfondo e motivo, vedere l'oggetto "Pulsante di bit".

**Funzione:**

• Imposta costante (Set constant): è possibile scegliere tra diversi tipi di dato; CommandHMI offre intero positivo a 16/32 bit, intero a 16/32 bit, intero positivo BCD a 16/32 bit e virgola mobile a 32 bit. La funzione scrive all'indirizzo di scrittura il valore costante impostato. Per esempio, con indirizzo di scrittura LW1 e costante 10, a ogni tocco del pulsante LW1 viene impostato a 10, qualunque sia il valore corrente.

• Inserisci valore (Enter value): è possibile scegliere tra diversi tipi di dato; toccando il pulsante di word compare una tastiera con cui inserire un valore compreso tra minimo e massimo. Come mostrato nella Figura 4-77:

<img src="../../../configuration-guide/basic-control/wordbutton.files/wordbutton1128.png" width="693" />

Figura 4-77

• Incremento (Increasing): con ritardo ("Delay parameter") pari a 0, la funzione è uguale a "Add". Con ritardo diverso da 0, il valore dell'indirizzo di scrittura aumenta della costante impostata e viene scritto nel registro.

• Decremento (Decreasing): con ritardo pari a 0, la funzione è uguale a "Subtract". Con ritardo diverso da 0, dopo il tempo impostato il valore dell'indirizzo di scrittura diminuisce della costante e viene scritto nel registro.

• Inserisci password (Enter Password): come "Enter Value", ma senza l'opzione delle cifre decimali.

• Somma (Add): dopo aver scelto tipo di dato, indirizzo di scrittura, costante e valore massimo, a ogni tocco del pulsante di word il valore del registro viene aumentato della costante rispetto al valore precedente, senza però superare il massimo impostato. Per esempio, con indirizzo di scrittura LW1, costante 5 e massimo 65535, a ogni clic sul pulsante il valore di LW1 aumenta di 5, ma non può superare 65535.

• Sottrai (Subtract): dopo aver scelto tipo di dato, indirizzo di scrittura, costante e valore minimo, a ogni tocco del pulsante di word il valore del registro viene diminuito della costante rispetto al valore precedente, senza però scendere sotto il minimo impostato. Per esempio, con indirizzo di scrittura LW1, costante 5 e minimo 0, a ogni clic sul pulsante il valore di LW1 diminuisce di 5, ma non può scendere sotto 0.

• Numero totale di cifre (Total number of digits): numero di cifre del dato, decimali compresi.

• Cifre decimali (Decimal digits): se il tipo di dato non è "virgola mobile a 32 bit" e sono impostate cifre decimali, il valore massimo inseribile viene diviso per 10 elevato alla n. Per esempio, con tipo di dato "intero positivo a 32 bit" e 3 decimali, l'utente può inserire solo valori da 0 a 99999.999.

• Macro: selezionando "Use Macro" compare l'elenco delle macro; l'utente può sceglierne una da eseguire alla pressione del pulsante di word. Nell'elenco a discesa compaiono solo le macro compilate.

<img src="../../../configuration-guide/basic-control/wordbutton.files/wordbutton3632.png" width="130" />

La scheda "Mark" del pulsante di word è simile a quella del "Pulsante di bit", con la differenza che non ha Status Text 1 né Status Picture 1, perché il pulsante di word ha un solo stato.

Se per il pulsante di word si seleziona il tipo di dato a 32 bit, l'indirizzo occupa due word. Per esempio, scrivendo in V10 di un PLC SIEMENS, vengono occupati i registri V10 e V11; se l'utente monitora anche V11 con un altro oggetto, il funzionamento non è corretto. Prestare attenzione all'uso dei tipi di dato a 32 bit per evitare errori.

Le schede Advanced e Visibility del pulsante di word sono uguali a quelle del pulsante di bit, a cui si rimanda anche per l'uso dei tasti di scelta rapida.
