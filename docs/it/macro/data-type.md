# Tipi di dati del linguaggio C

**1.  Interi**

I dati interi comprendono costanti intere e variabili intere. Le costanti intere sono numeri interi. Nel linguaggio C esistono tre tipi di costanti intere: ottali, esadecimali e decimali.

**2.  Costanti intere**

1\.  Costante intera ottale

Una costante intera ottale deve iniziare con 0: lo 0 è il prefisso delle costanti ottali. Le cifre ammesse vanno da 0 a 7. Le costanti ottali sono di solito senza segno. Esempi di costanti ottali valide:

015 (decimale: 13) 0101 (decimale: 65) 0177777 (decimale: 65535)

Esempi di costanti ottali non valide: 256 (manca il prefisso 0) 03A2 (contiene cifre non ottali) -0127 (contiene il segno meno)

2\.  Costante intera esadecimale

Una costante intera esadecimale ha il prefisso 0X o 0x. Le cifre ammesse sono 0-9, A-F o a-f.

Esempi di costanti esadecimali valide:

0X2A (decimale: 42) 0XA0 (decimale: 160) 0XFFFF (decimale: 65535) Esempi di costanti esadecimali non valide:

5A (manca il prefisso 0X)  0X3H (contiene cifre non esadecimali)

3\.  Costante intera decimale

Una costante intera decimale non ha prefisso. Le cifre ammesse vanno da 0 a 9. Esempi di costanti decimali valide:

237   -568   65535    1627

Esempi di costanti decimali non valide:

023 (il prefisso 0 non è ammesso)  23D (contiene cifre non decimali)

Nel programma queste notazioni si distinguono per il prefisso: non sbagliare il prefisso per evitare risultati errati.

4\.  Su un computer a 16 bit l'intero di base è a 16 bit, quindi l'intervallo dei valori rappresentabili è limitato. Le costanti decimali senza segno vanno da 0 a 65535, quelle con segno da -32768 a +32767. I numeri ottali senza segno vanno da 0 a 0177777, quelli esadecimali senza segno da 0X0 a 0XFFFF o da 0x0 a 0xFFFF. Se il valore supera questi intervalli, occorre usare un intero lungo, indicato dal suffisso "L" o "l". Per esempio:

Costanti decimali long 158L (decimale: 158)  358000L (decimale: 358000)

Costanti ottali long 012L (decimale: 10)  077L (decimale: 63) 0200000L (decimale: 65536)

Costanti esadecimali long  0X15L (decimale: 21) 0XA5L (decimale: 165)  0X10000L (decimale: 65536). Il valore della costante long 158L e della costante int 158 è lo stesso. Tuttavia, poiché 158L è un intero lungo, il compilatore C

gli riserva 4 byte di memoria, mentre per 158, intero di base, riserva 2 byte. Prestare quindi attenzione alle operazioni e ai formati di output per evitare errori. I numeri senza segno si indicano con un suffisso: le costanti intere senza segno hanno il suffisso "U" o "u". Per esempio: 358u,

0x38Au, 235Lu sono numeri senza segno. Prefisso e suffisso possono essere combinati per indicare tipi diversi. Per esempio,

0XA5Lu indica il numero esadecimale long senza segno A5, che in decimale vale 165.

**3.  Variabili intere**

Le variabili intere si suddividono come segue:

1\.  Int

Lo specificatore di tipo è int; occupa 2 byte di memoria e il suo valore è un intero di base.

2\.  Short int

Lo specificatore di tipo è short int o short. Il numero di byte occupati e l'intervallo di valori sono gli stessi di int.

3\.  Long int

Lo specificatore di tipo è long int o long; occupa 4 byte di memoria e il suo valore è un intero lungo.

4\.  Unsigned int

Lo specificatore di tipo è unsigned.

Il modificatore unsigned può essere combinato con i tre tipi precedenti:

(1)  Lo specificatore di tipo dell'intero senza segno è unsigned int o unsigned. (2)  Lo specificatore di tipo dell'intero corto senza segno è unsigned short.

(3)  Lo specificatore di tipo dell'intero lungo senza segno è unsigned long.

Gli interi senza segno occupano lo stesso numero di byte dei corrispondenti interi con segno, ma poiché manca il bit di segno non possono rappresentare numeri negativi. La tabella seguente riporta i byte di memoria e l'intervallo di valori dei vari tipi interi su ARM.

|                |                                        |                |
|----------------|----------------------------------------|----------------|
| Specificatore di tipo | Intervallo di valori                   | Byte allocati  |
| Int            | -2147483648~2147483647                 | ■■■■           |
| Short int      | -2147483648~2147483647                 | ■■■■           |
| Signed int     | -2147483648~2147483647                 | ■■■■           |
| Unsigned int   | 0~4294967295                           | ■■■■           |
| Long int       | -922337203685477808~922337203685477807 | ■■■■■■■■       |
| Unsigned long  | 0~18446744073709551615                 | ■■■■■■■■       |

**4.  Dichiarazione delle variabili intere**

Forma generale della dichiarazione di variabile: specificatore_di_tipo nome_variabile, nome_variabile, …. Esempi:

```c
int a,b,c; (a,b,c is integer variable)
long x,y; (x,y is long integer variable)
```

unsigned p,q; (p, q sono variabili intere senza segno)

Nella dichiarazione delle variabili occorre tenere presente quanto segue:

1\.  Dopo uno stesso specificatore di tipo si possono dichiarare più variabili dello stesso tipo, separando i nomi con una virgola. Tra lo specificatore di tipo e il nome della variabile deve esserci almeno uno spazio.

2\.  L'ultimo nome di variabile deve terminare con ";".

3\.  La dichiarazione di una variabile deve precederne l'uso; di norma si trova all'inizio del corpo della funzione.

\[Esercizio\] //1int a,b;

short int c; short d=100; a=d-20; b=a+d;

```c
c=a+b+d;
d=d-a+c-b.
```

**5.  Costanti in virgola mobile**

Le costanti reali sono dette anche costanti in virgola mobile. Nel linguaggio C i numeri in virgola mobile sono espressi solo in base decimale, in due forme: forma decimale e forma esponenziale.

1\.  Forma decimale

È composta da cifre 0-9 e dal punto decimale. Per esempio: 0.0, .25, 5.789, 0.13, 5.0, 300., -267.8230 sono numeri in virgola mobile validi.

2\.  Forma esponenziale

È composta da un numero decimale, dal simbolo di esponente "e" o "E" e dall'esponente (solo intero, eventualmente con segno). La forma di base è a E n (a è un numero decimale, n un intero decimale) e il valore è a*10^n. Per esempio, 2.1E5 (pari a 2.1*10^5), 3.7E-2 (pari a 3.7*10^-2), 0.5E7 (pari a 0.5*10^7), -2.8E-2 (pari a -2.8*10^-2). Esempi di numeri in virgola mobile non validi: 345 (manca il punto decimale)  E7 (manca il numero prima del simbolo di esponente) -5 (manca il simbolo di esponente) 53.-E3 (posizione errata del segno meno) 2.7E (manca l'esponente)

Nel linguaggio C standard i numeri in virgola mobile possono avere un suffisso: un numero con suffisso "f" o "F" è un numero in virgola mobile. Per esempio, 356f e 356. sono equivalenti.

**6.  Variabili in virgola mobile**

Le variabili in virgola mobile possono essere a precisione singola o doppia, con specificatori di tipo float e double. In Turbo C, il tipo a precisione singola occupa 4 byte (32 bit) di memoria, con un intervallo da 3.4E-38 a 3.4E+38 e solo 7 cifre significative. Il tipo a precisione doppia occupa 8 byte (64 bit), con un intervallo da 1.7E-308 a 1.7E+308, e

offre 16 cifre significative.

La forma e le regole di scrittura della dichiarazione delle variabili in virgola mobile sono le stesse degli interi. Per esempio:  float x,y;  (x, y sono variabili a precisione singola)

double a,b,c;  (a, b, c sono variabili a precisione doppia)

Le costanti in virgola mobile non si distinguono in precisione singola e doppia: sono tutte trattate come double. a  ■■■■

b   ■■■■■■■■

a&lt;---33333.33333

b&lt;---33333.33333333333;

\[Esercizio\] //float int a=32; float b;

double d; b=12345678; d=b\*100;

```c
d=d+a;
d=d+58.123456;
```

**7.  Caratteri**

I dati di tipo carattere comprendono costanti carattere e variabili carattere. Costanti carattere

Una costante carattere è un carattere racchiuso tra apici singoli. Per esempio, 'a', 'b', '=', '+', '?' sono costanti carattere valide. Nel linguaggio C le costanti carattere hanno le seguenti caratteristiche:

1.   La costante carattere deve essere racchiusa tra apici singoli, non tra virgolette doppie o altre parentesi.

2.   La costante carattere deve essere un singolo carattere, non una stringa.

3.   Il carattere può essere qualsiasi carattere del set di caratteri. Tuttavia, una cifra definita come carattere non può partecipare alle operazioni numeriche. Per esempio, '5' e 5 sono diversi: '5' è una costante carattere che non partecipa ai calcoli.

**8.  Variabili carattere**

Il valore di una variabile carattere è una costante carattere, cioè un singolo carattere. Lo specificatore di tipo è char. La forma e le regole di scrittura della dichiarazione delle variabili carattere sono le stesse delle variabili intere.

Per esempio:

char a,b;

Poiché a ogni variabile carattere è assegnato un byte di memoria, essa può contenere un solo carattere. Il valore del carattere è memorizzato come codice ASCII. Per esempio, il codice ASCII decimale di x è 120 e quello di y è

121\. Assegnare 'x' e 'y' alle variabili carattere a e b: a='x', b='y'. In realtà si memorizzano i valori 120 e 121 nelle celle a e b:

a 0   1    1   1    1   0    0   0 b 0   1    1   1    1   0    0   1

Per questo i caratteri possono essere trattati come interi. Il linguaggio C consente di assegnare valori carattere a variabili intere e valori interi a variabili carattere, e di stampare una variabile carattere come intero o un intero come carattere. L'intero occupa

2 byte, il carattere un solo byte. Quando un intero viene trattato come carattere, viene considerato solo il byte basso (8 bit). \[Esercizio\] //charint a=49;

char b; char d; b=a+10; d=a+b;

\[Esercizio\] //char c1,c2;

```c
c1='a';c2='b';
c1=c1-32;c2=c2-32;
```

**9.  Costanti stringa**

Una costante stringa è una sequenza di caratteri racchiusa tra virgolette doppie. Per esempio: "CHINA", "C program", "\$12.5" sono costanti stringa valide. La costante stringa è diversa dalla costante carattere. Le differenze sono le seguenti:

1\.  La costante carattere è racchiusa tra apici singoli, mentre la costante stringa è racchiusa tra virgolette doppie.

2\.  La costante carattere è un solo carattere, mentre la costante stringa contiene uno o più caratteri.

3\.  Un carattere può essere assegnato a una variabile carattere, una costante stringa no. Nel linguaggio C non esiste un tipo di variabile stringa corrispondente.

4\.  La costante carattere occupa un byte in memoria. Una costante stringa occupa tanti byte quanti sono i caratteri più 1; nel byte aggiuntivo viene memorizzato il carattere "\0" (codice ASCII 0), che è il terminatore della stringa. Per esempio, "C program" in memoria è C program\0. Anche se la costante carattere 'a' e la costante stringa ''a'' contengono entrambe un solo carattere, occupano una quantità di memoria diversa.

'a' occupa un byte di memoria, rappresentato come a

"a" occupa due byte di memoria, rappresentati come a\0. Costanti simboliche

**10. Costanti simboliche**

Nel linguaggio C una costante può essere rappresentata da un identificatore, detto costante simbolica. Deve essere definita prima dell'uso. La forma generale è:

#define identificatore costante

#define è una direttiva del preprocessore, detta direttiva di definizione di macro. Serve ad associare un identificatore a un valore costante: dopo la definizione, tutte le occorrenze dell'identificatore nel programma vengono sostituite dal valore costante. Per convenzione, gli identificatori delle costanti simboliche si scrivono in maiuscolo e quelli delle variabili in minuscolo, per distinguerli.

```c
#define PI 3.14159 void main(){
float s,r; r=5; s=PI*r*r;
printf("s=%f\n",s);
}
```

Definito con la direttiva di definizione di macro: PI vale 3.14159; s e r sono definite float.  5->r  PI*r*r->s

Visualizza il risultato del programma; float s,r, dove r=5 e s=PI*r*r. In questo programma, prima della funzione main, la direttiva di definizione di macro definisce PI come 3.14159, valore che sostituisce PI nel programma: s=PI*r*r equivale quindi a s=3.14159*r*r. Attenzione: una costante simbolica non è una variabile e il suo valore non può essere modificato in tutto il suo campo di validità; in altre parole, nel programma non è possibile riassegnarla con un'istruzione di assegnazione.
