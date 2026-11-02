# Istruzioni del programma C

La parte esecutiva di un programma C è costituita da istruzioni, ed è tramite l'esecuzione delle istruzioni che il programma svolge le sue funzioni. Le istruzioni C si dividono in cinque categorie:

1\.  Istruzione di espressione

2\.  Istruzione di controllo

3\.  Istruzione composta

4\.  Istruzione vuota

**1.  Istruzioni espressione**

Un'istruzione espressione è composta da un'espressione e da un punto e virgola. La sua forma generale è espressione;. Eseguire un'istruzione espressione significa calcolare il valore dell'espressione. Per esempio: x=y+z; è un'istruzione di assegnazione; y+z; esegue un'addizione ma il risultato non viene conservato, quindi non ha effetto pratico; i++; è un'istruzione di incremento che aumenta i di 1.

**2.  Istruzioni di controllo**

Le istruzioni di controllo gestiscono il flusso del programma, permettendo di realizzarne le diverse strutture.

Sono composte da parole chiave specifiche. Il linguaggio C dispone di nove istruzioni di controllo, suddivise in tre gruppi:

(1)  Istruzioni condizionali: istruzione if, istruzione switch

(2)  Istruzioni di ciclo

istruzione do while, istruzione while, istruzione for

(3)  Istruzioni di salto

istruzione break, istruzione goto, istruzione continue, istruzione return

**3.  Istruzioni vuote**

Un'istruzione composta solo da un punto e virgola si chiama istruzione vuota e non esegue nulla. Nel programma un'istruzione vuota può fungere da corpo vuoto di un ciclo. Per esempio, while (getchar()!='\n'); : finché il carattere inserito da tastiera non è Invio, l'inserimento viene ripetuto. In questo caso il corpo del ciclo è un'istruzione vuota.

**4.  Istruzioni di assegnazione**

Un'istruzione di assegnazione è composta da un'espressione di assegnazione e da un punto e virgola. La sua forma generale è variabile = espressione;. Funzioni e caratteristiche sono le stesse dell'espressione di assegnazione. È una delle istruzioni più usate nei programmi. Nel suo utilizzo occorre tenere presente quanto segue:

1\.  Poiché l'espressione a destra del segno di assegnazione "=" può essere a sua volta un'assegnazione, la forma Variabile=(variabile=espressione); è valida e si ottiene un'assegnazione annidata. La forma estesa è Variabile=Variabile=…=Espressione;

Per esempio:

```c
a=b=c=d=e=5; according to the right associativity of assignment operator, it is equivalent to: e=5 actually;
d=e; c=d; b=c; a=b;
```

2\.  Fare attenzione alla differenza tra l'assegnazione del valore iniziale nella dichiarazione di una variabile e l'istruzione di assegnazione.

L'assegnazione del valore iniziale fa parte della dichiarazione della variabile: la variabile inizializzata va separata dalle altre variabili dello stesso tipo con una virgola, mentre l'istruzione di assegnazione deve terminare con un punto e virgola.

3\.  Nella dichiarazione di variabili non è consentito assegnare il valore iniziale a più variabili in cascata. Per esempio, la dichiarazione seguente è errata: Int a=b=c=5 deve essere scritta int a=5,b=5,c=5. L'istruzione di assegnazione, invece, può essere concatenata.

4\.  Notare la differenza tra espressione di assegnazione e istruzione di assegnazione. L'espressione di assegnazione è un tipo di espressione e può essere usata ovunque sia ammessa un'espressione; l'istruzione di assegnazione no.

L'istruzione seguente è valida: if((x=y+5)>0) z=x; significato: se l'espressione x=y+5 è maggiore di 0, allora z=x.

L'istruzione seguente non è valida: if((x=y+5;)>0) z=x; poiché x=y+5; è un'istruzione, non può essere usata all'interno di un'espressione.
