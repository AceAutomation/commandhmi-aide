# Beginwaarden van variabelen en typeconversie

**1.  Beginwaarden van variabelen**

In een programma krijgen variabelen meestal een beginwaarde. Er zijn meerdere manieren om een beginwaarde toe te kennen; dit heet initialisatie. In de declaratie is de algemene vorm:

typeaanduiding variabele 1 = 1, variabele 2 = 2, ……; bijvoorbeeld:

```c
int a=b=c=5;
float x=3.2,y=3f,z=0.75;
char ch1='K',ch2='P';
```

Let op: aaneengeschakelde toekenning is in een declaratie niet toegestaan; a=b=c=5 is bijvoorbeeld ongeldig.

**2.  Typeconversie van variabelen**

Het type van een variabele kan worden omgezet, op twee manieren: automatische conversie en expliciete conversie.

Automatische conversie

Bij gemengde bewerkingen met verschillende gegevenstypen voert de compiler automatisch de conversie uit, volgens deze regels:

1\.  Hebben de gegevens in een bewerking verschillende typen, dan worden ze eerst naar hetzelfde type omgezet en daarna verwerkt.

2\.  De conversie gebeurt in de richting van de langere gegevenslengte, om de precisie te bewaren. Bij een bewerking met int en long wordt int bijvoorbeeld eerst naar long omgezet.

3\.  Alle floatbewerkingen gebeuren in double. Ook als de expressie alleen floats bevat, wordt voor de bewerking naar double omgezet.

4\.  char en short worden voor de bewerking naar int omgezet.

5\.  Bij een toekenning met verschillende typen links en rechts van het toekenningsteken wordt het type rechts omgezet naar het type links. Is het type rechts langer dan links, dan gaat een deel van de gegevens verloren en daalt de precisie; het verloren deel wordt afgerond.

**3.  Expliciete typeconversie**

Expliciete typeconversie gebeurt met de cast-operator. De algemene vorm is (typeaanduiding) (expressie). Ze zet het resultaat van de bewerking geforceerd om naar het opgegeven type. Bijvoorbeeld: (float) a zet a om naar float; (int)(x+y) zet het resultaat van x+y om naar een geheel getal. Aandachtspunten bij expliciete conversie:

1\.  Typeaanduiding en expressie moeten tussen haakjes staan (een enkele variabele hoeft niet tussen haakjes). Schrijft u (int)(x+y)

als (int)x+y, dan wordt x naar int omgezet en daarna y opgeteld.

2\.  Zowel expliciete als automatische conversie is een tijdelijke omzetting van de gegevenslengte voor de bewerking. Het type van de variabele in de declaratie verandert niet.
