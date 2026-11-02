# Timer

De timer is een object dat door de tijd wordt geactiveerd. In de software CommandHMI dient de timer om scripts te starten. Klik op <img src="../../../configuration-guide/extended-controls/timer.files/timer152.png" width="35" /> in de werkbalk of dubbelklik op een bestaande timer om de instellingen te openen:

<img src="../../../configuration-guide/extended-controls/timer.files/timer240.png" width="662" />

**Besturing**

• Uitvoeringsmodus: “Altijd uitvoeren” of “Triggeradres”.

1\. “Altijd uitvoeren”: het script wordt altijd uitgevoerd met de door de gebruiker ingestelde frequentie.

2\. “Triggeradres”: het script wordt met de ingestelde frequentie uitgevoerd als de opgegeven bit 1 is, en niet als hij 0 is.

• Adres: in de modus “Triggeradres” verschijnt het veld voor het bitadres dat de uitvoering van het script bestuurt. Bij de waarde 1 wordt het script uitgevoerd.

• Frequentie: uitvoeringsfrequentie van het script, van 0.1 tot 60 s.

• Aantal uitvoeringen: aantal keren dat het script wordt uitgevoerd. Bij 0 onbeperkt.

**Functie**

• Functietype: uit te voeren functie. In de software CommandHMI is de functie van de timer een script.

• Naam: naam van het uit te voeren script. Zonder script kan de timer niet worden ingesteld.

<img src="../../../configuration-guide/extended-controls/timer.files/timer1240.png" width="130" />

De grootte van de timer kan niet worden gewijzigd, de positie wel. Tijdens de werking van het project wordt de timer niet op de HMI getoond.
