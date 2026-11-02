# XY-Trenddiagramm

**Übersicht XY-Trenddiagramm:**

Dynamische, fortlaufende Anzeige veränderlicher Werte.

Es lassen sich mehrere Referenzkurven zeichnen; die Werte zweier aufeinanderfolgender Registeradressen dienen als waagerechte und senkrechte Koordinate, um Zusammenhänge genau und anschaulich zu beobachten.

Bis zu 8 Kurven (Liniendiagramm) können angezeigt werden.

XY-Trenddiagramm hinzufügen und Eigenschaften ändern erfolgt ähnlich wie beim Trenddiagramm; siehe Seite „Trenddiagramm“. Symbol: <img src="../../../configuration-guide/extended-controls/xy-trend.files/image002.jpg" width="36" />

Öffnen Sie das Eigenschaftsdialogfeld des XY-Trends; siehe die Einstellungen des Trenddiagramms. Zu beachten: Im Trenddiagramm steht jede Kurve für den Wert einer der aufeinanderfolgenden Adressen ab der Schreibadresse, im XY-Trenddiagramm für die Werte zweier aufeinanderfolgender Adressen ab der Schreibadresse.

**Anwendung des XY-Trenddiagramms:**

Farbe: Farbe der Messlinie (Referenzlinie).

Messadresse: Der Wert an der aktuellen Messlinie (Referenzlinie) wird in diese Adresse geschrieben.

Bei Datentyp 16 Bit und 4 Datengruppen werden, angenommen die eingegebene Adresse ist LW3, 8 aufeinanderfolgende Adresswerte gelesen:

LW3: Kurve 1, Wert der X-Achse

LW4: Kurve 1, Wert der Y-Achse

LW5: Kurve 2, Wert der X-Achse

LW6: Kurve 2, Wert der Y-Achse

LW7: Kurve 3, Wert der X-Achse

LW8: Kurve 3, Wert der Y-Achse

LW9: Kurve 4, Wert der X-Achse

LW10: Kurve 4, Wert der Y-Achse

Gelesen werden die 8 Adressen LW3-LW10. Bei 16-Bit-Daten und N Datengruppen werden also gemäß den Adressregeln der jeweiligen SPS 2 \* N aufeinanderfolgende Adresswerte gelesen.

Bei Datentyp 32 Bit und 3 Datengruppen werden, angenommen die eingegebene Adresse ist LW3, die Werte von 12 Adressen gelesen.

LW3: Kurve 1, Wert der X-Achse

LW5: Kurve 1, Wert der Y-Achse

LW7: Kurve 2, Wert der X-Achse

LW9: Kurve 2, Wert der Y-Achse

LW11: Kurve 3, Wert der X-Achse

LW13: Kurve 3, Wert der Y-Achse

Gelesen werden die 12 Adressen LW3-LW14. Bei 32-Bit-Daten und N Datengruppen werden also gemäß den Adressregeln der jeweiligen SPS 2 \* N Werte im Abstand von 2 gelesen.
