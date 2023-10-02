# Configuration des touches Model2

Lorsque la configuration automatique des contrôleurs n'est pas compatible avec votre manette ou si vous désirez modifier l'assignation des touches de votre manette, il est possible de créer une configuration personnalisée pour chaque jeu.

Voilà comment procéder.

### ÉTAPE 1 : Création d'une configuration pour le jeu

Par défaut, RetroBat force l'émulateur à utiliser les pilotes XINPUT driver, toutefois, si vous utilisez une manette qui n'est pas compatible avec le protocole XINPUT, vous devrez sélectionner le pilote DINPUT dans les options avancées du système :\


<div align="left">

<figure><img src="https://i.imgur.com/ZjWHF7p.png" alt=""><figcaption></figcaption></figure>

</div>

Démarrer ensuite le jeu depuis RetroBat.

Le jeu chargé, presser ALT + ENTREE sur votre clavier pour quitter le mode plein-écran et afficher le menu de l'émulateur:

<div align="left">

<figure><img src="https://i.imgur.com/MdPZYlG.png" alt=""><figcaption></figcaption></figure>

</div>

Ouvrir le menu **Game > Configure Controls**

<div align="left">

<figure><img src="https://i.imgur.com/Zklxxw2.png" alt=""><figcaption></figcaption></figure>

</div>

Dans l'écran suivant, effectuer la configuration souhaitée:

<div align="left">

<figure><img src="https://i.imgur.com/mkomNgQ.png" alt=""><figcaption></figcaption></figure>

</div>

Une fois terminé : fermer la fenêtre et quitter l'émulateur.

Le fichier de configuration est sauvegardé dans le dossier `\emulators\m2emulator\CFG`:

<div align="left">

<figure><img src="https://i.imgur.com/VzxUIcv.png" alt=""><figcaption></figcaption></figure>

</div>

### ÉTAPE 2 : copier le fichier de configuration dans le répertoire de destination

Selon le pilote sélectionné lors de la configuration (DINPUT ou XINPUT), le fichier de configuration généré à l'étape précédente doit être copié dans l'un des dossiers suivants:

* `\emulators\m2emulator\templatescfg\dinput` - pour le pilote dinput
* `\emulators\m2emulator\templatescfg\xinput` - pour le pilote xinput

<div align="left">

<figure><img src="https://i.imgur.com/1OhA1pS.png" alt=""><figcaption></figcaption></figure>

</div>

{% hint style="info" %}
RetroBat fournit des fichiers par défaut compatibles avec les manettes XInput ou les manettes Playstation 4 et 5 pour le pilote dinput, vous pouvez effacer les fichiers fournis par défaut avec votre propre fichier.
{% endhint %}

### Activer le paramétrage pour utiliser le fichier créé

Dès lors le fichier placé dans le bon dossier, lancer RetroBat et ouvrir le menu des options avancées du système model2:

<div align="left">

<figure><img src="https://i.imgur.com/OrvL14b.png" alt=""><figcaption></figcaption></figure>

</div>

Aller dans CONTROLS et définir le paramètre "**TYPE OF CONFIGURATION**" à la valeur "**TEMPLATES**":

<div align="left">

<figure><img src="https://i.imgur.com/Peg2hoI.png" alt=""><figcaption></figcaption></figure>

</div>

RetroBat affecte désormais le fichier précédemment copié au lancement du jeu.
