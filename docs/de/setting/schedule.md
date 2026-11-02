# Zeitplan

Mit dem Zeitplan lassen sich Ereignisse planen. Beispiel: Eine Fabrik startet die Maschinen werktags um 8:00 Uhr und schaltet sie um 18:00 Uhr ab.

Klicken Sie in der Standardliste auf „Zeitplan“; es öffnet sich das Dialogfeld des Zeitplans, wie unten.

<img src="../../setting/schedule.files/schedule706.png" width="728" />

 Abbildung 7-49 Dialogfeld Zeitplan

Klicken Sie auf „Neu“; es öffnet sich ein neues Dialogfeld, wie unten. Zuerst wird die Seite „Allgemein“ angezeigt.

<img src="../../setting/schedule.files/schedule984.png" width="694" />

  Abbildung 7-50 Dialogfeld Neuer Zeitplan

• Beschreibung:

Geben Sie hier einen Text ein, der die Funktion dieses Zeitplans verständlich macht.

• Start-/Endaktion beim Einschalten ausführen:

Liegt der Einschaltzeitpunkt des HMI nach der Startzeit, wird die Start-/Endaktion ausgeführt.

• Zieladresse:

Geben Sie Typ und Adresse des Ziels ein; der Wert wird zur Start-/Endzeit in diese Adresse geschrieben.

• Schreibvorgang:

Typen: „Konstante“ und „Adresse“. Bei „Konstante“ wird der angegebene Wert in die Zieladresse geschrieben. Bei „Adresse“ wird zur Start-/Endzeit der Wert der angegebenen Adresse in die Zieladresse geschrieben.

• Endaktion verwenden:

Ist diese Option aktiviert, wird der Wert des Schreibvorgangs zur Endzeit in die Zieladresse geschrieben.

 Klicken Sie nach der Seite „Allgemein“ auf die Seite „Zeitraum“, wie unten.

<img src="../../setting/schedule.files/schedule2016.png" width="694" />

  Abbildung 7-51 Seite „Zeitraum“

• Konstante: Aktivieren Sie Start-/Endzeit; zu diesen Zeitpunkten wird der entsprechende Schreibvorgang ausgeführt.

• Adresse: Start- und Endzeit des Zeitplans werden über einen Adressbereich gesteuert, wie unten.

 <img src="../../setting/schedule.files/schedule2396.png" width="693" />

 Abbildung 7-52 Steuerung über Adressen

Beispiel: Ist die Adresse LW0, dienen LW0~LW10 als Zeitplanadressen.

LW0: Steueradresse. Bei LW0 == 1 werden die Zeiten in das HMI geladen und der Zeitplan beginnt zu arbeiten. Nach dem Laden wird LW0 auf 0 zurückgesetzt;

LW1: Zeitplanstatus. Nach dem Laden der Zeiten (LW0 == 0) wird LW1 auf 1 gesetzt.

LW2: Aktionsmodus. Ist LW2 = 1 und liegt die aktuelle Zeit nach der Startzeit, wird der Schreibvorgang ausgeführt. Ist LW2 = 0, wird die Start-/Endaktion ausgeführt, wenn die aktuelle Zeit der Start-/Endzeit entspricht.

LW3: Wochentag der Startzeit; Wert = 2^(Nummer des Wochentags), LW3 = (0,1,4,8,16,32,64)

LW4~LW6: Stunden, Minuten, Sekunden der Startzeit.

LW7: Wochentag der Endzeit; Wert = 2^(Nummer des Wochentags), LW3 = (0,1,4,8,16,32,64)

LW8~LW10: Stunden, Minuten, Sekunden der Endzeit.

Entsprechend gilt: Ist LWn die Steueradresse, dienen LWn~LWn+10 als Zeitplanadressen, wie oben.

**Tipp:** Ist „Adresse“ aktiviert, vergessen Sie nicht, nach dem Einstellen der Start-/Endzeit die Steueradresse auf 1 zu setzen, damit der Zeitplan geladen wird. Andernfalls arbeitet der Zeitplan nicht.

Seite „Sperre“, wie unten:

<img src="../../setting/schedule.files/schedule3691.png" width="694" />

 Abbildung 7-53 Seite „Sperre“

Ist „Sperre verwenden“ aktiviert, arbeitet der Zeitplan nur, wenn die Bitadresse die Bedingung (0 oder 1) erfüllt.

Klicken Sie nach dem Einstellen der Parameter auf „OK“; ein Zeitplaneintrag wird angelegt, wie unten.

<img src="../../setting/schedule.files/schedule4054.png" width="732" />

  Abbildung 7-50 Angelegter Zeitplan
