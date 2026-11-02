# Exemple de protocole de communication libre (Free Port)

Paramétrage de la communication libre, comme ci-dessous :

<img src="../../macro/environment.files/image001.jpg" width="601" alt="ScreenShot00094.jpg" />

Le port COM est réglé sur Samkoon – NULL PLC

Les paramètres de communication par défaut sont les suivants :

<img src="../../macro/environment.files/image002.jpg" width="595" alt="ScreenShot00095.jpg" />

Créez d'abord trois écrans :

<img src="../../macro/environment.files/environment42.png" width="800" />

Écran 1

<img src="../../macro/environment.files/environment61.png" width="793" />

Écran 2

<img src="../../macro/environment.files/environment80.png" width="809" />

Écran 3

Les six objets à droite des écrans 1 et 3 sont des affichages numériques, d'adresses de surveillance LW60297, LW60298, LW60299, LW60300, LW60301 et LW60302 = 1, de haut en bas. Les deux objets rouges sont des voyants de bit, d'adresses LB100 et LB101. Les objets en bas de l'écran 3 sont des affichages numériques, à partir de LW400 avec un pas d'adresse de 1.

Réglages « Avancé » des deux boutons d'écran de l'écran 2 :

<img src="../../macro/environment.files/environment619.png" width="675" />

<img src="../../macro/environment.files/environment621.png" width="675" />

Réglage du script global :

<img src="../../macro/environment.files/environment646.png" width="437" />

<img src="../../macro/environment.files/environment648.png" width="437" />

**Code de Marco_COM :**

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
if (LB0==0) // 0 : état d'envoi ; 1 : état d'attente de réception
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
if (result<=0) // 0 : pas de réception ; 1 : réception erronée
{
LW1++; // timeout, début du comptage
if (LW1>=3) // Attend la durée de 3 exécutions de macro
{
LW1=0; // remise à zéro
LB0=0; // envoie l'indicateur de remise à zéro ; envoi au prochain passage
}
return; // sort directement
}
else // réception correcte
{
LW2=Gdata[0]&0xff; // traitement des données reçues
LW3=Gdata[1]&0xff;
LW4=Gdata[2];
LW5=Gdata[3];
LB0=0; // traitement terminé ; envoi au prochain passage
PUTCHARS(0,Pdata,0); //vide le tampon
}
}
}
```

**Code de Macro1 :**

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
char Pdata[20]; //tableau des données à envoyer
char Mdata[100]; //tableau des données reçues
int result; //longueur des données de réponse reçues
if (LB0==0) //LB0 est l'indicateur d'envoi/réception : 0 état d'envoi, 1 état d'attente de réception
{
Pdata[0]=0x02; //données à envoyer : lecture des registres de maintien ; le premier octet est l'adresse de l'esclave
Pdata[1]=0x03; //code fonction : lecture des registres de maintien
Pdata[2]=0x00; // adresse de début des données à lire
Pdata[3]=0x00;
Pdata[4]=0x00; //longueur en mots des données à lire
Pdata[5]=0x03;
Wcrc=CRC(Pdata,6); //calcule le CRC des données précédentes
Pdata[6]=(Wcrc&0xff); //échange octet fort et octet faible du CRC ; P6 prend l'octet faible
Pdata[7]=(Wcrc>>8); //P7 prend l'octet fort
PUTCHARS(0,Pdata,8); //fonction d'envoi : envoie toutes les données sur le port série
LB0=1; // envoi terminé ; au prochain passage, attente de la réception au lieu d'un envoi
return; //sort pour attendre la réception
}
```

else

```c
{
result=GETCHARS(0,Mdata);//fonction de réception : enregistre les données reçues dans le tableau Gdata
LW0=result; //vérifie la longueur reçue
if (result<=0) //0 : pas de réception ; 1 : réception erronée
{
LW1++; //timeout ; début du comptage
if (LW1>=3) //attend la durée de 3 exécutions de macro
{
LW1=0; //remise à zéro
LB0=0; //envoie l'indicateur de remise à zéro ; envoi au prochain passage
}
return; //sort directement
}
else //réception correcte
{
LW400=Mdata[0]&0xff; //traitement des données reçues
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
LB0=0; //traitement terminé ; envoi au prochain passage
PUTCHARS(0,Pdata,0); //vide le tampon
}
}
}
```

<img src="../../macro/environment.files/environment3382.png" width="130" />

Le nom et l'adresse des variables sont les mêmes dans la fenêtre de compilation.
