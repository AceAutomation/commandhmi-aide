# Modbus TCP/IP

Über MODBUS TCP lässt sich das HMI aus der Ferne steuern und überwachen.

**Einstellungen** mit dem HMI als Master:

Doppelklicken Sie nach dem Anlegen des Projekts auf „Verbindung 1“ (Connection 1), wie unten:

<img src="../../multpoint/modbustcpip.files/modbustcpip209.png" width="248" />

Es öffnet sich das Dialogfeld „Eigenschaften der Kommunikationsschnittstelle“ (Communication Port Properties), wie unten.

<img src="../../multpoint/modbustcpip.files/modbustcpip286.png" width="590" />

Klicken Sie im Dialogfeld „Port-Eigenschaften“ auf „Parameter“, um IP-Adresse und Port einzustellen (die des überwachten Geräts). Wählen Sie den Standard-Adressmodus und klicken Sie auf „OK“.

<img src="../../multpoint/modbustcpip.files/modbustcpip544.png" width="588" />

Im „Erweiterten Modus“ (Extended Mode) sind die hier eingestellte IP-Adresse und der Port wirkungslos; sie werden im Betrieb über die Funktionstaste „IP-Konfiguration der Slave-Geräte“ (Slave devices IP config) eingestellt.

Im Betrieb öffnet ein Druck auf diese Taste ein Fenster zur Eingabe der Stationsnummer; nach der Eingabe gelangen Sie zur Einstellung von IP und Port des Slaves, wie unten:

<img src="../../multpoint/modbustcpip.files/modbustcpip985.png" width="445" />

Laden Sie das Projekt danach in das HMI; verbinden Sie Master und Slave direkt oder über einen Router für Überwachung und Steuerung.

**Einstellungen der Slave-Station:**

**1. IP-Adresse einstellen**

Stellen Sie zuerst mit den DIP-Schaltern 1 und 3 die IP-Adresse des HMI ein: Geben Sie im angezeigten IP-Einstellungsfenster die IP-Adresse ein. In diesem Beispiel ist die IP-Adresse der Slave-Station 192.168.1.31. 2.

**2. Verbindungen anlegen**

Doppelklicken Sie nach dem Anlegen des Projekts auf „Verbindung 1“ (Connection 1), wie unten:

<img src="../../multpoint/modbustcpip.files/modbustcpip1527.png" width="229" />

Es öffnet sich das Dialogfeld „Eigenschaften der Kommunikationsschnittstelle“ (Communication Port Properties), wie unten.

<img src="../../multpoint/modbustcpip.files/modbustcpip1604.png" width="588" />

Nehmen Sie im obigen Dialogfeld folgende Einstellungen vor:

\* Verbindungsport: „Ethernet“ (siehe Abbildung).

<img src="../../multpoint/modbustcpip.files/modbustcpip1711.png" width="543" />

\* HMI-Standort: „Local“ wählen (siehe Abbildung).

<img src="../../multpoint/modbustcpip.files/modbustcpip1752.png" width="163" />

\* Verbindungsservice: „Modbus“ - „Modbus Slave TCP / IP“ wählen (siehe Abbildung).

<img src="../../multpoint/modbustcpip.files/modbustcpip1830.png" width="531" />

Klicken Sie im Dialogfeld „Port-Eigenschaften“ auf „Parameter“, um IP-Adresse (die der Slave-Station) und Port einzustellen. Klicken Sie auf „OK“.

<img src="../../multpoint/modbustcpip.files/modbustcpip2039.png" width="589" />

Laden Sie das Projekt in das HMI; verbinden Sie Master und Slave direkt oder über einen Router für Überwachung und Steuerung.

<img src="../../multpoint/modbustcpip.files/modbustcpip2198.png" width="130" />

Die Adresse ist die interne Adresse, wenn das HMI als Slave-Station eingestellt ist.
