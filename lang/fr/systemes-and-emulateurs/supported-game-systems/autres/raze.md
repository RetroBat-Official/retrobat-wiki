---
description: Raze
---

# Raze

<div align="left"><figure><img src="../../../.gitbook/assets/image (762).png" alt=""><figcaption></figcaption></figure></div>

## Présentation

**Raze** est un moteur moderne, basé sur GZDoom, pour les jeux du moteur Build : **Duke Nukem 3D**, **Blood**, **Shadow Warrior**, **Redneck Rampage**, **PowerSlave / Exhumed**, **NAM**, **World War II GI** et leurs extensions.

Il apporte le rendu OpenGL ou Vulkan, la haute résolution, les écrans larges et une interface commune à tous les jeux.

Les fichiers des jeux ne sont pas fournis : utilisez ceux de vos propres exemplaires.

{% embed url="https://raze.zdoom.org/about" %}

## En bref

<table><thead><tr><th width="286.5"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\raze</code></td></tr><tr><td><strong>Extensions</strong></td><td>.raze</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>raze</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (fichiers du jeu à fournir)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique (commandes de Raze, menu sur START)</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non : sauvegardes du jeu, sauvegarde / chargement rapide aux raccourcis</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr><tr><td><strong>Pistolets</strong></td><td>—</td></tr><tr><td><strong>Volants</strong></td><td>—</td></tr><tr><td><strong>BIOS optionnels</strong></td><td>—</td></tr></tbody></table>

Raze est aussi proposé dans le système [**Duke Nukem 3D**](duke-nukem-3d.md), avec les mêmes fichiers `.eduke32`.

## Jeux pris en charge

La liste des jeux et des versions reconnues est sur le wiki de ZDoom :

{% embed url="https://zdoom.org/wiki/Raze#Supported_games" %}

## BIOS

Aucun BIOS n'est nécessaire. Il faut les fichiers de chaque jeu (`.grp`, `.rff`, `.art`…), par exemple `DUKE3D.GRP` pour Duke Nukem 3D ou `BLOOD.RFF` et ses fichiers pour Blood.

## Quel format de jeu ?

Un jeu se lance avec un fichier texte `.raze` placé dans `roms\raze`.

| Contenu du fichier                                   | Effet                                                                        |
| ---------------------------------------------------- | ---------------------------------------------------------------------------- |
| Une seule ligne : chemin du fichier principal du jeu | Le fichier est lancé comme jeu principal (`-iwad`).                          |
| Plusieurs lignes : un paramètre de Raze par ligne    | Les lignes sont passées telles quelles à Raze (par exemple `-file`, `-map`). |

Un chemin qui commence par `/` ou `\` part du dossier du fichier `.raze`. Un chemin complet (`C:\...`) est aussi accepté.

## Contrôles

### Configuration automatique

RetroBat active la manette dans Raze et garde ses commandes par défaut. START ouvre le menu ; SELECT reste libre pour les raccourcis de RetroBat. Les commandes se changent dans **Options > Customize Controls** de Raze.

**CONTRÔLES > TOUJOURS COURIR** (activé par défaut) et **ZONE MORTE JOYSTICK** règlent la manette.

### Raccourcis

<table><thead><tr><th width="231.5">Raccourci</th><th>Action</th></tr></thead><tbody><tr><td>HOTKEY + START</td><td>Quitter</td></tr><tr><td>HOTKEY + SUD</td><td>Menu (Échap)</td></tr><tr><td>HOTKEY + OUEST</td><td>Sauvegarde rapide</td></tr><tr><td>HOTKEY + NORD</td><td>Chargement rapide</td></tr><tr><td>HOTKEY + R3</td><td>Capture d'écran</td></tr></tbody></table>

Pour plus de détails, voir la page [**Raccourcis**](../../../navigation/hotkeys.md).

## Dossiers

<table><thead><tr><th width="279">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Jeux et fichiers de lancement</td><td><code>roms\raze</code></td></tr><tr><td>Sauvegardes</td><td><code>saves\raze</code></td></tr><tr><td>Captures d'écran</td><td><code>screenshots\raze</code></td></tr><tr><td>Configuration</td><td><code>emulators\raze\raze_portable.ini</code></td></tr></tbody></table>

## Guides

### Ajouter un jeu

Créez un fichier texte, écrivez le chemin du fichier principal du jeu à partir du dossier du fichier, puis enregistrez-le avec l'extension `.raze` :

<div align="left"><figure><img src="../../../.gitbook/assets/image (763).png" alt=""><figcaption></figcaption></figure></div>

### Lancer un jeu avec des paramètres

Pour ajouter des fichiers (extension, mod) ou d'autres paramètres, écrivez un paramètre par ligne. Les lignes qui commencent par `/` ou `\` sont des chemins à partir du dossier du fichier :

<div align="left"><figure><img src="../../../.gitbook/assets/image (764).png" alt=""><figcaption></figcaption></figure></div>

Enregistrez le fichier avec l'extension `.raze` dans `roms\raze`.

## Problèmes connus

<table><thead><tr><th width="341.5">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>« raze file does not contain any launch argument »</td><td>Le fichier <code>.raze</code> est vide : indiquez le fichier du jeu.</td></tr><tr><td>Raze affiche la liste des jeux au lieu de lancer le jeu</td><td>Le chemin du fichier <code>.raze</code> est faux ou la version du jeu n'est pas reconnue (voir la liste des jeux pris en charge).</td></tr><tr><td>Le cadre décoratif n'apparaît pas</td><td>Il demande un <strong>RAPPORT D'ASPECT</strong> automatique ou 4/3.</td></tr></tbody></table>
