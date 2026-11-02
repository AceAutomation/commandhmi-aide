# Beispiel: freies Kommunikationsprotokoll (Free Port)

Einstellung der freien Kommunikation, wie unten:

<img src="../../macro/environment.files/image001.jpg" width="601" alt="ScreenShot00094.jpg" />

Der COM-Port wird auf Samkoon – NULL PLC eingestellt

Die Standard-Kommunikationsparameter sind:

<img src="../../macro/environment.files/image002.jpg" width="595" alt="ScreenShot00095.jpg" />

Legen Sie zunächst drei Bilder an:

<img src="../../macro/environment.files/environment42.png" width="800" />

Bild 1

<img src="../../macro/environment.files/environment61.png" width="793" />

Bild 2

<img src="../../macro/environment.files/environment80.png" width="809" />

Bild 3

Die sechs Objekte rechts in Bild 1 und 3 sind numerische Anzeigen mit den Überwachungsadressen LW60297, LW60298, LW60299, LW60300, LW60301 und LW60302 = 1 (von oben nach unten). Die beiden roten Objekte sind Bit-Lampen mit den Adressen LB100 und LB101. Die Objekte unten in Bild 3 sind numerische Anzeigen ab Adresse LW400 mit Adressabstand 1.

Einstellungen „Erweitert“ der beiden Bildwechsel-Tasten in Bild 2:

<img src="../../macro/environment.files/environment619.png" width="675" />

<img src="../../macro/environment.files/environment621.png" width="675" />

Einstellung des globalen Skripts:

<img src="../../macro/environment.files/environment646.png" width="437" />

<img src="../../macro/environment.files/environment648.png" width="437" />

**Code von Marco_COM:**

```c
#include "MacroInit.h"
void Macro_main(IN *p)
{
```

MarcoInit

```c
LW60297=0;
LW60298=3;
LW60299=0;
LW60300=1;
LW60302=1;
char Pdata[20];
char Gdata[100];
int result;
if (LB0==0) // 0: Sendezustand; 1: Warten auf Empfang
{
Pdata[0]=LW200;
Pdata[1]=LW201;
Pdata[2]=LW202;
Pdata[3]=LW203;
PUTCHARS(0,Pdata,4);
LB0=1; //
return; //
}
```

else

```c
{
result=GETCHARS(0,Gdata);
LW0=result;
if (result<=0) // 0: kein Empfang; 1: fehlerhafter Empfang
{
LW1++; // Timeout, Zählung beginnt
if (LW1>=3) // Wartezeit von 3 Skriptausführungen
{
LW1=0; // zurücksetzen
LB0=0; // Rücksetzkennung senden; beim nächsten Durchlauf senden
}
return; // direkt beenden
}
else // korrekter Empfang
{
LW2=Gdata[0]&0xff; // Verarbeitung der empfangenen Daten
LW3=Gdata[1]&0xff;
LW4=Gdata[2];
LW5=Gdata[3];
LB0=0; // Verarbeitung abgeschlossen; beim nächsten Durchlauf senden
PUTCHARS(0,Pdata,0); //Puffer leeren
}
}
}
```

**Code von Macro1:**

```c
#include "MacroInit.h"
void Macro_main(IN *p)
{
```

MarcoInit

```c
LW60297=0;
LW60298=4;
LW60299=0;
LW60300=1;
LW60302=2;
char Pdata[20]; //Array der zu sendenden Daten
char Mdata[100]; //Array der empfangenen Daten
int result; //Länge der empfangenen Antwortdaten
if (LB0==0) //LB0 ist die Sende-/Empfangskennung: 0 Sendezustand, 1 Warten auf Empfang
{
Pdata[0]=0x02; //Sendedaten: Halteregister lesen; das erste Byte ist die Adresse der Slave-Station
Pdata[1]=0x03; //Funktionscode: Halteregister lesen
Pdata[2]=0x00; // Startadresse der zu lesenden Daten
Pdata[3]=0x00;
Pdata[4]=0x00; //Wortlänge der zu lesenden Daten
Pdata[5]=0x03;
Wcrc=CRC(Pdata,6); //CRC der vorherigen Daten berechnen
Pdata[6]=(Wcrc&0xff); //High- und Low-Byte des CRC tauschen; P6 erhält das Low-Byte
Pdata[7]=(Wcrc>>8); //P7 erhält das High-Byte
PUTCHARS(0,Pdata,8); //Sendefunktion: alle Daten an die serielle Schnittstelle senden
LB0=1; // Senden abgeschlossen; beim nächsten Durchlauf auf Empfang warten statt zu senden
return; //beenden, um auf den Empfang zu warten
}
```

else

```c
{
result=GETCHARS(0,Mdata);//Empfangsfunktion: empfangene Daten im Array Gdata speichern
LW0=result; //Empfangslänge prüfen
if (result<=0) //0: kein Empfang; 1: fehlerhafter Empfang
{
LW1++; //Timeout; Zählung beginnt
if (LW1>=3) //Wartezeit von 3 Skriptausführungen
{
LW1=0; //zurücksetzen
LB0=0; //Rücksetzkennung senden; beim nächsten Durchlauf senden
}
return; //direkt beenden
}
else //korrekter Empfang
{
LW400=Mdata[0]&0xff; //Verarbeitung der empfangenen Daten
LW401=Mdata[1]&0xff;
LW402=Mdata[2];
LW403=Mdata[3];
LW404=Mdata[4];
LW405=Mdata[5];
LW406=Mdata[6];
LW407=Mdata[7];
LW408=Mdata[8];
LW409=Mdata[9];
LW410=Mdata[10];
LB0=0; //Verarbeitung abgeschlossen; beim nächsten Durchlauf senden
PUTCHARS(0,Pdata,0); //Puffer leeren
}
}
}
```

<img src="../../macro/environment.files/environment3382.png" width="130" />

Name und Adresse der Variablen sind im Kompilierfenster gleich.
