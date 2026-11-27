---
description: Microsoft
---

# Windows

<div align="left"><figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/5149a33eed46b2af638b06119397d4023b75131f/art/logos/windows.svg" alt=""><figcaption></figcaption></figure></div>

## Présentation

RetroBat ne sert pas qu'aux émulateurs : il lance aussi vos **jeux PC**. Un jeu Windows n'a besoin d'aucun émulateur. RetroBat le démarre, attend qu'il se ferme, puis revient à la liste des jeux.

Les jeux se rangent dans plusieurs systèmes :

<table><thead><tr><th width="212">Système</th><th width="150.5">Dossier</th><th>Contenu</th></tr></thead><tbody><tr><td><strong>Windows</strong></td><td><code>roms\windows</code></td><td>Vos jeux : raccourcis, exécutables, fichiers <code>.game</code>, dossiers…</td></tr><tr><td><strong>Steam</strong></td><td><code>roms\steam</code></td><td>Jeux Steam</td></tr><tr><td><strong>Epic Games</strong></td><td><code>roms\epic</code></td><td>Jeux de l'Epic Games Store</td></tr><tr><td><strong>GOG.com</strong></td><td><code>roms\gog</code></td><td>Jeux GOG Galaxy</td></tr><tr><td><strong>Amazon Prime Gaming</strong></td><td><code>roms\amazon</code></td><td>Jeux Amazon Games</td></tr><tr><td><strong>EA Games</strong></td><td><code>roms\eagames</code></td><td>Jeux EA (application EA)</td></tr></tbody></table>

Les dossiers des stores peuvent être remplis automatiquement par RetroBat (voir [**Guides**](windows.md#guides)). Vous pouvez aussi tout mettre dans `roms\windows`.

{% embed url="https://fr.wikipedia.org/wiki/Microsoft_Windows" %}

## En bref

<table><thead><tr><th width="264"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><p><code>roms\windows</code></p><p>(et <code>roms\steam</code>, <code>roms\epic</code>, <code>roms\gog</code>, <code>roms\amazon</code>, <code>roms\eagames</code>)</p></td></tr><tr><td><strong>Extensions</strong></td><td>.exe .bat .cmd .lnk .url .game .pc .win .windows .wine .zip .7z .rar .wsquashfs (stores : .url .bat, et .lnk sauf Steam)</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>windows (lancement direct du jeu)</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Non : réglages dans le jeu ou dans Steam</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non (selon le jeu)</td></tr><tr><td><strong>Pistolets</strong></td><td>Jeux compatibles DemulShooter</td></tr></tbody></table>

## Quel émulateur choisir ?

Il n'y a rien à choisir : le jeu est lancé directement par Windows.

## BIOS

Aucun BIOS n'est nécessaire.

## Quel format de jeu ?

| Format                                          | Exemple                                  | Ce que fait RetroBat                                                                                      |
| ----------------------------------------------- | ---------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| **Raccourci** `.lnk`                            | `Mon jeu.lnk`                            | Lance la cible du raccourci, avec ses paramètres.                                                         |
| **Raccourci internet** `.url`                   | `Mon jeu.url` (Steam, Epic, GOG, Amazon) | Lance le jeu par son store, puis attend le jeu lui-même.                                                  |
| **Fichier** `.game`                             | `Mon jeu.game`                           | Fichier texte : 1re ligne = chemin de l'exécutable, lignes suivantes = paramètres.                        |
| **Exécutable** `.exe`                           | `Mon jeu.exe`                            | Lance l'exécutable.                                                                                       |
| **Script** `.bat`, `.cmd`                       | `Mon jeu.bat`                            | Lance le script, et cherche l'exécutable qu'il démarre pour attendre la fin du jeu.                       |
| **Dossier** `.pc`, `.win`, `.windows`, `.wine`  | `Mon jeu.pc\`                            | Lance `autorun.cmd`, `autorun.bat`, `autoexec.cmd` ou `autoexec.bat`, sinon le premier `.exe` du dossier. |
| **Archive** `.zip`, `.7z`, `.rar`, `.wsquashfs` | `Mon jeu.zip`                            | Décompresse (ou monte) le jeu, puis le lance comme un dossier.                                            |

Le raccourci `.lnk` et le fichier `.game` sont les plus simples pour un jeu installé n'importe où sur le PC.

## Contrôles

RetroBat ne configure pas les manettes pour les jeux Windows : réglez-les dans le jeu, ou dans Steam pour les jeux Steam.

Le centre de contrôle de RetroBat n'est pas disponible pendant un jeu Windows.

### Raccourcis

<table><thead><tr><th width="210.25">Raccourci</th><th>Action</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Ferme le jeu (quand RetroBat a trouvé son exécutable)</td></tr></tbody></table>

### Pistolets

Pour les jeux de tir compatibles avec **DemulShooter** (The House of the Dead 2, 3 et Overkill, Heavy Fire, Big Buck Hunter, Operation Wolf Returns…), RetroBat démarre DemulShooter à partir de deux pistolets, quand **PISTOLETS > ACTIVER LES PISTOLETS** est actif. Le nom du fichier du jeu doit correspondre au nom attendu (par exemple `The House of the Dead 2.lnk`). Les autres options sont dans le même menu (**UTILISER DEMULSHOOTER** pour le forcer avec un seul pistolet, masquer le viseur ou l'arme…). Pour plus de détails, voir la page [**Pistolets**](../../../controleurs/supported-controllers/lightguns/).

## Dossiers

<table><thead><tr><th width="360.25">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Jeux</td><td><code>roms\windows</code></td></tr><tr><td>Jeux des stores</td><td><code>roms\steam</code>, <code>roms\epic</code>, <code>roms\gog</code>, <code>roms\amazon</code>, <code>roms\eagames</code></td></tr><tr><td>Jeux à ignorer pendant le scan d'un store</td><td><code>roms\&#x3C;store>\&#x3C;store>_ignore.txt</code></td></tr></tbody></table>

Les sauvegardes restent celles du jeu (en général dans les dossiers Documents ou AppData de Windows).

## Guides

### Ajouter un jeu installé

1. Faites un clic droit sur l'exécutable du jeu, puis **Envoyer vers > Bureau (créer un raccourci)**.
2. Déplacez le raccourci dans `roms\windows`, et renommez-le si besoin : son nom s'affiche dans la liste des jeux.

Autre méthode : créez un fichier texte `Mon jeu.game` dans `roms\windows`, contenant le chemin de l'exécutable sur la première ligne (et, si besoin, ses paramètres sur les lignes suivantes). Un chemin qui commence par `.\` part du dossier du fichier `.game`.

<div align="left"><figure><img src="../../../.gitbook/assets/image (783).png" alt=""><figcaption></figcaption></figure></div>

### Ajouter un jeu d'un store (Steam, Epic, GOG, Amazon, EA)

**Automatiquement** : activez **PARAMÈTRES DES JEUX > JEUX WINDOWS > SCANNER LES JEUX DES STORES (STEAM...)** (section **STORES DE JEUX ET LANCEURS**). Au démarrage, RetroBat crée un raccourci pour chaque jeu installé dans `roms\steam`, `roms\epic`, `roms\gog`, `roms\amazon` et `roms\eagames`, et retire ceux des jeux désinstallés.

| Option (JEUX WINDOWS)                               | Effet                                                                                                          |
| --------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| **SCANNER LES JEUX DES STORES (STEAM...)**          | Crée les raccourcis des jeux installés au démarrage de RetroBat.                                               |
| **SCANNER LES JEUX NON INSTALLÉS**                  | Ajoute aussi les jeux Steam de votre bibliothèque non installés.                                               |
| **CONSERVER LES JEUX AJOUTÉS MANUELLEMENT**         | Ne supprime pas les raccourcis que vous avez ajoutés vous-même dans les dossiers des stores.                   |
| **FERMER LE LAUNCHER EN QUITTANT**                  | Ferme Steam, Epic… en quittant le jeu. Par défaut, le store est fermé seulement s'il a été démarré par le jeu. |
| **DÉTECTION DES EXÉCUTABLES DANS LES FICHIERS BAT** | Cherche l'exécutable lancé par un fichier `.bat` ou `.cmd` (activé par défaut).                                |

Pour qu'un jeu ne soit plus ajouté par le scan, écrivez son identifiant dans `roms\<store>\<store>_ignore.txt` (un par ligne, par exemple `roms\steam\steam_ignore.txt`).

<div align="left"><figure><img src="../../../.gitbook/assets/image (784).png" alt=""><figcaption></figcaption></figure></div>

**À la main** : copiez le raccourci du jeu créé par le store (`.url`) dans `roms\windows` ou dans le dossier du store.

<div align="left"><figure><img src="../../../.gitbook/assets/image (789).png" alt=""><figcaption></figcaption></figure></div>

### Ajouter un jeu Xbox / Game Pass

Les jeux du Microsoft Store et du Game Pass sont des applications protégées.

* **Jeu installé dans `C:\XboxGames`** : ouvrez son dossier `Content`, faites un raccourci vers l'exécutable du jeu et placez-le dans `roms\windows`.
* **Raccourci créé par l'application Xbox** : placez-le dans `roms\windows`.&#x20;

<div align="left"><figure><img src="../../../.gitbook/assets/image (788).png" alt="" width="342"><figcaption></figcaption></figure></div>

RetroBat ne trouve pas toujours le jeu derrière ce raccourci. Créez alors à côté un fichier texte au même nom, avec l'extension `.uwp`, contenant le nom de l'application (visible dans les propriétés du raccourci, par exemple `Microsoft.SeaofThieves`). RetroBat en déduit l'exécutable du jeu.

<div align="left"><figure><img src="../../../.gitbook/assets/image (785).png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../../../.gitbook/assets/image (787).png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../../../.gitbook/assets/image (786).png" alt=""><figcaption></figcaption></figure></div>

### Ajouter un jeu Ubisoft Connect

Créez un fichier `.bat` dans `roms\windows`, qui lance le jeu par son adresse Ubisoft (`uplay://launch/<identifiant>/0`, visible dans un raccourci créé par Ubisoft Connect) puis attend la fin du jeu :

```batch
@echo OFF
REM Ubisoft game id
START uplay://launch/00000/0
TIMEOUT /t 30
:RUNNING
REM Exact name of the game executable
tasklist|findstr "MonJeu.exe" > nul
IF %errorlevel%==1 timeout /t 5 & GOTO ENDLOOP
timeout /t 2
GOTO RUNNING
:ENDLOOP
```

Remplacez `00000` par l'identifiant du jeu...&#x20;

<div align="left"><figure><img src="../../../.gitbook/assets/image (790).png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../../../.gitbook/assets/image (791).png" alt=""><figcaption></figcaption></figure></div>

... et `MonJeu.exe` par le nom de son exécutable (visible dans le Gestionnaire des tâches pendant le jeu ou dans le dossier du jeu).

<div align="left"><figure><img src="../../../.gitbook/assets/image (792).png" alt=""><figcaption></figcaption></figure></div>

Pour fermer aussi Ubisoft Connect en quittant, remplacez la ligne `IF` par :

```batch
IF %errorlevel%==1 timeout /t 5 & taskkill /F /IM upc.exe /T & GOTO ENDLOOP
```

Réglez Ubisoft Connect pour qu'il vous connecte automatiquement.

### La musique de RetroBat s'entend pendant le jeu

RetroBat attend la fin du jeu pour revenir à la liste des jeux. S'il ne trouve pas le jeu (jeu lancé par un launcher, mauvais exécutable détecté dans un store), il revient trop tôt et sa musique s'entend.

1. Lancez le jeu en dehors de RetroBat, jusqu'à la partie.
2. Ouvrez le Gestionnaire des tâches (**CTRL + MAJ + ÉCHAP**) et notez le nom de l'exécutable du jeu.
3. À côté du fichier du jeu (par exemple `Mon jeu.lnk`), créez un fichier texte au même nom, avec l'extension `.gameexe` : `Mon jeu.gameexe`.
4. Écrivez-y le nom de l'exécutable, avec ou sans `.exe`. Si le jeu démarre un second programme (launcher puis jeu), écrivez le second nom sur une deuxième ligne.

RetroBat attend alors la fin de ce programme. Le fichier `.gameexe` fonctionne avec tous les formats de jeu.

<div align="left"><figure><img src="../../../.gitbook/assets/image (793).png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../../../.gitbook/assets/image (794).png" alt=""><figcaption></figcaption></figure></div>

Si le jeu met longtemps à démarrer, augmentez **ÉMULATION > DÉLAI D'ATTENTE AVANT RETOUR** dans les options du jeu (30 secondes par défaut).

## Problèmes connus

<table><thead><tr><th width="350.25">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>La musique de RetroBat s'entend en jeu, ou RetroBat revient à la liste trop tôt</td><td>Voir <a href="windows.md#la-musique-de-retrobat-sentend-pendant-le-jeu"><strong>La musique de RetroBat s'entend pendant le jeu</strong></a>.</td></tr><tr><td>HOTKEY + START ne ferme pas le jeu</td><td>RetroBat n'a pas trouvé l'exécutable du jeu : ajoutez un fichier <code>.gameexe</code>.</td></tr><tr><td>Un jeu d'un store disparaît de la liste</td><td>Le scan retire les raccourcis des jeux désinstallés : activez <strong>CONSERVER LES JEUX AJOUTÉS MANUELLEMENT</strong> pour vos raccourcis ajoutés à la main.</td></tr><tr><td>Steam reste ouvert après le jeu</td><td>Activez <strong>FERMER LE LAUNCHER EN QUITTANT</strong>.</td></tr><tr><td>La manette ne marche pas en jeu</td><td>Le jeu ne reconnaît pas la manette : réglez-la dans le jeu, ou ajoutez le jeu à Steam et utilisez la configuration de Steam.</td></tr></tbody></table>
