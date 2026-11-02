# Animatie

Animatie: u legt vooraf de beweging van een element vast en bestuurt zijn positie op het traject met de gegevens van twee registers: het ene bestuurt de status, het andere de positie.

Het pictogram in de werkbalk is: <img src="../../../configuration-guide/new_add_control/dymicbutton.files/image002.jpg" width="28" />. Teken de bewegingspunten (maximaal 64) in het scherm en klik met de rechtermuisknop om het tekenen af te sluiten.

Dubbelklik op het object om het dialoogvenster van afbeelding 4-118 te openen:

Afbeelding 4-118   Pagina “Algemeen” van de animatie

Totaal aantal statussen: aantal statussen van het element

Positie:

Register: met “Register” worden status en positie van het element door de registergegevens bepaald.

Leesadres: worden status en positie door de registergegevens bepaald, dan moet het leesadres correct worden ingesteld. Het formaat staat in de tabel hieronder.

|           |                            |                              |
|-----------|----------------------------|------------------------------|
| Gegevenstype | Besturingsadres status | Besturingsadres positie |
| 16 bits    | Adres                    | Adres + 1                  |
| 32 bits    | Adres                    | Adres + 2                  |

Is het register bijvoorbeeld \[LW100\] en het formaat “16-bits positief geheel getal”, dan bevat \[LW100\] de status van het element en \[LW101\] de positie. In afbeelding 4-119 is bijvoorbeeld \[LW100\] = 2 en \[LW101\] = 1, dus toont het element status 2 op positie 1.

<img src="../../../configuration-guide/new_add_control/dymicbutton.files/image004.gif" width="520" />

Afbeelding 4-119

• Klok: met de optie “Klok” wisselt het element automatisch van status en positie. Met “Automatische positiebesturing” stelt u de manier in waarop status en positie wisselen.

• Snelheid: snelheid van de positiewissel in eenheden van 0,1 s. Bij 10 verschuift het element bijvoorbeeld elke seconde één positie.

• Terug: stel dat het element vier posities heeft: 0, 1, 2 en 3. Is deze optie niet aangevinkt, dan springt het element na de laatste positie (3) naar de beginpositie (0) en herhaalt het dezelfde volgorde.

Positie 0-&gt; positie 1-&gt; positie 2-&gt; positie 3-&gt; positie 0-&gt; positie 1-&gt; positie 2...

Is deze optie aangevinkt, dan keert het element na de laatste positie op zijn schreden terug. De volgorde van de posities is dan:

Positie 0-&gt; positie 1-&gt; positie 2-&gt; positie 3-&gt; positie 2-&gt; positie 1-&gt; positie 0...

Statuswissel: manier waarop de status verandert

U kunt kiezen tussen “Op positie” en “Op tijd”. Met “Op positie” verandert de status met de positie.

Met “Op tijd” veranderen positie en status volgens de punten op het scherm.

<img src="../../../configuration-guide/new_add_control/dymicbutton.files/image005.jpg" width="484" />

Afbeelding 4-120   Automatische positiebesturing

**Pagina “Profiel”:**

<img src="../../../configuration-guide/new_add_control/dymicbutton.files/image006.jpg" width="484" />

Grootte van de vectorafbeelding:

• Breedte: breedte van het <span id="OLE_LINK520"></span><span id="OLE_LINK521"></span>grafische object op de pagina “Algemeen”.

• Hoogte: hoogte van het grafische object op de pagina “Algemeen”.

• Traject: past de positie van de trajectpunten aan door ze te selecteren.

Zie voor de pagina's “Tekst” en “Afbeelding” de “Meerstandenlamp”.

<span id="OLE_LINK676"></span><span id="OLE_LINK677"></span>Zie voor de pagina “Zichtbaarheid” de “Bit-knop”.
