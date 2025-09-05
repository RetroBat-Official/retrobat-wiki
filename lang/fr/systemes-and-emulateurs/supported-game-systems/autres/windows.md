---
description: Microsoft
---

# Windows

<div align="left"><figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/5149a33eed46b2af638b06119397d4023b75131f/art/logos/windows.svg" alt=""><figcaption></figcaption></figure></div>

Système d'exploitation - Date de sortie : 1992

{% embed url="https://fr.wikipedia.org/wiki/Microsoft_Windows" %}

## Informations

Les jeux Windows ne nécessitent pas d'émulateurs pour être démarrés. Ils sont lancés depuis l'interface Retrobat directement.



<table data-header-hidden><thead><tr><th width="182"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> windows<br><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> amazon (for amazon store games)<br><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> eagames (for EA store EA games)<br><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> epic (for EPIC store games)<br><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> gog (for GOG games)<br><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> steam (for Steam games)</td></tr><tr><td><strong>Extensions</strong></td><td>.exe .bat .cmd .lnk .game .url .pc .win .windows .wine .7z .zip .rar .wsquashfs</td></tr></tbody></table>

## Note spéciale pour les jeux des Store

RetroBat peut automatiquement scanner au démarrage les jeux des stores amazon, eagames (uniquement les jeux développés par EA games), epic, gog et steam, cette fonctionnalité peut être activée dans le  MENU PRINCIPAL > PARAMETRES DES JEUX > JEUX WINDOWS:

<div align="left"><figure><img src="https://i.imgur.com/CaK00YK.png" alt=""><figcaption></figcaption></figure></div>

## Contrôles

Le paramétrage des contrôleurs s'effectue dans le jeu ou dans Steam.

## Information spécifique au système

### Ajouter un jeu

Créer un fichier texte et renseigner le chemin vers l'exécutable du jeu.

Sauvegarder le fichier avec l'extension ".game" et placer le fichier dans le dossier `\roms\windows`:

<div align="left"><figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FexdzL60ZuqPLldz2AYta%2Fuploads%2FsmgKWfLTbroDY2EHGOeg%2Fimage.png?alt=media&#x26;token=a1341c05-b022-477c-8ee3-99fc188e30fa" alt=""><figcaption></figcaption></figure></div>

### Ajouter un jeu Steam

Copier simplement le raccourci du jeu Steam (format .url) dans le dossier `roms\windows` de votre installation RetroBat:

<div align="left"><figure><img src="https://i.imgur.com/QBLRBGX.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="warning" %}
Si la musique du menu RetroBat est audible lors du jeu, appliquer [la méthode suivante](windows.md#what-to-do-if-retrobat-music-is-heard-in-the-background) pour corriger le problème.
{% endhint %}

### Ajouter un jeu EPIC Game Store

Copier simplement le raccourci du jeu EPIC (format .url) dans le dossier `roms\windows` de votre installation RetroBat:

<div align="left"><figure><img src="https://i.imgur.com/rh6uCHs.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="warning" %}
Si la musique du menu RetroBat est audible lors du jeu, appliquer [la méthode suivante](windows.md#what-to-do-if-retrobat-music-is-heard-in-the-background) pour corriger le problème.
{% endhint %}

### Ajouter un jeu Amazon Game Store

Copier simplement le raccourci du jeu Amazon Game (format .url) dans le dossier `roms\windows` de votre installation RetroBat:

<div align="left"><figure><img src="https://i.imgur.com/mW5Xme7.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="warning" %}
Si la musique du menu RetroBat est audible lors du jeu, appliquer [la méthode suivante](windows.md#what-to-do-if-retrobat-music-is-heard-in-the-background) pour corriger le problème.
{% endhint %}

### Ajouter un jeu Microsoft Gamepass

Localiser le dossier d'installation du jeu (par défaut `C:\XboxGames`).

Ouvrir le dossier "**Content**" et trouver l'exécutable du jeu:

<div align="left"><figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FexdzL60ZuqPLldz2AYta%2Fuploads%2F174BsD0BeF2I1TUidFCI%2Fimage%20(46).png?alt=media&#x26;token=48f33c86-4f76-4ab9-b524-d75287a3af4d" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Il est possible de trouver l'exécutable du jeu en pressant CTRL+ALT+SUPPR pour accéder au gestionnaire de tâches.
{% endhint %}

Créer un raccourci vers l'exécutable du jeu (_clic droit > envoyer vers > Bureau (raccourci)_)

Couper le raccourci et le coller dans le dossier `roms\windows` de l'installation RetroBat.

Le raccourci peut être renommé.\


{% hint style="warning" %}
Si la musique du menu RetroBat est audible lors du jeu, appliquer [la méthode suivante](windows.md#what-to-do-if-retrobat-music-is-heard-in-the-background) pour corriger le problème.
{% endhint %}

### Ajouter un jeu Microsoft Gamepass (format WUP)

Depuis l'application XBOX, créer un raccourci sur le bureau :

![](https://wiki.retrobat.org/~gitbook/image?url=https%3A%2F%2Fi.imgur.com%2FZHP8OUv.png\&width=768\&dpr=4\&quality=100\&sign=482e96af1b7cdf4b7e38ec8ea1b2c4ea54b424de0bfe768fcd3e449dfe78c085)

Couper et coller le raccourci à l'interieur du dossier `roms\windows` :

![](https://wiki.retrobat.org/~gitbook/image?url=https%3A%2F%2Fi.imgur.com%2FCTOgYjI.png\&width=768\&dpr=4\&quality=100\&sign=91be061016a458541d1bfd98079fb73f22f336514adb5c3b5e451bc00ff3c2a9)

Ensuite, faire un clique droit sur le raccourci, et retrouvez le nom de l'application UWP :

![](https://wiki.retrobat.org/~gitbook/image?url=https%3A%2F%2Fi.imgur.com%2FSQzxKUS.png\&width=768\&dpr=4\&quality=100\&sign=8e0b74d419f8f83688d81474ecffd70cca1448a47293dd8812f7e33e43c6b615)

Puis, créer un fichier texte, et à l'aide d'un éditeur de texte, renseigner le nom de l'application UWP à l'interieur du fichier :

![](https://wiki.retrobat.org/~gitbook/image?url=https%3A%2F%2Fi.imgur.com%2Fbly0vZ8.png\&width=768\&dpr=4\&quality=100\&sign=ce359e0b7666c19d44a26ce80a3bb2cf3f1a68852b0d3be9919dd509f55ff222)

Pour finir, enregistrer le fichier dans le même dossier que le raccourci du jeu, en remplaçant l'extension `.txt` par `.uwp` :

![](https://wiki.retrobat.org/~gitbook/image?url=https%3A%2F%2Fi.imgur.com%2FiWX2oXO.png\&width=768\&dpr=4\&quality=100\&sign=9efd47eecf4d442f4a5570f715cbe04f2a21b31d5ec02df082d45519099370c0)

{% hint style="info" %}
Cette seconde partie (la création du fichier uwp) est nécessaire : sans ce fichier, RetroBat n'attendra pas la fermeture du jeu et la musique du menu ES se fera entendre en arrière-plan.
{% endhint %}

### Ajouter un jeu UBISOFT (Ubisoft Connect)

{% hint style="info" %}
Assurez-vous que Ubisoft Connect soit configuré pour que votre utilisateur soit connecté automatiquement.
{% endhint %}

Créer un fichier .txt avec un nom permettant d'identifier le jeu.

Il existe 2 possibilités de gérer Ubisoft Connect lorsqu'un jeu est quitté:

* Fermer UBISOFT CONNECT en quittant le jeu
* Laisser UBISOFT CONNECT actif en quittant le jeu

La solution qui consiste à ne pas fermer Ubisoft Connect en quittant le jeu permet de lancer les jeux plus rapidement puisque le démarrage de Ubisoft Connect (et ses éventuelles mises à jour) ne sont pas effectuées à chaque lancement.

Voici le code à copier dans le fichier pour fermer **Ubisoft Connect** en quittant le jeu :

```batch
@echo OFF

REM AJOUTER ICI L'APPID UBISOFT:
START uplay://launch/00000/0

TIMEOUT /t 30
:RUNNING

REM AJOUTER LE NOM EXACT DE L'EXECUTABLE DU JEU, PAR EXEMPLE: "MonJeu.exe"
tasklist|findstr "MonJeu.exe" > nul

IF %errorlevel%==1 timeout /t 5 & taskkill /F /IM upc.exe /T & GOTO ENDLOOP
timeout /t 2
GOTO RUNNING
:ENDLOOP
```

Voici le code du fichier .bat sans fermeture de **Ubisoft Connect** :

```batch
@echo OFF

REM AJOUTER ICI L'APPID UBISOFT:
START uplay://launch/00000/0

TIMEOUT /t 30
:RUNNING

REM AJOUTER LE NOM EXACT DE L'EXECUTABLE DU JEU, PAR EXEMPLE: "MonJeu.exe"
tasklist|findstr "MonJeu.exe" > nul

IF %errorlevel%==1 timeout /t 5 & GOTO ENDLOOP
timeout /t 2
GOTO RUNNING
:ENDLOOP
```

**Il reste 2 informations à compléter dans le fichier ci-dessus : l'ID du jeu et le nom de l'exécutable.**

**Procéder comme suit pour trouver ces informations**

**ID DU JEU**

Ouvrir le client UBISOFT CONNECT, afficher la liste des jeux installés, effectuer un clic-droit sur le jeu et sélectionner l'option "Créer un raccourci sur le bureau":

<div align="left"><figure><img src="https://i.imgur.com/4oCOJA7.png" alt=""><figcaption></figcaption></figure></div>

Effectuer un clic droit sur le raccourci nouvellement créé et récupérer l'URL depuis les propriétés du raccourci:

<div align="left"><figure><img src="https://i.imgur.com/MmzV6ec.png" alt=""><figcaption></figcaption></figure></div>

Ensuite, récupérer le nom de l'exécutable du jeu comme suit:

Dans Ubisoft Connect, ouvrir lesinformations du jeu et afficher les propriétés:

<div align="left"><figure><img src="https://i.imgur.com/hpRecAI.png" alt=""><figcaption></figcaption></figure></div>

Cliquer sur le bouton "Ouvrir le dossier" dans la section "Fichiers locaux" et récupérer le nom de l'exécutable:

<div align="left"><figure><img src="https://i.imgur.com/CT9qODE.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Il est également possible de trouver le nom de l'exécutable du jeu en ouvrant le Gestionnaire des tâches lorsque le jeu est en cours.
{% endhint %}

Ensuite, copier ces deux informations dans le fichier .bat comme suit:

<div align="left"><figure><img src="https://i.imgur.com/BAx77xx.png" alt=""><figcaption></figcaption></figure></div>

Enfin sauvegarder le fichier bat dans le dossier `roms\windows` de votre installation RetroBat.

### Que faire si la musique du menu RetroBat est audible en jeu ? <a href="#what-to-do-if-retrobat-music-is-heard-in-the-background" id="what-to-do-if-retrobat-music-is-heard-in-the-background"></a>

Ce symptôme est généralement causé par le fait que RetroBatn'a pas réussi à détecter le process du jeu (l'éxecutable), les raisons peuvent être:

* un jeu avec un "launcher" qui est exécuté avant le jeu en lui-même
* une mauvaise détection de l'éxecutable dans les librairies Steam, Epic, Amazon...

Dans ce cas, la procédure ci-dessous permet de résoudre le problème:

* Lancer le jeu en dehors de RetroBat
* Attendre d'atteindre le jeu (la partie jouable du jeu)
* Appuyer sur CTRL + ALT + SUPPR pour ouvrir l'explorateur de tâches
* Repérer le nom du process du jeu (l'éxecutable du jeu):

<div align="left"><figure><img src="https://i.imgur.com/XXTVidn.png" alt=""><figcaption></figcaption></figure></div>

Créer un fichier dans le même dossier que le raccourci du jeu (généralement roms\windows) et préciser dans le fichier le nom exact du process du jeu (sans l'extension .exe):

<div align="left"><figure><img src="https://i.imgur.com/gWOi36k.png" alt=""><figcaption></figcaption></figure></div>

Sauvegarder le fichier et le nommer exactement comme le raccourci du jeu, changer l'extension par ".gameexe":

<div align="left"><figure><img src="https://i.imgur.com/Wr1vqVP.png" alt=""><figcaption></figcaption></figure></div>

RetroBat attend dorénavant la fin du process défini dans le fichier pour revenir à la liste de jeux !

{% hint style="info" %}
Cette méthode est compatible avec les jeux au format raccourcis (.lnk) et.url.
{% endhint %}
