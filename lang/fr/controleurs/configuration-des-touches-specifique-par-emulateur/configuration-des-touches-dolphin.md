# Configuration des touches Dolphin

La Gamecube et la Wii sont connus pour avoir une disposition de touches très spéciale, qui varie beaucoup d'un jeu à un autre.

Cela crée une situation complexe lorsqu'il s'agit de paramétrer les touches de l'émulateur.

Le guide suivant vous aidera à mettre en place et à utiliser une disposition de touches spécifique à un jeu dans l'émulateur Dolphin.

{% hint style="info" %}
Toutes les informations ci-dessous proviennent du wiki Dolphin :

[https://wiki.dolphin-emu.org/index.php?title=GameINI\_(Controller\_Settings)](https://wiki.dolphin-emu.org/index.php?title=GameINI_\(Controller_Settings\))
{% endhint %}

### ÉTAPE 1 : Création d'un profil dans Dolphin

Lancez _Dolphin.exe_, l’exécutable se trouve dans le dossier `\emulators\dolphin-emu` de votre installation RetroBat.

Cliquer sur l'icône "Manettes" dans la barre supérieure, puis sélectionner "Configurer" (choisir le système correspondant au jeu, cela fonctionne aussi bien pour Gamecube que pour Wii)

<div align="left"><figure><img src="https://i.imgur.com/ArzPI8J.png" alt=""><figcaption></figcaption></figure></div>

A la page suivante, configurer comme souhaité.

Une fois paramétré, renseigner un nom de profil, puis cliquer sur le bouton "Sauver".&#x20;

<div align="left"><figure><img src="https://i.imgur.com/aRFdvMe.png" alt=""><figcaption></figcaption></figure></div>

### ÉTAPE 2 : Assigner le profil au jeu

Fermer le menu de configuration des touches.

Depuis la liste des jeux, faire un clic-droit sur le jeu auquel appliquer le profil spécifique, et choisir "Propriétés"

<div align="left"><figure><img src="https://i.imgur.com/gK8pR96.png" alt=""><figcaption></figcaption></figure></div>

Sur l'écran suivant, choisir l'éditeur, et dans la section "User Config", spécifier le profil à utiliser

<div align="left"><figure><img src="https://i.imgur.com/nXUxwE9.png" alt=""><figcaption></figcaption></figure></div>

Renseigner le code suivant :

```
[Controls]
 %ControllerType% = %ProfileName%
```

Pour le %ControllerType%, les options suivantes peuvent être utilisés :

* PadProfile1 à PadProfile4 : pour les manettes Gamecube 1 à 4
* WiimoteProfile1 à WiimoteProfile4 : pour les manettes Wiimotes 1 à 4

%ProfileName% doit être égal au profil crée à l'étape 1 de ce guide.<br>

Cliquer sur "Fermer".

Le profil sauvegardé sera utilisé chaque fois que le jeu est démarré.



#### NB : Emplacement des fichiers de profils

Les profiles sauvegardés sont stockés dans le répertoire`\emulators\dolphin-emu\User\Config\Profiles` de votre installation RetroBat :

<div align="left"><figure><img src="https://i.imgur.com/r72aRwA.png" alt=""><figcaption></figcaption></figure></div>
