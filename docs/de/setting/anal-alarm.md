# Analoge Alarme

Öffnen Sie das Dialogfeld der analogen Alarme, wie in Abbildung 7-28:

Es gibt zwei Arten: Zahlenwert und Zahlenvergleich.

<img src="../../setting/anal-alarm.files/image002.jpg" width="145" />

Alarm mit Zahlenvergleich:

<img src="../../setting/anal-alarm.files/image007.jpg" width="599" />

Abbildung 7-28    Dialogfeld Analoge Alarme

So verwenden Sie analoge Alarme:

• Geben Sie zuerst die zu überwachende Adresse in der Spalte „Leseadresse“ (Read Address) ein. Hier wird die interne Adresse LW1 angenommen.

• Wählen Sie unter „Größe“ (Size) die Gesamtzahl der Alarme, d. h. die Anzahl der Adressen; der Datentyp bestimmt, wie die Adressen gelesen werden. Standardmäßig ist jede Adresse 16 Bit, und die Adressen sind fortlaufend; der Datentyp ist jedoch änderbar. In Abbildung 7-28 ist LW1 eine 32-Bit positive Ganzzahl, LW3 und LW4 sind 16-Bit positive Ganzzahlen. Bei 32-Bit-Daten ist die nächste gelesene Adresse also die vorherige plus 2, bei 16-Bit-Daten die vorherige plus 1.

• Die „Abtastzeit“ (Scanning time) des Alarms, also die Abtastfrequenz, ist einstellbar.

• Klicken Sie auf jeden Eintrag, um rechts im Feld „Grenzwert“ einen Wert einzugeben, und danach im Feld „Text“ den Alarmtext. Hier werden die Meldungen aus Abbildung 7-28 angenommen: Jeder Wert fällt in einen von vier Bereichen: Tief, Sehr tief, Hoch, Sehr hoch.

Siehe Abbildung 7-29:

<img src="../../setting/anal-alarm.files/image004.jpg" width="566" />

Abbildung 7-29    Die vier Wertebereiche der Adresse LW1

• Sehr tief: Ist der Wert kleiner als der eingestellte Grenzwert und „Verwenden“ aktiviert, wird der Alarm in der Alarmanzeige oder im dynamischen Alarmlaufband angezeigt;

• Tief: Ist der Wert größer oder gleich dem Grenzwert „Sehr tief“ und kleiner als der Grenzwert „Tief“ und „Verwenden“ aktiviert, wird der Alarm in der Alarmanzeige oder im dynamischen Alarmlaufband angezeigt;

• Hoch: Ist der Wert größer als der Grenzwert „Hoch“ und kleiner oder gleich dem Grenzwert „Sehr hoch“ und „Verwenden“ aktiviert, wird der Alarm in der Alarmanzeige oder im dynamischen Alarmlaufband angezeigt.

• Sehr hoch: Ist der Wert größer als der eingestellte Grenzwert und „Verwenden“ aktiviert, wird der Alarm in der Alarmanzeige oder im dynamischen Alarmlaufband angezeigt.

• U-Export: exportiert die Alarmeinstellungen

• U-Import: importiert die Alarmeinstellungen

Zur Option „Verwenden“ siehe „Digitale Alarme“.

Beim Alarm mit Zahlenwert wird ein Alarm ausgelöst, wenn der Wert den eingestellten Grenzwert erreicht.

Einstellungen unten: Ein Alarm wird ausgelöst, wenn der Wert 1, 12, 30 und 40 erreicht.

<img src="../../setting/anal-alarm.files/image006.jpg" width="130" />

Hinweis: Die HMI der HM-Serie unterstützen höchstens 10 analoge Alarme.
