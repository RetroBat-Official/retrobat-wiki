---
description: Diablo
---

# DevilutionX

<div align="left"><figure><img src="../../../.gitbook/assets/image (749).png" alt="" width="416"><figcaption></figcaption></figure></div>

## Présentation

**Diablo** (Blizzard, 1996) est un jeu de rôle et d'action qui a lancé le genre du « hack and slash ». Son extension **Hellfire** (Sierra, 1997) ajoute un personnage, des quêtes et deux zones.

RetroBat utilise **DevilutionX**, un portage du jeu d'origine : haute résolution, écran large, jeu à la manette, améliorations de confort.

Les fichiers du jeu ne sont pas fournis : utilisez ceux de votre propre exemplaire (CD, [GOG](https://www.gog.com/game/diablo), [Battle.net](https://eu.shop.battle.net/fr-fr/family/diablo)) ou la [version d'essai](http://ftp.blizzard.com/pub/demos/diablosw.exe).

{% embed url="https://github.com/diasurgical/devilutionX" %}

## En bref

<table><thead><tr><th width="279"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\devilutionx</code></td></tr><tr><td><strong>Extensions</strong></td><td>.game .win</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>devilutionx</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (fichiers du jeu à fournir)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique (commandes de DevilutionX)</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non : sauvegardes du jeu, sauvegarde / chargement rapide à la manette</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr><tr><td><strong>Pistolets</strong></td><td>—</td></tr><tr><td><strong>Volants</strong></td><td>—</td></tr><tr><td><strong>BIOS optionnels</strong></td><td>—</td></tr></tbody></table>

## BIOS

Aucun BIOS n'est nécessaire. Il faut les fichiers du jeu :

<table><thead><tr><th width="246.5">Jeu</th><th>Fichiers</th></tr></thead><tbody><tr><td>Diablo</td><td><code>diabdat.mpq</code></td></tr><tr><td>Diablo (version d'essai)</td><td><code>spawn.mpq</code></td></tr><tr><td>Hellfire</td><td><code>hellfire.mpq</code>, <code>hfmonk.mpq</code>, <code>hfmusic.mpq</code>, <code>hfvoice.mpq</code> (avec <code>diabdat.mpq</code>)</td></tr></tbody></table>

## Quel format de jeu ?

Chaque jeu est un dossier `.game` de `roms\devilutionx` qui contient ses fichiers `.mpq`.

Avec Diablo et Hellfire dans le même dossier, Diablo est lancé, sauf si le nom du dossier contient « hellfire ». **JEU** choisit DIABLO ou HELLFIRE.

## Contrôles

### Configuration automatique

DevilutionX reconnaît la manette et ses commandes par défaut. Toutes les manettes branchées dirigent le héros : **CONTRÔLES > MANETTE DU JOUEUR 1 UNIQUEMENT** les limite à celle du joueur 1 (par exemple si une autre manette dérive).

### Raccourcis

<table><thead><tr><th width="261.5">Raccourci</th><th>Action</th></tr></thead><tbody><tr><td>HOTKEY + START</td><td>Quitter</td></tr><tr><td>SELECT + L3</td><td>Sauvegarde rapide</td></tr><tr><td>START + L3</td><td>Chargement rapide</td></tr><tr><td>START + R3</td><td>Capture d'écran</td></tr></tbody></table>

Les raccourcis de la manette peuvent être désactivés avec **CONTRÔLES > RACCOURCIS MANETTE**.

## Dossiers

<table><thead><tr><th width="270.25">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Jeux</td><td><code>roms\devilutionx\&#x3C;jeu>.game</code></td></tr><tr><td>Sauvegardes</td><td><code>saves\devilutionx\&#x3C;jeu></code></td></tr><tr><td>Configuration</td><td><code>roms\devilutionx\&#x3C;jeu>.game\diablo.ini</code></td></tr></tbody></table>

## Guides

### Organisation des fichiers

Dans `roms\devilutionx`, créez un dossier `diablo.game` :

Copiez-y le fichier `diabdat.mpq` de votre CD ou de votre dossier d'installation (ou extrayez-le de l'installateur GOG) :

{% embed url="https://github.com/diasurgical/devilutionX/wiki/Extracting-the-.MPQs-from-the-GoG-installer" %}

Pour Hellfire, copiez aussi `hellfire.mpq`, `hfmonk.mpq`, `hfmusic.mpq` et `hfvoice.mpq` :

<div align="left"><figure><img src="../../../.gitbook/assets/image (750).png" alt=""><figcaption></figcaption></figure></div>

La version d'essai se lance avec `spawn.mpq` à la place de `diabdat.mpq` :

{% embed url="https://github.com/diasurgical/devilutionx-assets/releases/latest/download/spawn.mpq" %}

### Options

* **RÉSOLUTION INTERNE DU JEU** jusqu'à 1280x960, **ÉCRAN LARGE** pour remplir les écrans larges.
* **ÉMULATION > COURIR EN VILLE**, **RAMASSAGE AUTO DE L'OR**, **REMPLISSAGE AUTO DE LA CEINTURE**.
* **INTERFACE UTILISATEUR > BARRE D'EXPÉRIENCE**, **BARRE DE VIE DES ENNEMIS**, **NOMS DES OBJETS**.

### Mods

Les mods de DevilutionX sont listés sur le wiki du projet :

{% embed url="https://github.com/diasurgical/devilutionX/wiki/Mods-and-related-projects" %}

## Problèmes connus

<table><thead><tr><th width="347.75">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Le héros bouge seul</td><td>Une autre manette dérive : activez <strong>MANETTE DU JOUEUR 1 UNIQUEMENT</strong>, ou augmentez <strong>ZONE MORTE JOYSTICK</strong>.</td></tr><tr><td>Le jeu demande de choisir entre Diablo et Hellfire</td><td>Réglez <strong>JEU</strong>.</td></tr></tbody></table>
