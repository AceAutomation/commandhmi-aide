# Eigenschappen communicatiepoort

Met de eigenschappen van de communicatiepoort stelt u de communicatieparameters tussen de HMI en de aangesloten apparaten in.

Dubbelklik op “Verbinding” en op “Verbinding 1”, zoals in afbeelding 7-1:

<img src="../../setting/com.files/image004.jpg" width="532" />

Afbeelding 7-1      Dialoogvenster eigenschappen communicatiepoort COM1

Op de pagina “Verbinding” zijn PLC's van diverse merken en modellen beschikbaar, plus de “Verbindingsnaam” en het “Interval aaneengesloten PLC-adressen”

Klik op het tabblad “Parameters” van het dialoogvenster, zoals in afbeelding 7-2:

<img src="../../setting/com.files/image005.jpg" width="532" />

Afbeelding 7-2      Parameters communicatiepoort COM1

**Parameterinstellingen:**

Apparaatdienst: fabrikant, PLC-merk en CPU-model.

Poort: RS232 / 485/ 422

Baudrate: 1200/2400/4800/9600/19200/38400/57600/115200 / 187.5k

Pariteit: oneven / even / geen

Databits: 7/8

Stopbits: 1/2

Model: PLC-model

Stationsnummer HMI: stationsnummer van de HMI

Communicatietijd: de HMI stuurt gegevens naar de PLC en ontvangt gegevens van de PLC; pas na de ingestelde communicatietijd kan ze opnieuw verzenden.

Time-out 1 en time-out 2: deel eerst time-out 1 door time-out 2; in de afbeelding hierboven is de time-out 200ms. Heeft de HMI 200ms na het verzenden nog geen gegevens ontvangen, dan is er een time-out.

Aantal herhalingen: aantal keren dat de gegevens na een time-out opnieuw worden verzonden

Adresmodus: ① Standaardmodus: één seriële poort, één PLC; ② Uitgebreide modus: één seriële poort, meerdere PLC's van hetzelfde type

Interval aaneengesloten PLC-adressen: maximaal aantal woorden dat de PLC in één keer kan lezen
