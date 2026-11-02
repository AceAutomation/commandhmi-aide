# Istruzione switch

Il linguaggio C offre anche l'istruzione switch per la scelta tra più rami. La sua forma generale è:

switch(expression){

```c
case constant expression 1: statement 1;
case constant expression 2: statement 2;
```

…

```c
case constant expression n: statement n;
default: statement n+1;
}
```

Significato: viene calcolato il valore dell'espressione e confrontato uno per uno con i valori delle espressioni costanti che seguono. Quando il valore coincide con una delle espressioni costanti, vengono eseguite le istruzioni che la seguono, senza ulteriori confronti: l'esecuzione prosegue con le istruzioni di tutti i case successivi (salvo break). Se il valore non coincide con nessuna delle espressioni costanti dei case, vengono eseguite le istruzioni che seguono default.

Nell'uso dell'istruzione switch occorre tenere presente quanto segue:

1\.  Tutti i valori delle espressioni costanti dopo case devono essere diversi, altrimenti si verifica un errore.

2\.  Dopo case sono ammesse più istruzioni, che non devono necessariamente essere racchiuse tra {}.

3\.  L'ordine delle clausole case e default può essere modificato senza influire sull'esecuzione del programma.

4\.  La clausola default può essere omessa
