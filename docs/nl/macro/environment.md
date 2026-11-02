# Voorbeeld vrij communicatieprotocol

Instellingen van de vrije communicatieparameters, zoals hieronder:

<img src="../../macro/environment.files/image001.jpg" width="601" alt="ScreenShot00094.jpg" />

De COM-poort wordt ingesteld op Samkoon – NULL PLC

De standaardcommunicatieparameters zijn:

<img src="../../macro/environment.files/image002.jpg" width="595" alt="ScreenShot00095.jpg" />

Maak eerst drie schermen aan:

<img src="../../macro/environment.files/environment42.png" width="800" />

Scherm 1

<img src="../../macro/environment.files/environment61.png" width="793" />

Scherm 2

<img src="../../macro/environment.files/environment80.png" width="809" />

Scherm 3

De zes objecten rechts in scherm 1 en 3 zijn numerieke weergaven met van boven naar beneden de bewakingsadressen LW60297, LW60298, LW60299, LW60300, LW60301 en LW60302 = 1. De twee rode objecten zijn bitlampen met de bewakingsadressen LB100 en LB101. De objecten onderaan scherm 3 zijn numerieke weergaven vanaf adres LW400 met een adresinterval van 1.

De instellingen onder “Geavanceerd” van de twee schermknoppen in scherm 2 zijn:

<img src="../../macro/environment.files/environment619.png" width="675" />

<img src="../../macro/environment.files/environment621.png" width="675" />

Instelling globaal script:

<img src="../../macro/environment.files/environment646.png" width="437" />

<img src="../../macro/environment.files/environment648.png" width="437" />

**Code van Marco_COM:**

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
if (LB0==0) // 0 betekent verzendstatus; 1 betekent wachten op ontvangst
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
if (result<=0) // 0 betekent geen ontvangst, 1 betekent foutieve ontvangst
{
LW1++; // time-out, begin te tellen
if (LW1>=3) // Wacht de uitvoeringstijd van 3 scripts
{
LW1=0; // op nul zetten
LB0=0; // markering voor op nul zetten verzenden; de volgende keer verzenden
}
return; // direct afsluiten
}
else // correcte ontvangst
{
LW2=Gdata[0]&0xff; // verwerking van de ontvangen gegevens
LW3=Gdata[1]&0xff;
LW4=Gdata[2];
LW5=Gdata[3];
LB0=0; // verwerking voltooid; bij de volgende doorloop verzenden
PUTCHARS(0,Pdata,0); //buffer wissen
}
}
}
```

**Code van Macro1:**

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
char Pdata[20]; //te verzenden gegevens, opgeslagen in een array
char Mdata[100]; //ontvangen gegevens, opgeslagen in een array
int result; //lengte van de ontvangen antwoordgegevens
if (LB0==0) //LB0 is de vlag voor verzenden/ontvangen: 0 verzendstatus, 1 wachten op ontvangst
{
Pdata[0]=0x02; //te verzenden gegevens: holdingregisters lezen; de eerste byte is het adres van het slave-station
Pdata[1]=0x03; //functiecode: holdingregisters lezen
Pdata[2]=0x00; // beginadres van de te lezen gegevens
Pdata[3]=0x00;
Pdata[4]=0x00; //woordlengte van de te lezen gegevens
Pdata[5]=0x03;
Wcrc=CRC(Pdata,6); //CRC over de voorgaande gegevens
Pdata[6]=(Wcrc&0xff); //hoge en lage byte van de CRC verwisselen; P6 krijgt de lage byte
Pdata[7]=(Wcrc>>8); //P7 krijgt de hoge byte
PUTCHARS(0,Pdata,8); //verzendfunctie: alle gegevens naar de seriële poort sturen
LB0=1; // verzenden voltooid; bij de volgende doorloop op ontvangst wachten in plaats van te verzenden
return; //afsluiten en op ontvangst wachten
}
```

else

```c
{
result=GETCHARS(0,Mdata);//ontvangstfunctie: de ontvangen gegevens in de array Gdata opslaan
LW0=result; //ontvangen lengte controleren
if (result<=0) //0 betekent geen ontvangst, 1 betekent foutieve ontvangst
{
LW1++; //time-out; begin te tellen
if (LW1>=3) //wacht de uitvoeringstijd van 3 scripts
{
LW1=0; //op nul zetten
LB0=0; //markering voor op nul zetten verzenden; bij de volgende doorloop verzenden
}
return; //direct afsluiten
}
else //correcte ontvangst
{
LW400=Mdata[0]&0xff; //verwerking van de ontvangen gegevens
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
LB0=0; //verwerking voltooid; bij de volgende doorloop verzenden
PUTCHARS(0,Pdata,0); //buffer wissen
}
}
}
```

<img src="../../macro/environment.files/environment3382.png" width="130" />

Naam en adres van de variabelen zijn dezelfde als in het compileervenster van de functie.
