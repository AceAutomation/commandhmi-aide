# Doorgeefverbinding

Het touchscreen ondersteunt een bijzondere verbinding waarbij een HMI op afstand een PLC of ander apparaat bewaakt of bestuurt via de seriële poort van een andere HMI die met dat apparaat is verbonden. Het aangesloten apparaat kan dan vanaf twee of meer bedienposten worden bediend. De doorgeefverbinding is een zeer nuttige functie van de HMI.

Vóór het gebruik van de doorgeefverbinding moet u de volgende begrippen kennen:

• Lokale HMI: de HMI die met de PLC of het andere apparaat is verbonden.

• Externe HMI: de HMI die met de lokale HMI is verbonden en via de doorgifte de aangesloten apparaten bestuurt.

Voor een doorgeefverbinding moet de lokale HMI twee seriële poorten hebben. Het schema staat in afbeelding 8-12 en 8-13:

Doorgeefverbinding met twee schermen:

<img src="../../multpoint/penetrate.files/penetrate789.png" width="578" />

Afbeelding 8-12    Schema doorgeefverbinding met twee schermen

Doorgeefverbinding met meerdere schermen:

<img src="../../multpoint/penetrate.files/penetrate913.png" width="792" />

Afbeelding 8-13    Schema doorgeefverbinding met meerdere schermen

Lokale HMI: software-instellingen:

Dubbelklik op de aangemaakte verbinding; het venster met de eigenschappen van de communicatiepoort verschijnt. Kies COM1 als verbindingspoort. Voorbeeld met MITSUBISHI: COM1 van de lokale HMI is verbonden met een MITSUBISHI FX2N-PLC. De communicatieparameters moeten overeenkomen met die van de PLC of het andere apparaat. Zie afbeelding 8-14 en 8-15:

<img src="../../multpoint/penetrate.files/penetrate1423.png" width="589" />

Afbeelding 8-14    Pagina “Algemeen” van de eigenschappen communicatiepoort, lokale HMI

<img src="../../multpoint/penetrate.files/penetrate1500.png" width="587" />

Afbeelding 8-15: pagina COM1 van de eigenschappen communicatiepoort, lokale HMI

Maak een nieuwe verbinding aan, kies COM2 als verbindingspoort, voeg geen protocol toe, stel de eigenschappen als volgt in, met dezelfde poortinstellingen als seriële poort 1. Aanbevolen parameters: 9600, 8, None, 1. Kies bij de doorgeefeigenschap “Poort voor slave-scherm” en stel het aantal schermen in naar de werkelijke situatie. Zie afbeelding 8-16 en 8-17.

<img src="../../multpoint/penetrate.files/image001.jpg" width="598" alt="ScreenShot00093.jpg" />

Afbeelding 8-16    Pagina “Algemeen” van de eigenschappen communicatiepoort, lokale HMI

<img src="../../multpoint/penetrate.files/penetrate2042.png" width="589" />

Afbeelding 8-17    Pagina “Parameters” van de eigenschappen communicatiepoort, lokale HMI

Behoud voor de overige parameters de standaardwaarden. Daarmee is de lokale HMI ingesteld.

Externe HMI: software-instellingen:

Dubbelklik op de aangemaakte verbinding; het venster met de eigenschappen van de communicatiepoort verschijnt. Kies COM1 als verbindingspoort, “Op afstand” als HMI-locatie, en stel dezelfde communicatieparameters in als op de pagina COM2 van de lokale HMI (zie afbeelding 6 hierboven), zoals in afbeelding 8-18 en 8-19.

<img src="../../multpoint/penetrate.files/penetrate2646.png" width="589" />

Afbeelding 8-18    Pagina “Algemeen” van de eigenschappen communicatiepoort, externe HMI

<img src="../../multpoint/penetrate.files/penetrate2724.png" width="588" />

Afbeelding 8-19    Pagina “Parameters” van de eigenschappen communicatiepoort, externe HMI

Behoud voor de overige parameters de standaardwaarden. Daarmee is de externe HMI ingesteld.

<img src="../../multpoint/penetrate.files/penetrate2924.png" width="130" />

Opmerking: de bovenstaande instellingen gelden voor een doorgeefverbinding met twee schermen.

Opmerking: bij een doorgeefverbinding met meerdere schermen is de COM-instelling van de externe HMI gelijk aan die van de lokale HMI.

Opmerking: omdat alle communicatie met de PLC via COM1 van de lokale HMI loopt, is de communicatiesnelheid bij een doorgeefverbinding met meerdere schermen laag.
