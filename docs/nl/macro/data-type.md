# Gegevenstypen in C

**1.  Gehele getallen**

Gehele getallen omvatten gehele constanten en gehele variabelen. C kent drie soorten gehele constanten: octaal, hexadecimaal en decimaal.

**2.  Gehele constanten**

1\.  Octale gehele constanten

Een octale constante moet met 0 beginnen: 0 is het voorvoegsel van octale constanten. De cijfers zijn 0-7. Octale constanten zijn meestal zonder teken. Geldige octale getallen zijn bijvoorbeeld:

015 (decimaal: 13) 0101 (decimaal: 65) 0177777 (decimaal: 65535)

Ongeldige octale getallen: 256 (zonder voorvoegsel 0)    03A2 (bevat niet-octale cijfers)             -0127 (met minteken)

2\.  Hexadecimale gehele constanten

Een hexadecimale constante begint met 0X of 0x. De cijfers zijn 0-9, A-F of a-f.

Geldige hexadecimale getallen zijn bijvoorbeeld:

0X2A (decimaal: 42) 0XA0 (decimaal: 160)    0XFFFF (decimaal: 65535) Ongeldige hexadecimale getallen:

5A (zonder voorvoegsel 0X)                0X3H (bevat niet-hexadecimale cijfers)

3\.  Decimale gehele constanten

Een decimale constante heeft geen voorvoegsel. De cijfers zijn 0-9. Geldige decimale getallen zijn bijvoorbeeld:

237   -568   65535    1627

Ongeldige decimale getallen:

023 (voorvoegsel 0 niet toegestaan)          23D (bevat niet-decimale cijfers)

In een programma worden deze notaties onderscheiden door hun voorvoegsel. Schrijf het voorvoegsel dus correct om foute resultaten te vermijden.

4\.  Achtervoegsel van gehele constanten: op een 16-bits computer is een basisgeheel getal 16 bits, dus het bereik is beperkt. Decimale getallen zonder teken liggen tussen 0 ～ 65535, met teken tussen -32768 ～+32767. Octale getallen zonder teken liggen tussen 0 ～ 0177777, hexadecimale zonder teken tussen 0X0～0XFFFF of 0x0～0xFFFF. Valt een getal buiten dit bereik, dan moet het als long worden aangegeven, met het achtervoegsel "L" of "l". Bijvoorbeeld:

Decimale long-constanten 158L (decimaal: 158)   358000L (decimaal: -358000)

Octale long-constanten    012L (decimaal: 10)   077L (decimaal: 63)    0200000L (decimaal: 65536)

Hexadecimale long-constanten   0X15L (decimaal: 21)    0XA5L (decimaal: 165)   0X10000L (decimaal: 65536). In waarde is er geen verschil tussen de long-constante 158L en de int-constante 158. Omdat 158L een long is, reserveert de C-compiler

4 bytes opslag; voor 158 als int reserveert hij 2 bytes. Let dus op bij bewerkingen en uitvoerformaten om fouten te vermijden. Getallen zonder teken krijgen het achtervoegsel "U" of "u". Bijvoorbeeld:     358u,

0x38Au, 235Lu zijn getallen zonder teken. Voor- en achtervoegsels kunnen worden gecombineerd. Bijvoorbeeld:

0XA5Lu is het hexadecimale long-getal zonder teken A5, decimaal 165.

**3.  Gehele variabelen**

Gehele variabelen worden als volgt ingedeeld:

1\.  Int

Typeaanduiding int; neemt 2 bytes geheugen in. De waarde is altijd een basisgeheel getal.

2\.  Short int

Typeaanduiding short int of short. Aantal bytes en bereik zijn gelijk aan die van int.

3\.  Long int

Typeaanduiding long int of long; neemt 4 bytes geheugen in. De waarde is altijd een long.

4\.  Unsigned int

Typeaanduiding unsigned.

unsigned kan met de drie bovenstaande typen worden gecombineerd:

(1)   De typeaanduiding van unsigned int is unsigned int of unsigned. (2)   De typeaanduiding van unsigned short int is unsigned short.

(3)   De typeaanduiding van unsigned long int is unsigned long.

Typen zonder teken nemen evenveel geheugen in als de overeenkomstige typen met teken, maar kunnen zonder tekenbit geen negatieve getallen voorstellen. De tabel hieronder geeft het geheugengebruik en het bereik van de verschillende gehele typen op ARM.

|                |                                        |                |
|----------------|----------------------------------------|----------------|
| Typeaanduiding | Waardebereik                           | Bezette bytes |
| Int            | -2147483648~2147483647                 | ■■■■           |
| Short int      | -2147483648~2147483647                 | ■■■■           |
| Signed int     | -2147483648~2147483647                 | ■■■■           |
| Unsigned int   | 0~4294967295                           | ■■■■           |
| Long int       | -922337203685477808~922337203685477807 | ■■■■■■■■       |
| Unsigned long  | 0~18446744073709551615                 | ■■■■■■■■       |

**4.  Declaratie van gehele variabelen**

Algemene vorm van een variabelendeclaratie: typeaanduiding variabelenaam, …. Bijvoorbeeld:

```c
int a,b,c; (a,b,c is integer variable)
long x,y; (x,y is long integer variable)
```

unsigned p,q;    (p,q   zijn gehele variabelen zonder teken)

Aandachtspunten bij het declareren van variabelen:

1\.  Na één typeaanduiding mogen meerdere variabelen van hetzelfde type staan, gescheiden door komma's. Tussen typeaanduiding en variabelenaam moet minstens één spatie staan.

2\.  De laatste variabelenaam moet met ";" eindigen.

3\.  Een variabele moet vóór het gebruik worden gedeclareerd, meestal aan het begin van de functiebody.

\[Oefening\]    //1int a,b;

short int c; short d=100; a=d-20; b=a+d;

```c
c=a+b+d;
d=d-a+c-b.
```

**5.  Floatconstanten**

Reële constanten heten ook drijvendekommaconstanten (float). In C worden ze alleen decimaal geschreven, in twee vormen: decimale vorm en exponentiële vorm

1\.  Decimale vorm

Bestaat uit de cijfers 0-9 en een decimale punt. Bijvoorbeeld: 0.0,.25,5.789,0.13,5.0,300.,-267.8230 zijn geldige floatgetallen.

2\.  Exponentiële vorm

Bestaat uit een decimaal getal, het exponentteken "e" of "E" en een exponent (alleen geheel, eventueel met teken). De basisvorm is a E n (a decimaal getal, n decimaal geheel getal) met als waarde a\*10,n. Bijvoorbeeld 2.1E5 (gelijk aan 2.1\*10,5), 3.7E-2    (gelijk aan 3.7\*10,)-2\*) 0.5E7 (gelijk aan 0.5\*10,7), -2.8E-2 (gelijk aan -2.8\*10,)-2\*). Ongeldige floatgetallen zijn: 345 (zonder decimale punt)      E7 (geen cijfer vóór het exponentteken) -5 (zonder exponentteken) 53.-E3   (minteken op de verkeerde plaats) 2.7E (zonder exponent)

In standaard C kunnen floatgetallen een achtervoegsel hebben: een getal met "f" of "F" is een float. 356f en 356 zijn bijvoorbeeld gelijkwaardig.

**6.  Floatvariabelen**

Floatvariabelen zijn enkelvoudig of dubbel, met de typeaanduidingen float en double. In Turbo C neemt een float vier bytes (32 bits) in, met een bereik van 3.4E-38～3.4E+38 en slechts zeven significante cijfers. Een double neemt 8 bytes (64 bits) in, met een bereik van 1.7E-308 ～ 1.7E+308 en

zestien significante cijfers.

Vorm en schrijfregels van de declaratie van floatvariabelen zijn gelijk aan die van gehele variabelen. Bijvoorbeeld:  float x,y;    (x,y zijn enkelvoudige floats)

double a,b,c;   (a,b,c zijn dubbele floats)

Floatconstanten worden niet onderscheiden in enkelvoudig en dubbel: alle floatconstanten worden als double behandeld. a   ■■■■

b   ■■■■■■■■

a&lt;---33333.33333

b&lt;---33333.33333333333;

\[Oefening\]    //float int a=32; float b;

double d; b=12345678; d=b\*100;

```c
d=d+a;
d=d+58.123456;
```

**7.  Tekens**

Tekens omvatten tekenconstanten en tekenvariabelen. Tekenconstanten

Een tekenconstante is één teken tussen enkele aanhalingstekens. 'a'. 'b', '=', '+', , '?' zijn bijvoorbeeld geldige tekenconstanten. In C hebben tekenconstanten de volgende kenmerken:

1.   Een tekenconstante staat tussen enkele aanhalingstekens, niet tussen dubbele of andere haakjes.

2.   Een tekenconstante is één teken, geen tekenreeks.

3.   Een teken kan elk teken uit de tekenset zijn. Een als teken gedefinieerd cijfer doet echter niet mee aan numerieke bewerkingen. '5' en 5 zijn bijvoorbeeld verschillend: '5' is een tekenconstante die niet meedoet aan bewerkingen.

**8.  Tekenvariabelen**

De waarde van een tekenvariabele is een tekenconstante, dus één teken. De typeaanduiding is char. Vorm en schrijfregels van de declaratie zijn gelijk aan die van gehele variabelen.

Bijvoorbeeld:

char a,b;

Elke tekenvariabele krijgt één byte geheugen en bevat dus maar één teken. Het teken wordt als ASCII-code in het geheugen opgeslagen. De decimale ASCII-code van x is bijvoorbeeld 120, die van y

121\. Kent u 'x' en 'y' toe aan de tekenvariabelen a en b: a='x', b='y', dan worden in feite 120 en 121 in a en b opgeslagen:

a 0   1    1   1    1   0    0   0 b 0   1    1   1    1   0    0   1

Ze kunnen dus als gehele getallen worden beschouwd. C staat toe dat een teken aan een gehele variabele wordt toegekend en een geheel getal aan een tekenvariabele. Een tekenvariabele kan als geheel getal worden uitgevoerd en een geheel getal als teken. Een geheel getal is

2 bytes, een teken 1 byte. Wordt een geheel getal als teken behandeld, dan worden alleen de lage acht bits gebruikt. \[Oefening\]    //charint a=49;

char b; char d; b=a+10; d=a+b;

\[Oefening\]    //char c1,c2;

```c
c1='a';c2='b';
c1=c1-32;c2=c2-32;
```

**9.  Tekenreeksconstanten**

Een tekenreeksconstante is een reeks tekens tussen dubbele aanhalingstekens. Bijvoorbeeld: "CHINA". "C program", "\$12.5"  zijn  geldige  tekenreeksconstanten.  Tekenreeksconstanten  verschillen  van  tekenconstanten.  De verschillen zijn:

1\.  Een tekenconstante staat tussen enkele aanhalingstekens, een tekenreeksconstante tussen dubbele.

2\.  Een tekenconstante is één teken, een tekenreeksconstante bevat één of meer tekens.

3\.  Een teken kan aan een tekenvariabele worden toegekend, een tekenreeksconstante niet. C kent geen tekenreeksvariabele.

4\.  Een tekenconstante neemt één byte geheugen in. Een tekenreeksconstante neemt het aantal tekens plus 1 byte in. In die extra byte staat het teken "\0" (ASCII-code 0), het eindteken van de reeks. "C program" staat bijvoorbeeld als C program\0 in het geheugen. Hoewel de tekenconstante 'a' en de tekenreeksconstante ''a'' allebei één teken hebben, nemen ze verschillend veel geheugen in.

'a' neemt één byte in, weergegeven als a

''a'' neemt twee bytes in, weergegeven als a\0.

**10. Symbolische constanten**

In C kan een constante worden aangeduid met een identifier: een symbolische constante. Ze moet vóór het gebruik worden gedefinieerd. De algemene vorm is:

\#define identifier constante

Daarbij is \#define een preprocessorinstructie, de macrodefinitie. Ze koppelt de identifier aan de waarde van de constante; daarna wordt de identifier overal in het programma door die waarde vervangen. Om ze te onderscheiden schrijft men symbolische constanten meestal in hoofdletters en variabelen in kleine letters.

```c
#define PI 3.14159 void main(){
float s,r; r=5; s=PI*r*r;
printf("s=%f\n",s);
}
```

Gedefinieerd met een macrodefinitie: PI is 3.14159, en s,r zijn als float gedefinieerd.    5-&gt;r     PI\*r\*r-&gt;s

Toon het resultaat float s,r, met r=5 en s=PI\*r\*r. In dit programma wordt vóór de functie main met een macrodefinitie PI gelijkgesteld aan 3.14159, wat PI in het programma vervangt. s=PI\*r\*r is dus gelijk aan s=3.14159\*r\*r. Let op: een symbolische constante is geen variabele. Haar waarde kan binnen haar bereik niet veranderen; een toekenning eraan is in het programma niet toegestaan.
