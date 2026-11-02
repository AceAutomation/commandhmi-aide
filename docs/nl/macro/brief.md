# Samenvatting van de paragraaf

**1.  Gegevenstypen in C**

Basistypen, samengestelde typen, pointertypen en void

**2.  Indeling en kenmerken van de basistypen**

|                   |        |                                         |
|-------------------|--------|-----------------------------------------|
| Typeaanduiding    | Byte   | Waardebereik                            |
| char              | 1      | C-tekenset                         |
| int               | 4      | -214783648～214783647                   |
| short int         | 4      | -214783648～214783647                   |
| long int          | 8      | -922337203685477808～922337203685477807 |
| unsigned          | 4      | 0～4294967295                           |
| unsigned long     | 8      | 0～1844744073709551615                  |
| float             | 4      | 3/4E-38～3/4E+38                        |
| double            | 8      | 1/7E-308～1/7E+308                      |

**3.  Achtervoegsels van constanten**

L of l voor long int

U of u voor unsigned

F of f voor float

**4.  Soorten constanten**

Int, long int, unsigned, float, char, tekenreeks, symbolische constante en escapeteken

**5.  Conversie van gegevenstypen**

Automatische conversie

Bij gemengde bewerkingen met verschillende gegevenstypen converteert het systeem automatisch van het kleinere naar het grotere type. Bij toekenning tussen verschillende typen converteert het systeem ook automatisch, van het type rechts naar het type links.

Expliciete conversie

Wordt uitgevoerd met de cast-operator.

**6.  Prioriteit en associativiteit van operatoren**

In het algemeen hebben unaire operatoren een hoge en toekenningsoperatoren een lage prioriteit. Rekenkundige operatoren hebben een hogere prioriteit dan relationele en logische. De meeste operatoren zijn links-associatief; unaire, ternaire en toekenningsoperatoren zijn rechts-associatief.

**7.  Expressie**

Een expressie is een formule opgebouwd uit constanten, variabelen en functies, verbonden door operatoren. Elke expressie heeft een waarde en een type. Een expressie wordt geëvalueerd in de volgorde die de prioriteit en associativiteit van de operatoren bepalen.

**8.  Array**

1\.  De array is de meest gebruikte gegevensstructuur bij het programmeren. Er zijn numerieke arrays (int-arrays, float-arrays), tekenarrays, en de later beschreven pointerarrays en structuurarrays.

2\.  Een array kan een-, twee- of meerdimensionaal zijn.

3\.  De declaratie van een array bestaat uit typeaanduiding, arraynaam en arraylengte (aantal elementen). Een arrayelement heet ook geïndexeerde variabele. Het arraytype is het waardetype van de geïndexeerde variabelen.

4\.  Een array krijgt op drie manieren waarden: initialisatie, dynamische toekenning via een invoerfunctie, en toekenningsinstructies. Een numerieke array kan niet in zijn geheel met één toekenning worden gevuld, ingevoerd of uitgevoerd, maar wordt element voor element verwerkt met een do-instructie.
