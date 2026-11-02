# Valore iniziale delle variabili e conversione di tipo

**1.  Assegnazione del valore iniziale alle variabili**

Nei programmi è frequente assegnare un valore iniziale alle variabili. Il linguaggio prevede vari metodi per farlo, detti inizializzazione. Nella dichiarazione delle variabili, la forma generale dell'inizializzazione è:

specificatore_di_tipo variabile1 = valore1, variabile2 = valore2, ……; per esempio:

```c
int a=b=c=5;
float x=3.2,y=3f,z=0.75;
char ch1='K',ch2='P';
```

Nota: nella dichiarazione non è ammessa l'assegnazione concatenata; per esempio a=b=c=5 non è valido.

**2.  Conversione di tipo delle variabili**

Il tipo di una variabile può essere convertito in due modi: con la conversione automatica o con la conversione forzata.

Conversione automatica

Quando in un'operazione mista intervengono dati di tipo diverso, il compilatore esegue automaticamente la conversione, secondo le regole seguenti:

1\.  Se i tipi di dati coinvolti in un'operazione sono diversi, vengono prima convertiti in un unico tipo e poi si esegue l'operazione.

2\.  La conversione avviene verso il tipo di lunghezza maggiore per garantire la massima precisione. Per esempio, in un'operazione tra int e long, int viene convertito in long prima del calcolo.

3\.  Tutte le operazioni in virgola mobile avvengono in double. Anche se l'espressione contiene solo float, viene convertita in double per il calcolo.

4\.  char e short devono essere convertiti in int per il calcolo.

5\.  In un'assegnazione, se i tipi ai due lati del segno di assegnazione sono diversi, il tipo del valore a destra viene convertito nel tipo a sinistra. Se il dato a destra è più lungo di quello a sinistra, una parte dei dati va persa e la precisione diminuisce. La parte persa viene arrotondata.

**3.  Conversione di tipo forzata**

La conversione forzata si ottiene con l'operatore di conversione di tipo (cast). La sua forma generale è (specificatore_di_tipo) (espressione) e serve a convertire forzatamente il risultato dell'operazione nel tipo indicato. Per esempio, (float) a converte a in float; (int)(x+y) converte il risultato di x+y in intero. Nella conversione forzata occorre tenere presente quanto segue:

1\.  Lo specificatore di tipo e l'espressione devono essere racchiusi tra parentesi (una singola variabile può non esserlo). Ad esempio (int)(x+y)

viene scritto (int)x+y, significa convertire x in int e poi sommare y.

2\.  Sia la conversione forzata sia quella automatica sono solo conversioni temporanee della lunghezza dei dati ai fini dell'operazione; non modificano il tipo della variabile nella sua dichiarazione.
