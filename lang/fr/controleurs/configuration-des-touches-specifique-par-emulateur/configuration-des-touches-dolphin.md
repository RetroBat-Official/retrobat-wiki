# Configuration des touches Dolphin

La Gamecube et la Wii sont connus pour avoir une disposition de touches très spéciale, qui varie beaucoup d'un jeu à un autre.

Cela crée une situation complexe lorsqu'il s'agit de paramétrer les touches de l'émulateur.

Le guide suivant vous aidera à comprendre et à mettre en place et à utiliser une disposition de touches spécifique à un jeu dans l'émulateur Dolphin.

{% hint style="info" %}
Toutes les informations ci-dessous proviennent du wiki Dolphin :

[https://wiki.dolphin-emu.org/index.php?title=GameINI\_(Controller\_Settings)](https://wiki.dolphin-emu.org/index.php?title=GameINI_\(Controller_Settings\))
{% endhint %}

## Utiliser l'autoconfiguration RetroBat

La plupart des paramètres de configuration des manettes sont gérés automatiquement par RetroBat. Voici quelques précisions concernant les consoles GameCube et Wii.

### GameCube

RetroBat propose plusieurs configurations de boutons pour la GameCube ; ces profils déterminent l'emplacement des boutons sur votre manette physique.

L'option est disponible dans le menu **CONFIGURATION AVANCÉE DU SYSTÈME > CONTRÔLES** :

<figure><img src="../../.gitbook/assets/image (89).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Vous trouverez plus d'informations concernant les profiles sur [la page Gamecube](../../systemes-and-emulateurs/supported-game-systems/consoles-de-jeu/nintendo-consoles-de-jeu/gamecube.md#creation-dun-profil-de-controle-specifique-pour-un-jeu).
{% endhint %}

Outre les profils de boutons, RetroBat propose également une option permettant de modifier le type de manette :

<div align="left"><figure><img src="../../.gitbook/assets/image (90).png" alt=""><figcaption></figcaption></figure></div>

Cela modifiera automatiquement le type de manette connectée à l'émulateur Dolphin :

<div align="left"><figure><img src="../../.gitbook/assets/image (83).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Vous pouvez trouver plus d'informations au sujet de l'adaptateur Gamecube [sur cette page](../../systemes-and-emulateurs/supported-game-systems/consoles-de-jeu/nintendo-consoles-de-jeu/gamecube.md#utilisation-dun-adaptateur-gamecube).
{% endhint %}

### Wii

RetroBat propose plusieurs configurations de touches pour les Wiimotes émulées ; ces profils déterminent la manière dont votre manette est mappée sur la manette Wii d'origine (Wiimote ou manette classique).

<div align="left"><figure><img src="../../.gitbook/assets/image (91).png" alt=""><figcaption></figcaption></figure></div>

Vous pouvez trouver plus d'informations [ici](../../systemes-and-emulateurs/supported-game-systems/consoles-de-jeu/nintendo-consoles-de-jeu/wii.md#wiimote-emulee).

Certains jeux Wii étaient également compatibles avec la manette GameCube. Pour activer l'émulation de la manette GameCube sur Wii, activez l'option dans **CONFIGURATION AVANCÉE DU SYSTÈME > CONTRÔLES** :

<div align="left"><figure><img src="../../.gitbook/assets/image (92).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Cela permettra d'utiliser les mêmes options que pour les manettes Gamecube, y compris les configurations Gamecube et l'utilisation d'une manette de la console originale.
{% endhint %}

## Utilisation d'une manette de la console originale

### Gamecube

RetroBat est fourni avec un fichier nommé "**GCControllers.json**" situé dans le répertoire `\system\resources\inputmapping` de votre installation RetroBat :

<div align="left"><figure><img src="../../.gitbook/assets/image (86).png" alt=""><figcaption></figcaption></figure></div>

Ce fichier permet de configurer automatiquement une manette spécifique, en fonction de son GUID, dans l'émulateur Dolphin.

L'exemple ci-dessus concerne les adaptateurs Mayflash GC 2 Player ; les différentes valeurs à indiquer dans le fichier sont les suivantes :

* **Emulator :** dolphin (le fichier peut également être utilisé avec le core libretro)
* **Name** : pour information seulement
* **Guid**: permet à RetroBat d'activer la configuration spécifique en fonction de la manette connectée (le GUID SDL de la manette se trouve dans le fichier es\_input.cfg ou dans le fichier emulatorlauncher.log après le lancement d'un jeu). Il est possible de saisir plusieurs GUID si une manette comporte plusieurs versions.
* **Driver** : peut être utilisé pour forcer le pilote Dolphin à utiliser pour la manette
* **Mapping**: le mappage à définir dans le fichier `GCPadNew.ini` , pour chaque bouton. Pour connaître le mappage de la manette, effectuez la configuration manuellement en lançant dolphin.exe, fermez Dolphin, puis ouvrez le fichier GCPadNew.ini.
* **HotkeyMapping** : le mappage des raccourci pour le contrôleur (modifiera le fichier `Hotkeys.ini`)
* **ControllerInfo** : peut être utilisé pour déterminer si le paramètre doit être activé dans le menu RetroBat :

<figure><img src="../../.gitbook/assets/image (94).png" alt=""><figcaption></figcaption></figure>

### Wii

RetroBat permet de configurer Dolphin pour qu'il utilise de véritables Wiimotes. La meilleure façon d'utiliser celles-ci avec Dolphin est d'utiliser le Mayflash Dolphin ; toutefois, il est également possible de le faire en synchronisant les Wiimotes avec Windows via Bluetooth et en utilisant une barre infrarouge standard.

Si vous utilisez de vrai Wiimotes, alors rendez-vous dans le menu **CONFIGURATION AVANCÉE DU SYSTÈME > CONTRÔLES** pour activer la fonctionnalité :

<figure><img src="../../.gitbook/assets/image (93).png" alt=""><figcaption></figcaption></figure>

## Utiliser un profil personnalisé de touches

La définition d'un profil de saisie personnalisé contournera complètement le mécanisme de configuration automatique de RetroBat.

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
