# Een eenvoudig scriptvoorbeeld

Maak een nieuw project aan en kies het juiste HMI-model. De scriptmodule voert de volgende eenvoudige rekenfuncties uit: het script Init initialiseert de numerieke invoerobjecten met de elementen van de array char source \[4\] = {2, 3, 4, 5}; via de numerieke invoerobjecten worden externe gegevens ingevoerd; met de knop “=” wordt het script ADDSUM uitgevoerd en het resultaat in een object getoond.

Werkwijze:

**Stap 1: &lt;Nieuw script aanmaken&gt;**

Klik links in de werkbalk op de snelknop “Scripteditor”; er verschijnt een dialoogvenster.

**Stap 2: &lt;Het script Init aanmaken&gt;**

Klik in de scripteditor op de knop <img src="../../macro/example.files/example866.png" width="25" />; er verschijnt een nieuw script in de lijst “Niet opgeslagen”, zoals in afbeelding 5-7. Wijzig de naam van het script in het veld “Script” en bewerk de broncode in het bewerkingsvenster, zoals in afbeelding 5-8

<img src="../../macro/example.files/example1100.png" width="886" />

Afbeelding 5-7      Nieuw script

<img src="../../macro/example.files/example1126.png" width="1087" />

Afbeelding 5-8 Script Init bewerken

<img src="../../macro/example.files/example1156.png" width="130" />

Scriptnamen mogen alleen bestaan uit cijfers (0-9), Engelse letters (a-z, A-Z) en het onderstrepingsteken (\_). Voer de volgende inhoud in, zoals in afbeelding 5-9:

**Stap 3: &lt;Variabelen instellen&gt;**

Leg in het venster van afbeelding 5-9 de eigenschappen vast, zoals naam en type van de variabelen. Dubbelklik in het venster “Variabeleninstellingen” of kies met de rechtermuisknop “Nieuwe variabele” om het dialoogvenster van afbeelding 5-10 te openen, waarin u de externe variabelen instelt.

<img src="../../macro/example.files/example1677.png" width="499" />

Afbeelding 5-9 Tabblad Scriptcode

Naam: voer achtereenvolgens LW0, LW1, LW2, LW3 in als variabelenaam;

Gegevenstype: 16-bits geheel getal;

Lezen/schrijven: kies lezen en schrijven;

De adressen zijn: LW0 = 0, LW1 = 1, LW2 = 2, LW3 = 3;

Het resultaat van de instellingen staat in afbeelding 5-10.

<img src="../../macro/example.files/example1981.png" width="843" />

Afbeelding 5-10     Variabeleninstellingen

**Stap 4: &lt;Het bronbestand compileren&gt;**

Compileer na de stappen hierboven: klik op de compileerknop zoals in afbeelding 5-11; het script wordt automatisch opgeslagen, gecompileerd, gelinkt en op fouten gecontroleerd.

<img src="../../macro/example.files/example2223.png" width="800" />

Afbeelding 5-11    Uitvoer van informatie

Toont het uitvoervenster “0 errors! Compile successfully”, dan is het script aangemaakt en automatisch toegevoegd aan de lijst met gecompileerde scripts; anders verschijnt een foutmelding en komt het script in de lijst met mislukte compilaties. De gebruiker past het script aan tot het compileren lukt.

**Stap 5: &lt;Het script ADDSUM aanmaken&gt;**

Volg stap 2 - 4 om het script ADDSUM aan te maken, zoals in afbeelding 5-13

&lt;1&gt;: voer “ADDSUM” in als scriptnaam.

&lt;2&gt;: voer de omcirkelde inhoud in het codevenster in.

&lt;3&gt;: stel de eigenschappen van de variabelen in het venster “Variabeleninstellingen” in.

&lt;4&gt;: klik op de compileerknop.

<img src="../../macro/example.files/example2991.png" width="1168" />

Afbeelding 5-13    Het script ADDSUM aanmaken

**Stap 6: &lt;Objecten bewerken&gt;**

&lt;1&gt;. Plaats de objecten in het scherm van het project en geef ze de juiste grootte, zoals in afbeelding 5-14.

<img src="../../macro/example.files/example3164.png" width="558" />

Afbeelding 5-14    Indeling van de objecten

&lt;2&gt;. Stel de eigenschappen van de objecten in

Klik met de rechtermuisknop op het object “Numerieke invoer” en stel adres en eigenschappen van elk object in, zoals in afbeelding 5-15.

<img src="../../macro/example.files/example3375.png" width="660" />

Afbeelding 5-15    Eigenschappen numerieke invoer

Zorg dat de variabelenadressen LW0, LW1, LW2, LW3 en SumLW overeenkomen met het “schrijfadres” (afbeelding 5-15) van elk object. Klik op “OK” om de instellingen op te slaan.

&lt;3&gt;. Eigenschappen van de bit-knop instellen

<img src="../../macro/example.files/example3658.png" width="661" />

Afbeelding 5-16 (Eigenschappen bit-knop)

&lt;4&gt;. Eigenschappen van de timer

Kies het script Init en klik op “OK” om de instellingen op te slaan.

<img src="../../macro/example.files/example3792.png" width="661" />

Afbeelding 5-17    Eigenschappen timer

&lt;5&gt;. Kies de pagina “Label” -&gt; “Tekst” van de functieknop en voer het teken “+” in het tekstvak in, zoals in afbeelding 5-18.

<img src="../../macro/example.files/example3963.png" width="662" />

Afbeelding 5-18    Eigenschappen functieknop

**Stap 7: compileren en naar de HMI downloaden**

&lt;1&gt;: klik op het compileerpictogram.

<img src="../../macro/example.files/example4101.png" width="64" />

Afbeelding 5-19    Project compileren

&lt;2&gt;: kies “Downloaden (D) -&gt; USB-download (D)” en klik in het dialoogvenster op “Downloaden”. Herstart de HMI.

U kunt ook de snelknop Compileren en downloaden gebruiken.

**Stap 8: &lt;Resultaat testen&gt;**

Na het herstarten van de HMI verschijnt het volgende scherm (afbeelding 5-20).

Dat komt doordat bij het opstarten eerst het script Init door de timer wordt uitgevoerd.

<img src="../../macro/example.files/example4642.png" width="484" />

Afbeelding 5-20    Weergave van de beginwaarden

Voer bijvoorbeeld “31, 42, 53, 64” in de numerieke objecten in en klik op de knop “=” om het script ADDSUM uit te voeren; het resultaat is 190, zoals in afbeelding 5-21:

<img src="../../macro/example.files/example5009.png" width="481" />

Afbeelding 5-21     Weergave van het resultaat

Hiermee zijn het bewerken, compileren, downloaden en testen van het script en alle benodigde functies met succes afgerond.
