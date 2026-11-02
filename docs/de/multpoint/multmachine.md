# Verbindung „ein HMI, mehrere Geräte“

Die HMI der Serie erlauben neben „ein Gerät, mehrere HMI“ auch die Verbindung „ein HMI, mehrere Geräte“ mit SPS über das MODBUS-Protokoll. Dabei greift ein Touchscreen direkt auf die Register mehrerer angeschlossener SPS zu, sofern diese MODBUS unterstützen. Wählen Sie in den Einstellungen unter „Geräteservice“ auf der Seite „Allgemein“ Modbus RTU und rechts Modbus RTU Master: Der Touchscreen ist dann Master, alle SPS sind Slaves. Der Touchscreen kann nun auf die Register der SPS zugreifen; deren Registernamen entsprechen denen des MODBUS-Protokolls.

<img src="../../multpoint/multmachine.files/multmachine744.png" width="506" />

Abbildung 8-8      Verbindung „ein HMI, mehrere Geräte“

<img src="../../multpoint/multmachine.files/multmachine805.png" width="590" />

Abbildung 8-9      Touchscreen als Master einstellen

<img src="../../multpoint/multmachine.files/multmachine857.png" width="588" />

Abbildung 8-10    Ist der Touchscreen Master, ist der erweiterte Modus erforderlich

Nach dieser Einstellung sind die SPS-Adressen in den Eigenschaften der Kommunikationsschnittstelle wirkungslos. Bei der Adresseingabe für ein Objekt erscheint das Adresseingabefeld in Abbildung 8-11. Rechts neben dem Registernamen befindet sich eine Auswahlliste, in der die Slave-Adresse der SPS gewählt wird.

<img src="../../multpoint/multmachine.files/multmachine1294.png" width="251" />

Abbildung 8-11    Adresseingabefeld

<img src="../../multpoint/multmachine.files/multmachine1326.png" width="130" />

**Adressen zur Freigabe der Kommunikation je Station im erweiterten Modus:**

Jeder seriellen Schnittstelle sind 16 Worte für die Freigabe der Stationsnummern zugeordnet, also höchstens 256 Stationen; Basisadresse ist LW59000

COM1 entspricht 59010~59025: LW59010 den Stationen 0~15, LW59011 den Stationen 16~31 usw.

COM2 entspricht 59026~59041: LW59026 den Stationen 0~15, LW59027 den Stationen 16~31 usw.

Ethernet entspricht 59026~59041: LW59026 den Stationen 0~15, LW59027 den Stationen 16~31 usw.

Beim Start des HMI ist alles freigegeben; per Skript lässt sich jede Station über ihr Bit freigeben oder sperren.

<img src="../../multpoint/multmachine.files/multmachine1993.png" width="130" />

Hinweis: Da RS232 keine Mehrpunktverbindung unterstützt, ist ein Umsetzer RS485/RS232 nötig, wenn die SPS der Verbindung „ein HMI, mehrere Geräte“ keine RS485-Schnittstelle hat.
