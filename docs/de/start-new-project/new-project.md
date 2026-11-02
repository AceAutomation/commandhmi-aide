# Neues Projekt anlegen

Dieser Schritt ist zum Anlegen eines neuen Projekts nötig. Wählen Sie „Neues Projekt“ im Menü „Datei“ oder die Schaltfläche „Neues Projekt“ <img src="../../start-new-project/new-project.files/new-project136.png" width="28" /> in der Werkzeugleiste; CommandHMI öffnet das Dialogfeld „Neues Projekt“, in dem Name und Speicherpfad des Projekts festgelegt werden. Wählen Sie das passende HMI-Modell; „OK“ legt das Projekt an und öffnet die Einstellungen der Kommunikationsschnittstelle; „Abbrechen“ schließt das Dialogfeld.

**1. Dialogfeld Neues Projekt**

Projektname:

Pfad: Speicherpfad der neuen Projektdatei; Standard ist C: \\

Modell: für Projekte verfügbare Modelle:

HM-035AE(320\*240)        HM-035UE(320\*240)        HM-043AE()480\*272        HM-043D(480\*272)        HM-043AD(480-272)        HM-043BE(480\*272)        HM-043BS(480\*272)        HM-043QE(480\*272)        HM-043UE(480\*272)        HM-043TE(480\*272)        HM-050AS(480\*272)        HM-050AE(480\*272)        HM-050BS(800\*480)        HM-050BE(800\*480)        HM-057AE(640\*480)        HM-070AS(800\*480)        HM-070AE(800\*480)        HM-070BS(800\*480)        HM-070BE(800\*480)        HM-070GS(800\*480)        HM-070GE(800\*480)        HM-070QS(800\*480)        HM-070QE(800\*480)        HM-070GG(800\*480)        HM-070GW(800\*480)        HM-070MS(800\*480)        HM-070ME(800\*480)        HM-070MG(800\*480)        HM-070MW(800\*480)        HM-T070XS(1024\*600)        HM-102AS(800\*480)        HM-102AE(800\*480)        HM-102BS(1024\*600)        HM-102BE(1024\*600)        HM-102CW(1024\*600)        HM-102CG(1024\*600)        HM-102HE(1024\*600)        HM-102HS(1024\*600)        HM-121AS(800\*600)        HM-121AE(800\*600)        HM-H150AS(1024\*768)        HM-156QS(1920\*1080)

Standardmodell ist HM-070AE(800\*480); die Auflösung (800 \* 480) in Klammern wird im Dialogfeld nicht angezeigt.

Anzeigemodus: Ausrichtung des Touchscreens im Projekt. Zur Wahl stehen:

Horizontal: Projektierung mit horizontalem Touchscreen.

Vertikal: Projektierung mit vertikalem Touchscreen.

Standard ist Horizontal.

<img src="../../start-new-project/new-project.files/image002.jpg" width="547" alt="ScreenShot00217.jpg" />

Abbildung 3-1      Dialogfeld Neues Projekt

Im Dialogfeld „Neues Projekt“ oben werden Name, Pfad, Modell und Anzeigemodus festgelegt; klicken Sie dann auf „Weiter“, um die Kommunikationsschnittstelle einzustellen.

Das konkrete Modell richtet sich nach dem HMI-Modell des Benutzers.

<img src="../../start-new-project/new-project.files/new-project1533.png" width="130" />

Der Name des neuen Projekts darf folgende Zeichen nicht enthalten: \\ /: \* "&lt;&gt; \|?.

Der Speicherort des neuen Projekts darf folgende Zeichen nicht enthalten: \\ /: \* "&lt;&gt; \|?.

## 2. Dialogfeld Kommunikationseinstellungen

Im Dialogfeld Kommunikationseinstellungen werden die Parameter der Kommunikationsschnittstelle des HMI eingestellt. Nur mit korrekten Parametern ist eine normale Kommunikation zwischen SPS und Touchscreen gewährleistet. Die Parameter hängen vom angeschlossenen SPS-Modell ab.

Verbindungsname: Name der Kommunikationsschnittstelle.

Geräteservice: Wahl von SPS-Marke und CPU-Typ.

Verbindungsschnittstelle: COM-Port oder Ethernet-Port.

Intervall zusammenhängender SPS-Adressen: Bereich fortlaufender SPS-Adressen; der Standardwert wird empfohlen.

##

<img src="../../start-new-project/new-project.files/new-project2298.png" width="624" />

Abbildung 3-2      Dialogfeld Kommunikationseinstellungen

Im Dialogfeld oben wird der Geräteservice passend zum angeschlossenen Gerät gewählt. Für eine Ethernet-Verbindung wählen Sie unter „Verbindungsart“ die Option „Direktverbindung (Ethernet)“.

Verbindungs-ID: interner Parameter, nicht änderbar!

Die Kommunikationseigenschaften lassen sich auch später über „Verbindung“ im Projektmanager einstellen; die übrigen Parameter werden in den Kommunikationseigenschaften eingestellt.

**3.       Dialogfeld Bildeigenschaften**

Klicken Sie im Dialogfeld Kommunikationseinstellungen auf „Weiter“; es öffnet sich das Dialogfeld „Neues Bild“, in dem Name und Hintergrundfarbe des Bilds festgelegt werden. Standardname ist eine Bildnummer, Standardhintergrund ist Blau. Bei jedem neuen Bild vergibt CommandHMI eine Bildnummer, die die Reihenfolge der Bilder im Projekt angibt. Die Nummerierung beginnt bei 1: Das erste Bild hat die Nummer 1, Nr. 5 ist das fünfte Bild. Zum Ändern der Hintergrundfarbe klicken Sie auf das Rechteck hinter „Hintergrundfarbe“; es öffnet sich die Farbauswahl. Mit über zweihundert Farben zur schnellen Auswahl bietet CommandHMI eine sehr große Farbauswahl. Reicht das nicht, klicken Sie unten rechts in der Farbauswahl auf „Farbe anpassen“. Wählen Sie im Dialogfeld „Benutzerdefinierte Farben“ zuerst eine Grundfarbe, dann im mittleren Feld den Farbton; passen Sie die Farbe durch Ziehen mit der Maus an, auch im senkrechten Balken rechts, und klicken Sie auf „OK“. Grundfarbwerte lassen sich auch direkt eingeben.

<img src="../../start-new-project/new-project.files/new-project4278.png" width="626" />

Abbildung 3-3      Dialogfeld Neues Bild

<img src="../../start-new-project/new-project.files/new-project4313.png" width="506" />

Abbildung 3-4      Dialogfeld Farbauswahl

Auch eigene Grafiken können als Bildhintergrund dienen. Klicken Sie auf das Pfadsymbol, um die Grafik zu wählen.

<img src="../../start-new-project/new-project.files/new-project4463.png" width="331" />

Abbildung 3-5      Pfad der Grafik einstellen

Klicken Sie auf „OK“; das System öffnet sofort das neu angelegte Bild. Die Vorbereitungen sind abgeschlossen, nun kann das eigene Projekt bearbeitet werden.
