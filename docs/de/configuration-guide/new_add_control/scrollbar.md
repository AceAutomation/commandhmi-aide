# Bildlaufleiste

Die Bildlaufleiste ist ein Objekt zum Durchblättern der Daten tabellarischer Objekte, damit der Benutzer sie schnell durchsehen kann. Unterstützt werden nur folgende Objekte: Alarmanzeige, Anzeige historischer Alarme, Rezeptdatenanzeige, historische Datenanzeige, Bedienprotokoll

Das Objekt wird verwendet, wenn das zugehörige Objekt zu viele Daten enthält, um sie auf einmal anzuzeigen; damit lässt sich der restliche Teil der Daten anzeigen

<img src="../../../configuration-guide/new_add_control/scrollbar.files/image004.jpg" width="859" alt="ScreenShot00819.jpg" />

Dialogfeld Bildlaufleiste

Die Funktionen des Objekts im Einzelnen (es gibt zwei Arten: Blättertasten und Bildlaufleiste)

Ø  Bildlaufleiste: steuert das Blättern der Tabellendaten mit einer Bildlaufleiste

<img src="../../../configuration-guide/new_add_control/scrollbar.files/image005.jpg" width="859" alt="ScreenShot00820.jpg" />

l  Hintergrundfarbe: Hintergrundfarbe des Objekts

l  Symbolfarbe: Farbe der Symbole des Objekts

l  Richtung: Richtung, in der die Bildlaufleiste die Tabellendaten verschiebt

n  Horizontal: steuert die waagerechte Anzeige der Tabellendaten

n  Vertikal: steuert die senkrechte Anzeige der Tabellendaten

l  Nummer des zugehörigen Objekts: Befindet sich eines der oben genannten Objekte im aktuellen Bild, kann die Bildlaufleiste damit verknüpft werden. Ist keines vorhanden, erscheint die Fehlermeldung „Das zugehörige Objekt darf nicht leer sein“. Die Objektnummer steht oben links am Objekt.

Beispiel mit der historischen Datenanzeige und der Wirkung der Bildlaufleiste

Die historische Datenanzeige enthält 75 Einträge; Anzeige und Bildlaufleiste stehen ganz unten

<img src="../../../configuration-guide/new_add_control/scrollbar.files/image008.jpg" width="585" alt="ScreenShot00822.jpg" />

Wird die Bildlaufleiste in die Mitte geschoben, sieht die Datenanzeige so aus:

<img src="../../../configuration-guide/new_add_control/scrollbar.files/image008.jpg" width="585" alt="ScreenShot00822.jpg" />

Ø  Blättertasten: steuern das Blättern der Tabellendaten mit Tasten

<img src="../../../configuration-guide/new_add_control/scrollbar.files/image006.jpg" width="859" alt="ScreenShot00821.jpg" />

l Rahmenfarbe: Rahmenfarbe des Objekts

l  Hintergrundfarbe: Hintergrundfarbe des Objekts

l  Symbolfarbe: Farbe der Symbole im Objekt

l  Richtung

n  Horizontal: steuert die waagerechte Anzeige der Tabellendaten

n  Vertikal: steuert die senkrechte Anzeige der Tabellendaten

l  Nummer des zugehörigen Objekts: siehe oben

l Funktionstasten

n  Tastenabstand: Abstand zwischen den Tasten

n  Zum Anfang/zum Ende: verschiebt die Tabellendaten an den Anfang bzw. das Ende; stehen die Daten bereits dort, meldet ein Dialog, dass der Vorgang ungültig ist (wie bei den beiden folgenden Tasten)

n  Seite hoch/Seite runter bzw. Seite links/Seite rechts: verschiebt jeweils um eine Seite

n  Hoch/runter bzw. links/rechts: verschiebt jeweils um einen Eintrag in die entsprechende Richtung

n  Pause: Ändern sich die Tabellendaten gerade, hält ein Klick die Änderung an; ein erneuter Klick hebt die Pause auf. Ist die Tabellenrichtung fest, ändert sich nichts, und ein Klick meldet, dass die Funktion ungültig ist. Beispiel mit der historischen Datenanzeige: Die Abbildung unten zeigt die Wirkung der Blättertasten

Die historische Datenanzeige enthält 71 Einträge

<img src="../../../configuration-guide/new_add_control/scrollbar.files/image008.jpg" width="585" alt="ScreenShot00822.jpg" />

Ein Klick auf die Pausentaste <img src="../../../configuration-guide/new_add_control/scrollbar.files/suspend.jpg" width="40" alt="suspend" /> im laufenden Projekt hält die Aktualisierung der Tabelle an und öffnet folgenden Dialog

<img src="../../../configuration-guide/new_add_control/scrollbar.files/image009.jpg" width="257" alt="ScreenShot00826.jpg" />

Ein erneuter Klick auf die Pausentaste <img src="../../../configuration-guide/new_add_control/scrollbar.files/suspend.jpg" width="40" alt="suspend" /> aktualisiert die Tabelle wieder und öffnet folgenden Dialog

<img src="../../../configuration-guide/new_add_control/scrollbar.files/image010.jpg" width="265" alt="ScreenShot00827.jpg" />

Ein Klick auf die Taste <img src="../../../configuration-guide/new_add_control/scrollbar.files/screenshot00849.jpg" width="44" /> ändert die historische Datenanzeige wie unten: Die Daten springen an den Anfang. Ebenso springen die Daten mit der Ende-Taste <img src="../../../configuration-guide/new_add_control/scrollbar.files/screenshot00850.jpg" width="32" /> ans Ende

<img src="../../../configuration-guide/new_add_control/scrollbar.files/image011.jpg" width="585" alt="ScreenShot00828.jpg" />

Ein Klick auf die Taste „Nächste Seite“ <img src="../../../configuration-guide/new_add_control/scrollbar.files/screenshot00851.jpg" width="40" /> ändert die historische Datenanzeige wie unten: Eine Seite enthält höchstens 5 Einträge, und mit „Nächste Seite“ werden die nächsten 5 angezeigt. Ebenso zeigt die Taste „Vorherige Seite“ <img src="../../../configuration-guide/new_add_control/scrollbar.files/image015.jpg" width="37" alt="ScreenShot00529.jpg" /> die vorherigen 5 Einträge an

<img src="../../../configuration-guide/new_add_control/scrollbar.files/image012.jpg" width="584" alt="2019_7_27_15_06_20.jpg" />

Ein Klick auf die Taste <img src="../../../configuration-guide/new_add_control/scrollbar.files/image017.jpg" width="40" alt="ScreenShot00530.jpg" /> ändert die historische Datenanzeige wie unten: Oben wird ein Eintrag mehr angezeigt; ebenso unten beim Klick auf die Taste <img src="../../../configuration-guide/new_add_control/scrollbar.files/image018.jpg" width="37" alt="ScreenShot00532.jpg" />

<img src="../../../configuration-guide/new_add_control/scrollbar.files/image013.jpg" width="584" alt="2019_7_27_15_06_54.jpg" />
