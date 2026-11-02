# Array monodimensionali

Nella progettazione dei programmi, l'array organizza in modo ordinato più variabili dello stesso tipo, per comodità. L'insieme ordinato di elementi dello stesso tipo si chiama array. Nel linguaggio C l'array è un tipo di dato costruito. Un array è composto da più elementi, che possono essere di tipo base o di tipo costruito. Di conseguenza, in base al tipo degli elementi, gli array si distinguono in array numerici, array di caratteri, array di puntatori, array di strutture, ecc.

Questa sezione presenta gli array numerici e gli array di caratteri; gli altri saranno descritti nelle sezioni successive. Nel linguaggio C, per utilizzare un array è necessario prima dichiararlo. La forma generale della dichiarazione di un array è: specificatore_di_tipo nome_array \[espressione_costante\]. Lo specificatore di tipo può essere qualsiasi tipo base o costruito. Il nome dell'array è l'identificatore definito dall'utente. L'espressione costante tra parentesi quadre indica il numero di elementi, detto anche lunghezza dell'array.

Per esempio:

int a\[10\]; l'array di interi a contiene 10 elementi.

float b\[10\],c\[20\]; l'array float b contiene 10 elementi; l'array float c contiene 20 elementi. char ch\[20\]; l'array di caratteri ch contiene 20 elementi.

Per la dichiarazione degli array occorre tenere presente quanto segue:

1\.  Il tipo dell'array corrisponde al tipo di valore dei suoi elementi. In uno stesso array, tutti gli elementi hanno lo stesso tipo di dato.

2\.  Il nome dell'array deve rispettare le regole di scrittura degli identificatori.

3\.  Il nome dell'array non può coincidere con il nome di un'altra variabile. Per esempio:   void main ()

```c
{
int a;
float a[10];
```

……

} non è corretto

4\.  L'espressione costante tra parentesi quadre indica il numero di elementi. Per esempio, a \[5\] indica che l'array a contiene 5 elementi. Tuttavia l'indice parte da 0, quindi i cinque elementi sono a\[0\],a\[1\],a\[2\],a\[3\],a\[4\].

5\.  Tra parentesi quadre non si può indicare il numero di elementi tramite una variabile, ma è possibile usare una costante simbolica o un'espressione costante. Per esempio:

\#define FD    5

```c
void main ()
{
int a[3+2],b[7+FD];
```

……

```c
} is legal. However, the following expression form is incorrect. void main()
{
int n=5;
int a[n];
```

……

}

6\.  Una stessa dichiarazione di tipo può dichiarare più array e più variabili.

Per esempio: int a,b,c,d,k1\[10\],k2\[20\];

**1.  Rappresentazione degli elementi di un array**

Gli elementi sono l'unità di base di un array. Ciascun elemento è anche una variabile, identificata dal nome dell'array e da un indice. L'indice indica il numero d'ordine dell'elemento nell'array. La forma generale di un elemento è: nome_array \[indice\]. L'indice può essere solo una costante intera o un'espressione intera; se ha una parte decimale, il C lo converte automaticamente in intero. Per esempio, a\[5\], a\[i+j\], a\[i++\] sono elementi validi. Un elemento di array è spesso chiamato variabile indicizzata. Una variabile indicizzata può essere usata solo dopo aver definito l'array. In C le variabili indicizzate si usano una per una, non l'array nel suo insieme.

La forma generale dell'inizializzazione è: static specificatore_di_tipo nome_array \[espressione_costante\]={valore……}. Qui static indica la classe di memorizzazione statica. In C possono essere inizializzati solo gli array statici e gli array esterni (i concetti di memorizzazione statica ed esterna saranno introdotti nel capitolo 5). I dati tra {  } sono i valori iniziali dei singoli elementi, separati da virgole, per esempio static int a\[10\]={ 0,1,2,3,4,5,6,7,8,9  }, che equivale a a\[0\]=0;a\[1\]=1...a\[9\]=9;

**2.  Nel linguaggio C l'inizializzazione degli array segue alcune regole:**

1\.  È possibile assegnare il valore iniziale solo ad alcuni elementi. Se i valori tra {    } sono meno degli elementi, vengono inizializzati solo i primi. Per esempio: static int a\[10\]={0,1,2,3,4} indica che il valore iniziale

viene assegnato ai primi 5 elementi a\[0\]～a\[4\], mentre agli ultimi 5 elementi viene assegnato automaticamente 0.

2\.  Il valore iniziale va assegnato elemento per elemento: non è possibile assegnare un valore all'intero array. Per esempio, per assegnare 1 a 10 elementi si deve scrivere static int a\[10\]={1,1,1,1,1,1,1,1,1,1} e non static int a\[10\]=1.

3\.  Se a un array statico non viene assegnato alcun valore iniziale, tutti gli elementi valgono 0.

4\.  Se si inizializzano tutti gli elementi, il numero di elementi può essere omesso nella dichiarazione. Per esempio: static int a\[5\]={1,2,3,4,5} può essere scritto     static int a\[\]={1,2,3,4,5}. È anche possibile assegnare i valori dinamicamente durante l'esecuzione del programma, per esempio con un ciclo e la funzione scanf, elemento per elemento.

**3.  Array di caratteri**

Un array destinato a memorizzare caratteri si chiama array di caratteri. La dichiarazione di un array di caratteri ha la stessa forma di quella di un array numerico, vista in precedenza. Per esempio: char c\[10\]. Poiché caratteri e interi sono simili, è possibile definirlo anche come int c\[10\], ma in questo caso ogni elemento occupa 2 byte di memoria. Un array di caratteri può anche essere bidimensionale. Per esempio, char c\[5\]\[10\] è un array di caratteri bidimensionale. Un array di caratteri può essere inizializzato nella dichiarazione. Prendiamo ad esempio static char c\[10\]={`c`,`  `,`p`,`r`,o`,g`,r`,`a`,`m`}. Dopo l'assegnazione, i valori degli elementi dell'array c sono c\[0\]c\[1\]c\[2\]c\[3\]c\[4\]c \[5\]c\[6\]c\[7\]c\[8\]c\[9\]. In questo caso c\[9\] non viene assegnato e il sistema gli attribuisce automaticamente il valore 0. Quando si assegna un valore iniziale a tutti gli elementi, la lunghezza può essere omessa, per esempio static char c\[\]={`c`,` `,`p`,`r`,`o`,`g`,`r`,`a`,`m`}: in questo caso la lunghezza dell'array c è 9.

Il linguaggio C consente di inizializzare un array con una stringa di caratteri. Per esempio, static char c\[\]={'c', ' ','p','r','o','g','r','a','m'} può essere scritto static char c\[\]={"C program"} oppure static char c\[\]="C program" senza {}. L'inizializzazione con una stringa occupa un byte in più rispetto all'assegnazione carattere per carattere: questo byte memorizza il terminatore di stringa '\0'. In memoria l'array c contiene quindi C program\0, dove '\0' viene aggiunto automaticamente dal compilatore C. Grazie al terminatore '\0', nell'inizializzazione con una stringa di solito non si specifica la lunghezza dell'array, che viene calcolata automaticamente dal sistema. Con le stringhe, l'input e l'output degli array di caratteri diventano semplici e pratici: oltre all'inizializzazione con una stringa, è possibile leggere e scrivere in un'unica operazione l'intera stringa di un array di caratteri con le funzioni printf e scanf, senza dover gestire ogni carattere singolarmente in un ciclo.
