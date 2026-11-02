# Istruzione for

L'istruzione for è un'istruzione di ciclo del linguaggio C particolarmente potente e di ampio impiego. La sua forma generale è:

for (Espressione 1;Espressione 2;Espressione 3)

istruzione;

Espressione 1: di solito assegna il valore iniziale alla variabile di ciclo ed è un'espressione di assegnazione. Il valore iniziale può anche essere assegnato alla variabile di ciclo al di fuori dell'istruzione for; in questo caso l'espressione può essere omessa.

Espressione 2: di solito è la condizione di ciclo, un'espressione relazionale o logica. Espressione 3: di solito modifica il valore della variabile di ciclo ed è un'espressione di assegnazione.

Le tre espressioni possono essere espressioni con virgola, cioè ciascuna può essere composta da più espressioni. Tutte e tre sono facoltative e possono essere omesse.

L'"istruzione" della forma generale è il corpo del ciclo. Il funzionamento dell'istruzione for è il seguente:

1\.  Per prima cosa si calcola il valore dell'espressione 1.

2\.  Poi si calcola il valore dell'espressione 2. Se è vero (diverso da 0), il corpo del ciclo viene eseguito ancora una volta; altrimenti si esce dal ciclo.

3\.  Si calcola il valore dell'espressione 3 e si torna al passo 2. Durante l'esecuzione del for, l'espressione 1 viene calcolata una sola volta, mentre le espressioni 2 e 3 possono essere ripetute più volte. Il corpo del ciclo può essere eseguito molte volte oppure mai.

Nell'uso dell'istruzione for occorre tenere presente quanto segue:

1\.  Ogni espressione dell'istruzione for può essere omessa, ma i punti e virgola devono essere presenti. Per esempio:

<1>for(;espressione; espressione) espressione 1 omessa

<2>for(espressione; espressione;) espressione 3 omessa

<3>for(;;) tutte le espressioni omesse

2\.  Se alla variabile di ciclo è già stato assegnato un valore iniziale, l'espressione 1 può essere omessa, come nell'esempio 3.27. Se l'espressione

2 o 3, si rischia un ciclo infinito: in questo caso il ciclo deve essere terminato all'interno del corpo del ciclo.

3\.  Il corpo del ciclo può essere un'istruzione vuota.

```c
#include" stdio.h" void main(){
int n=0;
printf("input a string:\n"); for(;getchar()!='\n';n++); printf("%d",n);
}
```

In questo esempio l'espressione 1 dell'istruzione for è omessa e l'espressione 3 non modifica la variabile di ciclo ma conta i caratteri inseriti. Il conteggio, che normalmente avverrebbe nel corpo del ciclo, viene quindi svolto nell'espressione, e il corpo del ciclo è un'istruzione vuota. Attenzione: il punto e virgola dell'istruzione vuota è indispensabile. Se manca, l'istruzione printf successiva viene eseguita come corpo del ciclo. Al contrario, se il corpo del ciclo non è un'istruzione vuota, non bisogna mettere il punto e virgola dopo la parentesi dell'espressione: in quel caso il corpo del ciclo verrebbe considerato un'istruzione vuota e non verrebbe ripetuto. Questi sono errori di programmazione frequenti, a cui prestare la massima attenzione.
