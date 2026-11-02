# FAQ et solutions

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>       <strong>N°</strong></p></td>
<td colspan="2"><p><strong>Symptôme</strong></p></td>
<td><p><strong>Cause</strong></p></td>
<td><p><strong>Solution</strong></p></td>
</tr>
<tr class="even">
<td rowspan="6"><p><strong>Affichage</strong></p></td>
<td rowspan="5"><p>Écran noir</p></td>
<td rowspan="3"><p>Écran noir dès la mise sous tension</p></td>
<td><p>Problème d'alimentation</p></td>
<td><p>1、Vérifiez le raccordement de l'alimentation ; 2、Vérifiez le type d'alimentation ; changez-la si ce n'est pas une alimentation 24 V CC (±20 %) indépendante.</p></td>
</tr>
<tr class="odd">
<td><p>Erreur dans le projet, par exemple mauvaise utilisation d'une macro : pointeur nul, pointeur non initialisé, dépassement de tableau, division par 0.</p></td>
<td><p>Mettez le commutateur DIP 2 sur ON et rechargez un projet simple pour tester ; si une macro fonctionne mal, déboguez-la et corrigez sa programmation.</p></td>
</tr>
<tr class="even">
<td><p>Panne de l'unité principale : nappe LCD corrodée, quartz défectueux, etc.</p></td>
<td><p>Contactez le service après-vente pour une réparation en atelier.</p></td>
</tr>
<tr class="odd">
<td rowspan="2"><p>Écran noir soudain en fonctionnement normal ; ou écran noir intermittent, blocage</p></td>
<td><p>Problème d'alimentation</p></td>
<td><p>Vérifiez le câble d'alimentation et l'alimentation.</p></td>
</tr>
<tr class="even">
<td><p>Panne de l'unité principale</p></td>
<td><p>Contactez le service après-vente pour une réparation en atelier.</p></td>
</tr>
<tr class="odd">
<td colspan="2"><p>Lignes verticales ou horizontales à l'écran</p></td>
<td><p>Défaut du LCD</p></td>
<td><p>Si les lignes apparaissent sur tous les écrans, contactez le service après-vente pour une réparation en atelier.</p></td>
</tr>
<tr class="even">
<td rowspan="4"><p><strong>Tactile</strong></p></td>
<td colspan="2" rowspan="2"><p>Réaction lente au toucher, objets difficiles à actionner</p></td>
<td><p>Problème d'installation</p></td>
<td><p>1. Vérifiez que la découpe n'est pas trop petite au point de comprimer l'IHM ; sinon, refaites-la aux bonnes dimensions ; 2. Vérifiez que les vis de fixation ne sont pas trop serrées et répartissez l'effort sur les quatre coins de façon aussi homogène que possible.</p></td>
</tr>
<tr class="odd">
<td><p>Projet mal conçu</p></td>
<td><p>Trop d'informations, de macros en arrière-plan, de variables et d'objets dans un écran ; modifiez le programme et répartissez raisonnablement les objets et les écrans.</p></td>
</tr>
<tr class="even">
<td colspan="2"><p>Toucher inopérant</p></td>
<td><p>Étalonnage des coordonnées ou dalle tactile endommagée</p></td>
<td><p>1. Mettez le commutateur DIP 1 sur ON pour étalonner les coordonnées ;</p>
<p>2. <span id="OLE_LINK4"></span><span id="OLE_LINK3"></span>Si cela ne suffit pas, contactez le service après-vente pour une réparation en atelier.</p></td>
</tr>
<tr class="odd">
<td colspan="2"><p>Saisie décalée (sur le clavier, on appuie sur A et X ou autre s'affiche)</p></td>
<td><p>Défaut de la dalle tactile</p></td>
<td><p>Contactez le service après-vente pour une réparation en atelier.</p></td>
</tr>
<tr class="even">
<td rowspan="9"><p><strong>Défaut de communication</strong></p></td>
<td rowspan="6"><p>Communication interrompue entre l'IHM et l'automate</p></td>
<td rowspan="3"><p>Aucune communication</p></td>
<td><p>Défaut de l'équipement communicant (automate, microcontrôleur, etc.)</p></td>
<td><p>Vérifiez le bon état du port de communication et la concordance des paramètres de communication.</p></td>
</tr>
<tr class="odd">
<td><p>Défaut du port de communication de l'IHM</p></td>
<td><p>Contactez le service après-vente pour une réparation en atelier.</p></td>
</tr>
<tr class="even">
<td><p>Câble de communication déconnecté</p></td>
<td><p>Utilisez si possible le câble spécifique CommandHMI.</p></td>
</tr>
<tr class="odd">
<td rowspan="3"><p>Communication interrompue après un certain temps de fonctionnement normal</p></td>
<td><p>Connexions du câble de communication corrodées ou oxydées après une longue utilisation.</p></td>
<td><p>Remplacez ou ressoudez le câble de communication.</p></td>
</tr>
<tr class="even">
<td><p>Perturbations de l'environnement</p></td>
<td><p>Éloignez ou blindez la source de perturbations ; utilisez un câble blindé ; soignez la mise à la terre</p></td>
</tr>
<tr class="odd">
<td><p>Panne de l'unité principale de l'IHM (champ magnétique ou courant intense, foudre sur site)</p></td>
<td><p>Contactez le service après-vente pour une réparation en atelier.</p></td>
</tr>
<tr class="even">
<td colspan="2" rowspan="3"><p>L'IHM ne se connecte pas au PC, téléchargement impossible.</p></td>
<td><p>Pilote USB mal installé sur le PC</p></td>
<td><p>Choisissez le pilote correspondant au système et réinstallez le pilote USB.</p></td>
</tr>
<tr class="odd">
<td><p>Taille et modèle d'IHM différents de l'IHM réelle.</p></td>
<td><p>Sélectionnez le bon modèle d'IHM dans le logiciel de configuration.</p></td>
</tr>
<tr class="even">
<td><p>Port de téléchargement de l'IHM endommagé</p></td>
<td><p>Contactez le service après-vente pour une réparation en atelier. (Vérification : reliez une autre IHM avec le même câble USB et le même PC ; si le téléchargement fonctionne, le défaut vient du port USB de l'IHM.)</p></td>
</tr>
<tr class="odd">
<td rowspan="3"><p><strong>Application</strong></p></td>
<td colspan="2"><p>Configuration inutilisable</p></td>
<td><p>Objet ou macro non valide dans la configuration</p></td>
<td><p>Corrigez la configuration</p></td>
</tr>
<tr class="even">
<td colspan="2"><p>Échec de compilation des macros</p></td>
<td><p>Répertoire d'installation de HM dans les variables d'environnement</p></td>
<td><p>Placez le répertoire d'installation de CommandHMI en tête dans les variables d'environnement.</p></td>
</tr>
<tr class="odd">
<td colspan="2"><p>Les simulations hors ligne et en ligne ne fonctionnent pas.</p></td>
<td><p>Logiciel lancé sans droits d'administrateur</p></td>
<td><p>Exécutez CommandHMI en tant qu'administrateur</p></td>
</tr>
</tbody>
</table>
