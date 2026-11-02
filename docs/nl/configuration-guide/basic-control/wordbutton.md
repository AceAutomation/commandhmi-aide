# Woordknop

De woordknop ondersteunt de bewerkingen Constante, Waarde invoeren, Verhogen, Verlagen, Wachtwoord invoeren, Optellen en Aftrekken op een dataregisteradres van het aangesloten apparaat.

Een woordknop toevoegen:

• Kies het pictogram woordknop<img src="../../../configuration-guide/basic-control/wordbutton.files/wordbutton222.png" width="29" /> in de werkbalk; het dialoogvenster van afbeelding 4-76 verschijnt:

<img src="../../../configuration-guide/basic-control/wordbutton.files/wordbutton308.png" width="664" />

Afbeelding 4-76 Dialoogvenster Woordknop

<img src="../../../configuration-guide/basic-control/wordbutton.files/wordbutton345.png" width="130" />

Zie voor vorm, randkleur, voorgrondkleur, achtergrondkleur en patroon het object “Bit-knop”.

**Functie:**

• Constante: CommandHMI biedt diverse gegevenstypen: positief geheel getal van 16/32 bits, geheel getal van 16/32 bits, positief BCD-getal van 16/32 bits en drijvende komma van 32 bits. De ingestelde constante wordt naar het schrijfadres geschreven. Met schrijfadres LW1 en constante 10 zet elke aanraking LW1 op 10, ongeacht de huidige waarde.

• Waarde invoeren: kies het gegevenstype; bij aanraken van de woordknop verschijnt een toetsenbord om een waarde tussen minimum en maximum in te voeren. Zoals in afbeelding 4-77:

<img src="../../../configuration-guide/basic-control/wordbutton.files/wordbutton1128.png" width="693" />

Afbeelding 4-77

• Verhogen: is de vertraging 0, dan werkt dit als “Optellen”. Is ze niet 0, dan wordt de waarde van het schrijfadres met de constante verhoogd en naar het register geschreven.

• Verlagen: is de vertraging 0, dan werkt dit als “Aftrekken”. Is ze niet 0, dan wordt na de ingestelde tijd de waarde met de constante verlaagd en naar het register geschreven.

• Wachtwoord invoeren: gelijk aan “Waarde invoeren”, maar zonder decimalen.

• Optellen: na het instellen van gegevenstype, schrijfadres, constante en maximum telt elke aanraking van de woordknop de constante bij de huidige registerwaarde op, zonder het ingestelde maximum te overschrijden. Met schrijfadres LW1, constante 5 en maximum 65535 telt elke klik 5 bij LW1 op, dat nooit boven 65535 komt.

• Aftrekken: na het instellen van gegevenstype, schrijfadres, constante en minimum trekt elke aanraking van de woordknop de constante van de huidige registerwaarde af, zonder onder het ingestelde minimum te komen. Met schrijfadres LW1, constante 5 en minimum 0 trekt elke klik 5 van LW1 af, dat nooit onder 0 komt.

• Totaal aantal cijfers: aantal cijfers van het gegeven, inclusief decimalen.

• Decimalen: is het gegevenstype geen “drijvende komma van 32 bits” en zijn er decimalen, dan wordt de maximale invoerwaarde gedeeld door 10 tot de macht n. Bijvoorbeeld: bij “positief geheel getal van 32 bits” en 3 decimalen kan de gebruiker alleen 0 tot 99999.999 invoeren.

• Script: vink “Script gebruiken” aan om de lijst met scripts te tonen. De gebruiker kiest een script dat bij het indrukken van de woordknop wordt uitgevoerd. Alleen gecompileerde scripts staan in de lijst.

<img src="../../../configuration-guide/basic-control/wordbutton.files/wordbutton3632.png" width="130" />

De pagina “Label” van de woordknop is vergelijkbaar met die van de “Bit-knop”, maar heeft geen Tekst status 1 en Afbeelding status 1, omdat de woordknop maar één status heeft.

Bij een 32-bits gegevenstype neemt het adres van de woordknop twee woorden in. Wordt bijvoorbeeld naar V10 van een SIEMENS-PLC geschreven, dan worden V10 en V11 bezet. Bewaakt een ander object V11, dan werkt dat niet goed. Let op bij 32-bits gegevenstypen.

De pagina's “Geavanceerd” en “Zichtbaarheid” van de woordknop zijn gelijk aan die van de Bit-knop; zie voor sneltoetsen de Bit-knop.
