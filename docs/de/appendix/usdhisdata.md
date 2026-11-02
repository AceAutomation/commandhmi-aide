# Datenexport per USB-Stick

Die HMI der HM-Serie können historische Daten, Rezepte, historische Alarme und Screenshots auf einen USB-Stick exportieren.

Da CommandHMI mehrere Gruppen historischer Daten unterstützt, muss für den Export eine Gruppennummer angegeben werden. LW60408 enthält die Gruppennummer der gewählten historischen Daten. Beispiel: LW60408 = 1 bedeutet, dass sich Import und Export per USB-Stick auf die historischen Daten der Gruppe 0 beziehen und auf keine andere.

Hinweis: Ist der eingegebene Wert größer als die höchste Gruppe minus 1, ist die Funktion wirkungslos.

**Historische Daten per USB-Stick exportieren**

1\. USB-Stick einstecken

2\. Gruppennummer der zu importierenden/exportierenden historischen Daten im Register LW60408 einstellen.

3\. LB60127 auf ON setzen: Das HMI kopiert die Datei der Datengruppe als hisdatai.csv auf den USB-Stick; bei Gruppennummer 1 als hisdata1.csv.

LB60128 auf ON setzen: Das HMI kopiert die Datei der Datengruppe auf den USB-Stick; um Gruppe 1 zu importieren, die Datei hisdata1.csv nennen.

Diese Trigger werden nach Abschluss des Exports automatisch auf OFF zurückgesetzt

Für den Export lokaler Daten werden die LW-Register LW60359-LW60429 verwendet

**Rezepte exportieren**

Da CommandHMI mehrere Rezeptgruppen unterstützt, muss für den Rezeptexport LW61143 eingestellt werden.

1\. USB-Stick einstecken.

2\. Gruppennummer in LW61143 einstellen.

3\. LB60163 auf ON setzen: Das HMI kopiert die Rezeptdatei der Gruppe auf den USB-Stick

4\. Diese Trigger werden nach Abschluss des Exports automatisch auf OFF zurückgesetzt

Hinweis: Die auf den Computer exportierten historischen Daten lassen sich nicht direkt öffnen; dazu wird das Konvertierungstool SK_SQL_CSV.exe <img src="../../appendix/usdhisdata.files/image002.jpg" width="86" /> im Stammverzeichnis der HM-Projektierungssoftware benötigt.

Mit diesem Tool wird die exportierte Datei in eine direkt lesbare CSV-Datei umgewandelt. Starten Sie das Tool per Doppelklick.

Fortschritt: Fortschritt der Umwandlung.

Dateiname: Auswahl der umzuwandelnden Datei.

Wählen Sie „historische Daten“ oder „Alarme“. Die Kodierung ist fest auf ANSI eingestellt. Klicken Sie anschließend auf „Generate CSV“. Bei 100 % im Fortschrittsbalken ist die Umwandlung abgeschlossen.

**Screenshots per USB-Stick**

1\. USB-Stick einstecken

2\. Legen Sie bei der Projektierung eine Funktionstaste -&gt; Screenshot an und wählen Sie „Auf USB-Stick exportieren“

3\. Bei Berührung dieser Funktionstaste speichert das HMI das aktuelle Bild im entsprechenden Speicher

<img src="../../appendix/usdhisdata.files/image004.gif" width="595" />

Hinweis:

 • Den USB-Stick während des Exports nicht abziehen;

• Die Stromversorgung während des Exports nicht unterbrechen;

• Auf ausreichend freien Speicher auf dem USB-Stick achten.

<img src="../../appendix/usdhisdata.files/image004.gif" width="595" />
