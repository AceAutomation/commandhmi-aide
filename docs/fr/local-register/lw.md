# LW

LW

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>adresse</th>
<th>description</th>
<th>Notes</th>
<th>lecture/écriture</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>59010~59057</td>
<td>En mode étendu, désactive la communication avec le numéro de station indiqué. Stations 0~255,<br />
chaque adresse correspond à 16 numéros de station : 59010 correspond aux stations 0~15, etc. Si le bit X vaut 1, la communication avec la station X est autorisée ; s'il vaut 0,<br />
la communication avec la station X est coupée.</td>
<td>COM1: 59010~59025<br />
COM2: 59026~59041<br />
COM3: 59106~59121<br />
Ethernet: 59042~59057</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>59058~59105</td>
<td>Indication de l'état de communication par numéro de station, stations 0~255.<br />
chaque adresse correspond à 16 numéros de station : 59058 correspond aux stations 0~15, etc. Si le bit X vaut 1,<br />
la communication avec cette station est en défaut ; s'il vaut 0, la communication est normale.</td>
<td>COM1: 59058~59073<br />
COM2: 59074~59089<br />
COM3: 59154~59169<br />
Ethernet: 59090~59105</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60000</td>
<td>heure locale : secondes</td>
<td>Code BCD, plage valide 0-59</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60001</td>
<td>heure locale</td>
<td>Code BCD, plage valide 0-59</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60002</td>
<td>heure locale</td>
<td>Code BCD, plage valide 0-23</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60003</td>
<td>heure locale : jour</td>
<td>Code BCD, plage valide 1-31</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60004</td>
<td>heure locale : mois</td>
<td>Code BCD, plage valide 1-12</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60005</td>
<td>heure locale : année</td>
<td>Code BCD, plage valide 0-9999</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60006</td>
<td>heure locale : jour de la semaine</td>
<td>Code BCD, plage valide 1-7</td>
<td>R</td>
</tr>
<tr class="even">
<td>60007</td>
<td>durée de fonctionnement du système</td>
<td>Durée de fonctionnement du système, en heures</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60008</td>
<td>durée de fonctionnement du système</td>
<td>Temps écoulé depuis le démarrage, en minutes</td>
<td>R</td>
</tr>
<tr class="even">
<td>60009</td>
<td>Durée de fonctionnement en secondes</td>
<td>Temps écoulé depuis le démarrage, en secondes</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60010</td>
<td>Numéro de l'écran courant</td>
<td>Numéro de l'écran affiché</td>
<td>R</td>
</tr>
<tr class="even">
<td>60012</td>
<td>langue courante</td>
<td>Numéro de la langue correspondante</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60013</td>
<td>Limite haute de saisie numérique</td>
<td>À l'ouverture du clavier personnalisé, affiche en ASCII la limite haute autorisée</td>
<td>R</td>
</tr>
<tr class="even">
<td>60023</td>
<td>Limite basse de saisie numérique</td>
<td>À l'ouverture du clavier personnalisé, affiche en ASCII la limite basse autorisée</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60033</td>
<td>Données saisies affichées sur le clavier</td>
<td>Données saisies affichées sur le clavier (caractères tapés), affichage ASCII</td>
<td>R</td>
</tr>
<tr class="even">
<td>60065</td>
<td>Utilisateur connecté</td>
<td>numéro de l'utilisateur courant</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60066</td>
<td>Mot de passe de l'utilisateur connecté</td>
<td>Affiche le mot de passe de l'utilisateur courant, 16 caractères, affichage ASCII</td>
<td>R</td>
</tr>
<tr class="even">
<td>60074</td>
<td>Nom de l'utilisateur connecté</td>
<td>Affiche le nom de l'utilisateur courant, 32 caractères, affichage ASCII</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60090</td>
<td>Utilisateur 1 activé</td>
<td>0 - désactivé, 1 - activé</td>
<td>R</td>
</tr>
<tr class="even">
<td>60091</td>
<td>Utilisateur 2 activé</td>
<td>0 - désactivé, 1 - activé</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60092</td>
<td>Utilisateur 3 activé</td>
<td>0 - désactivé, 1 - activé</td>
<td>R</td>
</tr>
<tr class="even">
<td>60093</td>
<td>Utilisateur 4 activé</td>
<td>0 - désactivé, 1 - activé</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60094</td>
<td>Utilisateur 5 activé</td>
<td>0 - désactivé, 1 - activé</td>
<td>R</td>
</tr>
<tr class="even">
<td>60095</td>
<td>Utilisateur 6 activé</td>
<td>0 - désactivé, 1 - activé</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60096</td>
<td>Utilisateur 7 activé</td>
<td>0 - désactivé, 1 - activé</td>
<td>R</td>
</tr>
<tr class="even">
<td>60097</td>
<td>Utilisateur 8 activé</td>
<td>0 - désactivé, 1 - activé</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60098</td>
<td>Nom de l'utilisateur 1</td>
<td>32 caractères, affichage ASCII</td>
<td>R</td>
</tr>
<tr class="even">
<td>60114</td>
<td>Nom de l'utilisateur 2</td>
<td>32 caractères, affichage ASCII</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60130</td>
<td>Nom de l'utilisateur 3</td>
<td>32 caractères, affichage ASCII</td>
<td>R</td>
</tr>
<tr class="even">
<td>60146</td>
<td>Nom de l'utilisateur 4</td>
<td>32 caractères, affichage ASCII</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60162</td>
<td>Nom de l'utilisateur 5</td>
<td>32 caractères, affichage ASCII</td>
<td>R</td>
</tr>
<tr class="even">
<td>60178</td>
<td>Nom de l'utilisateur 6</td>
<td>32 caractères, affichage ASCII</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60194</td>
<td>Nom de l'utilisateur 7</td>
<td>32 caractères, affichage ASCII</td>
<td>R</td>
</tr>
<tr class="even">
<td>60210</td>
<td>Nom de l'utilisateur 8</td>
<td>32 caractères, affichage ASCII</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60226</td>
<td>Mot de passe de l'utilisateur 1</td>
<td>16 caractères, affichage ASCII</td>
<td>R</td>
</tr>
<tr class="even">
<td>60234</td>
<td>Mot de passe de l'utilisateur 2</td>
<td>16 caractères, affichage ASCII</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60242</td>
<td>Mot de passe de l'utilisateur 3</td>
<td>16 caractères, affichage ASCII</td>
<td>R</td>
</tr>
<tr class="even">
<td>60250</td>
<td>Mot de passe de l'utilisateur 4</td>
<td>16 caractères, affichage ASCII</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60258</td>
<td>Mot de passe de l'utilisateur 5</td>
<td>16 caractères, affichage ASCII</td>
<td>R</td>
</tr>
<tr class="even">
<td>60266</td>
<td>Mot de passe de l'utilisateur 6</td>
<td>16 caractères, affichage ASCII</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60274</td>
<td>Mot de passe de l'utilisateur 7</td>
<td>16 caractères, affichage ASCII</td>
<td>R</td>
</tr>
<tr class="even">
<td>60282</td>
<td>Mot de passe de l'utilisateur 8</td>
<td>16 caractères, affichage ASCII</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60290</td>
<td>délai de l'économiseur d'écran</td>
<td>Affiche le délai de l'économiseur d'écran défini dans la configuration, plage 0~60</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60291</td>
<td>Période de clignotement des voyants</td>
<td>Période de clignotement des voyants, minimum 0,1, en s</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60292</td>
<td>Position X au toucher</td>
<td>Coordonnée X du point touché</td>
<td>R</td>
</tr>
<tr class="even">
<td>60293</td>
<td>Position Y au toucher</td>
<td>Coordonnée Y du point touché</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60294</td>
<td>Position X au relâchement</td>
<td>Coordonnée X au relâchement du toucher</td>
<td>R</td>
</tr>
<tr class="even">
<td>60295</td>
<td>Position Y au relâchement</td>
<td>Coordonnée Y au relâchement du toucher</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60296</td>
<td>état du toucher</td>
<td>1-touché, 0-relâché</td>
<td>R</td>
</tr>
<tr class="even">
<td>60297</td>
<td>Parité de COM1</td>
<td>Paramètres de communication, parité : 0-NONE, 1-EVEN, 2-ODD</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60298</td>
<td>Vitesse de COM1</td>
<td>Paramètres de communication, vitesse : 0-1200, 1-2400, 2-4800, 3-9600, 4-19200, 5-38400, 6-57600, 7-115200</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60299</td>
<td>Bits de stop de COM1</td>
<td>Paramètres de communication, bits de stop : 0-1 bit, 1-2 bits</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60300</td>
<td>Longueur des données de COM1</td>
<td>Paramètres de communication, longueur des données : 0-7 bits, 1-8 bits</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60301</td>
<td>Adresse HMI de COM1</td>
<td>Paramètres de communication, adresse IHM</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60302</td>
<td>Adresse PLC de COM1</td>
<td>Paramètres de communication, adresse automate</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60303</td>
<td>COM1 : intervalle d'adresses automate consécutives</td>
<td>Longueur maximale d'adresses consécutives lues en une seule communication</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60304</td>
<td>COM1 : temps de communication</td>
<td>Délai de communication</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60305</td>
<td>COM1 : nombre de tentatives</td>
<td>Nombre de réémissions en cas de défaut de communication</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60306</td>
<td>COM1 : mode d'adressage</td>
<td>Mode d'adressage : 0-standard, 1-étendu</td>
<td>R</td>
</tr>
<tr class="even">
<td>60307</td>
<td>COM1 : timeout de communication</td>
<td>Règle le délai d'attente (timeout) de communication, en ms</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60308</td>
<td>COM1 : temps d'attente actuel de la communication</td>
<td>Temps d'attente actuel de la communication, en ms</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60309</td>
<td>COM1 : emplacement de l'IHM</td>
<td>0-local 1-distant</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60312</td>
<td>Parité de COM2</td>
<td>Paramètres de communication, parité : 0-NONE, 1-EVEN, 2-ODD</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60313</td>
<td>Vitesse de COM2</td>
<td>Paramètres de communication, vitesse : 0-1200, 1-2400, 2-4800, 3-9600, 4-19200, 5-38400, 6-57600, 7-115200</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60314</td>
<td>Bits de stop de COM2</td>
<td>Paramètres de communication, bits de stop : 0-1 bit, 1-2 bits</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60315</td>
<td>Longueur des données de COM2</td>
<td>Paramètres de communication, longueur des données : 0-7 bits, 1-8 bits</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60316</td>
<td>Adresse HMI de COM2</td>
<td>Paramètres de communication, adresse IHM</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60317</td>
<td>Adresse PLC de COM2</td>
<td>Paramètres de communication, adresse automate</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60318</td>
<td>COM2 : intervalle d'adresses automate consécutives</td>
<td>Longueur maximale d'adresses consécutives lues en une seule communication</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60319</td>
<td>COM2 : temps de communication</td>
<td>Délai de communication</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60320</td>
<td>COM2 : nombre de tentatives</td>
<td>Nombre de réémissions en cas de défaut de communication</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60321</td>
<td>COM2 : mode d'adressage</td>
<td>Mode d'adressage : 0-standard, 1-étendu</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60322</td>
<td>COM2 : timeout de communication</td>
<td>Règle le délai d'attente (timeout) de communication, en ms</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60323</td>
<td>COM2 : temps d'attente actuel de la communication</td>
<td>Temps d'attente actuel de la communication, en ms</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60324</td>
<td>COM2 : emplacement de l'IHM</td>
<td>0-local, 1-distant</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61270</td>
<td>Parité de COM3</td>
<td>Paramètres de communication, parité : 0-NONE, 1-EVEN, 2-ODD</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61271</td>
<td>Vitesse de COM3</td>
<td>Paramètres de communication, vitesse : 0-1200, 1-2400, 2-4800, 3-9600, 4-19200, 5-38400, 6-57600, 7-115200</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61272</td>
<td>Bits de stop de COM3</td>
<td>Paramètres de communication, bits de stop : 0-1 bit, 1-2 bits</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61273</td>
<td>Longueur des données de COM3</td>
<td>Paramètres de communication, longueur des données : 0-7 bits, 1-8 bits</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61274</td>
<td>Adresse HMI de COM3</td>
<td>Paramètres de communication, adresse IHM</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61275</td>
<td>Adresse PLC de COM3</td>
<td>Paramètres de communication, adresse automate</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61276</td>
<td>COM3 : intervalle d'adresses automate consécutives</td>
<td>Longueur maximale d'adresses consécutives lues en une seule communication</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61277</td>
<td>COM3 : temps de communication</td>
<td>Délai de communication</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61278</td>
<td>COM3 : nombre de tentatives</td>
<td>Nombre de réémissions en cas de défaut de communication</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61279</td>
<td>COM3 : mode d'adressage</td>
<td>Mode d'adressage : 0-standard, 1-étendu</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61280</td>
<td>COM3 : timeout de communication</td>
<td>Règle le délai d'attente (timeout) de communication, en ms</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61281</td>
<td>COM3 : temps d'attente actuel de la communication</td>
<td>Temps d'attente actuel de la communication, en ms</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61282</td>
<td>COM3 : emplacement de l'IHM</td>
<td>0-local, 1-distant</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60327</td>
<td>Nombre d'alarmes historiques</td>
<td>Nombre total d'alarmes historiques enregistrées</td>
<td>R/double mot</td>
</tr>
<tr class="even">
<td>60329</td>
<td>Nombre d'enregistrements historiques</td>
<td>Nombre total d'enregistrements de données historiques</td>
<td>R/double mot</td>
</tr>
<tr class="odd">
<td>60333</td>
<td>langue du clavier</td>
<td>1-clavier chinois, 0-clavier anglais, pour le clavier standard</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60334</td>
<td>Utilisation du processeur</td>
<td>Taux d'utilisation du processeur du système</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60335</td>
<td>Luminosité actuelle du rétroéclairage</td>
<td>Luminosité actuelle du rétroéclairage (140~450)</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60337</td>
<td>Date de création du projet : année</td>
<td>Année de création du fichier de projet courant</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60338</td>
<td>Date de création du projet : mois</td>
<td>Mois de création du fichier de projet courant</td>
<td>R</td>
</tr>
<tr class="even">
<td>60339</td>
<td>Date de création du projet : jour</td>
<td>Jour de création du fichier de projet courant</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60340</td>
<td>langue utilisateur courante</td>
<td>définit la langue courante</td>
<td>W</td>
</tr>
<tr class="even">
<td>60359</td>
<td>À 1, copie sur la clé USB les alarmes historiques de la plage de numéros indiquée</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60361</td>
<td>À 1, copie sur la clé USB les alarmes historiques de la plage de temps indiquée</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60363</td>
<td>Export des alarmes historiques : numéro de début</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60365</td>
<td>Export des alarmes historiques : numéro de fin</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60367</td>
<td>Export des alarmes historiques : heure de début</td>
<td>Longueur 6 mots : année, mois, jour, heure, minute et seconde.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60373</td>
<td>Export des alarmes historiques : heure de fin</td>
<td>Longueur 6 mots : année, mois, jour, heure, minute et seconde.</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60379</td>
<td>Nom du fichier d'export des alarmes historiques sur clé USB</td>
<td>longueur 22 caractères</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60408</td>
<td>Adresse de contrôle du groupe courant de données historiques</td>
<td>Indique le groupe courant de données historiques</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60409</td>
<td>À 1, copie sur la clé USB les données historiques de la plage de numéros indiquée</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60411</td>
<td>À 1, copie sur la clé USB les données historiques de la plage de temps indiquée</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60413</td>
<td>Export des données historiques : numéro de début</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60415</td>
<td>Export des données historiques : numéro de fin</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60417</td>
<td>Export des données historiques : heure de début</td>
<td>Longueur 6 mots : année, mois, jour, heure, minute et seconde.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60423</td>
<td>Export des données historiques : heure de fin</td>
<td>Longueur 6 mots : année, mois, jour, heure, minute et seconde.</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60429</td>
<td>Nom du fichier d'export des données historiques sur clé USB</td>
<td>longueur 24 caractères</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60441</td>
<td>Tampon de modification du mot de passe utilisateur 1</td>
<td>longueur 16 caractères, affichage ASCII</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60449</td>
<td>Activer la modification du mot de passe utilisateur 1</td>
<td>À 1, le mot de passe de l'utilisateur 1 est remplacé par celui du tampon, puis remise à zéro automatique.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60451</td>
<td>Tampon de modification du mot de passe utilisateur 2</td>
<td>longueur 16 caractères, affichage ASCII</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60459</td>
<td>Activer la modification du mot de passe utilisateur 2</td>
<td>À 1, le mot de passe de l'utilisateur 2 est remplacé par celui du tampon, puis remise à zéro automatique.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60461</td>
<td>Tampon de modification du mot de passe utilisateur 3</td>
<td>longueur 16 caractères, affichage ASCII</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60469</td>
<td>Activer la modification du mot de passe utilisateur 3</td>
<td>À 1, le mot de passe de l'utilisateur 3 est remplacé par celui du tampon, puis remise à zéro automatique.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60471</td>
<td>Tampon de modification du mot de passe utilisateur 4</td>
<td>longueur 16 caractères, affichage ASCII</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60479</td>
<td>Activer la modification du mot de passe utilisateur 4</td>
<td>À 1, le mot de passe de l'utilisateur 4 est remplacé par celui du tampon, puis remise à zéro automatique.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60481</td>
<td>Tampon de modification du mot de passe utilisateur 5</td>
<td>longueur 16 caractères, affichage ASCII</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60489</td>
<td>Activer la modification du mot de passe utilisateur 5</td>
<td>À 1, le mot de passe de l'utilisateur 5 est remplacé par celui du tampon, puis remise à zéro automatique.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60491</td>
<td>Tampon de modification du mot de passe utilisateur 6</td>
<td>longueur 16 caractères, affichage ASCII</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60499</td>
<td>Activer la modification du mot de passe utilisateur 6</td>
<td>À 1, le mot de passe de l'utilisateur 6 est remplacé par celui du tampon, puis remise à zéro automatique.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60501</td>
<td>Tampon de modification du mot de passe utilisateur 7</td>
<td>longueur 16 caractères, affichage ASCII</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60509</td>
<td>Activer la modification du mot de passe utilisateur 7</td>
<td>À 1, le mot de passe de l'utilisateur 7 est remplacé par celui du tampon, puis remise à zéro automatique.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60511</td>
<td>Tampon de modification du mot de passe utilisateur 8</td>
<td>longueur 16 caractères, affichage ASCII</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60519</td>
<td>Activer la modification du mot de passe utilisateur 8</td>
<td>À 1, le mot de passe de l'utilisateur 8 est remplacé par celui du tampon, puis remise à zéro automatique.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60520</td>
<td>Modèle d'IHM</td>
<td>40 caractères</td>
<td>R</td>
</tr>
<tr class="even">
<td>60540</td>
<td>version du bootloader</td>
<td>40 caractères</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60560</td>
<td>version du système d'exploitation</td>
<td>40 caractères</td>
<td>R</td>
</tr>
<tr class="even">
<td>60580</td>
<td>version du logiciel</td>
<td>40 caractères</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60600</td>
<td>Activation du journal des opérations</td>
<td>À 1, les opérations sont enregistrées</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60601</td>
<td>Nombre d'enregistrements d'opérations</td>
<td>Affiche le nombre actuel d'enregistrements d'opérations</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60602</td>
<td>Capture d'écran</td>
<td>À 1, effectue une capture d'écran, puis remise à zéro automatique</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60603</td>
<td>Emplacement des captures d'écran</td>
<td>0-clé USB</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60604</td>
<td>Activer la protection IHM</td>
<td>À 1, la protection IHM est utilisée</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60605</td>
<td>Nombre de niveaux de mot de passe de la protection IHM</td>
<td>Nombre de niveaux de mot de passe de la protection IHM, jusqu'à 15</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60606-60835</td>
<td>Réglage de la durée de validité de la protection IHM</td>
<td>60606-60628 : année, mois, jour, heure, minute, seconde et écran d'avertissement d'expiration du mot de passe de niveau 1, ainsi que le mot de passe de déverrouillage (16 caractères)<br />
60629-60651 : année, mois, jour, heure, minute, seconde et écran d'avertissement d'expiration du mot de passe de niveau 2, ainsi que le mot de passe de déverrouillage (16 caractères)<br />
60652-60674 : année, mois, jour, heure, minute, seconde et écran d'avertissement d'expiration du mot de passe de niveau 3, ainsi que le mot de passe de déverrouillage (16 caractères)<br />
60675-60697 : année, mois, jour, heure, minute, seconde et écran d'avertissement d'expiration du mot de passe de niveau 4, ainsi que le mot de passe de déverrouillage (16 caractères)<br />
60698-60720 : année, mois, jour, heure, minute, seconde et écran d'avertissement d'expiration du mot de passe de niveau 5, ainsi que le mot de passe de déverrouillage (16 caractères)<br />
60721-60743 : année, mois, jour, heure, minute, seconde et écran d'avertissement d'expiration du mot de passe de niveau 6, ainsi que le mot de passe de déverrouillage (16 caractères)<br />
60744-60766 : année, mois, jour, heure, minute, seconde et écran d'avertissement d'expiration du mot de passe de niveau 7, ainsi que le mot de passe de déverrouillage (16 caractères)<br />
60767-60789 : année, mois, jour, heure, minute, seconde et écran d'avertissement d'expiration du mot de passe de niveau 8, ainsi que le mot de passe de déverrouillage (16 caractères)<br />
60790-60812 : année, mois, jour, heure, minute, seconde et écran d'avertissement d'expiration du mot de passe de niveau 9, ainsi que le mot de passe de déverrouillage (16 caractères)<br />
60813-60835 : année, mois, jour, heure, minute, seconde et écran d'avertissement d'expiration du mot de passe de niveau 10, ainsi que le mot de passe de déverrouillage (16 caractères)</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>63000-63114</td>
<td>Réglage de la durée de validité de la protection IHM</td>
<td>63000-63022 : année, mois, jour, heure, minute, seconde et écran d'avertissement d'expiration du mot de passe de niveau 11, ainsi que le mot de passe de déverrouillage (16 caractères)<br />
63023-63045 : année, mois, jour, heure, minute, seconde et écran d'avertissement d'expiration du mot de passe de niveau 12, ainsi que le mot de passe de déverrouillage (16 caractères)<br />
63046-63068 : année, mois, jour, heure, minute, seconde et écran d'avertissement d'expiration du mot de passe de niveau 13, ainsi que le mot de passe de déverrouillage (16 caractères)<br />
63069-63091 : année, mois, jour, heure, minute, seconde et écran d'avertissement d'expiration du mot de passe de niveau 14, ainsi que le mot de passe de déverrouillage (16 caractères)<br />
63092-63114 : année, mois, jour, heure, minute, seconde et écran d'avertissement d'expiration du mot de passe de niveau 15, ainsi que le mot de passe de déverrouillage (16 caractères)</td>
<td></td>
</tr>
<tr class="odd">
<td>63115~63130</td>
<td>Adresse de saisie du mot de passe de niveau maximal</td>
<td>63115~63131 : adresse de modification du mot de passe de niveau maximal (16 caractères) ; après saisie, écrivez 1 dans LW63131 pour le rendre effectif</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>63131</td>
<td>Adresse de validation du mot de passe de niveau maximal</td>
<td>63115~63130 : après saisie du mot de passe de niveau maximal, écrivez 1 à cette adresse pour le rendre effectif</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60836</td>
<td>Enregistrement dans l'IHM</td>
<td>À 1, les réglages de protection IHM sont enregistrés dans l'IHM, puis remise à zéro automatique.</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60837</td>
<td>Réinitialiser la protection IHM</td>
<td>Ramène la protection IHM à son état initial. Les utilisateurs déjà déverrouillés doivent déverrouiller à nouveau</td>
<td>W</td>
</tr>
<tr class="odd">
<td>60997</td>
<td>Affectation de l'entrée USB.</td>
<td>Par défaut 0 : clavier ou souris USB. À 1 : lecteur de codes-barres</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60998</td>
<td>Caractère de fin de lecture du code 2D USB : 0-ENTER, 1-TAB+ENTER</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60999</td>
<td>Longueur du code lu par le lecteur 2D USB</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61000 - 61127</td>
<td>Stockage et utilisation du code 2D lu</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61128</td>
<td>Utilisation des paramètres d'imprimante</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61138</td>
<td>Import de recette : ID de la recette source</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61139</td>
<td>Import de recette : ID de la recette de destination</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61140</td>
<td>ID de la recette à effacer</td>
<td>-1 si la valeur initiale est affichée en entier 16 bits ; sinon 65535</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61141</td>
<td>Change le groupe de recettes courant pendant le fonctionnement de l'IHM</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61143</td>
<td>Numéro de groupe pour l'import/export des recettes sur clé USB</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61146</td>
<td>Numéro de la fenêtre à imprimer lors d'une impression déclenchée par registre</td>
<td>Saisissez le numéro de la fenêtre à imprimer, puis activez LB60175 pour lancer l'impression (remise à zéro automatique)</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>62020-62039</td>
<td>Nom de la recette courante</td>
<td>Objet d'affichage ASCII, codage Unicode, longueur 20 ; affiche le nom de la recette courante</td>
<td>R</td>
</tr>
<tr class="odd">
<td>62040</td>
<td>Choix du niveau utilisateur de connexion</td>
<td>Niveau utilisateur avec lequel se connecter ; correspond au niveau coché dans « Paramètres de l'écran tactile » → « Mots de passe utilisateur »</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>62041~62056</td>
<td>Adresse de saisie du mot de passe de connexion</td>
<td>Saisissez le mot de passe correspondant au niveau défini en 62040. Le mot de passe de niveau maximal déverrouille tous les niveaux (16 caractères) et termine la connexion.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>62057</td>
<td>Registre du nombre de prolongations de l'IHM</td>
<td>Si l'option de prolongation est cochée dans la protection IHM, ce registre modifie le nombre de prolongations ; valeur par défaut 1</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>63141~63146</td>
<td>Date d'expiration du mot de passe dynamique</td>
<td>Année, mois, jour, heure, minute, seconde : LW63141~63146, entier 16 bits ; après saisie de la date, activez LB60182 pour la rendre effective (remise à zéro automatique)</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>63147~63152</td>
<td>Adresse de la clé du mot de passe dynamique</td>
<td>Modifie la clé du mot de passe dynamique, adresse LW63147, type ASCII, longueur 6 ; activez LB60179 pour la rendre effective (remise à zéro automatique)</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>63153~63184</td>
<td>Modification du nom de recette</td>
<td>Objet de saisie ASCII, longueur 32 ; la modification devient effective avec LB60180</td>
<td>W</td>
</tr>
<tr class="odd">
<td>63186~63189</td>
<td>Adresse IP de l'équipement Ethernet</td>
<td>Adresse IP de l'équipement Ethernet en mode standard, entier 16 bits. Après réglage de l'IP, du port et du numéro de station, activez LB60178 pour les rendre effectifs</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>63190</td>
<td>Numéro de station de l'équipement Ethernet</td>
<td>Numéro de station de l'équipement Ethernet en mode standard, entier 16 bits. L'IP, le port et le numéro de station deviennent effectifs en activant LB60178</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>63191</td>
<td>Port de l'équipement Ethernet</td>
<td>Port de l'équipement Ethernet en mode standard, entier 16 bits. Après réglage de l'IP, du port et du numéro de station, activez LB60178 pour les rendre effectifs</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60838~60853</td>
<td>Nom de l'utilisateur connecté</td>
<td>Gestion des droits : affiche le nom de l'utilisateur connecté ; objet : affichage ASCII, longueur 32</td>
<td>R</td>
</tr>
<tr class="odd">
<td>63200~63215</td>
<td>Groupe de l'utilisateur connecté</td>
<td>Gestion des droits : affiche le groupe de l'utilisateur connecté (son premier groupe) ; objet : affichage ASCII, longueur 32</td>
<td>R</td>
</tr>
</tbody>
</table>
