# Structure du répertoire RetroBat

Une fois RetroBat installé, le répertoire contient les dossiers et fichiers suivants  :

<div align="left">

<figure><img src="https://i.imgur.com/MwQl2t9.png" alt=""><figcaption></figcaption></figure>

</div>

## Répertoire "bios"&#x20;

Ce répertoire est celui où doivent être placés (à de rares exceptions près) les bios et firmware de tous les systèmes.

Vous trouverez plus de précisions sur les fichiers de bios sur chaque [page individuelle de système](https://wiki.retrobat.org/v/francais/systemes-and-emulateurs/supported-game-systems).&#x20;



## Répertoire "emulators"

Dans ce répertoire se trouvent tous les émulateurs utilisés.

Retroarch est fourni par défaut lors de l'installation de RetroBat. Pour tous les autres émulateurs, ils seront téléchargés quand vous en aurez besoin, en lançant un jeu utilisant cet émulateur, ou en lançant celui-ci directement depuis le menu système RetroBat.

{% hint style="info" %}
Certains émulateurs ne sont pas fournis automatiquement par Retrobat.&#x20;

Les émulateurs suivants doivent être téléchargés par vos soins et placés dans les dossiers correspondants :

* Yuzu (& early-access)
* Ryujinx
* PICO-8
* 3DSen
* TeknoParrot
{% endhint %}

## Répertoire "library"

Ce répertoire peut être utilisé pour y placer des revues digitales, qui apparaîtront dans le système "Library" et pourront être consultés avec Retrobat en utilisant le core libretro **imageviewer**.

## Répertoire "roms"

Il s'agit du répertoire où les roms de jeux devront être copiés, chaque jeu devant être mis dans le sous-dossier du système correct correspondant au jeu, et possédant une extension acceptée par l'émulateur de ce système.

Vous trouverez plus de précisions sur les extensions acceptées sur chaque [page individuelle de système](https://wiki.retrobat.org/v/francais/systemes-and-emulateurs/supported-game-systems).&#x20;

## Répertoire "saves"

Ce répertoire contient les sauvegardes de jeu, également si vous utilisez la fonctionnalité de sauvegarde en jeu issu de l'émulateur pour enregistrer votre progression.

## Répertoire "screenshots"

Ce répertoire contient toutes les captures d'écran prises durant la session de jeu.



{% hint style="info" %}
Si vous constatez qu'une sauvegarde ou une capture d'écran ne s'enregistre pas dans le bon répertoire, merci de prendre contact avec la team RetroBat qui fera le nécessaire pour corriger au plus vite.
{% endhint %}
