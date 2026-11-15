---
description: Microsoft
---

# Xbox 360

<div align="left"><figure><img src="../../../../.gitbook/assets/image (601).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Présentation

La **Xbox 360** est la deuxième console de salon de Microsoft. Elle sort en novembre 2005, un an avant la PlayStation 3 et la Wii, et lance la génération de la haute définition. Elle repose sur un processeur PowerPC à trois cœurs (Xenon) et une puce graphique ATI (Xenos) dotée de mémoire vidéo intégrée.

Son service en ligne **Xbox Live**, avec les succès, les profils et le **Xbox Live Arcade** (petits jeux téléchargeables), a marqué la génération. La console s'est vendue à environ 84 millions d'exemplaires, malgré les pannes des premiers modèles (le « cercle rouge de la mort »). Parmi ses jeux marquants : Halo 3, Gears of War, Forza Motorsport, Mass Effect, Fable II, Red Dead Redemption ou Left 4 Dead.

RetroBat utilise **Xenia**, le seul émulateur Xbox 360, en plusieurs versions : **Xenia Canary** (défaut), **Xenia Edge**, **Xenia Manager** et **Xenia** (version d'origine).

{% embed url="https://fr.wikipedia.org/wiki/Xbox_360" %}

## En bref

<table><thead><tr><th width="251.5"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\xbox360</code></td></tr><tr><td><strong>Extensions</strong></td><td>.iso .xex .xcp .zar .m3u .xbox360 .decomp</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>xenia-canary</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Non (Xenia reconnaît lui-même les manettes)</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr></tbody></table>

## Quel émulateur choisir ?

| Émulateur                 | Points forts                                                                                                                                                                                                                                         | Limites                                                                                                                                                                             |
| ------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **xenia-canary** (défaut) | Version la plus suivie et la plus compatible. Patchs de jeux, profils, réglages de la console (langue, résolution, format d'image).                                                                                                                  | Demande un PC récent (Direct3D 12 ou Vulkan).                                                                                                                                       |
| **xenia-edge**            | Version dérivée de Canary, avec des corrections et des réglages par jeu. Mode PAL 50 Hz.                                                                                                                                                             | Contrôles uniquement par SDL (pas de choix du type de contrôleur). Ses réglages par jeu passent avant ceux de RetroBat (voir [Guides](xbox-360.md#reglages-par-jeu-de-xenia-edge)). |
| **xenia-manager**         | Lanceur qui installe et gère les versions de Xenia. RetroBat peut utiliser la configuration de chaque jeu faite dans Xenia Manager. Trois versions : **canary**, **mousehook** (souris et clavier pour les jeux de tir), **netplay** (jeu en ligne). |                                                                                                                                                                                     |
| **xenia**                 | Version d'origine.                                                                                                                                                                                                                                   | N'évolue plus : moins compatible que Canary, moins d'options.                                                                                                                       |

La liste de compatibilité de Xenia Canary ([github.com/xenia-canary/game-compatibility](https://github.com/xenia-canary/game-compatibility/issues)) indique l'état de chaque jeu. Si un jeu ne fonctionne pas avec Canary, essayez Edge.

## BIOS

La Xbox 360 n'a pas de BIOS à fournir : Xenia remplace le système de la console par son propre code.

### Langue de la console

La langue des jeux est celle des réglages de la console émulée. Par défaut, RetroBat reprend la langue de RetroBat (anglais si elle n'existe pas sur Xbox 360). L'option **ÉMULATION > LANGUE** force une autre langue.

Avec Canary et Xenia Manager, RetroBat écrit aussi dans les réglages de la console (fichier `xconfig.settings`) le format d'image (**RAPPORT D'ASPECT DE LA CONSOLE**), la norme vidéo (**VIDÉO > STANDARD VIDÉO**) et la résolution de sortie (**VIDÉO > RÉSOLUTION INTERNE DU JEU**).

## Quel format de jeu ?

<table><thead><tr><th width="170.25">Format</th><th>Remarques</th></tr></thead><tbody><tr><td><strong>.iso</strong></td><td>Image du disque. C'est le format le plus courant. Un dossier qui contient une image <code>.iso</code> peut aussi être lancé : RetroBat prend la première image trouvée.</td></tr><tr><td><strong>.xex</strong></td><td>Jeu extrait : lancez le fichier <code>default.xex</code> du dossier du jeu.</td></tr><tr><td><strong>.zar</strong></td><td>Jeu compressé en un seul fichier (ZArchive), selon l'émulateur.</td></tr><tr><td><strong>.xcp</strong></td><td>Paquet de contenu Xbox Live, selon l'émulateur.</td></tr><tr><td><strong>.m3u</strong>, <strong>.xbox360</strong></td><td>Fichier texte qui donne le chemin du jeu, pour les jeux sans extension (Xbox Live Arcade, Games on Demand) : voir <a href="xbox-360.md#lancer-un-jeu-xbox-live-arcade-ou-games-on-demand">Guides</a>.</td></tr><tr><td>.decomp</td><td>Portage PC, voir la page <a href="../../autres/recomp.md"><strong>Recompilations</strong></a>.</td></tr></tbody></table>

Les archives `.zip` et `.7z` ne sont pas acceptées.

## Contrôles

### Configuration des manettes

RetroBat ne configure pas les manettes pour Xenia : l'émulateur les reconnaît lui-même, jusqu'à 4 joueurs. L'ordre des joueurs est celui de Xenia, il peut différer de celui de RetroBat.

L'option **CONTRÔLES > TYPE DE CONTRÔLEUR** (Canary, Xenia Manager, Xenia) choisit comment Xenia lit les manettes :

<table><thead><tr><th width="216.5">Choix</th><th>Utilisation</th></tr></thead><tbody><tr><td><strong>SDL</strong> (par défaut)</td><td>Toutes les manettes (Xbox, PlayStation, Switch…).</td></tr><tr><td><strong>MANETTE XBOX</strong></td><td>Manettes Xbox (XInput) uniquement.</td></tr><tr><td><strong>CLAVIER</strong></td><td>Clavier.</td></tr></tbody></table>

Xenia Edge utilise toujours SDL.

<table><thead><tr><th width="245.25">Xbox 360</th><th>Manette</th></tr></thead><tbody><tr><td>A, B, X, Y</td><td>SUD, EST, OUEST, NORD</td></tr><tr><td>LB, RB</td><td>L1, R1</td></tr><tr><td>LT, RT</td><td>L2, R2</td></tr><tr><td>Back, Start</td><td>SELECT, START</td></tr><tr><td>Clics des sticks</td><td>L3, R3</td></tr><tr><td>Croix directionnelle, sticks</td><td>Croix directionnelle, sticks</td></tr></tbody></table>

**Xenia Manager, version mousehook** : la souris et le clavier se règlent dans Xenia Manager, RetroBat ne les modifie pas.

### Raccourcis

<table><thead><tr><th width="247.75">Raccourci</th><th>Action</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quitter</td></tr></tbody></table>

Les autres raccourcis de RetroBat (menu, sauvegardes d'état, avance rapide…) ne sont pas gérés pour Xenia, qui n'a pas de sauvegardes d'état.

## Dossiers

<table><thead><tr><th width="327.75">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Configuration de Canary</td><td><code>emulators\xenia-canary\xenia-canary.config.toml</code></td></tr><tr><td>Configuration d'Edge</td><td><code>emulators\xenia-edge\xenia-edge.config.toml</code></td></tr><tr><td>Configuration de Xenia</td><td><code>emulators\xenia\xenia.config.toml</code></td></tr><tr><td>Émulateurs de Xenia Manager</td><td><code>emulators\xenia-manager\Emulators\Xenia Canary</code> (<code>Xenia Mousehook</code>, <code>Xenia Netplay</code>)</td></tr><tr><td>Bibliothèque de Xenia Manager</td><td><code>emulators\xenia-manager\Config\games.json</code></td></tr><tr><td>Contenu (sauvegardes, profils, mises à jour, contenus téléchargeables)</td><td><code>saves\xbox360\xenia\content</code></td></tr></tbody></table>

Toutes les versions de Xenia utilisent le même dossier `content` : les sauvegardes et les profils sont partagés entre Canary, Edge, Xenia Manager et Xenia.

Au premier lancement, RetroBat déplace dans `saves\xbox360\xenia\content` le dossier `content` de la version de Xenia lancée, pour garder vos sauvegardes. Si vous aviez aussi des sauvegardes dans une autre version, copiez le contenu de son dossier `content` (par exemple `emulators\xenia-edge\content`) dans `saves\xbox360\xenia\content`.

Avec une configuration de jeu de Xenia Manager, c'est le dossier réglé dans Xenia Manager qui est utilisé.

## Guides

### Lancer un jeu Xbox Live Arcade ou Games on Demand

Ces jeux se présentent sous forme d'une suite de dossiers, qui se termine par un fichier sans extension. Par exemple, pour Banjo-Tooie :

`roms\xbox360\Banjo Tooie\58410955\000D0000\ABB9CAB336175357D09F2D922735D23C62F90DDD`

1. Créez un fichier texte dans `roms\xbox360`, avec l'extension `.m3u` ou `.xbox360` (par exemple `Banjo Tooie.m3u`).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (602).png" alt=""><figcaption></figcaption></figure></div>

2. Écrivez sur la première ligne le chemin du fichier du jeu, à partir de `roms\xbox360` :

```
\Banjo Tooie\58410955\000D0000\ABB9CAB336175357D09F2D922735D23C62F90DDD
```

3. Mettez à jour la liste des jeux : c'est ce fichier qui apparaît dans RetroBat.

### Utiliser les profils

Les profils Xbox 360 gardent les sauvegardes et les succès de chaque joueur dans Xenia.

1. Créez le profil dans Xenia Canary ou Edge (menu de l'émulateur), puis quittez.
2. Dans RetroBat, choisissez **ÉMULATION > PROFIL JOUEUR 1** (à 4) et sélectionnez le dossier du profil dans `saves\xbox360\xenia\content` (son nom est l'identifiant du profil, 16 caractères).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (604).png" alt=""><figcaption></figcaption></figure></div>

Le profil doit se trouver dans `saves\xbox360\xenia\content`, sinon RetroBat l'ignore.

### Utiliser la configuration de Xenia Manager

1. Installez les versions de Xenia depuis Xenia Manager (`emulators\xenia-manager`), puis ajoutez vos jeux et réglez-les dans Xenia Manager.
2. Dans RetroBat, choisissez l'émulateur **xenia-manager** et la version (**canary**, **mousehook** ou **netplay**) pour le système ou le jeu.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (603).png" alt=""><figcaption></figcaption></figure></div>

Au lancement, RetroBat cherche le jeu dans la bibliothèque de Xenia Manager (`Config\games.json`), d'après le nom de son fichier. Si le jeu a une configuration, RetroBat la donne à Xenia et n'applique pas ses propres options. Sinon, les options de RetroBat sont utilisées, comme avec Canary.

### Réglages par jeu de Xenia Edge

Xenia Edge applique les réglages par jeu de son dossier `config` (`<identifiant du jeu>.config.toml`), qui passent avant ceux de RetroBat. Pour que les options de RetroBat s'appliquent, activez **ÉMULATION > IGNORER LES RÉGLAGES OPTIMISÉS** : le dossier est mis de côté pendant la partie, puis remis en place.

### Autres options utiles

<table><thead><tr><th width="315.25">Option</th><th>Effet</th></tr></thead><tbody><tr><td><strong>RÉSOLUTION INTERNE</strong></td><td>Augmente la résolution de rendu, de 1280x720 (par défaut) à 5120x2880.</td></tr><tr><td><strong>PILOTES > VIDÉO</strong></td><td>DIRECT3D12 ou VULKAN. Par défaut, Xenia choisit.</td></tr><tr><td><strong>ÉMULATION > CHARGER LES PATCHS</strong></td><td>Canary et Edge : applique les patchs de jeux du dossier <code>patches</code> de l'émulateur (corrections, 60 images par seconde…).</td></tr><tr><td><strong>VIDÉO > LIMITE DE FPS</strong></td><td>Canary et Edge : 60 images par seconde par défaut.</td></tr><tr><td><strong>ÉMULATION > RAFRAÎCHIR L'ÉTAT DES PAGES MÉMOIRE</strong></td><td>Canary et Edge : corrige les personnages invisibles dans les jeux Team Ninja.</td></tr><tr><td><strong>VIDÉO > RELECTURE DES RESOLVE</strong></td><td>Nécessaire pour certains jeux, mais ralentit beaucoup l'émulation.</td></tr><tr><td><strong>ÉMULATION > MASQUE DE LICENCE</strong></td><td>Active les contenus téléchargés (<strong>PREMIÈRE LICENCE ACTIVÉE</strong> par défaut).</td></tr></tbody></table>

## Problèmes connus

<table><thead><tr><th width="335.25">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Le jeu ne démarre pas</td><td>Vérifiez l'état du jeu dans la liste de compatibilité, puis essayez Edge, ou changez de pilote vidéo (<strong>PILOTES > VIDÉO</strong>).</td></tr><tr><td>La manette ne répond pas</td><td>Vérifiez <strong>CONTRÔLES > TYPE DE CONTRÔLEUR</strong> : <strong>SDL</strong> pour toutes les manettes, <strong>MANETTE XBOX</strong> pour les manettes Xbox.</td></tr><tr><td>Les joueurs ne sont pas dans le bon ordre</td><td>L'ordre est géré par Xenia : branchez les manettes dans l'ordre des joueurs avant de lancer le jeu.</td></tr><tr><td>Saccades au début d'une partie</td><td>Les shaders sont compilés au premier passage : laissez <strong>VIDÉO > COMPILATION DES SHADERS ASYNCHRONE</strong> activée.</td></tr><tr><td>Personnages ou objets invisibles</td><td>Activez <strong>ÉMULATION > RAFRAÎCHIR L'ÉTAT DES PAGES MÉMOIRE</strong> (jeux Team Ninja), ou essayez <strong>VIDÉO > RELECTURE DES RESOLVE</strong>.</td></tr><tr><td>Les options de RetroBat ne s'appliquent pas avec Edge</td><td>Activez <strong>ÉMULATION > IGNORER LES RÉGLAGES OPTIMISÉS</strong> (voir <a href="xbox-360.md#reglages-par-jeu-de-xenia-edge">Guides</a>).</td></tr><tr><td>Les options de RetroBat ne s'appliquent pas avec Xenia Manager</td><td>Le jeu a une configuration dans Xenia Manager : réglez-le dans Xenia Manager.</td></tr><tr><td>Un jeu Xbox Live Arcade n'apparaît pas</td><td>Créez un fichier <code>.m3u</code> ou <code>.xbox360</code> (voir <a href="xbox-360.md#lancer-un-jeu-xbox-live-arcade-ou-games-on-demand">Guides</a>).</td></tr></tbody></table>
