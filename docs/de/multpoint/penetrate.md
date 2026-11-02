# Durchgangsverbindung

Die Touchscreens erlauben eine besondere Verbindungsart: Ein entferntes HMI überwacht oder steuert eine SPS oder ein anderes Gerät über die serielle Schnittstelle eines anderen HMI, das mit diesem Gerät verbunden ist. Das Gerät kann so von zwei oder mehr Bedienstellen aus bedient werden. Die Durchgangsverbindung ist eine sehr nützliche Funktion des HMI.

Vor der Verwendung der Durchgangsverbindung sollten folgende Begriffe bekannt sein:

• Lokales HMI: das mit der SPS oder dem Gerät verbundene HMI.

• Entferntes HMI: das mit dem lokalen HMI verbundene HMI, das die Geräte über die Durchgangsverbindung steuert.

Für eine Durchgangsverbindung braucht das lokale HMI zwei serielle Schnittstellen. Die Schemata zeigen die Abbildungen 8-12 und 8-13:

Durchgangsverbindung mit zwei HMI:

<img src="../../multpoint/penetrate.files/penetrate789.png" width="578" />

Abbildung 8-12    Schema der Durchgangsverbindung mit zwei HMI

Durchgangsverbindung mit mehreren HMI:

<img src="../../multpoint/penetrate.files/penetrate913.png" width="792" />

Abbildung 8-13    Schema der Durchgangsverbindung mit mehreren HMI

Lokales HMI: Softwareeinstellungen:

Doppelklicken Sie auf die angelegte Verbindung; es öffnet sich das Eigenschaftsfenster der Kommunikationsschnittstelle. Wählen Sie COM1 als Verbindungsport. Beispiel MITSUBISHI: COM1 des lokalen HMI ist mit einer MITSUBISHI FX2N verbunden. Die Kommunikationsparameter müssen zur angeschlossenen SPS bzw. zum Gerät passen. Siehe Abbildungen 8-14 und 8-15:

<img src="../../multpoint/penetrate.files/penetrate1423.png" width="589" />

Abbildung 8-14    Seite „Allgemein“ der Schnittstelleneigenschaften des lokalen HMI

<img src="../../multpoint/penetrate.files/penetrate1500.png" width="587" />

Abbildung 8-15: Seite COM1 der Schnittstelleneigenschaften des lokalen HMI

Legen Sie eine neue Verbindung an, wählen Sie COM2 als Verbindungsport, fügen Sie unter „Verbindung“ kein Protokoll hinzu und stellen Sie die Eigenschaften wie folgt ein, mit denselben seriellen Parametern wie Port 1. Empfohlen: 9600, 8, None, 1. Wählen Sie als Durchgangseigenschaft „Port zum Slave-HMI“ (Connect Slave Screen Port) und stellen Sie die Anzahl der HMI entsprechend ein. Siehe Abbildungen 8-16 und 8-17.

<img src="../../multpoint/penetrate.files/image001.jpg" width="598" alt="ScreenShot00093.jpg" />

Abbildung 8-16    Seite „Allgemein“ der Schnittstelleneigenschaften des lokalen HMI

<img src="../../multpoint/penetrate.files/penetrate2042.png" width="589" />

Abbildung 8-17    Seite „Parameter“ der Schnittstelleneigenschaften des lokalen HMI

Für die übrigen Parameter die Standardwerte belassen. Damit ist das lokale HMI eingestellt.

Entferntes HMI: Softwareeinstellungen:

Doppelklicken Sie auf die angelegte Verbindung; es öffnet sich das Eigenschaftsfenster der Kommunikationsschnittstelle. Wählen Sie COM1 als Verbindungsport und „Entfernt“ (Remote) als HMI-Standort und stellen Sie dieselben Kommunikationsparameter ein wie auf der Seite COM2 des lokalen HMI (siehe Abbildung 6 oben), wie in den Abbildungen 8-18 und 8-19.

<img src="../../multpoint/penetrate.files/penetrate2646.png" width="589" />

Abbildung 8-18    Seite „Allgemein“ der Schnittstelleneigenschaften des entfernten HMI

<img src="../../multpoint/penetrate.files/penetrate2724.png" width="588" />

Abbildung 8-19    Seite „Parameter“ der Schnittstelleneigenschaften des entfernten HMI

Für die übrigen Parameter die Standardwerte belassen. Damit ist das entfernte HMI eingestellt.

<img src="../../multpoint/penetrate.files/penetrate2924.png" width="130" />

Hinweis: Diese Einstellungen gelten für die Durchgangsverbindung mit zwei HMI.

Hinweis: Bei einer Durchgangsverbindung mit mehreren HMI entspricht die COM-Einstellung der entfernten HMI der des lokalen HMI.

Hinweis: Da alle Daten über COM1 des lokalen HMI mit der SPS ausgetauscht werden, ist die Kommunikation bei einer Durchgangsverbindung mit mehreren HMI langsam.
