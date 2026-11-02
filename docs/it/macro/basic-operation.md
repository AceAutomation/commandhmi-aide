# Operatori di base ed espressioni

**Categorie, priorità e associatività degli operatori**

Il linguaggio C dispone di numerosi operatori ed espressioni, cosa piuttosto rara tra i linguaggi di alto livello. È proprio questa ricchezza di operatori ed espressioni a rendere completo il linguaggio C, ed è una delle sue caratteristiche principali.

Gli operatori del C hanno priorità diverse e, inoltre, una propria associatività. In un'espressione, l'ordine di calcolo dipende non solo dalla priorità degli operatori ma anche dalla loro associatività, che determina se l'operazione procede da sinistra a destra o da destra a sinistra. Questa associatività, assente in altri linguaggi di alto livello, aumenta la complessità del linguaggio C.

Categorie di operatori

Gli operatori del linguaggio C si possono classificare come segue:

**1.  Operatori aritmetici**

Servono per le operazioni sui dati: addizione (+), sottrazione (-), moltiplicazione (*), divisione (/), resto (modulo, %), incremento (++) e decremento (--).

**2.  Operatori relazionali**

Servono per le operazioni di confronto: maggiore di (>), minore di (<), uguale a (==), maggiore o uguale a (>=), minore o uguale a (<=) e diverso da (!=).

**3.  Operatori logici**

Servono per le operazioni logiche: AND (&&), OR (\|\|) e NOT (!).

**4.  Operatori sui bit**

Operano sui dati a livello di singolo bit: AND bit a bit (&), OR bit a bit (\|), NOT bit a bit (~), OR esclusivo bit a bit (^), scorrimento a sinistra (&lt;&lt;) e scorrimento a destra (&gt;&gt;).

**5.  Operatori di assegnazione**

Servono per le operazioni di assegnazione: assegnazione semplice (=), assegnazione aritmetica composta (+=,-=,*=, /=, %=)

e assegnazione composta sui bit (&=,\|=, ^=,&gt;&gt;=,&lt;&lt;=).

**6.  Operatore condizionale**

È un operatore ternario per la valutazione condizionale (?:).

**7.  Operatore virgola**

Serve per combinare più espressioni in un'unica espressione (,).

**8.  Operatori sui puntatori**

Servono per due operazioni: lettura del contenuto (*) e lettura dell'indirizzo (&).

**9.  Operatore sizeof**

Serve per calcolare la dimensione dei dati.

**10. Operatori speciali**

Comprendono le parentesi (), l'indice \[\] e altri.
