# Configuration des touches RetroArch

Si la configuration des boutons ne vous convient pas pour un jeu ou un système complet géré par Retroarch (cores libretro), il est possible de créer une configuration spécifique pour un jeu.\
\
Voici comment procéder.\


Ouvrir RetroBat et démarrer un jeu pour lequel il est nécessaire de créer un paramétrage spécifique des touches.\
\
Une fois dans le jeu, appuyer sur les touches SELECT + ![](<../../.gitbook/assets/image (20).png>) simultanément pour ouvrir le menu  RetroArch, et choisir **Menu rapide**&#x20;

<div align="left">

<figure><img src="https://i.imgur.com/w1hW2nI.png" alt=""><figcaption></figcaption></figure>

</div>

Dans le MENU RAPIDE, aller dans la section " **Touches** "

<div align="left">

<figure><img src="https://i.imgur.com/thwZ08G.png" alt=""><figcaption></figcaption></figure>

</div>

Puis, sélectionner le port souhaité et paramétrer comme désiré :

<div align="left">

<figure><img src="https://i.imgur.com/NBbomL3.png" alt=""><figcaption></figcaption></figure>

</div>

\
Dans cet exemple, la touche Analogique gauche haut du Retropad a été mappé sur la touche défini comme A dans RetroBat (qui correspond à la touche W sur le clavier) :

<div align="left">

<figure><img src="https://i.imgur.com/4aS0EX9.png" alt=""><figcaption></figcaption></figure>

</div>

{% hint style="info" %}
Il est à noter que vous ne pouvez reparamétrer que les touches qui ont été paramétrées par RetroBat dans Retroarch selon le contrôleur utilisé.

S'il est nécessaire d'ajouter des touches qui n'ont pas été au préalable configuré dans RetroBat, il faut alors également changer le paramétrage dans les réglages généraux de Retroarch.

[(cliquer ici pour en savoir plus)](configuration-des-touches-retroarch.md#principe-du-mapping-des-controleurs-de-retroarch)
{% endhint %}

Une fois le paramétrage fait, sortir et retourner sur le menu **TOUCHES**, puis sélectionner "_Gérer les fichiers de remappage_" :

<div align="left">

<figure><img src="https://i.imgur.com/7gkrHwE.png" alt=""><figcaption></figcaption></figure>

</div>

Dans le sous-menu suivant, sauvegarder la configuration des touches pour le jeu (et il ne s'appliquera que pour celui-ci)

Une fois sauvegardé, le nouveau fichier de configuration sera utilisé au prochain lancement du jeu.

{% hint style="info" %}
Il n'est pas possible d'utiliser l'option "Sauvegarder le remappage pour le coeur", celui-ci étant utilisé par RetroBat, il sera automatiquement supprimé au démarrage suivant.
{% endhint %}

<div align="left">

<figure><img src="https://i.imgur.com/UadIDbH.png" alt=""><figcaption></figcaption></figure>

</div>

## Information complémentaire

### Emplacement des fichiers de configuration des touches

Les fichiers sont stockés dans le répertoire suivant de votre installation RetroBat :&#x20;

`\emulators\retroarch\config\remaps\<nom abrégé du core>\`

<div align="left">

<figure><img src="https://i.imgur.com/ljP0sMO.png" alt=""><figcaption></figcaption></figure>

</div>

_Comme il est possible de voir sur cet exemple : la valeur renseignée pour l'entrée "input\_player1\_stk\_l\_y-" est la valeur 8 (qui correspond à la modification faite précédemment)._

### Principe du mapping des contrôleurs de RetroArch

Les informations sur la façon dont RetroArch gère les contrôles se trouvent dans le lien suivant :&#x20;

{% embed url="https://docs.libretro.com/guides/input-and-controls/" %}

RetroArch fonctionne sur un mapping des contrôleurs en 2 étapes:

* Étape 1 : Paramétrage de la manette physique avec le "Retropad" de Retroarch
* Étape 2 : Paramétrage du "Retropad" avec le contrôleur de la console ou de l'ordinateur original

Le guide sur cette page ne traite que de la seconde étape, car nous partons du principe que vous avez correctement paramétré votre contrôleur dans RetroBat et que tous les boutons physiques de votre manette ont bien été passés à RetroArch.



Le paramétrage fait à l'étape 1 se trouve dans le menu suivant de RetroArch :

<div align="left">

<figure><img src="https://i.imgur.com/HFlwynw.png" alt=""><figcaption></figcaption></figure>

</div>

{% hint style="info" %}
Changer le paramétrage selon l'étape 1 n'est pas recommandé, et qui plus est serait inutile puisqu'automatiquement réécrit par RetroBat au prochain lancement de Retroarch depuis RetroBat.
{% endhint %}

