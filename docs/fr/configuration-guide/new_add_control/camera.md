# Caméra

L'objet Caméra permet d'enregistrer une vidéo ou de capturer des images depuis une caméra externe ; ses réglages se présentent ainsi :

![](../../../configuration-guide/new_add_control/camera.files/001.png)

USB : l'utilisation d'une caméra USB nécessite une IHM avec un système Linux 4.9.84 (001) ou supérieur ;

Caméra réseau : le flux d'entrée est au format RTSP ; par exemple, pour une caméra Hikvision, le format du flux est :

admin:xl123456@192.168.1.63:554/ch1/sub/av_stream;

Composition du flux : nom de compte : mot de passe@adresse IP : les quatre premiers éléments sont définis par l'utilisateur selon les paramètres de la caméra, la suite est fixée par la marque de la caméra.

Astuce !

Qu'il s'agisse d'une caméra USB ou réseau, une résolution trop élevée provoque du retard ou des saccades à l'écran : il faut alors réduire la résolution, la fréquence d'images, etc. du flux. Les caméras USB doivent fournir un flux vidéo mjpeg, les caméras réseau un flux encodé h264. Les caméras Hikvision ont été testées et validées ; pour les autres marques, il faut se fier aux essais réels.

Capture d'images : après activation de la capture déclenchée par adresse, un dossier « video » est créé sur la clé USB pour enregistrer les vidéos ou images capturées.

Format d'enregistrement : en mode image, au maximum 60 s d'images peuvent être enregistrées. Les caméras réseau enregistrent au format MP4, les caméras USB au format AVI.

Image : si le format d'enregistrement est Image, le fichier est enregistré au format JPG.

\[Démarrer/arrêter l'import\] : à 1, la caméra connectée est activée et le flux vidéo est importé ; à 0, la caméra est arrêtée et le flux fermé. \[Pause\] : met en pause l'affichage de la caméra, la vidéo continuant d'être transmise. Pour les adresses de contrôle, seule l'adresse de démarrage/arrêt est à définir ; l'adresse de pause est l'adresse de démarrage plus 1.

Par exemple, si l'adresse de démarrage/import est LW N, l'adresse de pause est LW N+1.

Pour la page d'affichage, voir le bouton « Bouton de bit ».
