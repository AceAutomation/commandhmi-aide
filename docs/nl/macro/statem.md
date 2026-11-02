# Instructies van een C-programma

Het uitvoerende deel van een C-programma bestaat uit instructies; de functie van het programma wordt gerealiseerd door ze uit te voeren. C-instructies vallen in vijf categorieën:

1\.  Expressie-instructies

2\.  Besturingsinstructies

3\.  Samengestelde instructies

4\.  Lege instructies

**1.  Expressie-instructie**

Een expressie-instructie bestaat uit een expressie en een puntkomma. De algemene vorm is expressie;. Bij de uitvoering wordt de waarde van de expressie berekend. Bijvoorbeeld: x=y+z; is een toekenning; y+z; voert een optelling uit, maar het resultaat wordt niet bewaard en heeft dus geen nut; i++; verhoogt i met 1.

**2.  Besturingsinstructie**

Een besturingsinstructie stuurt het verloop van het programma en realiseert zo de verschillende programmastructuren.

Ze bestaat uit speciale sleutelwoorden. C kent negen besturingsinstructies, in drie soorten:

(1)   Voorwaardelijke instructies: if-instructie, switch-instructie

(2)   Lusinstructies

do while-instructie, while-instructie, for-instructie

(3)   Sprongopdrachten

break-instructie, goto-instructie, continue-instructie, return-instructie

**3.  Lege instructie**

Een instructie die alleen uit een puntkomma bestaat, heet een lege instructie en doet niets. In een programma kan ze dienen als lege lusbody. Bijvoorbeeld while (getchar()!='\n'): zolang het via het toetsenbord ingevoerde teken geen Enter is, moet opnieuw worden ingevoerd. Hier is de lusbody een lege instructie.

**4.  Toekenningsinstructie**

Een toekenningsinstructie bestaat uit een toekenningsexpressie en een puntkomma. De algemene vorm is variabele = expressie. Functie en kenmerken zijn gelijk aan die van de toekenningsexpressie. Het is een van de meest gebruikte instructies. Aandachtspunten bij het gebruik:

1\.  Omdat rechts van het teken "=" weer een toekenningsexpressie mag staan, is de vorm variabele=(variabele=expressie); geldig, wat nesting oplevert. Uitgeschreven: variabele=variabele=…=expressie;

Bijvoorbeeld:

```c
a=b=c=d=e=5; according to the right associativity of assignment operator, it is equivalent to: e=5 actually;
d=e; c=d; b=c; a=b;
```

2\.  Let op het verschil tussen een beginwaarde in de declaratie en een toekenningsinstructie.

Een beginwaarde hoort bij de declaratie van de variabele; variabelen met een beginwaarde worden door komma's van andere variabelen gescheiden, terwijl een toekenningsinstructie met een puntkomma moet eindigen.

3\.  In een declaratie mogen niet meerdere variabelen achter elkaar dezelfde beginwaarde krijgen. De volgende declaratie is bijvoorbeeld fout: int a=b=c=5 moet worden geschreven als int a=5,b=5,c=5. Een toekenningsinstructie mag wel aaneengeschakeld zijn.

4\.  Let op het verschil tussen een toekenningsexpressie en een toekenningsinstructie. Een toekenningsexpressie is een expressie en mag overal staan waar een expressie is toegestaan; een toekenningsinstructie niet.

De volgende instructie is geldig: if((x=y+5)&gt;0) z=x; betekenis: is x=y+5 groter dan 0, dan krijgt z de waarde van x.

De volgende instructie is ongeldig: if((x=y+5;)&gt;0) z=x; want x=y+5; is een instructie en mag niet in een expressie staan.
