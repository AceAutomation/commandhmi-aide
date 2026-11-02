# Receptvoorbeeld

Het volgende voorbeeld toont de instelling en weergave van een recept.

1\. **Een recept aanmaken**

Klik in de projectbeheerder met de rechtermuisknop op “Recept”, zoals in afbeelding 1:

<img src="../../case/formula-case.files/formula-case168.png" width="284" />

Afbeelding 11 Recept aanmaken

Dubbelklik om het recept te openen, zoals in afbeelding 2:

<img src="../../case/formula-case.files/formula-case254.png" width="514" />

Afbeelding 12 Algemene instellingen van het recept

Zet de receptlengte op 4: elk recept bevat 4 gegevens. Het totaal is 10, dus 10 recepten. Stel het schrijfadres van het recept in de PLC in op D50 en kies positief geheel getal van 16 bits; het recept wordt naar de registers D50, D51, D52 en D53 geschreven. De leesinstellingen zijn gelijk aan die van het schrijfadres.

2\. **Gegevenselementen van het recept instellen:**

<img src="../../case/formula-case.files/formula-case637.png" width="511" />

Afbeelding 13 Gegevenselementen van het recept

Klik na het instellen van de receptnaam op “OK”. Gebruik het object numerieke invoer/weergave om de receptgegevens op het touchscreen te tonen. Kies het interne adres RWI0 voor de numerieke invoer/weergave: de ingevoerde en getoonde waarde is het receptnummer. RWI0 geeft het receptnummer aan; de waarde 2 betekent recept 2, enz. Gebruik numerieke invoer/weergaven om de gegevens van D50 tot D53 te tonen. Gebruik de functies van de “Functieknop” om een recept op te slaan of te lezen. Zie “Functieknop”.

<img src="../../case/formula-case.files/formula-case1276.png" width="663" />

Afbeelding 14 Object “Numerieke invoer/weergave” voor het receptgegeven D50

Stel het object numerieke invoer/weergave in en plaats het op het scherm:

<img src="../../case/formula-case.files/formula-case1422.png" width="746" />

Afbeelding 15 Scherm met receptweergave

Receptparameters kunnen met numerieke invoer/weergave worden gewijzigd; met functieknoppen kunnen recepten worden bekeken, gelezen en geschreven.
