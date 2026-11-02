# Eigenschaften der Kommunikationsschnittstelle

Hier werden die Kommunikationsparameter zwischen HMI und angeschlossenen Geräten eingestellt.

Doppelklicken Sie auf „Verbindung“ (Link) und dann auf Verbindung 1, wie in Abbildung 7-1:

<img src="../../setting/com.files/image004.jpg" width="532" />

Abbildung 7-1      Dialogfeld Eigenschaften COM1

Auf der Seite „Verbindung“ stehen zahlreiche SPS-Marken und -Modelle zur Wahl, außerdem „Verbindungsname“ und „Intervall zusammenhängender SPS-Adressen“

Klicken Sie auf die Registerkarte „Parameter“, wie in Abbildung 7-2:

<img src="../../setting/com.files/image005.jpg" width="532" />

Abbildung 7-2      Parameter der Kommunikationsschnittstelle COM1

**Parameter:**

Geräteservice: Hersteller, SPS-Marke und CPU-Modell.

Port: RS232 / 485/ 422

Baudrate: 1200/2400/4800/9600/19200/38400/57600/115200 / 187.5k

Parität: Odd / Even / None

Datenbits: 7/8

Stoppbits: 1/2

Modell: SPS-Modell

HMI-Stationsnummer: Stationsnummer des HMI

Kommunikationszeit: Das HMI sendet Daten an die SPS und empfängt deren Antwort; erneut senden kann es erst nach Ablauf dieser Zeit.

Timeout 1 und Timeout 2: Der Timeout ergibt sich aus Timeout 1 und Timeout 2; in der obigen Abbildung beträgt er 200 ms. Hat das HMI 200 ms nach dem Senden keine Antwort erhalten, liegt ein Timeout vor.

Wiederholungen: Anzahl der erneuten Übertragungen nach einem Timeout

Adressmodus: ① Standardmodus: eine serielle Schnittstelle mit einer SPS; ② Erweiterter Modus: eine serielle Schnittstelle mit mehreren SPS gleichen Typs

Intervall zusammenhängender SPS-Adressen: maximale Anzahl Worte, die die SPS auf einmal lesen kann
