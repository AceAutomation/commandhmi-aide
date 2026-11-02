# PLC-besturing

Met de PLC-besturing worden schermwissel, wijziging van gebruikersniveau, receptwissel en het schrijven van recepten door de PLC bestuurd. Dubbelklik op “PLC-besturing” in de “projectbeheerder”; het dialoogvenster van afbeelding 7-8 verschijnt:

Afbeelding 7-8      Dialoogvenster PLC-besturing

• Recept wisselen: de HMI wisselt van recept volgens de waarde van dit adres.

• Recept schrijven: de HMI schrijft het recept volgens de waarde van dit adres.

• Huidig gebruikersniveau: de HMI bepaalt het huidige gebruikersniveau volgens de waarde van dit adres.

• Schermwissel via woordadres: de HMI wisselt van scherm volgens de waarde van dit woordadres; bij de waarde n springt ze naar scherm n.

• Schermwissel via bitadres: dubbelklik op de regel “Nieuw”; het dialoogvenster van afbeelding 7-9 verschijnt:

Nieuwe bitbesturing scherm:

<img src="../../setting/plc-control.files/image004.jpg" width="458" />

Nieuwe woordbesturing scherm

<img src="../../setting/plc-control.files/image006.jpg" width="497" />

Scherm: de PLC-woordbesturing springt alleen tussen schermen

Venster: de PLC-woordbesturing springt alleen tussen vensters

Scherm/venster: de PLC-woordbesturing springt tussen schermen en vensters

<img src="../../setting/plc-control.files/image005.jpg" width="130" />

Opmerking: bij schermwissel via de PLC heeft de eerst gelezen waarde geen invloed op de schermwissel. Pas als de waarde van het PLC-register verschilt van de eerst gelezen waarde, werkt de functie.
