# HMI-Schutz

Mit dem HMI-Schutz wird ein Zeitraum festgelegt, in dem das HMI normal funktioniert. Danach wechselt das HMI zu einem bestimmten Bild, in dem ein Passwort zur weiteren Nutzung eingegeben werden muss.

Doppelklicken Sie im Projektmanager auf „HMI-Schutz“, um das Dialogfeld in Abbildung 7-14 zu öffnen:

<img src="../../setting/hmi-protect.files/hmi-protect343.png" width="622" />

Abbildung 7-14    Dialogfeld HMI-Schutz

Beispiel zur Anwendung dieser Funktion:

➢„Entsperrpasswort“ aktivieren: Beim nächsten Öffnen des HMI-Schutzes ist ein Passwort erforderlich.

➢„Alle Ebenen freigeben“ aktivieren: Wird dieses Passwort beim Entsperren eingegeben, werden alle Ebenen des HMI-Schutzes aufgehoben.

➢„HMI-Schutz“ aktivieren: Die Seite „Schutzeinstellungen“ öffnet sich automatisch, wie unten:

<img src="../../setting/hmi-protect.files/hmi-protect743.png" width="623" />

Abbildung 7-15    Einstellungen des HMI-Schutzes

Stellen Sie die „Gesamtzahl der Passwortebenen“ auf 3; wählen Sie die Schaltfläche 1, dann 2009-04-01 und 12-00-00 in der Spalte „Zeitlimit“ unter „Parameter“; wählen Sie Bild 1 als „Warnbild“; stellen Sie das „Entsperrpasswort“ auf 1111. Damit ist der Schutz der Ebene 1 eingestellt.

Stellen Sie ebenso Zeitlimits und Passwörter für die Ebenen 2 und 3 ein.

• alle Ebenen aufheben

Ist diese Funktion aktiviert und das Passwort festgelegt, hebt dieses Passwort alle Ebenen des HMI-Schutzes auf

•  Passwort beim Öffnen

Ist diese Funktion aktiviert und das Passwort festgelegt, muss es beim nächsten Öffnen des HMI-Schutzes eingegeben werden, um die Informationen anzuzeigen

•  Passwortschutz aktivieren

Aktiviert den HMI-Schutz. Einzelheiten werden unter „Schutzeinstellungen“ festgelegt.

• Schutzeinstellungen

Gesamtzahl der Passwortebenen: bis zu 15 Ebenen des HMI-Schutzes für verschiedene Zeiträume

Aktuelle Passwortebene: Die folgenden Parameter gelten für die aktuelle Ebene

Parameter:

Nutzungsdauer: Ablaufdatum des HMI-Schutzes

Warnbild bei Ablauf: Bild, das beim Ablauf des HMI-Schutzes angezeigt wird

Entsperrpasswort: Passwort, das den HMI-Schutz nach Ablauf aufhebt

Erweiterte Einstellungen:

Verbleibende Tage anzeigen: zeigt die Tage bis zum Ende der eingestellten Schutzdauer

Vorwarnung:

Anzahl der Tage vor Ende der Schutzdauer, ab der gewarnt wird

Verzögerung:

Nach Ablauf der Schutzdauer wird während der eingestellten Anzahl Tage das angegebene Bild im angegebenen Intervall angezeigt

Vorrang von Vorwarnung und Verzögerung

Vorwarnung aktiviert, Verzögerung aktiviert: Vorwarnung gilt

Vorwarnung nicht aktiviert, Verzögerung aktiviert: Verzögerung gilt

Vorwarnung aktiviert, Verzögerung aktiviert, Funktion „Verzögerte Entsperrung des HMI-Schutzes“ der Funktionstaste nicht verwendet: Vorwarnung gilt

Vorwarnung aktiviert, Verzögerung aktiviert, Funktion „Verzögerte Entsperrung des HMI-Schutzes“ der Funktionstaste verwendet: Verzögerung gilt

•  Anwendungsbeispiel:

Angenommen, die Gesamtzahl der Passwortebenen ist 3. Wählen Sie dann 0 unter „Aktuelle Passwortebene“. Wählen Sie unter „Parameter“ in der Spalte „Nutzungsdauer“ das Ablaufdatum, z. B. 2009/04/01. Geben Sie in der nächsten Spalte die Uhrzeit ein, z. B. 12:00:00. Wählen Sie unter „Warnbild bei Ablauf“ das Bild, z. B. Bild 1. Geben Sie unter „Entsperrpasswort“ das Passwort ein, z. B. 1111. Der HMI-Schutz der Ebene 1 ist eingestellt.

Wählen Sie dann 1 unter „Aktuelle Passwortebene“. Wählen Sie unter „Parameter“ in der Spalte „Nutzungsdauer“ das Datum, z. B. 2009-04-05. Geben Sie in der nächsten Spalte die Uhrzeit ein, z. B. 12-00-00. Wählen Sie unter „Warnbild bei Ablauf“ das Bild, z. B. Bild 2. Geben Sie unter „Entsperrpasswort“ das Passwort ein, z. B. 2222. Der HMI-Schutz der Ebene 2 ist eingestellt.

Wählen Sie dann 2 unter „Aktuelle Passwortebene“. Wählen Sie unter „Parameter“ in der Spalte „Nutzungsdauer“ das Datum, z. B. 2009-04-10. Geben Sie in der nächsten Spalte die Uhrzeit ein, z. B. 12-00-00. Wählen Sie unter „Warnbild bei Ablauf“ das Bild, z. B. Bild 3. Geben Sie unter „Entsperrpasswort“ das Passwort ein, z. B. 3333. Der HMI-Schutz der Ebene 3 ist eingestellt.

3 Einstellungen des HMI-Schutzes nach Klick auf „OK“.

Angenommen, heute ist der 2009-04-01, 08-00-00 Uhr. Die Nutzungsdauer des HMI-Schutzes der Ebene 1 endet am 2009-04-01 um 12-00-00. Da dieser Zeitpunkt noch nicht erreicht ist, funktioniert das HMI normal. Vier Stunden später, am 2009-04-01 um 12-00-00, wechselt das HMI automatisch zu dem für diesen Zeitraum eingestellten Bild. Damit das HMI weiter genutzt und andere Bilder bedient werden können, fügen Sie in diesem Bild (Bild 1) eine Funktionstaste mit der Funktion „HMI-Schutz entsperren“ hinzu. Nach Ablauf der Ebene 1 klicken Sie auf diese Taste und geben im Eingabefeld das Entsperrpasswort der Ebene 1 ein, hier 1111; damit ist der Passwortschutz aufgehoben.

Nach dem Entsperren der Ebene 1 funktioniert das HMI normal. Einige Zeit später, am 2009-04-05 um 12-00-00, ist die Zeit der Ebene 2 erreicht; das HMI wechselt automatisch zum eingestellten Schutzbild (Bild 2). Ebenso muss der Benutzer die Funktionstaste mit der Funktion „HMI-Schutz entsperren“ verwenden und das Passwort der Ebene 2 (2222) eingeben; danach funktioniert das HMI normal.

Da auch die Ebene 3 eingestellt ist, muss der Benutzer am 2009-04-10 um 12-00-00 ebenso die Funktionstaste „HMI-Schutz entsperren“ verwenden und das Entsperrpasswort der Ebene 3 (3333) eingeben; danach funktioniert das HMI wieder normal.

Sind alle 3 Ebenen entsperrt, ist der HMI-Schutz aufgehoben und das HMI funktioniert normal.

Die obigen Beispiele zeigen die Verwendung des HMI-Schutzes. Für weitere Passwortebenen ist das Vorgehen gleich; orientieren Sie sich an diesen Beispielen.
