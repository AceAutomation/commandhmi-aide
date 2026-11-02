# Programmi con struttura a diramazione

**Operatori ed espressioni relazionali**

In un programma capita spesso di confrontare due valori per decidere come proseguire. Gli operatori che confrontano i valori si chiamano operatori relazionali. Il linguaggio C dispone dei seguenti operatori relazionali:

<  minore di

<= minore o uguale a

> maggiore di

>= maggiore o uguale a

== uguale a

!= diverso da

Gli operatori relazionali sono operatori binari con associatività a sinistra. La loro priorità è inferiore a quella degli operatori aritmetici e superiore a quella degli operatori di assegnazione. Tra i sei operatori relazionali, <, <=, >, >= hanno la stessa priorità, superiore a quella di == e !=, che a loro volta hanno la stessa priorità.

**Espressioni relazionali**

La forma generale di un'espressione relazionale è: espressione operatore_relazionale espressione. Per esempio, a+b>c-d, x>3/2, 'a'+1<c, -i-5*j==k+1 sono espressioni relazionali valide. Poiché anche un'espressione relazionale è un'espressione, è possibile annidarle, per esempio a>(b>c), a!=(c==d), ecc. Il valore di un'espressione relazionale è "vero" o "falso", rappresentato rispettivamente da "1" e "0".

**1.  Operatori ed espressioni logiche**

Nel linguaggio C gli operatori logici sono l'operatore AND &&, l'operatore OR \|\| e l'operatore NOT !. Gli operatori AND && e OR \|\| sono binari con associatività a sinistra. L'operatore NOT ! è unario con associatività a destra. La relazione di priorità tra gli operatori logici e gli altri operatori è la seguente:

In base alla priorità degli operatori si ottiene quanto segue:

a>b && c>d equivale a (a>b) &&  (c>d)

!b==c\|\|d&lt;a equivale a ((!b)==c)\|\|(d&lt;a)

a+b>c && x+y<b equivale a ((a+b)>c) && ((x+y)<b) Valutazione delle operazioni logiche

Il risultato di un'operazione logica può essere vero o falso, rappresentato rispettivamente da 1 e 0. Le regole di valutazione sono le seguenti:

1\.  L'operazione AND && dà vero solo se entrambi i valori sono veri; altrimenti dà falso. Per esempio, 5&gt;0

&& 4>2: poiché 5>0 è vero e 4>2 è vero, il risultato è vero.

2\.  L'operazione OR \|\| dà vero se almeno uno dei due valori è vero, e falso solo se entrambi sono falsi. Prendiamo ad esempio 5&gt;0\|\|5&gt;8: poiché 5&gt;0 è vero, il risultato è vero.

3\.  L'operazione NOT ! dà falso se l'operando è vero e vero se l'operando è falso.

Per esempio, il risultato di !(5>0) è falso.

Nel linguaggio C il risultato di un'operazione logica rappresenta "vero" con "1" e "falso" con "0". Viceversa, quando si valuta se un valore è vero o falso, 0 rappresenta falso e qualsiasi valore diverso da zero rappresenta vero. Per esempio, poiché 5 e 3 sono diversi da zero, il valore di 5&&3 è "vero" (cioè 1).

Un altro esempio: il valore di 5\|\|0 è "vero" (cioè 1).

La forma generale di un'espressione logica è: espressione operatore_logico espressione. Le espressioni possono a loro volta essere espressioni logiche, formando così un annidamento, per esempio (a&&b)&&c. Grazie all'associatività a sinistra degli operatori logici, questa espressione può essere scritta a&&b&&c. Il valore di un'espressione logica è il risultato finale delle varie operazioni logiche, con "1" per "vero" e "0" per "falso".

**2.  Istruzione if**

L'istruzione if permette di costruire una struttura a diramazione: in base alle condizioni indicate, decide quale ramo del programma eseguire. L'istruzione if del linguaggio C ha tre forme di base.

1\.  La prima forma è la forma base: if (espressione) istruzione

Significato: se il valore dell'espressione è vero, viene eseguita l'istruzione che segue, altrimenti no.

2\.  La seconda forma è if-else: if(espressione)

istruzione 1; else istruzione 2;

Significato: se il valore dell'espressione è vero, viene eseguita l'istruzione 1, altrimenti l'istruzione 2.

Leggere due interi e restituire il maggiore. Si confrontano a e b con un'istruzione if-else: se a è maggiore, il risultato è a;

altrimenti b.

**3.  La terza forma è if-else-if.**

Nelle prime due forme l'istruzione if si usa normalmente per due rami. Quando i rami possibili sono più di due, si utilizza l'istruzione if-else-if, la cui forma di base è:

if(espressione 1)

istruzione 1;

else if(espressione 2)

istruzione  2;

else if(espressione 3)

istruzione  3;

…

else if(espressione m)

istruzione m; else istruzione n;

Significato: le espressioni vengono valutate in sequenza. Appena un valore risulta vero, viene eseguita l'istruzione corrispondente e il programma prosegue dopo l'intera istruzione if. Se tutte le espressioni sono false, viene eseguita l'istruzione n, dopodiché il programma prosegue normalmente.

**Nell'uso dell'istruzione if occorre tenere presente quanto segue:**

(1)  In tutte e tre le forme dell'istruzione if, dopo if si trova un'espressione, di solito logica o relazionale. Può però trattarsi anche di altre espressioni, come un'assegnazione o persino una semplice variabile. Per esempio, if(a=5) istruzione e if(b) istruzione sono ammesse. Se il valore dell'espressione è diverso da 0, la condizione è vera. In if(a=5)…; il valore dell'espressione è sempre diverso da 0, quindi l'istruzione che segue viene sempre eseguita. Questa situazione non dovrebbe presentarsi in un programma, ma la sintassi è corretta.

Un altro esempio, frammento di programma: if(a=b)

```c
printf("%d",a); else printf("a=0");
```

Significato dell'istruzione: assegna b ad a; se il valore non è 0, lo stampa, altrimenti stampa la stringa "a=0". Questo tipo di costrutto è frequente nei programmi.

(2)  Nell'istruzione if, l'espressione della condizione deve essere racchiusa tra parentesi tonde e l'istruzione deve terminare con un punto e virgola.

(3)  In tutte e tre le forme dell'istruzione if, le istruzioni devono essere istruzioni singole. Se si vuole eseguire un gruppo di istruzioni in base a una condizione, il gruppo deve essere racchiuso tra {} per formare un'istruzione composta. Attenzione: dopo } non va messo il punto e virgola.

Per esempio:

```c
if(a>b){ a++; b++;
}
else{ a=0;
b=10;
}
```

**4.  Operatore condizionale ed espressione condizionale**

Quando l'istruzione condizionale esegue solo una semplice assegnazione, di solito la si sostituisce con un'espressione condizionale, che semplifica il codice e migliora l'efficienza di esecuzione.

L'operatore condizionale ? : è un operatore ternario, cioè coinvolge tre operandi. La forma generale di un'espressione condizionale è:

Espressione 1 ? Espressione 2 : Espressione 3

Regola di valutazione: se l'espressione 1 è vera, il valore dell'espressione condizionale è quello dell'espressione 2; altrimenti è quello dell'espressione 3. L'espressione condizionale si usa di solito nelle istruzioni di assegnazione. Per esempio:

```c
if(a>b) max=a;
else max=b;
```

max=(a>b)?a:b; è la forma con espressione condizionale. Significato: se a>b è vero, assegna a a max, altrimenti assegna b a max.

Nell'uso delle espressioni condizionali occorre tenere presente quanto segue:

1\.  La priorità dell'operatore condizionale è inferiore a quella degli operatori relazionali e aritmetici, ma superiore a quella degli operatori di assegnazione. Di conseguenza, in max=(a&gt;b)?a:b si possono togliere le parentesi: max=a&gt;b?a:b.

2\.  I simboli ? e : formano un'unica coppia di operatori e non possono essere usati separatamente.

3\.  L'associatività dell'operatore condizionale è da destra a sinistra.
