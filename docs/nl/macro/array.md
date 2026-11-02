# Eendimensionale array

Bij het programmeren groepeert een array voor het gemak meerdere variabelen van hetzelfde type in geordende vorm. Een geordende verzameling gegevenselementen van hetzelfde type heet een array. In C is een array een samengesteld gegevenstype. Een array bestaat uit meerdere arrayelementen, die basistypen of samengestelde typen kunnen zijn. Naar het type van de elementen onderscheidt men numerieke arrays, tekenarrays, pointerarrays, structuurarrays enz.

Deze paragraaf behandelt numerieke arrays en tekenarrays; de andere komen in de volgende paragrafen aan bod. Een array moet in C eerst worden gedeclareerd voordat hij wordt gebruikt. De algemene vorm van de declaratie is: typeaanduiding arraynaam    \[constante expressie\]. Daarbij is de typeaanduiding een basistype of samengesteld type, de arraynaam de door de gebruiker gedefinieerde identifier, en geeft de constante expressie tussen vierkante haken het aantal elementen aan, ook wel de lengte van de array genoemd.

Bijvoorbeeld:

int a\[10\]; de int-array a bevat 10 elementen.

float b\[10\],c\[20\]; de float-array b bevat 10 elementen, de float-array c 20 elementen. char ch\[20\]; de tekenarray ch bevat 20 elementen.

Bij de declaratie van een array gelden de volgende punten:

1\.  Het arraytype is in feite het waardetype van de elementen. Binnen één array hebben alle elementen hetzelfde gegevenstype.

2\.  De naam van de array volgt de regels voor identifiers.

3\.  De naam van de array mag niet gelijk zijn aan die van een andere variabele. Bijvoorbeeld:   void main ()

```c
{
int a;
float a[10];
```

……

} is fout

4\.  De constante expressie tussen vierkante haken geeft het aantal elementen aan. a \[5\] betekent bijvoorbeeld dat de array a 5 elementen bevat. De index begint echter bij 0, dus de vijf elementen zijn a\[0\],a\[1\],a\[2\],a\[3\],a\[4\].

5\.  Tussen de vierkante haken mag geen variabele staan als aantal elementen, wel een symbolische constante of een constante expressie. Bijvoorbeeld:

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

6\.  In één declaratie mogen meerdere arrays en variabelen worden beschreven.

Bijvoorbeeld: int a,b,c,d,k1\[10\],k2\[20\];

**1.  Notatie van arrayelementen**

Arrayelementen zijn de basiseenheid van een array. Elk element is een variabele, aangeduid met de naam van de array en een index. De index geeft het volgnummer van het element in de array. De algemene vorm is: arraynaam \[index\]. De index is een gehele constante of een gehele expressie; heeft hij decimalen, dan maakt C er automatisch een geheel getal van. a\[5\],a\[i+j\],a\[i++\] zijn bijvoorbeeld geldige arrayelementen. Een arrayelement heet ook geïndexeerde variabele en kan pas worden gebruikt als de array is gedefinieerd. In C worden de geïndexeerde variabelen één voor één gebruikt, niet de hele array in één keer.

De algemene vorm van de initialisatie is: static typeaanduiding arraynaam \[constante expressie\]=\[waarde……\]. Daarbij staat static voor de statische opslagklasse. In C kunnen alleen statische en externe arrays bij de declaratie worden geïnitialiseerd (de begrippen statische en externe opslag komen in hoofdstuk 5 aan bod). De gegevens tussen {    } zijn de beginwaarden van de elementen, gescheiden door komma's, zoals static int a\[10\]={    0,1,2,3,4,5,6,7,8,9   }, wat gelijk is aan a\[0\]=0;a\[1\]=1...a\[9\]=9;

**2.  Voor de initialisatie van arrays gelden in C de volgende regels:**

1\.  Een deel van de elementen kan een beginwaarde krijgen. Staan tussen {    } minder waarden dan er elementen zijn, dan krijgen alleen de eerste elementen een beginwaarde. Bijvoorbeeld: static int a\[10\]={0,1,2,3,4} betekent dat de beginwaarde

alleen wordt toegekend aan de eerste 5 elementen a\[0\]～a\[4\]; de laatste 5 elementen krijgen automatisch 0.

2\.  Beginwaarden worden per element toegekend; een array kan niet in zijn geheel een waarde krijgen. Om 10 elementen de waarde 1 te geven, schrijft u static int a\[10\]={1,1,1,1,1,1,1,1,1,1} en niet static int a\[10\]=1.

3\.  Krijgt een geïnitialiseerde array geen beginwaarden, dan zijn alle elementen 0.

4\.  Krijgen alle elementen een waarde, dan mag het aantal elementen in de declaratie worden weggelaten. Bijvoorbeeld: static int a\[5\]={1,2,3,4,5} kan worden geschreven als     static int a\[\]={1,2,3,4,5}. Tijdens de uitvoering van het programma kunnen de elementen ook dynamisch, één voor één, een waarde krijgen, bijvoorbeeld met een do-instructie en de functie scanf.

**3.  Tekenarray**

Een array waarin tekens worden opgeslagen, heet een tekenarray. De declaratie is gelijk aan die van een numerieke array, bijvoorbeeld: char c\[10\]. Omdat tekens en gehele getallen verwant zijn, kan ook int c\[10\] worden gebruikt, maar dan neemt elk element 2 bytes geheugen in. Een tekenarray kan tweedimensionaal zijn. Zo is  char  c\[5\]\[10\]  een  tweedimensionale  tekenarray.  Een  tekenarray  kan  bij  de  declaratie  worden  geïnitialiseerd,  bijvoorbeeld static char c\[10\]={\`c\`,\`    \`,\`p\`,\`r\`,o\`,g\`,r\`,\`a\`,\`m\`}. Na de toekenning zijn de elementen van array c c\[0\]c\[1\]c\[2\]c\[3\]c\[4\]c \[5\]c\[6\]c\[7\]c\[8\]c\[9\]. Daarbij krijgt c\[9\] geen waarde en zet het systeem het automatisch op 0. Krijgen alle elementen een beginwaarde, dan mag de lengte worden weggelaten, zoals static char c\[\]={\`c\`,\`    \`,\`p\`,\`r\`,\`o\`,\`g\`,\`r\`,\`a\`,\`m\`}; de lengte van array C is dan 9.

In  C  kan  een  array  ook  met  een  tekenreeks  worden  geïnitialiseerd.  Bijvoorbeeld  static  char  c\[\]={'c',  ' ','p','r','o','g','r','a','m'} kan worden geschreven als static char c\[\]={"C program"} of zonder {} als static char c\[\]="C program". Toekenning met een tekenreeks neemt één byte meer in dan toekenning per element: die byte bevat het eindteken '\0' van de tekenreeks. In het geheugen staat array c dus als C program\0, waarbij \`\0' automatisch door C wordt toegevoegd. Dankzij het teken '\0' wordt de lengte van de array bij initialisatie met een tekenreeks meestal niet opgegeven, maar door het systeem bepaald. Met tekenreeksen worden in- en uitvoer van tekenarrays eenvoudig: naast initialisatie met een tekenreeks kan de hele tekenreeks van een array in één keer worden ingevoerd en uitgevoerd met de functies printf en scanf, zonder elk teken afzonderlijk met een do-instructie te verwerken.
