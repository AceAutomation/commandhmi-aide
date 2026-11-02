# Samenvatting van de paragraaf

1\.  Naar het verloop van de uitvoering bestaan programma's uit drie basisstructuren: sequentie, vertakking en lus.

2\.  De kleinste eenheid in de uitvoering van een programma is de instructie. C kent vijf soorten instructies:

(1)   Expressie-instructie: een expressie gevolgd door een puntkomma. De meest gebruikte is de toekenning.

(2)   Functieaanroep: een functieaanroep gevolgd door een puntkomma.

(3)   Besturingsinstructie: stuurt het verloop van het programma en bestaat uit een speciaal sleutelwoord en de benodigde expressie. Vooral voorwaardelijke instructies, lussen, sprongopdrachten enz.

(4)   Samengestelde instructie: meerdere instructies tussen {}. Ze geldt als één instructie en kan overal staan waar een instructie is toegestaan, zoals in een lusbody.

(5)   Lege instructie: alleen een puntkomma, zonder functie.

3\.  Relationele en logische expressies zijn twee belangrijke soorten expressies, vooral gebruikt voor de voorwaarden van vertakkingen en lussen.

4\.  C biedt meerdere vormen van voorwaardelijke instructies voor vertakkingen. (1)   De if-instructie dient vooral voor een enkelvoudige keuze.

(2)   De if-else-instructie dient vooral voor een tweevoudige keuze.

(3)   De if-else-if-instructie en de switch-instructie dienen voor meervoudige keuzes. Deze vormen zijn meestal onderling uitwisselbaar.

5\.  C kent drie lusinstructies.

(1)   De for-instructie dient vooral voor lussen met een beginwaarde, een stapgrootte en een vast aantal herhalingen. (2)   Wordt het aantal herhalingen of de voorwaarde pas tijdens de lus bepaald, gebruik dan while

of do-while.

(3)   De drie lusinstructies kunnen in elkaar worden genest. Lussen mogen naast elkaar staan, maar niet kruisen. (4)   Een sprong kan uit een lus leiden, maar niet van buitenaf in een lus.

(5)   Vermijd oneindige lussen: zorg dat de lusvariabele tijdens de uitvoering verandert, zodat de lusvoorwaarde uiteindelijk onwaar wordt en de lus eindigt.

6\.  Overzicht van de instructies in C

Naam                                Algemene vorm

Eenvoudige instructie                Expressie-instructie; lege instructie                           ;

Voorwaardelijke instructie          if(expressie)instructie;

if(expressie)instructie 1; else instructie 2;

if(expressie 1)instructie 1;   else if(expressie 2) instructie 2…else instructie n; switch-instructie                 switch(expressie){ case constante: instructie…default: instructie;   } lusinstructie                           while-instructie

```c
while(expression)statement;
for statement for(expression 1; expression 2; expression 3) statement; break statement break;
continue statement continue;
return statement return(expression);
```
