---
description: Sony
---

# Playstation 4

<div align="left"><figure><img src="../../../../.gitbook/assets/image (527).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Présentation

La **PlayStation 4** sort en novembre 2013. Après le processeur très particulier de la PS3, Sony revient à une architecture proche de celle d'un PC, plus simple pour les développeurs. La manette DualShock 4 ajoute un pavé tactile, un bouton Share et une barre lumineuse.

La console connaît un immense succès, avec plus de 117 millions d'exemplaires vendus, et accueille des jeux comme Bloodborne, God of War, Marvel's Spider-Man ou The Last of Us Part II. Deux révisions sortent en 2016 : la PS4 Slim et la PS4 Pro, plus puissante.

L'émulation de la PS4 est récente. **shadPS4**, le seul émulateur proposé par RetroBat, progresse vite mais reste jeune : beaucoup de jeux ne fonctionnent pas encore.

{% embed url="https://fr.wikipedia.org/wiki/PlayStation_4" %}

## En bref

<table><thead><tr><th width="262.75"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\ps4</code></td></tr><tr><td><strong>Extensions</strong></td><td>.ps4 .zar .m3u .lnk .decomp</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>shadps4</td></tr><tr><td><strong>BIOS</strong></td><td>Modules système de la PS4 dans <code>emulators\shadps4\user\sys_modules</code> (non contrôlés par RetroBat)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, gérée par shadPS4</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr></tbody></table>

## Quel émulateur choisir ?

shadPS4 est le seul émulateur PS4 de RetroBat.

<table><thead><tr><th width="172">Émulateur</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>shadps4</strong> (défaut)</td><td>Fait tourner un nombre croissant de jeux, plusieurs versions installables côte à côte.</td><td>Émulateur jeune : beaucoup de jeux ne démarrent pas ou plantent. Demande un PC puissant.</td></tr></tbody></table>

La liste de compatibilité de shadPS4 ([shadps4.net](https://shadps4.net/compatibility/)) indique l'état de chaque jeu.

**Version de l'émulateur** : l'option **ÉMULATION > VERSION DE L'ÉMULATEUR** permet de choisir la version de shadPS4 utilisée. Par défaut, RetroBat lance la version stable la plus récente installée. Le choix **SÉLECTIONNÉ DANS LE LAUNCHER** reprend la version choisie dans le lanceur de shadPS4, **PRÉVERSION** la préversion la plus récente.

## BIOS

La PS4 n'a pas de BIOS à fournir, mais shadPS4 peut charger des **modules système** de la console (fichiers `.sprx`), nécessaires au bon fonctionnement de certains jeux. Ils doivent être extraits de votre propre PS4.

<table><thead><tr><th width="320.25">Fichiers</th><th>Emplacement</th></tr></thead><tbody><tr><td>Modules <code>.sprx</code> (<code>libSceNgs2.sprx</code>, <code>libSceFont.sprx</code>…)</td><td><code>emulators\shadps4\user\sys_modules</code></td></tr></tbody></table>

La liste des modules reconnus se trouve dans la documentation de shadPS4. RetroBat ne vérifie pas ces fichiers.

## Quel format de jeu ?

<table><thead><tr><th width="166.5">Format</th><th>Remarques</th></tr></thead><tbody><tr><td><strong>Dossier <code>.ps4</code></strong></td><td>Le dossier du jeu, qui contient <code>eboot.bin</code>, renommé avec <code>.ps4</code> à la fin : <code>roms\ps4\Mon jeu.ps4</code>.</td></tr><tr><td><strong>.zar</strong></td><td>Le jeu compressé en un seul fichier (ZArchive), lu directement par shadPS4.</td></tr><tr><td>.m3u</td><td>Fichier texte dont la première ligne donne le chemin du jeu, à partir de <code>roms\ps4</code> (voir <a href="playstation-4.md#utiliser-un-fichier-.m3u">Guides</a>).</td></tr><tr><td>.lnk</td><td>Raccourci Windows : ses arguments sont transmis à shadPS4.</td></tr><tr><td>.decomp</td><td>Portage PC, voir la page <a href="../../autres/recomp.md"><strong>Recompilations</strong></a>.</td></tr></tbody></table>

shadPS4 n'installe pas les fichiers `.pkg` : le jeu doit d'abord être extrait en dossier.

## Contrôles

### Configuration automatique

RetroBat ne configure pas les manettes pour shadPS4 : l'émulateur les reconnaît lui-même. Les manettes Xbox et DualShock fonctionnent sans réglage.

* L'ordre des joueurs peut différer de celui de RetroBat.
* Pour changer les boutons, ouvrez les réglages de shadPS4 (bouton Controller). Les réglages sont enregistrés par jeu.
* L'option **CONTRÔLES > ACTIVER LE MOTION CONTROL**, active par défaut, utilise le gyroscope des manettes compatibles.

### Raccourcis

<table><thead><tr><th width="208.25">Raccourci</th><th>Action</th><th>Clavier</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quitter</td><td>—</td></tr><tr><td>—</td><td>Plein écran</td><td>F11</td></tr><tr><td>—</td><td>Compteur d'images par seconde</td><td>F10</td></tr><tr><td>—</td><td>Capture d'écran</td><td>F12</td></tr><tr><td>—</td><td>Capture d'écran avec les fenêtres et menus affichés</td><td>ALT + F12</td></tr></tbody></table>

## Dossiers

| Contenu                                  | Dossier                                                           |
| ---------------------------------------- | ----------------------------------------------------------------- |
| Contenus additionnels (DLC)              | `roms\ps4\DLC`                                                    |
| Sauvegardes (dossier « home » de la PS4) | `saves\ps4\shadps4\home`                                          |
| Modules système                          | `emulators\shadps4\user\sys_modules`                              |
| Configuration de shadPS4                 | `emulators\shadps4\user\config.json`                              |
| Configurations par jeu de shadPS4        | `emulators\shadps4\user\custom_configs`                           |
| Patches et codes de triche               | `emulators\shadps4\user\patches`, `emulators\shadps4\user\cheats` |
| Captures d'écran                         | `emulators\shadps4\user\screenshots`                              |
| Versions de shadPS4                      | `emulators\shadps4\launcher\versions`                             |

## Guides

### Ajouter un jeu

1. Copiez le dossier du jeu dans `roms\ps4`. Il porte en général l'identifiant du jeu (par exemple `CUSA00900`) et contient le fichier `eboot.bin`.
2. Renommez-le en ajoutant `.ps4` à la fin, par exemple `Mon jeu.ps4`.
3. Mettez à jour la liste des jeux de RetroBat.

### Compresser un jeu en .zar

Un jeu PS4 compte des milliers de fichiers. Le format ZArchive le réunit en un seul fichier compressé, que shadPS4 lit sans l'extraire.

1. Compressez le dossier du jeu avec l'outil ZArchive.
2. Placez le fichier `.zar` obtenu dans `roms\ps4`.

Ce format demande shadPS4 0.17.0 ou plus récent.

### Utiliser un fichier .m3u

Le fichier `.m3u` permet de garder le dossier du jeu sous son nom d'origine. Sa première ligne donne le chemin du fichier à lancer, à partir de `roms\ps4` :

```
CUSA00900\eboot.bin
```

Les lignes vides et celles qui commencent par `#` sont ignorées.

### Réglages par jeu de shadPS4

shadPS4 peut enregistrer des réglages propres à chaque jeu, et il les utilise par défaut. L'option **ÉMULATION > IGNORER LES RÉGLAGES PAR JEU** les ignore et applique toujours les réglages de RetroBat.

### Autres options utiles

| Option                                      | Effet                                                                                           |
| ------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| **ÉMULATION > LANGUE**                      | Langue de la console émulée. Par défaut, c'est celle de RetroBat.                               |
| **ÉMULATION > CORRECTIF RED-ZONE**          | Expérimental : peut corriger des plantages dans certains jeux. À laisser désactivé sauf besoin. |
| **INTERFACE UTILISATEUR > AFFICHER LE GUI** | Affiche la fenêtre de shadPS4. Elle reste ouverte après le jeu : **HOTKEY + START** la ferme.   |

<div align="left"><figure><img src="../../../../.gitbook/assets/image (528).png" alt=""><figcaption></figcaption></figure></div>

## Problèmes connus

| Problème                                                   | Solution                                                                                                                                                                                     |
| ---------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Le jeu ne démarre pas ou plante                            | Vérifiez son état dans la liste de compatibilité de shadPS4. Essayez une autre version avec **VERSION DE L'ÉMULATEUR**, et ajoutez les modules système (voir [BIOS](playstation-4.md#bios)). |
| Message « Unable to find any game in the provided folder » | Le dossier `.ps4` ne contient pas de fichier `eboot.bin`.                                                                                                                                    |
| Un fichier `.zar` ne se lance pas                          | Utilisez shadPS4 0.17.0 ou plus récent.                                                                                                                                                      |
| Les manettes ne sont pas dans le bon ordre                 | L'ordre est géré par shadPS4 et peut différer de celui de RetroBat.                                                                                                                          |
| Mes réglages RetroBat ne sont pas appliqués à un jeu       | Un réglage par jeu de shadPS4 passe avant : activez **IGNORER LES RÉGLAGES PAR JEU**.                                                                                                        |

