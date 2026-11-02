# Camera

Het cameraobject neemt video op of legt beelden vast van een externe camera; de objectpagina is als volgt:

![](../../../configuration-guide/new_add_control/camera.files/001.png)

USB: een via USB aangesloten camera vereist een HMI-systeem Linux 4.9.84 (001) of hoger;

Netwerkcamera: het invoerformaat van de stream is RTSP; het streamformaat van een Hikvision-camera is bijvoorbeeld:

admin:xl123456@192.168.1.63:554/ch1/sub/av_stream;

Opbouw van de stream: accountnaam: wachtwoord@IP-adres: de eerste vier onderdelen stelt de gebruiker in volgens de cameraparameters; de rest wordt door het cameramerk bepaald.

Tip!

Bij zowel USB- als netwerkcamera's leidt een te hoge resolutie tot vertraging of haperingen bij weergave op het touchscreen; verlaag dan resolutie, framerate enz. USB-camera's ondersteunen MJPEG-videostreams, netwerkcamera's moeten H.264-streams ondersteunen. Hikvision-camera's zijn getest en gevalideerd; test andere merken in de praktijk.

Beeldvastlegging: bij activering van de vastlegging via een adres wordt op de USB-stick een map “video” aangemaakt voor de vastgelegde video's of beelden.

Opnameformaat: bij videoformaat is de maximale opnameduur 60 s. Netwerkcamera's slaan video op in MP4, USB-camera's in AVI.

Beeld: bij beeldformaat wordt het bestand als JPG opgeslagen.

\[Import starten/stoppen\]: bij invoer 1 wordt de camera ingeschakeld en de videostream geïmporteerd; bij invoer 0 wordt de aangesloten camera uitgeschakeld en de stream gesloten. \[Pauzebesturing\]: pauzeert de weergave van de camerabeelden; de video wordt verder overgedragen. Bij het instellen van het besturingsadres hoeft alleen het start-/stopadres te worden opgegeven; het pauzeadres is het startadres plus 1.

Is het start-/importadres bijvoorbeeld LW N, dan is het pauzeadres LW N+1.

Zie voor de weergavepagina de knop “Positieschakelaar”.
