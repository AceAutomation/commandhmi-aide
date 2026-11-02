# Verbindung „ein Gerät, mehrere HMI“

Die Touchscreens der Serie CommandHMI erlauben die Verbindung „ein Gerät, mehrere HMI“ mit einer SPS über das MODBUS-Protokoll. Die Touchscreens werden nacheinander verbunden, der erste mit der SPS. Erste Möglichkeit: Alle Touchscreens sind Slave, die SPS ist Master. Doppelklicken Sie im Projektmanager auf „COM1-Verbindung“; es öffnet sich das Eigenschaftsfenster der Kommunikationsschnittstelle. Wählen Sie unter „Geräteservice“ auf der Seite „Allgemein“ Modbus RTU und rechts Modbus RTU Slave. Zweite Möglichkeit: Der erste, mit der SPS verbundene Touchscreen ist Master, SPS und übrige Touchscreens sind Slave. Wählen Sie dann für den ersten Touchscreen unter „Geräteservice“ auf der Seite „Allgemein“ Modbus RTU und rechts Modbus RTU Master, stellen Sie auf der Seite „Parameter“ den erweiterten Modus ein und weisen Sie die Adressen der Touchscreens zu. Die als Slave eingestellten Touchscreens kommunizieren dann über den ersten Touchscreen mit der SPS. In beiden Fällen kommuniziert nur der Master mit den Slaves; die Slaves untereinander kommunizieren nicht.

SPS als Master, alle Touchscreens als Slave:

1. Die Kommunikationsschnittstelle der SPS ist RS232; Verdrahtung und Einstellungen zeigen die Abbildungen 8-1, 8-2 und 8-3:

<img src="../../multpoint/multhmi.files/multhmi1428.png" width="577" />

Abbildung 8-1  Schema „ein Gerät, mehrere HMI“ mit der SPS (RS232) als Master

<img src="../../multpoint/multhmi.files/multhmi1528.png" width="589" />

Abbildung 8-2 MODBUS-Protokoll wählen und als Slave einstellen

<img src="../../multpoint/multhmi.files/multhmi1593.png" width="588" />

Abbildung 8-3 Stationsadresse des HMI zuweisen

2. Die Kommunikationsschnittstelle der SPS ist RS485; die Verdrahtung zeigt Abbildung 8-4:

<img src="../../multpoint/multhmi.files/multhmi1744.png" width="598" />

Abbildung 8-4  Schema „ein Gerät, mehrere HMI“ mit der SPS (RS485) als Master

Ist die Schnittstelle der SPS RS485, sind alle Touchscreens Slave, und die Einstellungen entsprechen denen bei RS232. Siehe Abbildungen 8-2 und 8-3.

Sind alle HMI der Serie Slave, können bis zu 255 HMI verbunden werden. Je mehr Touchscreens verbunden sind, desto langsamer wird jedoch die Reaktion.

 Erster Touchscreen als Master, SPS und alle anderen HMI als Slave:

1.Die Kommunikationsschnittstelle der SPS ist RS232; Verdrahtung und Einstellungen zeigen die Abbildungen 8-5, 8-6 und 8-7:

<img src="../../multpoint/multhmi.files/multhmi2462.png" width="579" />

Abbildung 8-5   Schema „ein Gerät, mehrere HMI“ mit der SPS (RS232) als Slave

<img src="../../multpoint/multhmi.files/multhmi2563.png" width="588" />

Abbildung 8-6 MODBUS-Protokoll für das erste HMI wählen und als Master einstellen

<img src="../../multpoint/multhmi.files/multhmi2650.png" width="590" />

Abbildung 8-7 Ist der erste Touchscreen Master, ist der erweiterte Modus erforderlich

Die Einstellungen der Touchscreens als Slave entsprechen weitgehend den Abbildungen 8-2 und 8-3.

<img src="../../multpoint/multhmi.files/multhmi2852.png" width="130" />

Hinweis: Da RS232 keine Mehrpunktverbindung unterstützt, ist ein Umsetzer RS485/RS232 nötig, wenn die SPS der Verbindung „ein Gerät, mehrere HMI“ keine RS485-Schnittstelle hat.

Hinweis: Ist ein Touchscreen der Serie in der Verbindung „ein Gerät, mehrere HMI“ Master, muss sein Adressmodus auf Multiprotokoll eingestellt sein.

Mit Modbus als Master können grundsätzlich bis zu 255 Slaves hinzugefügt werden; je mehr Slaves, desto langsamer die Kommunikation.
