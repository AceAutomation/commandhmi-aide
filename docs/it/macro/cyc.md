# Programmi con struttura a ciclo

La struttura a ciclo è una struttura fondamentale dei programmi. Finché una determinata condizione è soddisfatta, un blocco di programma viene eseguito ripetutamente, fino a quando la condizione non è più soddisfatta. La condizione si chiama condizione di ciclo e il blocco eseguito ripetutamente si chiama corpo del ciclo. Il linguaggio C offre diverse istruzioni di ciclo, con cui realizzare strutture a ciclo differenti.

**1.  Istruzione while**

Forma generale dell'istruzione while: while (espressione) istruzione;

dove l'espressione è la condizione di ciclo e l'istruzione è il corpo del ciclo.

Significato dell'istruzione while: viene calcolato il valore dell'espressione; se è vero (diverso da 0), viene eseguito il corpo del ciclo.

Nell'uso dell'istruzione while occorre tenere presente quanto segue:

1\.  L'espressione dell'istruzione while è di solito un'espressione relazionale o logica. Finché il valore dell'espressione è vero (diverso da 0), il ciclo continua.

2\.  Se il corpo del ciclo contiene una o più istruzioni, deve essere racchiuso tra {} per formare un'istruzione composta.

3\.  Prestare attenzione alle condizioni del ciclo per evitare cicli infiniti.

**2.  Istruzione do-while**

Forma generale dell'istruzione do-while:

```c
do statement;
while (expression);
```

dove l'istruzione è il corpo del ciclo e l'espressione è la condizione di ciclo. Significato dell'istruzione do-while:

il corpo del ciclo viene eseguito una prima volta, poi viene valutata l'espressione. Se il valore è vero (diverso da 0), il ciclo continua; altrimenti termina.

La differenza tra do-while e while è che do-while prima esegue e poi verifica la condizione: il corpo del ciclo viene quindi eseguito almeno una volta. L'istruzione while, invece, prima verifica e poi esegue: se la condizione non è soddisfatta, il corpo del ciclo non viene eseguito nemmeno una volta.

Le istruzioni while e do-while possono di solito essere riscritte l'una nell'altra.

In questo esempio la condizione di ciclo è stata riscritta come --n, altrimenti verrebbe eseguita un'iterazione in più. Nell'uso dell'istruzione do-while occorre tenere presente quanto segue:

1\.  Nelle istruzioni if e while non si mette il punto e virgola dopo l'espressione, mentre l'espressione dell'istruzione do-while deve terminare con il punto e virgola.

2\.  L'istruzione do-while può formare cicli annidati ed essere annidata con l'istruzione while e viceversa.

3\.  Il corpo del ciclo tra do e while è composto da più istruzioni racchiuse tra {} per formare un'istruzione composta.

4\.  Quando si converte un do-while in while o viceversa, fare attenzione a modificare le condizioni di controllo del ciclo.
