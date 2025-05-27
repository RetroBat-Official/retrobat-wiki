# Configuration des touches RetroArch

Si la configuration des boutons ne vous convient pas pour un jeu ou un système complet géré par Retroarch (cores libretro), il est possible de créer une configuration spécifique pour un jeu.\
\
Voici comment procéder.\


Ouvrir RetroBat et démarrer un jeu pour lequel il est nécessaire de créer un paramétrage spécifique des touches.\
\
Une fois dans le jeu, appuyer sur les touches SELECT + ![](<../../.gitbook/assets/image (20).png>) simultanément pour ouvrir le menu  RetroArch, et choisir **Menu rapide**&#x20;

<div align="left"><figure><img src="https://i.imgur.com/w1hW2nI.png" alt=""><figcaption></figcaption></figure></div>

Dans le MENU RAPIDE, aller dans la section " **Touches** "

<div align="left"><figure><img src="https://i.imgur.com/thwZ08G.png" alt=""><figcaption></figcaption></figure></div>

Puis, sélectionner le port souhaité et paramétrer comme désiré :

<div align="left"><figure><img src="https://i.imgur.com/NBbomL3.png" alt=""><figcaption></figcaption></figure></div>

\
Dans cet exemple, la touche Analogique gauche haut du Retropad a été mappé sur la touche défini comme A dans RetroBat (qui correspond à la touche W sur le clavier) :

<div align="left"><figure><img src="https://i.imgur.com/4aS0EX9.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Il est à noter que vous ne pouvez reparamétrer que les touches qui ont été paramétrées par RetroBat dans Retroarch selon le contrôleur utilisé.

S'il est nécessaire d'ajouter des touches qui n'ont pas été au préalable configuré dans RetroBat, il faut alors également changer le paramétrage dans les réglages généraux de Retroarch.

[(cliquer ici pour en savoir plus)](configuration-des-touches-retroarch.md#principe-du-mapping-des-controleurs-de-retroarch)
{% endhint %}

Une fois le paramétrage fait, sortir et retourner sur le menu **TOUCHES**, puis sélectionner "_Gérer les fichiers de remappage_" :

<div align="left"><figure><img src="https://i.imgur.com/7gkrHwE.png" alt=""><figcaption></figcaption></figure></div>

Dans le sous-menu suivant, sauvegarder la configuration des touches pour le jeu (et il ne s'appliquera que pour celui-ci)

Une fois sauvegardé, le nouveau fichier de configuration sera utilisé au prochain lancement du jeu.

{% hint style="info" %}
Il n'est pas possible d'utiliser l'option "Sauvegarder le remappage pour le coeur", celui-ci étant utilisé par RetroBat, il sera automatiquement supprimé au démarrage suivant.
{% endhint %}

<div align="left"><figure><img src="https://i.imgur.com/UadIDbH.png" alt=""><figcaption></figcaption></figure></div>

## Modification des raccourcis (hotkeys)

Il est possible de modifier les raccourcis définis par RetroBat dans RetroArch, que ce soit pour les raccourcis manettes ou clavier, pour cela il est nécessaire de modifier des fichiers.

Les fichiers "modèles" sont situés dans le dossier `\system\resources\inputmapping\` de l'installation RetroBat:

<div align="left"><figure><img src="https://i.imgur.com/7arWxJQ.png" alt=""><figcaption></figcaption></figure></div>

Le fichier **retroarch\_controller\_hotkeys.yml** sera utilisé pour modifier l'assignation des raccourcis manette, et le fichier **retroarch\_kb\_hotkeys.yml** permet de modifier l'assignation des raccourcis clavier.

### Modifier les raccourcis manette

Copier le fichier **retroarch\_controller\_hotkeys.yml** vers le dossier `\user\inputmapping\` de l'installation RetroBat.

Ouvrir le fichier avec votre éditeur de texte préféré.

<div align="left"><figure><img src="https://i.imgur.com/56fMWG9.png" alt=""><figcaption></figcaption></figure></div>

Le fichier est au format yml, il est entièrement commenté par défaut.

La première chose à faire est de décommenter toutes les lignes de la section relative aux assignations, ainsi que le titre du "conteneur yml" de la section, pour cela il faut supprimer le caractère # de toutes les lignes à partir de la ligne `#default:` :

<div align="left"><figure><img src="https://i.imgur.com/sKvwNrH.png" alt=""><figcaption></figcaption></figure></div>

Dans cet exemple, nous allons remplacer les assignations des raccourcis avance rapide **(fast-forward)** et retour arrière **(rewind)** par les boutons R1 et L1, et déplacer les actions **disk\_eject** et **ai\_service** sur les boutons du pad directionnel:

pour cela, il faut assigner la fonction **rewind** à pageup (L1) et la fonction **hold\_fast\_forward** ) à pagedown (R1), puis enfin assigner les fonctions **disk\_eject\_toggle** et **ai\_service** aux boutons du pad directionnel (left & right):

<div align="left"><figure><img src="https://i.imgur.com/2ChUyvp.png" alt=""><figcaption></figcaption></figure></div>

Maintenant, sauvegarder le fichier:

<div align="left"><figure><img src="https://i.imgur.com/FuOpezx.png" alt=""><figcaption></figcaption></figure></div>

Au prochain lancement d'un jeu avec RetroArch, les boutons assignés aux raccourcis seront ceux définis dans le fichier:

<div align="left"><figure><img src="https://i.imgur.com/QngnHVJ.png" alt=""><figcaption></figcaption></figure></div>

Il est également possible d'assigner des raccourcis différents pour les différents coeurs libretro, dans l'exemple ci-dessous, l'assignation de l'avance rapide pour le coeur flycast est définie sur "toggle" au lieu de "hold":

<div align="left"><figure><img src="https://i.imgur.com/74WCTF9.png" alt=""><figcaption></figcaption></figure></div>

### Modifier les raccourcis clavier

Copier le fichier **retroarch\_kb\_hotkeys.yml** dans le dossier `\user\inputmapping\` de votre installation RetroBat.

Ouvrir le fichier avec votre éditeur de texte préféré.

<div align="left"><figure><img src="https://i.imgur.com/3PElZkI.png" alt=""><figcaption></figcaption></figure></div>

Le fichier est au format yml, il est entièrement commenté par défaut.

La première chose à faire est de décommenter toutes les lignes de la section relative aux assignations, ainsi que le titre du "conteneur yml" de la section, pour cela il faut supprimer le caractère # de toutes les lignes à partir de la ligne `#default:` :

<div align="left"><figure><img src="https://i.imgur.com/Iw4cFSw.png" alt=""><figcaption></figcaption></figure></div>

Dans cet exemple, nous allons remplacer les assignations des raccourcis avance rapide **(fast-forward)** et retour arrière **(rewind)** par les touches F9 et F10:

pour cela, remplacer simplement l'assignation des fonctions **input\_rewind et input\_hold\_fast\_forward** par f9 et f10:

<div align="left"><figure><img src="https://i.imgur.com/TEFpuRj.png" alt=""><figcaption></figcaption></figure></div>

Maintenant, sauvegarder le fichier:

<div align="left"><figure><img src="https://i.imgur.com/jpb23KY.png" alt=""><figcaption></figcaption></figure></div>

Au prochain lancement d'un jeu avec RetroArch, les touches assignées aux raccourcis seront ceux définis dans le fichier:

<div align="left"><figure><img src="https://i.imgur.com/pqvfj3r.png" alt=""><figcaption></figcaption></figure></div>

Il est également possible d'assigner des raccourcis différents pour les différents coeurs libretro, dans l'exemple ci-dessous, l'assignation de l'avance rapide pour le coeur flycast est définie sur "toggle" au lieu de "hold":

<div align="left"><figure><img src="https://i.imgur.com/7MvE8bh.png" alt=""><figcaption></figcaption></figure></div>

## Information complémentaire

### Emplacement des fichiers de configuration des touches

Les fichiers sont stockés dans le répertoire suivant de votre installation RetroBat :&#x20;

`\emulators\retroarch\config\remaps\<nom abrégé du core>\`

<div align="left"><figure><img src="https://i.imgur.com/ljP0sMO.png" alt=""><figcaption></figcaption></figure></div>

_Comme il est possible de voir sur cet exemple : la valeur renseignée pour l'entrée "input\_player1\_stk\_l\_y-" est la valeur 8 (qui correspond à la modification faite précédemment)._

### Principe du mapping des contrôleurs de RetroArch

Les informations sur la façon dont RetroArch gère les contrôles se trouvent dans le lien suivant :&#x20;

{% embed url="https://docs.libretro.com/guides/input-and-controls/" %}

RetroArch fonctionne sur un mapping des contrôleurs en 2 étapes:

* Étape 1 : Paramétrage de la manette physique avec le "Retropad" de Retroarch
* Étape 2 : Paramétrage du "Retropad" avec le contrôleur de la console ou de l'ordinateur original

Le guide sur cette page ne traite que de la seconde étape, car nous partons du principe que vous avez correctement paramétré votre contrôleur dans RetroBat et que tous les boutons physiques de votre manette ont bien été passés à RetroArch.



Le paramétrage fait à l'étape 1 se trouve dans le menu suivant de RetroArch :

<div align="left"><figure><img src="https://i.imgur.com/HFlwynw.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Changer le paramétrage selon l'étape 1 n'est pas recommandé, et qui plus est serait inutile puisqu'automatiquement réécrit par RetroBat au prochain lancement de Retroarch depuis RetroBat.
{% endhint %}

