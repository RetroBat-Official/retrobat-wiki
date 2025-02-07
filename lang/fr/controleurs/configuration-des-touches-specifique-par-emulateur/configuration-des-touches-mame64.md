# Configuration des touches MAME64

L'émulateur MAME64 est compatible nativement avec des manettes XInput.\
\
Lors de l'utilisation d'un autre type de manette (ou simplement pour définir un paramétrage des touches spécifique), il est possible de créer une configuration personnalisée avec cet émulateur.

## ÉTAPE 0 : Préambule

Au lancement, MAME parcourt plusieurs dossiers pour définir la configuration à utiliser, l'ordre de priorité utilisé est le suivant (du moins prioritaire au plus prioritaire - cela signifie que le dernier fichier trouvé aura la priorité sur les autres):

1. Configuration native de l'émulateur
2. Fichier default.cfg dans le dossier `\bios\mame\cfg` (si existant)
3. Fichier spécifique au jeu dans le dossier `\bios\mame\cfg` (si existant - doit porter exactement le nom de la rom de jeu)
4. Fichier de configuration contrôleur situé dans `\saves\mame\ctrlr` selon la sélection faite par l'utilisateur depuis l'interface RetroBat

## ÉTAPE 1 : Création du fichier de configuration des touches dans MAME

Démarrer _mame.exe_, l’exécutable se trouve dans le répertoire `emulators\mame` de votre installation RetroBat.

Cliquer sur "General Settings":

<div align="left"><figure><img src="https://i.imgur.com/7FfrAyr.png" alt=""><figcaption></figcaption></figure></div>

Sélectionner "Input Assignments"

<div align="left"><figure><img src="https://i.imgur.com/P23EUU1.png" alt=""><figcaption></figcaption></figure></div>

Sélectionner les touches à assigner :

* La section "User Interface" vous permet de choisir les touches servant à la navigation dans les menus MAME
* Les sections Player X permettent d'assigner les touches qui seront utilisées dans les jeux pour les différents joueurs

<div align="left"><figure><img src="https://i.imgur.com/pgXcIQM.png" alt=""><figcaption></figcaption></figure></div>

Attribuer les touches comme désiré :

<div align="left"><figure><img src="https://i.imgur.com/kxVLMtw.png" alt=""><figcaption></figcaption></figure></div>

En utilisant les touches gauche et droite (ou les boutons), il est possible de rajouter une touche pour effectuer la même action, ou de réinitialiser le paramétrage de la touche.

<div align="left"><figure><img src="https://i.imgur.com/ubjsXry.png" alt=""><figcaption><p>Vous pouvez compléter...</p></figcaption></figure></div>

<div align="left"><figure><img src="https://i.imgur.com/6pGoFrF.png" alt=""><figcaption><p>Ou bien supprimer et réinitialiser</p></figcaption></figure></div>

Une fois le paramétrage effectué, revenir en arrière et cliquer sur "Save Settings" :

<div align="left"><figure><img src="https://i.imgur.com/pDLsvFJ.png" alt=""><figcaption></figcaption></figure></div>

Un fichier nommé "default.cfg" sera sauvegardé dans le répertoire`\emulators\mame\cfg`.

<div align="left"><figure><img src="https://i.imgur.com/PmZJO4I.png" alt=""><figcaption></figcaption></figure></div>



## ÉTAPE 2 : Utiliser le fichier cfg

Ouvrir le fichier default.cfg et vérifier le contenu :

<div align="left"><figure><img src="https://i.imgur.com/tYgSbfM.png" alt=""><figcaption></figcaption></figure></div>

Le fichier est au format xml, le paramétrage précédemment renseigné se situe dans la section \<input> du fichier.\
\
&#xNAN;_&#x44;ans l'exemple, la touche "Q" du clavier a été attribué à l'action "UI\_MENU" qui ouvre le menu MAME._

Enfin, déplacer le fichier default.cfg vers le dossier `\bios\mame\cfg` de votre installation : ce profil devient alors le profil par défaut.

## ÉTAPE 3 : Créer un profil contrôleur dédié

Procéder comme expliqué à l'étape 1, puis renommer le fichier selon l'une des valeurs ci-dessous :&#x20;

* custom1.cfg
* custom2.cfg
* ...
* custom8.cfg

Déplacer le fichier dans le répertoire `\saves\mame\ctrlr` de votre installation RetroBat :

<div align="left"><figure><img src="https://i.imgur.com/15wt2XH.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Il est également possible de réaliser le paramétrage des touches directement dans le fichier .cfg si vous vous sentez à l'aise avec la structure xml du document.\
\
D'autres informations concernant la structure du fichier se trouvent ici : \
[http://mirrors.arcadecontrols.com/easyemu/mameguidenew/mameguide-controlini.htm](http://mirrors.arcadecontrols.com/easyemu/mameguidenew/mameguide-controlini.htm)\
[https://docs.mamedev.org/advanced/ctrlr\_config.html](https://docs.mamedev.org/advanced/ctrlr_config.html)
{% endhint %}

## ÉTAPE 4 : Sélectionner le profil de touche depuis RetroBat

Depuis le [menu jeu](../../navigation/system-view-and-game-view.md#vue-jeux) MAME, appuyer sur SELECT pour ouvrir le menu [Options d'affichage](../../navigation/view-options.md) et sélectionner "CONFIGURATION AVANCÉE DU SYSTÈME"

<div align="left"><figure><img src="https://i.imgur.com/6LP55Wp.png" alt=""><figcaption></figcaption></figure></div>

S'assurer que MAME64 soit défini comme émulateur par défaut et naviguer jusqu'au sous-menu CONTROLS :

<div align="left"><figure><img src="https://i.imgur.com/gC4dECi.png" alt=""><figcaption></figcaption></figure></div>

Sélectionner l'option "CONTROLLER PROFILE" et choisir dans la liste le profil correspondant au fichier que vous avez créé :

{% hint style="info" %}
RetroBat propose 8 profils personnalisés ainsi que la possibilité d'utiliser un fichier de profil par jeu.

Pour utiliser le profil par jeu, le nom du fichier doit correspondre au nom du jeu (sans l'extension), par exemple il faut appeler le fichier de configuration "wjammers.cfg" pour le jeu "wjammers.zip" (WindJammers).
{% endhint %}

<div align="left"><figure><img src="https://i.imgur.com/SzXa5UY.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
N’hésitez pas à partager les fichiers que vous avez créé avec l'équipe RetroBat si vous avez un profil général pouvant être partagé avec d'autres utilisateurs.
{% endhint %}
