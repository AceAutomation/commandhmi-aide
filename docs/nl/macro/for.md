# for-instructie

De for-instructie is de krachtigste en meest gebruikte lusinstructie van C. De algemene vorm is:

for (expressie 1;expressie 2;expressie 3)

instructie;

Expressie 1: geeft meestal de lusvariabele een beginwaarde; het is een toekenning. De beginwaarde mag ook buiten de for-instructie worden toegekend; dan kan deze expressie worden weggelaten.

Expressie 2: meestal de lusvoorwaarde, een relationele of logische expressie. Expressie 3: wijzigt meestal de waarde van de lusvariabele; het is een toekenning.

Deze drie expressies mogen komma-expressies zijn, dus elk uit meerdere expressies bestaan. Alle drie zijn optioneel en kunnen worden weggelaten.

De “instructie” in de algemene vorm is de lusbody. Betekenis van de for-instructie:

1\.  Eerst wordt expressie 1 berekend.

2\.  Daarna wordt expressie 2 berekend. Is die waar (niet 0), dan wordt de lusbody nog eens uitgevoerd; anders wordt de lus verlaten.

3\.  Expressie 3 wordt berekend en het programma keert terug naar stap 2. In de for-lus wordt expressie 1 één keer berekend; expressie 2 en 3 kunnen vaak worden herhaald. De lusbody kan vele keren of helemaal niet worden uitgevoerd.

Aandachtspunten bij de for-instructie:

1\.  Elke expressie in de for-instructie kan worden weggelaten, maar de puntkomma's moeten blijven. Bijvoorbeeld:

&lt;1&gt;for(expressie; expressie) expressie weggelaten

&lt;2&gt;for(expressie; expressie;) expressie weggelaten

&lt;3&gt;for(;expressie; expressie) alle expressies weggelaten

2\.  Heeft de lusvariabele al een beginwaarde, dan kan expressie 1 worden weggelaten, zoals in voorbeeld 3.27. Wordt expressie

2 of 3 weggelaten, dan kan een oneindige lus ontstaan; de lus moet dan in de lusbody worden beëindigd.

3\.  De lusbody kan een lege instructie zijn.

```c
#include" stdio.h" void main(){
int n=0;
printf("input a string:\n"); for(;getchar()!='\n';n++); printf("%d",n);
}
```

In dit voorbeeld is expressie 1 van de for-instructie weggelaten en dient expressie 3 niet om de lusvariabele te wijzigen, maar om de ingevoerde tekens te tellen. Het tellen, dat normaal in de lusbody zou gebeuren, gebeurt dus al in de expressie, en de lusbody is een lege instructie. Let op: de puntkomma na de lege instructie is essentieel. Ontbreekt die, dan wordt de volgende printf-instructie als lusbody uitgevoerd. Omgekeerd mag, als de lusbody geen lege instructie is, na het haakje van de expressie geen puntkomma staan; anders wordt de lusbody als lege instructie gezien en niet herhaald. Dit zijn veelgemaakte programmeerfouten waarop u goed moet letten.
