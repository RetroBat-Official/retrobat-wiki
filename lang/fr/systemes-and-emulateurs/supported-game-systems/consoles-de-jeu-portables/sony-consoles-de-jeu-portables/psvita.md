---
description: Sony
---

# PlayStation Vita

<div align="left"><figure><img src="../../../../.gitbook/assets/image (590).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Présentation

La **PlayStation Vita** sort en décembre 2011 au Japon, puis en février 2012 en Europe et aux États-Unis. Elle succède à la PSP avec un grand écran OLED tactile, un pavé tactile à l'arrière, deux sticks analogiques, un gyroscope et deux caméras.

Sony lance en 2013 un modèle plus fin à écran LCD, puis la **PlayStation TV**, une petite console de salon qui fait tourner les jeux Vita sur la télévision avec une manette DualShock. La production s'arrête en 2019. La console accueille des jeux comme Uncharted: Golden Abyss, Gravity Rush, Persona 4 Golden, Tearaway ou WipEout 2048, et de nombreux jeux indépendants.

**Vita3K**, l'émulateur proposé par RetroBat, est le premier émulateur de PS Vita capable de lancer des jeux du commerce. Il progresse vite, mais la compatibilité varie beaucoup d'un jeu à l'autre.

{% embed url="https://fr.wikipedia.org/wiki/PlayStation_Vita" %}

## En bref

<table><thead><tr><th width="270.25"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\psvita</code></td></tr><tr><td><strong>Extensions</strong></td><td>.m3u .psvita .vpk .zip .decomp</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>vita3k</td></tr><tr><td><strong>BIOS</strong></td><td>Firmware PS Vita à installer dans Vita3K (automatique depuis <code>bios\vita3k</code>, voir BIOS)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, gérée par Vita3K</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr></tbody></table>

## Quel émulateur choisir ?

Vita3K est le seul émulateur PS Vita de RetroBat.

<table><thead><tr><th width="122">Émulateur</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>vita3k</strong> (défaut)</td><td>Lance de nombreux jeux du commerce et homebrews, résolution augmentée, textures personnalisées, codes de triche, mode PlayStation TV pour jouer à plusieurs.</td><td>Émulateur jeune : beaucoup de jeux ont encore des bugs ou ne démarrent pas. Pas de sauvegardes instantanées.</td></tr></tbody></table>

La liste de compatibilité de Vita3K ([vita3k.org](https://vita3k.orghttps/vita3k.org/compatibility)) indique l'état de chaque jeu.

## BIOS

Vita3K a besoin du **firmware** de la PS Vita. Il se compose de trois paquets, tous fournis par Sony :

| Fichier                 | Contenu                           | Utilité                                                               |
| ----------------------- | --------------------------------- | --------------------------------------------------------------------- |
| `PSP2UPDAT.PUP`         | Firmware de la console            | Nécessaire à la plupart des jeux                                      |
| `PSP2UPDAT_FONT.PUP`    | Polices du système                | Recommandé : sans lui, les textes de certains jeux ne s'affichent pas |
| `PSP2UPDAT_PREINST.PUP` | Contenu préinstallé de la console | Facultatif                                                            |

Les trois fichiers se téléchargent sous le même nom (`PSP2UPDAT.PUP`) : renommez-les comme dans le tableau. Les noms `font_fresh.pup` et `preinst_fresh.pup` sont aussi acceptés pour les polices et le contenu préinstallé.

RetroBat contrôle ces trois fichiers comme BIOS optionnels : une fois le firmware installé, ils ne sont plus nécessaires.

Le firmware ne se lit pas depuis le dossier `bios` : il doit être **installé** dans le dossier de données de Vita3K. RetroBat s'en charge :

1. Téléchargez le firmware sur le site de PlayStation (page « Mise à jour du logiciel système PS Vita »). Les liens vers les polices et le contenu préinstallé sont donnés par la fenêtre d'accueil de Vita3K (**Help > View Welcome Dialog**).
2. Renommez les fichiers et placez-les dans `bios\vita3k`.
3. Lancez un jeu : RetroBat installe les paquets manquants avant de démarrer le jeu. Une fenêtre indique l'installation en cours.

L'installation n'a lieu qu'une fois. Les fichiers de `bios\vita3k` peuvent ensuite être conservés pour une réinstallation.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (591).png" alt=""><figcaption></figcaption></figure></div>

### Installer le firmware depuis Vita3K

Vous pouvez aussi installer le firmware depuis l'interface de Vita3K :

1. Lancez une première fois un jeu depuis RetroBat, puis quittez-le : Vita3K enregistre ainsi le dossier de données de RetroBat.
2. Ouvrez Vita3K depuis le menu des émulateurs de RetroBat.
3. Choisissez **File > Install Firmware (.PUP)** et installez chaque fichier `.PUP` l'un après l'autre.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (592).png" alt=""><figcaption></figcaption></figure></div>

Si vous ouvrez Vita3K sans avoir jamais lancé de jeu, il propose son propre dossier de données (dans le dossier `AppData` de Windows) : le firmware installé à cet endroit n'est pas vu par RetroBat.

## Quel format de jeu ?

Les jeux PS Vita doivent être **installés** dans Vita3K avant de pouvoir être lancés. RetroBat installe automatiquement les paquets et les dossiers au premier lancement.

<table><thead><tr><th width="162">Format</th><th>Installation</th><th>Remarques</th></tr></thead><tbody><tr><td><strong>.vpk</strong></td><td>Automatique au premier lancement</td><td>Paquet de jeu ou de homebrew.</td></tr><tr><td><strong>.zip</strong></td><td>Automatique au premier lancement</td><td>Jeu décrypté compressé (dump NoNpDrm par exemple).</td></tr><tr><td><strong>Dossier <code>.psvita</code></strong></td><td>Automatique au premier lancement</td><td>Le dossier du jeu, qui contient <code>eboot.bin</code> et <code>sce_sys</code>, renommé avec <code>.psvita</code> à la fin.</td></tr><tr><td>.m3u</td><td>Jeu déjà installé</td><td>Fichier texte qui contient l'identifiant du jeu (voir <a href="psvita.md#utiliser-un-fichier-.m3u">Guides</a>).</td></tr><tr><td>Fichier <code>.psvita</code></td><td>Jeu déjà installé</td><td>Fichier vide dont le nom contient l'identifiant du jeu entre crochets : <code>WipEout 2048 [PCSA00029].psvita</code>.</td></tr><tr><td>.decomp</td><td>—</td><td>Portage PC, voir la page <a href="../../autres/recomp.md"><strong>Recompilations</strong></a>.</td></tr></tbody></table>

RetroBat lit l'identifiant du jeu (par exemple `PCSE00000`) dans le fichier `param.sfo` du paquet ou du dossier. S'il ne le trouve pas, il le cherche entre crochets dans le nom du fichier : `Street Fighter X Tekken [PCSE00005].vpk`.

Les fichiers `.pkg` ne sont pas lancés par RetroBat : installez-les depuis Vita3K (**File > Install Package (.pkg)**), avec leur licence (zRIF), puis utilisez un fichier `.m3u`.

## Contrôles

### Configuration automatique

RetroBat ne configure pas les boutons des manettes : Vita3K reconnaît lui-même les manettes et applique sa disposition par défaut à chaque lancement. Les manettes Xbox, DualShock 4 et DualSense fonctionnent sans réglage.

<table><thead><tr><th width="305.25">PS Vita</th><th>Manette</th></tr></thead><tbody><tr><td>Croix</td><td>SUD</td></tr><tr><td>Rond</td><td>EST</td></tr><tr><td>Carré</td><td>OUEST</td></tr><tr><td>Triangle</td><td>NORD</td></tr><tr><td>L, R</td><td>L1, R1</td></tr><tr><td>SELECT, START</td><td>SELECT, START</td></tr><tr><td>Croix directionnelle, sticks</td><td>Croix directionnelle, sticks</td></tr><tr><td>Bouton PS</td><td>GUIDE</td></tr></tbody></table>

* Les boutons L2, R2, L3 et R3 et les vibrations n'existent que sur la PlayStation TV : ils ne fonctionnent qu'avec l'option **CONTRÔLES > MODE PLAYSTATION TV**.
* Le gyroscope des manettes compatibles (DualShock 4, DualSense…) est utilisé pour les jeux qui en ont besoin.
* L'option **ÉMULATION > BOUTON DE CONFIRMATION** choisit le bouton qui valide dans les menus du système : **CROIX** (par défaut) ou **CERCLE** (convention japonaise).

### Écran et pavé tactiles

<table><thead><tr><th width="239.5">Action</th><th width="163.25">Souris</th><th>Manette DualShock 4 / DualSense</th></tr></thead><tbody><tr><td>Toucher l'écran avant</td><td>Clic gauche</td><td>Pavé tactile</td></tr><tr><td>Toucher le pavé arrière</td><td>Clic droit</td><td>Pavé tactile, après un appui sur le pavé</td></tr></tbody></table>

Pour le pavé tactile de la manette, un appui sur le pavé (ou la touche T du clavier) passe de l'écran avant au pavé arrière, et inversement.

### Clavier

Au clavier, Vita3K utilise ces touches par défaut :

<table><thead><tr><th width="284">PS Vita</th><th>Clavier</th></tr></thead><tbody><tr><td>Stick gauche</td><td>W, A, S, D</td></tr><tr><td>Stick droit</td><td>I, J, K, L</td></tr><tr><td>Croix directionnelle</td><td>Flèches</td></tr><tr><td>Triangle, Rond, Croix, Carré</td><td>V, C, X, Z</td></tr><tr><td>L, R</td><td>Q, E</td></tr><tr><td>SELECT, START</td><td>MAJ droite, ENTRÉE</td></tr><tr><td>Bouton PS</td><td>P</td></tr></tbody></table>

Les touches peuvent être modifiées dans Vita3K (**Settings > Controls**, catégorie **Keyboard**).

### Raccourcis

| Raccourci          | Action                                  | Clavier |
| ------------------ | --------------------------------------- | ------- |
| **HOTKEY + START** | Quitter                                 | ÉCHAP   |
| —                  | Plein écran                             | F11     |
| —                  | Passer de l'écran avant au pavé arrière | T       |

La capture d'écran n'a pas de touche par défaut : elle peut être ajoutée dans Vita3K (**Settings > Controls**, catégorie **Hotkeys**), comme le remplacement des textures.

## Dossiers

<table><thead><tr><th width="352.75">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Dossier de données de Vita3K (pref-path)</td><td><code>saves\psvita\vita3k</code></td></tr><tr><td>Jeux installés</td><td><code>saves\psvita\vita3k\ux0\app\&#x3C;identifiant></code></td></tr><tr><td>Mises à jour et contenus additionnels (DLC) installés</td><td><code>saves\psvita\vita3k\ux0\patch</code>, <code>saves\psvita\vita3k\ux0\addcont</code></td></tr><tr><td>Sauvegardes des jeux</td><td><code>saves\psvita\vita3k\ux0\user\00\savedata</code></td></tr><tr><td>Fichiers du firmware à installer</td><td><code>bios\vita3k</code></td></tr><tr><td>Configuration de Vita3K</td><td><code>emulators\vita3k\config.yml</code></td></tr><tr><td>Configurations par jeu de Vita3K</td><td><code>emulators\vita3k\config</code></td></tr><tr><td>Textures personnalisées</td><td><code>emulators\vita3k\textures\import\&#x3C;identifiant></code></td></tr><tr><td>Codes de triche</td><td><code>emulators\vita3k\cheats</code></td></tr><tr><td>Patchs</td><td><code>emulators\vita3k\patch</code></td></tr><tr><td>Captures d'écran</td><td><code>emulators\vita3k\screenshots</code></td></tr></tbody></table>

Le dossier de données peut être déplacé avec l'option **ÉMULATION > CHANGER LE DOSSIER PREF-PATH**. Il contient les jeux installés : prévoyez la place nécessaire.

**Mode portable de Vita3K** : si un dossier `portable` non vide se trouve à côté de `Vita3K.exe`, Vita3K y range tout (configuration, données dans `portable\fs`, triche, captures…) et l'option CHANGER LE DOSSIER PREF-PATH est ignorée. Un dossier `portable` vide est supprimé par RetroBat.

## Guides

### Ajouter un jeu

1. Copiez le fichier `.vpk` ou `.zip`, ou le dossier du jeu renommé en `.psvita`, dans `roms\psvita`.
2. Mettez à jour la liste des jeux de RetroBat.
3. Lancez le jeu. Au premier lancement, RetroBat fait installer le jeu par Vita3K : une fenêtre indique la progression, puis le jeu démarre. Les lancements suivants sont directs.

Une fois le jeu installé, le paquet n'est plus utilisé. Pour gagner de la place, vous pouvez le remplacer par un fichier `.m3u`.

### Utiliser un fichier .m3u

Le fichier `.m3u` lance un jeu déjà installé dans Vita3K. Créez dans `roms\psvita` un fichier texte nommé comme le jeu, par exemple `WipEout 2048.m3u`, qui contient uniquement l'identifiant du jeu :

```
PCSA00029
```

L'identifiant est affiché dans la liste des jeux de Vita3K. C'est aussi le nom du dossier du jeu dans `saves\psvita\vita3k\ux0\app`.

### Mises à jour et DLC

Les mises à jour et les contenus additionnels s'installent depuis Vita3K (**File > Install Archive (.zip / .vpk / .vci)** ou **File > Install Package (.pkg)**). Ouvrez Vita3K depuis le menu des émulateurs de RetroBat.

### Jouer à plusieurs

L'option **CONTRÔLES > MODE PLAYSTATION TV** émule une PlayStation TV, qui accepte jusqu'à 4 manettes pour les jeux multijoueurs en local. Elle active aussi L2, R2, L3, R3 et les vibrations. Les jeux qui demandent l'écran tactile peuvent ne pas fonctionner dans ce mode.

### Textures personnalisées

Vita3K peut remplacer les textures d'un jeu par des textures en haute définition.

1. Placez le pack de textures dans `emulators\vita3k\textures\import`, dans un dossier au nom de l'identifiant du jeu (par exemple `import\PCSA00029`).
2. Activez l'option **RENDU VISUEL > TEXTURES PERSONNALISÉES**.

### Codes de triche

Vita3K lit les bases de codes des plugins FinalCheat / VitaCheat (fichiers `.psv`).

1. Placez le fichier de codes dans `emulators\vita3k\cheats`, nommé avec l'identifiant du jeu (par exemple `PCSA00147.psv`).
2. Ouvrez Vita3K depuis le menu des émulateurs de RetroBat, puis **Manage > Cheats**.
3. Cochez les codes à activer et cliquez sur **Save** : ils seront actifs au prochain lancement du jeu.

L'option **ÉMULATION > ACTIVER LA TRICHE**, active par défaut, permet de désactiver tous les codes sans les décocher.

### Réglages par jeu de Vita3K

Vita3K peut enregistrer des réglages propres à chaque jeu. Par défaut, RetroBat les ignore et applique ses propres réglages. L'option **ÉMULATION > UTILISER LA CONFIG PAR JEU DE VITA3K** utilise les réglages par jeu de Vita3K, qui passent alors avant ceux de RetroBat.

### Autres options utiles

<table><thead><tr><th width="324">Option</th><th>Effet</th></tr></thead><tbody><tr><td><strong>RÉSOLUTION INTERNE</strong></td><td>Augmente la résolution de rendu (jusqu'à 8X). La résolution native est 960x544.</td></tr><tr><td><strong>ÉMULATION > LANGUE</strong></td><td>Langue de la console émulée. Par défaut, c'est celle de RetroBat.</td></tr><tr><td><strong>ÉMULATION > HACK FPS</strong></td><td>Fait tourner certains jeux à 30 images par seconde à 60.</td></tr><tr><td><strong>VIDÉO > MAPPAGE MÉMOIRE</strong></td><td>Vulkan uniquement. Améliore les performances et corrige de nombreux bugs graphiques, mais peut être instable sur certaines cartes graphiques.</td></tr><tr><td><strong>VIDÉO > PRÉCISION DE RENDU</strong></td><td><strong>HAUTE</strong> (par défaut) ou <strong>STANDARD</strong>, plus rapide mais moins précise.</td></tr><tr><td><strong>PILOTES > VIDÉO</strong></td><td>Vulkan (par défaut) ou OpenGL.</td></tr><tr><td><strong>AUDIO > SUPPORT AUDIO NGS</strong></td><td>Bibliothèque audio utilisée par de nombreux jeux. À désactiver seulement si un jeu plante ou a des problèmes de son.</td></tr><tr><td><strong>MODULES > MÉTHODE DE GESTION DES MODULES</strong></td><td><strong>AUTOMATIQUE</strong> laisse Vita3K choisir les modules du firmware à charger (recommandé). <strong>RÉGLAGES DE L'ÉMULATEUR</strong> garde les modules choisis dans Vita3K.</td></tr></tbody></table>

## Problèmes connus

<table><thead><tr><th width="337.75">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Message « PS Vita game … is not installed in Vita3K »</td><td>Le fichier <code>.m3u</code> ou <code>.psvita</code> désigne un jeu qui n'est pas installé. Vérifiez l'identifiant, ou lancez une fois le paquet <code>.vpk</code> / <code>.zip</code> du jeu pour l'installer.</td></tr><tr><td>Le premier lancement d'un jeu semble bloqué</td><td>Vita3K installe le jeu : attendez la fin de la barre de progression. Les gros jeux peuvent prendre plusieurs minutes.</td></tr><tr><td>Textes manquants ou carrés à la place des lettres</td><td>Le pack de polices n'est pas installé : ajoutez <code>PSP2UPDAT_FONT.PUP</code> dans <code>bios\vita3k</code> (voir BIOS).</td></tr><tr><td>Le jeu ne démarre pas ou plante</td><td>Vérifiez son état dans la liste de compatibilité de Vita3K et que le firmware est installé. Essayez de changer <strong>MAPPAGE MÉMOIRE</strong> ou le pilote vidéo.</td></tr><tr><td>Écran noir avec OpenGL sur un processeur graphique AMD intégré</td><td>Activez <strong>VIDÉO > DÉSACTIVER LE MASK BIT (OPENGL)</strong>.</td></tr><tr><td>Les touches modifiées dans Vita3K reviennent à leur valeur par défaut</td><td>RetroBat réinitialise les boutons des manettes à chaque lancement. Les touches du clavier, elles, sont conservées.</td></tr><tr><td>Deux manettes identiques ne fonctionnent pas en mode PlayStation TV</td><td>Limite de Vita3K : utilisez des manettes de modèles différents.</td></tr><tr><td>Mes réglages RetroBat ne sont pas appliqués à un jeu</td><td>Un réglage par jeu de Vita3K est utilisé : désactivez <strong>UTILISER LA CONFIG PAR JEU DE VITA3K</strong>.</td></tr></tbody></table>
