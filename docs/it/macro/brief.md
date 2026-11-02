# Riepilogo della sezione

**1.  Tipi di dati in C**

Tipi base, tipi costruiti, tipi puntatore e tipo void

**2.  Classificazione e caratteristiche dei tipi base**

|                   |        |                                         |
|-------------------|--------|-----------------------------------------|
| Specificatore di tipo | Byte | Intervallo di valori |
| char | 1 | Set di caratteri C |
| int               | 4      | -214783648～214783647                   |
| short int         | 4      | -214783648～214783647                   |
| long int          | 8      | -922337203685477808～922337203685477807 |
| unsigned          | 4      | 0～4294967295                           |
| unsigned long     | 8      | 0～1844744073709551615                  |
| float             | 4      | 3/4E-38～3/4E+38                        |
| double            | 8      | 1/7E-308～1/7E+308                      |

**3.  Suffissi delle costanti**

L o l per long int

U o u per unsigned

F o f per float

**4.  Tipi di costanti**

Int, long int, unsigned, float, char, stringhe di caratteri, costanti simboliche e caratteri di escape

**5.  Conversione dei tipi di dati**

Conversione automatica

Nelle operazioni miste tra dati di tipo diverso, il sistema esegue una conversione automatica dal tipo con meno byte a quello con più byte. Anche nelle assegnazioni tra dati di tipo diverso il sistema converte automaticamente il tipo del valore a destra nel tipo della variabile a sinistra.

Conversione forzata (cast)

Si effettua con l'operatore di conversione forzata (cast).

**6.  Priorità e associatività degli operatori**

In generale, gli operatori unari hanno priorità alta e gli operatori di assegnazione priorità bassa. Gli operatori aritmetici hanno priorità più alta degli operatori relazionali e logici. La maggior parte degli operatori ha associatività a sinistra; gli operatori unari, l'operatore ternario e l'assegnazione hanno associatività a destra.

**7.  Espressioni**

Un'espressione è una formula composta da costanti, variabili e funzioni collegate da operatori. Ogni espressione ha un valore e un tipo. Il calcolo di un'espressione segue l'ordine stabilito dalla priorità e dall'associatività degli operatori.

**8.  Array**

1\.  L'array è la struttura dati più comune nella programmazione. Esistono array numerici (array di int, array di float), array di caratteri, nonché array di puntatori e array di strutture, descritti più avanti.

2\.  Un array può essere monodimensionale, bidimensionale o multidimensionale.

3\.  La dichiarazione di un array comprende lo specificatore di tipo, il nome dell'array e la sua lunghezza (numero di elementi). Gli elementi dell'array sono detti anche variabili indicizzate. Il tipo dell'array corrisponde al tipo di valore delle variabili indicizzate.

4\.  Un array può essere valorizzato in tre modi: con l'inizializzazione, con l'assegnazione dinamica tramite funzioni di input e con istruzioni di assegnazione. Un array numerico non può essere assegnato, letto o scritto nel suo insieme con una sola istruzione, ma va gestito elemento per elemento con un ciclo.
