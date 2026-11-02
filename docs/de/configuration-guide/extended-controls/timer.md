# Timer

Der Timer ist ein zeitgesteuertes Objekt. In der Projektierungssoftware CommandHMI dient er zum Auslösen von Skripten. Klicken Sie auf <img src="../../../configuration-guide/extended-controls/timer.files/timer152.png" width="35" /> in der Werkzeugleiste oder doppelklicken Sie auf einen vorhandenen Timer, um seine Einstellungen zu öffnen:

<img src="../../../configuration-guide/extended-controls/timer.files/timer240.png" width="662" />

**Steuerung**

• Ausführungsmodus: „Immer ausführen“ oder „Adressgesteuert“.

1\. „Immer ausführen“: Das Skript wird ständig mit der eingestellten Frequenz ausgeführt.

2\. „Adressgesteuert“: Das Skript wird mit der eingestellten Frequenz ausgeführt, wenn das angegebene Bit 1 ist, und nicht ausgeführt, wenn es 0 ist.

• Adresse: Im Modus „Adressgesteuert“ erscheint ein Eingabefeld für die Bitadresse, die die Ausführung des Skripts steuert. Bei Wert 1 läuft das Skript.

• Frequenz: Ausführungsintervall des gewählten Skripts, 0,1 bis 60 s.

• Ausführungsanzahl: Anzahl der Ausführungen des gewählten Skripts. Bei 0 wird es ständig ausgeführt.

**Funktion**

• Funktionstyp: Art der auszuführenden Funktion. In der Projektierungssoftware CommandHMI ist dies beim Timer ein Skript.

• Name: Name des auszuführenden Skripts. Ohne vorhandenes Skript kann der Timer nicht eingestellt werden.

<img src="../../../configuration-guide/extended-controls/timer.files/timer1240.png" width="130" />

Die Größe des Timers ist nicht änderbar, die Position schon. Im laufenden Projekt wird der Timer auf dem HMI nicht angezeigt.
