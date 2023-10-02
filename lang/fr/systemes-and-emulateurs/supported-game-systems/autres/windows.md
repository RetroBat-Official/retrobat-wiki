---
description: Microsoft
---

# Windows

<div align="left">

<figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/5149a33eed46b2af638b06119397d4023b75131f/art/logos/windows.svg" alt=""><figcaption></figcaption></figure>

</div>

Système d'exploitation - Date de sortie : 1992

{% embed url="https://fr.wikipedia.org/wiki/Microsoft_Windows" %}

## Informations

Les jeux Windows ne nécessitent pas d'émulateurs pour être démarrés. Ils sont lancés depuis l'interface Retrobat directement.



<table data-header-hidden><thead><tr><th width="182"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> windows</td></tr><tr><td><strong>Extensions</strong></td><td>.exe .bat .cmd .lnk .url .pc .win .windows .wine .7z .zip .rar .wsquashfs</td></tr></tbody></table>

## Contrôles

Le paramétrage des contrôleurs s'effectue dans le jeu ou dans Steam.

## Information spécifique au système

### Ajouter un jeu

Effectuer un clic droit sur l'exécutable du jeu et sélectionner "Copier", puis aller dans le répertoire `\roms\windows`, effectuer un clic droit, et sélectionner "Coller le raccourci"

<div align="left">

<figure><img src="https://i.imgur.com/47WNq9D.png" alt=""><figcaption><p>Le raccourci de PROJECT CARS</p></figcaption></figure>

</div>



### Ajouter un jeu Steam

Copier simplement le raccourci du jeu Steam (format .url) dans le dossier `roms\windows` de votre installation RetroBat:

<div align="left">

<figure><img src="https://i.imgur.com/QBLRBGX.png" alt=""><figcaption></figcaption></figure>

</div>

### Ajouter un jeu EPIC Game Store

Copier simplement le raccourci du jeu EPIC (format .url) dans le dossier `roms\windows` de votre installation RetroBat:

<div align="left">

<figure><img src="https://i.imgur.com/rh6uCHs.png" alt=""><figcaption></figcaption></figure>

</div>

### Ajouter un jeu Amazon Game Store

Copier simplement le raccourci du jeu Amazon Game (format .url) dans le dossier `roms\windows` de votre installation RetroBat:

<div align="left">

<figure><img src="https://i.imgur.com/mW5Xme7.png" alt=""><figcaption></figcaption></figure>

</div>

### Ajouter un jeu Microsoft GamePass

Localiser le répertoire d'installation du jeu sur votre ordinateur (par défaut dans `C:\XboxGames`).

Ouvrir le dossier "**Content**" dans le dossier du jeu et localiser l'executable du jeu:

![](<../../../.gitbook/assets/image (35).png>)

{% hint style="info" %}
Il est également possible de détecter l'exécutable du jeu en lançant le jeu et en faisant CTRL+ALT+SUPPR pour afficher le gestionnaire de tâches.
{% endhint %}

Créer un raccourci vers ce fichier (_clic droit > envoyer vers > Bureau (créer un raccourci)_)

Couper le raccourci créé sur le bureau et coller ce dernier dans le dossier `roms\windows` de RetroBat.

Il est possible de renommer le raccourci si vous le souhaitez.

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

<div align="left">

<figure><img src="https://i.imgur.com/4oCOJA7.png" alt=""><figcaption></figcaption></figure>

</div>

Effectuer un clic droit sur le raccourci nouvellement créé et récupérer l'URL depuis les propriétés du raccourci:

<div align="left">

<figure><img src="https://i.imgur.com/MmzV6ec.png" alt=""><figcaption></figcaption></figure>

</div>

Ensuite, récupérer le nom de l'exécutable du jeu comme suit:

Dans Ubisoft Connect, ouvrir lesinformations du jeu et afficher les propriétés:

<div align="left">

<figure><img src="https://i.imgur.com/hpRecAI.png" alt=""><figcaption></figcaption></figure>

</div>

Cliquer sur le bouton "Ouvrir le dossier" dans la section "Fichiers locaux" et récupérer le nom de l'exécutable:

<div align="left">

<figure><img src="https://i.imgur.com/CT9qODE.png" alt=""><figcaption></figcaption></figure>

</div>

{% hint style="info" %}
Il est également possible de trouver le nom de l'exécutable du jeu en ouvrant le Gestionnaire des tâches lorsque le jeu est en cours.
{% endhint %}

Ensuite, copier ces deux informations dans le fichier .bat comme suit:

<div align="left">

<figure><img src="https://i.imgur.com/BAx77xx.png" alt=""><figcaption></figcaption></figure>

</div>

Enfin sauvegarder le fichier bat dans le dossier `roms\windows` de votre installation RetroBat.
