# Programma's met vertakkingen

**Relationele operatoren en expressies**

In een programma vergelijkt men vaak twee waarden om te bepalen hoe verder te gaan. De operatoren die waarden vergelijken, heten relationele operatoren. C kent de volgende relationele operatoren:

&lt;   kleiner dan

&lt;= kleiner dan of gelijk aan

&gt; groter dan

&gt;= groter dan of gelijk aan

== gelijk aan

!= ongelijk aan

De relationele operatoren zijn binair en links-associatief. Hun prioriteit is lager dan die van de rekenkundige operatoren en hoger dan die van de toekenningsoperatoren. Van de zes relationele operatoren hebben &lt;,&lt;=,&gt;,&gt;= dezelfde prioriteit, hoger dan die van ==   en !=. ==    en != hebben onderling dezelfde prioriteit.

**Relationele expressie**

De    algemene    vorm    van    een    relationele    expressie    is    expressie    relationele    operator    expressie.    Bijvoorbeeld a+b&gt;c-d,x&gt;3/2,'a'+1&lt;c,-i-5\*j==k+1 zijn geldige relationele expressies. Omdat een expressie zelf weer een relationele expressie kan zijn, is nesting mogelijk, zoals a&gt;(b&gt;c),a!=(c==d) enz. De waarde van een relationele expressie is “waar” of “onwaar”, weergegeven als “1” en “0”.

**1.  Logische operatoren en expressies**

C kent de logische operatoren EN &&, OF \|\| en NIET !. EN && en OF \|\| zijn binair en links-associatief; NIET ! is unair en rechts-associatief. De prioriteit van de logische operatoren ten opzichte van de andere operatoren is als volgt:

Uit de prioriteit van de operatoren volgt:

a&gt;b && c&gt;d is gelijk aan (a&gt;b) &&   (c&gt;d)

!b==c\|\|d&lt;a is gelijk aan ((!b)==c)\|\|(d&lt;a)

a+b&gt;c && x+y&lt;b is gelijk aan ((a+b)&gt;c) && ((x+y)&lt;b) Waarde van logische bewerkingen

Het resultaat van een logische bewerking is waar of onwaar, weergegeven als 1 en 0. De regels zijn:

1\.  Bij EN && is het resultaat waar als beide waarden waar zijn; anders onwaar. Bijvoorbeeld 5&gt;0

&& 4&gt;2: omdat 5&gt;0 waar is en 4&gt;2 waar is, is het resultaat waar.

2\.  Bij OF \|\| is het resultaat waar als een van beide waarden waar is, en onwaar als beide onwaar zijn. Bijvoorbeeld 5&gt;0\|\|5&gt;8: omdat 5&gt;0 waar is, is het resultaat waar.

3\.  Bij NIET ! is het resultaat onwaar als de operand waar is, en waar als de operand onwaar is.

Het resultaat van !(5&gt;0) is bijvoorbeeld onwaar.

In C wordt het resultaat van een logische bewerking weergegeven als “1” voor “waar” en “0” voor “onwaar”. Omgekeerd geldt bij het beoordelen van een waarde: 0 is onwaar en elke andere waarde is waar. Omdat 5 en 3 bijvoorbeeld niet nul zijn, is 5&&3 “waar” (dus 1).

Nog een voorbeeld: 5\|\|0 is “waar” (dus 1).

De algemene vorm van een logische expressie is expressie – logische operator – expressie. De expressies kunnen zelf ook logische expressies zijn, wat nesting oplevert, bijvoorbeeld (a&&b) &&c. Door de links-associativiteit van de logische operatoren kan dit worden geschreven als a&&b&&c. De waarde van een logische expressie is het eindresultaat van de logische bewerkingen, weergegeven als “1” (waar) en “0” (onwaar).

**2.  if-instructie**

Met de if-instructie maakt u een vertakking: afhankelijk van de opgegeven voorwaarde wordt bepaald welk deel van het programma wordt uitgevoerd. De if-instructie van C heeft drie basisvormen.

1\.  De eerste vorm is de basisvorm: if (expressie) instructie

Betekenis: is de expressie waar, dan wordt de volgende instructie uitgevoerd, anders niet.

2\.  De tweede vorm is if-else: if(expressie)

instructie 1; else instructie 2;

Betekenis: is de expressie waar, dan wordt instructie 1 uitgevoerd, anders instructie 2.

Voer twee gehele getallen in en geef het grootste weer. Vergelijk a en b met een if-else-instructie: is a groter, dan wordt a weergegeven;

anders b.

**3.  De derde vorm is if-else-if.**

De eerste twee vormen worden meestal voor twee vertakkingen gebruikt. Bij meer keuzes gebruikt men de if-else-if-instructie. De basisvorm is:

if(expressie 1)

instructie 1;

else if(expressie 2)

instructie   2;

else if(expressie 3)

instructie   3;

…

else if(expressie m)

instructie m; else instructie n;

Betekenis: de expressies worden achtereenvolgens geëvalueerd. Is er een waar, dan wordt de bijbehorende instructie uitgevoerd en gaat het programma verder na de if-instructie. Zijn alle expressies onwaar, dan wordt instructie n uitgevoerd. Daarna gaat het programma verder.

**Aandachtspunten bij de if-instructie:**

(1)   In alle drie de vormen volgt na if een expressie, meestal een logische of relationele expressie. Het mag ook een andere expressie zijn, zoals een toekenning of zelfs een variabele. if(a=5) instructie en if(b) instructie zijn bijvoorbeeld toegestaan. Zolang de waarde van de expressie niet 0 is, is ze waar. In if(a=5)…; is de expressie nooit 0, dus wordt de volgende instructie altijd uitgevoerd. Dit komt in programma's zelden voor, maar de syntaxis is geldig.

Nog een voorbeeld, programmafragment: if(a=b)

```c
printf("%d",a); else printf("a=0");
```

Betekenis van de instructie: ken b toe aan a; is die waarde niet 0, dan wordt ze weergegeven, anders de tekenreeks “a=0”. Dit soort toepassing komt in programma's vaak voor.

(2)   In de if-instructie moet de voorwaarde tussen haakjes staan, en de instructie eindigt met een puntkomma.

(3)   In alle drie de vormen moeten de instructies enkelvoudig zijn. Moet bij een voorwaarde een groep instructies worden uitgevoerd, dan moet die tussen {} staan om een samengestelde instructie te vormen. Let op: na } staat geen puntkomma.

Bijvoorbeeld:

```c
if(a>b){ a++; b++;
}
else{ a=0;
b=10;
}
```

**4.  Voorwaardelijke operator en voorwaardelijke expressie**

Wordt in een voorwaardelijke instructie alleen één toekenning uitgevoerd, dan gebruikt men meestal een voorwaardelijke expressie: die vereenvoudigt het programma en verhoogt de efficiëntie.

De voorwaardelijke operator ? : is ternair: er zijn drie waarden bij de bewerking betrokken. De algemene vorm van een voorwaardelijke expressie is:

Expressie 1 ? Expressie 2: Expressie 3

Evaluatieregel: is expressie 1 waar, dan is de waarde van expressie 2 de waarde van de voorwaardelijke expressie; anders is de waarde van expressie 3 de waarde van de hele expressie. Voorwaardelijke expressies worden meestal in toekenningen gebruikt. Bijvoorbeeld:

```c
if(a>b) max=a;
else max=b;
```

max=(a&gt;b)?a:b; is een voorwaardelijke expressie. Betekenis: is a&gt;b waar, dan krijgt max de waarde a, anders b.

Bij het gebruik van voorwaardelijke expressies gelden de volgende aandachtspunten:

1\.  De prioriteit van de voorwaardelijke operator is lager dan die van de relationele en rekenkundige operatoren, maar hoger dan die van de toekenning. max=(a&gt;b)?a:b kan dus zonder haakjes worden geschreven als max=a&gt;b?a:b.

2\.  ? en : vormen een paar en kunnen niet afzonderlijk worden gebruikt.

3\.  De voorwaardelijke operator is rechts-associatief.
