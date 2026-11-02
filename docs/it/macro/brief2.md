# Riepilogo della sezione

1\.  Dal punto di vista dell'esecuzione, un programma si compone di tre strutture di base: struttura sequenziale, struttura a diramazione e struttura a ciclo.

2\.  L'unità di base dell'esecuzione di un programma è l'istruzione. Il linguaggio C prevede cinque tipi di istruzioni:

(1)  Istruzione espressione: qualsiasi espressione seguita da un punto e virgola. L'istruzione espressione più comune è l'assegnazione.

(2)  Istruzione di chiamata di funzione: una chiamata di funzione seguita da un punto e virgola.

(3)  Istruzione di controllo: serve a controllare il flusso del programma ed è composta da parole chiave specifiche e dalle espressioni necessarie. Comprende principalmente le istruzioni di esecuzione condizionale, le istruzioni di ciclo, l'istruzione goto, ecc.

(4)  Istruzione composta: è formata da più istruzioni racchiuse tra {}. Un'istruzione composta è considerata come un'unica istruzione e può essere usata ovunque sia ammessa un'istruzione, per esempio come corpo di un ciclo.

(5)  Istruzione vuota: è formata solo da un punto e virgola e non esegue alcuna operazione.

3\.  Le espressioni relazionali e le espressioni logiche sono due tipi di espressioni importanti, usati principalmente per le condizioni di esecuzione condizionale e dei cicli.

4\.  Il linguaggio C offre diverse forme di istruzione condizionale per realizzare strutture a diramazione. (1)   L'istruzione if si usa principalmente per una scelta a una via.

(2)  L'istruzione if-else si usa principalmente per una scelta a due vie.

(3)  Le istruzioni if-else-if e switch si usano per scelte a più vie. Queste forme di istruzione condizionale sono in genere intercambiabili.

5\.  Il linguaggio C offre tre istruzioni di ciclo.

(1)  L'istruzione for si usa principalmente quando sono noti il valore iniziale della variabile di ciclo, l'incremento e il numero di iterazioni. (2)  Quando il numero di iterazioni e la condizione di controllo si determinano durante l'esecuzione del ciclo, si possono usare le istruzioni while

o do-while.

(3)  Le tre istruzioni di ciclo possono essere annidate tra loro per formare cicli annidati. I cicli possono essere in parallelo ma non incrociati. (4)  Un'istruzione di salto può far uscire il flusso dal corpo del ciclo, ma non può farlo entrare nel corpo del ciclo dall'esterno.

(5)  Evitare i cicli infiniti: occorre assicurarsi che la variabile di ciclo venga modificata durante l'esecuzione, in modo che la condizione di ciclo diventi prima o poi falsa e il ciclo termini.

6\.  Riepilogo delle istruzioni del linguaggio C

Nome Forma generale

Istruzione semplice Istruzione espressione; Istruzione vuota ;

Istruzione condizionale if(espressione)istruzione;

if(espressione)istruzione 1; else istruzione 2;

if(espressione 1)istruzione 1;  else if(espressione 2) istruzione 2…else istruzione n; istruzione switch switch(espressione){ case costante: istruzione…default: istruzione;  } istruzione di ciclo while

```c
while(expression)statement;
for statement for(expression 1; expression 2; expression 3) statement; break statement break;
continue statement continue;
return statement return(expression);
```
