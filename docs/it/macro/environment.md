# Esempio di protocollo di comunicazione libero (Free Port)

Impostazione dei parametri della comunicazione libera, come mostrato di seguito:

<img src="../../macro/environment.files/image001.jpg" width="601" alt="ScreenShot00094.jpg" />

La porta COM è impostata su Samkoon – NULL PLC

I parametri di comunicazione predefiniti sono i seguenti:

<img src="../../macro/environment.files/image002.jpg" width="595" alt="ScreenShot00095.jpg" />

Per prima cosa, creare tre pagine:

<img src="../../macro/environment.files/environment42.png" width="800" />

Pagina 1

<img src="../../macro/environment.files/environment61.png" width="793" />

Pagina 2

<img src="../../macro/environment.files/environment80.png" width="809" />

Pagina 3

I sei oggetti sul lato destro delle pagine 1 e 3 sono oggetti di visualizzazione numerica, i cui indirizzi di monitoraggio sono, dall'alto verso il basso, LW60297, LW60298, LW60299, LW60300, LW60301 e LW60302 = 1. I due oggetti rossi sono spie di bit con indirizzi di monitoraggio LB100 e LB101. Gli oggetti nella parte inferiore della pagina 3 sono oggetti di visualizzazione numerica a partire dall'indirizzo LW400, con un passo di 1.

Le impostazioni "Avanzate" dei due pulsanti di pagina nella pagina 2 sono:

<img src="../../macro/environment.files/environment619.png" width="675" />

<img src="../../macro/environment.files/environment621.png" width="675" />

Impostazione dello script globale:

<img src="../../macro/environment.files/environment646.png" width="437" />

<img src="../../macro/environment.files/environment648.png" width="437" />

**Codice di Marco_COM:**

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
if (LB0==0) // 0 indica lo stato di invio; 1 indica lo stato di attesa ricezione
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
if (result<=0) // 0 indica nessuna ricezione, 1 indica ricezione errata
{
LW1++; // timeout, inizia il conteggio
if (LW1>=3) // Attende il tempo di esecuzione di 3 macro
{
LW1=0; // azzeramento
LB0=0; // invia il flag di azzeramento; invio alla prossima esecuzione
}
return; // esce direttamente
}
else // ricezione corretta
{
LW2=Gdata[0]&0xff; // elaborazione dei dati ricevuti
LW3=Gdata[1]&0xff;
LW4=Gdata[2];
LW5=Gdata[3];
LB0=0; // elaborazione completata; invio alla prossima esecuzione
PUTCHARS(0,Pdata,0); //svuota il buffer
}
}
}
```

**Codice di Macro1:**

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
char Pdata[20]; //array dei dati da inviare
char Mdata[100]; //array dei dati ricevuti
int result; //lunghezza dei dati di risposta ricevuti
if (LB0==0) //LB0 è il flag di invio/ricezione: 0 stato di invio, 1 stato di attesa ricezione
{
Pdata[0]=0x02; //dati da inviare: lettura dei registri di mantenimento; il primo byte è l'indirizzo dello slave
Pdata[1]=0x03; //codice funzione: lettura dei registri di mantenimento
Pdata[2]=0x00; // indirizzo iniziale dei dati da leggere
Pdata[3]=0x00;
Pdata[4]=0x00; //lunghezza in word dei dati da leggere
Pdata[5]=0x03;
Wcrc=CRC(Pdata,6); //calcola il CRC dei dati precedenti
Pdata[6]=(Wcrc&0xff); //scambia byte alto e basso del CRC; P6 prende il byte basso
Pdata[7]=(Wcrc>>8); //P7 prende il byte alto
PUTCHARS(0,Pdata,8); //funzione di invio: invia tutti i dati alla porta seriale
LB0=1; // invio completato; alla prossima esecuzione attende la ricezione invece di inviare
return; //esce per attendere la ricezione
}
```

else

```c
{
result=GETCHARS(0,Mdata);//funzione di ricezione: salva i dati ricevuti nell'array Gdata
LW0=result; //controlla la lunghezza ricevuta
if (result<=0) //0 indica nessuna ricezione, 1 indica ricezione errata
{
LW1++; //timeout; inizia il conteggio
if (LW1>=3) //attende il tempo di esecuzione di 3 macro
{
LW1=0; //azzeramento
LB0=0; //invia il flag di azzeramento; invio alla prossima esecuzione
}
return; //esce direttamente
}
else //ricezione corretta
{
LW400=Mdata[0]&0xff; //elaborazione dei dati ricevuti
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
LB0=0; //elaborazione completata; invio alla prossima esecuzione
PUTCHARS(0,Pdata,0); //svuota il buffer
}
}
}
```

<img src="../../macro/environment.files/environment3382.png" width="130" />

Nome e indirizzo delle variabili sono gli stessi nella finestra di compilazione della funzione.
