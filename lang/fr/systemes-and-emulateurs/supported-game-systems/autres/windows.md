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

{% hint style="info" %}
Le programme BATGUI.EXE permet de simplifier la procédure décrite ci-dessous.&#x20;

Aller à la section [BATGUI ](../../../utilisation-avancee/batgui.md)du wiki.
{% endhint %}

Créer un fichier .txt avec un nom permettant d'identifier le jeu.

Il existe 2 possibilités de gérer STEAM lorsqu'un jeu est quitté:

* Fermer STEAM en quittant le jeu
* Laisser STEAM actif en quittant le jeu

La solution qui consiste à ne pas quitter STEAM en quittant le jeu permet de lancer les jeux plus rapidement puisque le démarrage de STEAM (et ses éventuelles mises à jour) ne sont pas effectuées à chaque lancement.

Voici le code à copier dans le fichier pour fermer STEAM en quittant le jeu :

<pre class="language-batch"><code class="lang-batch"><strong>@echo OFF
</strong>
REM AJOUTER L'ID STEAM ICI:
START steam://rungameid/000000

TIMEOUT /t 30
:RUNNING

REM AJOUTER LE NOM EXACT DE L'EXECUTABLE DU JEU, PAR EXEMPLE: "MonJeu.exe"
tasklist|findstr "MonJeu.exe" > nul

if %errorlevel%==1 timeout /t 5 &#x26; taskkill /F /IM Steam.exe /T &#x26; GOTO ENDLOOP
timeout /t 2
GOTO RUNNING
:ENDLOOP
</code></pre>

Ci-dessous le code à copier dans le fichier pour ne pas fermer STEAM en quittant le jeu :

```batch
@echo OFF

REM AJOUTER L'ID STEAM ICI:
START steam://rungameid/000000

TIMEOUT /t 30
:RUNNING

REM AJOUTER LE NOM EXACT DE L'EXECUTABLE DU JEU, PAR EXEMPLE: "MonJeu.exe"
tasklist|findstr "MonJeu.exe" > nul

if %errorlevel%==1 timeout /t 5 & GOTO ENDLOOP
timeout /t 2
GOTO RUNNING
:ENDLOOP
```

Le fichier .txt ci-dessus devra être sauvegardé dans le dossier `roms\windows` avec l'extension .bat (en remplaçant l'extension .txt)..

**Il reste 2 informations à compléter dans le fichier ci-dessus : l'ID du jeu et le nom de l'exécutable.**

**Procéder comme suit pour trouver ces informations**

**ID DU JEU**

Ouvrir le client STEAM et cocher l'option "Afficher les barres d'adresse Web quand elles sont disponibles" dans les paramètres de l'interface (s'assurer également que STEAM ne démarre pas en mode Big Picture dans le même menu).

<div align="left">

<figure><img src="https://i.imgur.com/Tx6xGq9.png" alt=""><figcaption></figcaption></figure>

</div>

L'ID du jeu est disponible sur la page du jeu dans le magasin STEAM

<div align="left">

<figure><img src="https://i.imgur.com/5sbDKY4.png" alt=""><figcaption></figcaption></figure>

</div>

Il est également possible de récupérer l'ID STEAM depuis le raccourci du jeu, pour cela effectuer un clic droit sur le raccourci et sélectionner Propriétés:

<div align="left">

<figure><img src="https://i.imgur.com/L62Gcq2.png" alt=""><figcaption></figcaption></figure>

</div>

**Exécutable**

Trouver l'exécutable du jeu depuis la Bibliothèque STEAM, en effectuant un clic-droit sur le jeu et en sélectionnant **Gérer > Parcourir les fichiers locaux** :

<div align="left">

<figure><img src="https://i.imgur.com/7PtrRgB.png" alt=""><figcaption></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://i.imgur.com/WwHq15Q.png" alt=""><figcaption></figcaption></figure>

</div>

{% hint style="info" %}
Il est également possible de trouver le nom de l'exécutable du jeu en ouvrant le Gestionnaire des tâches lorsque le jeu est en cours.
{% endhint %}

Enfin, copier les 2 informations dans le fichier .bat aux emplacements suivants :

<div align="left">

<figure><img src="https://i.imgur.com/CHGYrxn.png" alt=""><figcaption></figcaption></figure>

</div>

### Ajouter un jeu EPIC Game Store

{% hint style="info" %}
Assurez-vous que EPIC Game Launcher soit configuré pour que votre utilisateur soit connecté automatiquement.
{% endhint %}

#### Étape 1:

Copier le raccourci du jeu créé par le launcher Epic Launcher dans le dossier`roms\windows\.EPIC\` de votre installation RetroBat:

<div align="left">

<figure><img src="https://i.imgur.com/ZkFCDNI.png" alt=""><figcaption></figcaption></figure>

</div>

{% hint style="info" %}
Le dossier .EPIC doit être créé, il n'est pas créé en standard lors de l'installation de RetroBat.
{% endhint %}

#### Étape 2:

Créér un fichier .bat avec un nom permettant au scrapeur de trouver le jeu.

2 possibilités s'offrent à vous:

* Quitter automatiquement le launcher EPIC à la sortie du jeu
* Laisser le launcher EPIC tourner après la sortie du jeu

La solution consistant à laisser le Launcher EPIC tourné permet de lancer les jeux plus rapidement, puisque l'étape de connection au launcher n'est pas effectuée à chaque fois.

Voici le code du fichier .bat avec fermeture du **EpicGameLauncher** :

```batch
@echo OFF

REM AJOUTER ICI LE CHEMIN DU RACCOURCI DU JEU EPIC:
START "" "C:\retrobat\roms\windows\.EPIC\Death Stranding.url"

TIMEOUT /t 30
:RUNNING

REM AJOUTER LE NOM EXACT DE L'EXECUTABLE DU JEU, PAR EXEMPLE: "MonJeu.exe"
tasklist|findstr "DeathStranding.exe" > nul

IF %errorlevel%==1 timeout /t 5 & taskkill /F /IM EpicGamesLauncher.exe /T & GOTO ENDLOOP
timeout /t 2
GOTO RUNNING
:ENDLOOP
```

Voici le code du fichier .bat sans fermeture du **EpicGameLauncher** :

```batch
@echo OFF

REM AJOUTER ICI LE CHEMIN DU RACCOURCI DU JEU EPIC:
START "" "C:\retrobat\roms\windows\.EPIC\Death Stranding.url"

TIMEOUT /t 30
:RUNNING

REM AJOUTER LE NOM EXACT DE L'EXECUTABLE DU JEU, PAR EXEMPLE: "MonJeu.exe"
tasklist|findstr "DeathStranding.exe" > nul

IF %errorlevel%==1 timeout /t 5 & GOTO ENDLOOP
timeout /t 2
GOTO RUNNING
:ENDLOOP
```

#### Étape 3:

Placer le fichier .bat dans le dossier `roms\windows` de votre installation RetroBat:

<div align="left">

<figure><img src="https://i.imgur.com/gxEOZNB.png" alt=""><figcaption></figcaption></figure>

</div>

Assurez-vous que les informations suivantes soient correctes dans le fichier:

<div align="left">

<figure><img src="https://i.imgur.com/FiGNJLZ.png" alt=""><figcaption></figcaption></figure>

</div>

La première information est le lien vers l'emplacement exact du raccourci, comme expliqué à l'étape 1.

La seconde information est le nom exact de l'éxécutable du jeu, cette information doit absolument être correcte afin de permettre le retour à l'interface RetroBat une fois la session de jeu terminée.

Le nom de l'éxécutable du jeu peut être trouvée dans le dossier d'installation du jeu ou dans le gestionnaire de tâche Windows lorsque le jeu est en cours (CTRL + ALT + SUPPR) :

<div align="left">

<figure><img src="https://i.imgur.com/9CejRnl.png" alt=""><figcaption></figcaption></figure>

</div>

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
