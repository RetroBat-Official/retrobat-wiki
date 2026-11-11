---
description: Nintendo
---

# Wii

<div align="left"><figure><img src="../../../../.gitbook/assets/image (514).png" alt="" width="425"><figcaption></figcaption></figure></div>

## Présentation

La **Wii** est la cinquième console de salon de Nintendo, après la GameCube. Elle sort en Amérique du Nord en novembre 2006, au Japon et en Europe en décembre 2006. Plutôt que de miser sur la puissance, Nintendo mise sur une nouvelle façon de jouer : la **Wiimote**, une télécommande qui détecte les mouvements et sert de pointeur grâce à une barre infrarouge (la _Sensor Bar_) posée près du téléviseur.

On la tient à la verticale comme une télécommande, à l'horizontale comme une manette NES, ou avec le **Nunchuk**, une seconde poignée avec un stick, branchée dessus. D'autres accessoires s'y ajoutent : la **manette classique**, la **Balance Board** de Wii Fit, le volant Wii Wheel, les guitares et batteries de Guitar Hero et Rock Band…

Succès mondial, elle se vend à plus de 100 millions d'exemplaires. Elle lit aussi les jeux GameCube, et propose des jeux téléchargeables : **WiiWare** et **Console Virtuelle** (jeux NES, Super Nintendo, Nintendo 64, Mega Drive…). Sa ludothèque compte de nombreux classiques : Wii Sports, Mario Kart Wii, Super Mario Galaxy 1 et 2, New Super Mario Bros. Wii, The Legend of Zelda: Twilight Princess et Skyward Sword, Super Smash Bros. Brawl, Metroid Prime 3, Donkey Kong Country Returns, Xenoblade Chronicles, Wii Fit…

**Les jeux GameCube vont dans le système** [**GameCube**](gamecube.md) (`roms\gamecube`), pas dans le système Wii.

{% embed url="https://fr.wikipedia.org/wiki/Wii" %}

## En bref

<table><thead><tr><th width="257.75"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\wii</code></td></tr><tr><td><strong>Extensions</strong></td><td>.gcz .iso .ciso .dol .wbfs .wad .rvz .wia .zip .7z .squashfs .json .elf .decomp</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>dolphin</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro, Dolphin</td></tr><tr><td><strong>RetroAchievements</strong></td><td>cores libretro, Dolphin</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr><tr><td><strong>Pistolets</strong></td><td>Dolphin</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="117.5">Émulateur</th><th width="125.25">Pour qui ?</th><th width="279.5">Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>dolphin</strong> (par défaut)</td><td>Tout le monde</td><td>Le plus compatible et le plus complet : vraies Wiimotes (DolphinBar), Wiimote émulée réglable jeu par jeu, accessoires (guitare, batterie, uDraw…), pistolets, HD, packs de textures, jeux modifiés (Riivolution).</td><td>—</td></tr><tr><td><strong>lr-dolphin</strong></td><td>Utilisateurs de RetroArch</td><td>Fonctions de RetroArch (shaders, menu RetroArch).</td><td>Basé sur une version plus ancienne de Dolphin, moins compatible, moins de types de Wiimote. Ne lit pas les .zip, .7z et .json.</td></tr></tbody></table>

**Dans le doute, gardez dolphin.**

## BIOS

Aucun BIOS n'est nécessaire : Dolphin lance les jeux Wii directement.

Le **menu Wii** (l'écran d'accueil de la console, avec ses chaînes) est optionnel : voir [Guides](wii.md#utiliser-le-menu-wii).

### Changer la langue des jeux

C'est la langue de la console : les jeux l'utilisent quand ils la proposent (c'est le cas de la plupart des jeux européens).

Dans les options avancées du système ou du jeu (Dolphin), réglez **ÉMULATION > LANGUE** : japonais, anglais, allemand, français, espagnol, italien ou néerlandais. Par défaut, c'est la langue de RetroBat.

{% hint style="info" %}
Dolphin crée les réglages de la console au premier lancement d'un jeu Wii. La langue choisie ne s'applique donc qu'à partir du deuxième lancement.
{% endhint %}

## Quel format de jeu ?

<table><thead><tr><th width="196.5">Format</th><th width="150.75">dolphin</th><th width="94.5">lr-dolphin</th><th>Remarques</th></tr></thead><tbody><tr><td><strong>.iso</strong> (conseillé)</td><td>✔</td><td>✔</td><td>Image du disque, non compressée (4,4 Go, ou 8 Go pour les doubles couches).</td></tr><tr><td><strong>.rvz</strong> (conseillé)</td><td>✔</td><td>✔</td><td>Format compressé de Dolphin, sans perte.</td></tr><tr><td>.wbfs</td><td>✔</td><td>✔</td><td>Format des chargeurs USB de la Wii.</td></tr><tr><td>.gcz / .wia / .ciso</td><td>✔</td><td>✔</td><td>Autres formats compressés.</td></tr><tr><td>.wad</td><td>✔</td><td>✔</td><td>Jeux <strong>WiiWare</strong> et <strong>Console Virtuelle</strong>, chaînes.</td></tr><tr><td>.dol / .elf</td><td>✔</td><td>✔</td><td>Programmes homebrew.</td></tr><tr><td>.zip / .7z / .squashfs</td><td>✔ (décompressé au lancement)</td><td>✘</td><td>Chargement plus lent.</td></tr><tr><td>.json</td><td>✔</td><td>✘</td><td>Jeux modifiés avec des patchs Riivolution.</td></tr></tbody></table>

Pour convertir un jeu en .rvz, ouvrez Dolphin (`emulators\dolphin-emu\Dolphin.exe`), faites un clic droit sur le jeu, puis **Convertir le fichier…** et choisissez le format **RVZ**.

## Contrôles

### Trois façons de jouer

L'option **CONTRÔLES > TYPE DE WIIMOTE** permet de choisir comment vous jouez :

<table><thead><tr><th width="246.5">TYPE DE WIIMOTE</th><th>Ce que vous utilisez</th></tr></thead><tbody><tr><td><strong>ÉMULÉE</strong> (par défaut)</td><td>Votre manette (Xbox, PlayStation…) joue le rôle de la Wiimote et de ses accessoires. RetroBat la configure automatiquement, jusqu'à 4 joueurs.</td></tr><tr><td><strong>RÉELLE</strong></td><td>De vraies Wiimotes, connectées avec une <strong>DolphinBar</strong> ou en Bluetooth. Vos manettes jouent alors le rôle de <strong>manettes GameCube</strong> (pour les jeux Wii qui les acceptent).</td></tr><tr><td><strong>RÉELLE COMME ÉMULÉE</strong></td><td>De vraies Wiimotes, lues par Dolphin comme une Wiimote émulée. Les variantes <strong>(NUNCHUK)</strong> et <strong>(CC)</strong> ajoutent un Nunchuk ou une manette classique émulés.</td></tr></tbody></table>

### Wiimote émulée : choisir la bonne manette

Les jeux Wii ne se jouent pas tous de la même façon : certains tiennent la Wiimote à la verticale, d'autres à l'horizontale, avec un Nunchuk ou avec la manette classique. L'option **CONTRÔLES > TYPE DE WIIMOTE ÉMULÉE**, à [régler **jeu par jeu**](../../../../navigation/game-options.md), choisit le type de contrôleur que reçoit le jeu.

Le nom des modes **WIIMOTE : X/Y** indique le rôle des deux sticks de votre manette, le stick gauche d'abord, puis le stick droit :

<table><thead><tr><th width="206.5">Mot</th><th>Rôle du stick</th></tr></thead><tbody><tr><td><strong>CURSEUR</strong></td><td>Viser l'écran (pointeur infrarouge).</td></tr><tr><td><strong>BALANCEMENT</strong></td><td>Agiter la Wiimote dans une direction (coup d'épée, lancer…).</td></tr><tr><td><strong>INCLINAISON</strong></td><td>Pencher la Wiimote.</td></tr><tr><td><strong>NUNCHUK</strong></td><td>Stick du Nunchuk.</td></tr></tbody></table>

Par exemple, **WIIMOTE : NUNCHUK/CURSEUR** place le stick du Nunchuk sur le stick gauche et le pointeur sur le stick droit.

Quelques exemples de réglages :

| Jeu                                                                     | TYPE DE WIIMOTE ÉMULÉE        |
| ----------------------------------------------------------------------- | ----------------------------- |
| New Super Mario Bros. Wii, Kirby's Return to Dream Land, Mario Kart Wii | WIIMOTE : HORIZONTALE         |
| Super Mario Galaxy, Zelda: Twilight Princess, Metroid Prime 3           | WIIMOTE : NUNCHUK/CURSEUR     |
| Wii Sports                                                              | WIIMOTE : CURSEUR/BALANCEMENT |
| Xenoblade Chronicles, Monster Hunter Tri                                | CLASSIC CONTROLLER            |

### Wiimote verticale (par défaut)

Sans réglage particulier, la Wiimote est tenue à la verticale, sans accessoire :

<table><thead><tr><th width="275.25">Manette RetroBat</th><th>Wiimote</th></tr></thead><tbody><tr><td>SUD</td><td>A</td></tr><tr><td>EST</td><td>B</td></tr><tr><td>OUEST</td><td>1</td></tr><tr><td>NORD</td><td>2</td></tr><tr><td>L1 / R1</td><td>− / +</td></tr><tr><td>SELECT</td><td>HOME</td></tr><tr><td>Croix directionnelle</td><td>Croix directionnelle</td></tr><tr><td>Stick gauche</td><td>Pointeur (viser l'écran)</td></tr><tr><td>Stick droit</td><td>Inclinaison</td></tr><tr><td>L3</td><td>Figer le pointeur</td></tr><tr><td>R3</td><td>Inclinaison réduite</td></tr></tbody></table>

### Wiimote horizontale

Mode **WIIMOTE : HORIZONTALE**, pour les jeux qui se jouent comme une manette NES :

<table><thead><tr><th width="261.5">Manette RetroBat</th><th>Wiimote</th></tr></thead><tbody><tr><td>SUD</td><td>2</td></tr><tr><td>OUEST</td><td>1</td></tr><tr><td>NORD</td><td>A</td></tr><tr><td>EST</td><td>B</td></tr><tr><td>L2</td><td>Secouer</td></tr><tr><td>L1 / R1</td><td>Incliner à gauche / à droite</td></tr><tr><td>SELECT / START</td><td>− / +</td></tr><tr><td>Croix directionnelle</td><td>Croix directionnelle</td></tr></tbody></table>

### Wiimote + Nunchuk

Modes **WIIMOTE : NUNCHUK/…** et **WIIMOTE : …/NUNCHUK**. Les boutons A, B, 1 et 2 restent ceux de la Wiimote verticale :

<table><thead><tr><th width="305.25">Manette RetroBat</th><th>Wiimote + Nunchuk</th></tr></thead><tbody><tr><td>SUD / EST / OUEST / NORD</td><td>A / B / 1 / 2</td></tr><tr><td>L1 / R1</td><td>C / Z (Nunchuk)</td></tr><tr><td>SELECT / START</td><td>− / +</td></tr><tr><td>Croix directionnelle</td><td>Croix directionnelle</td></tr><tr><td>Stick du côté NUNCHUK</td><td>Stick du Nunchuk</td></tr><tr><td>Autre stick</td><td>Curseur, balancement ou inclinaison, selon le mode</td></tr><tr><td>L2 / R2 (mode NUNCHUK/…)</td><td>Secouer le Nunchuk / secouer la Wiimote</td></tr><tr><td>L2 / R2 (mode …/NUNCHUK)</td><td>Secouer la Wiimote / secouer le Nunchuk</td></tr></tbody></table>

**BALANCEMENT DU NUNCHUK** remplace le geste « secouer le Nunchuk » par un balancement, pour les jeux qui le demandent.

### Manette classique

Mode **CLASSIC CONTROLLER** :

<table><thead><tr><th width="227.25">Manette RetroBat</th><th width="234.5">Manette classique</th><th>Avec INVERSER LES BOUTONS A/B/X/Y = DISPOSITION XBOX</th></tr></thead><tbody><tr><td>EST</td><td>A</td><td>B</td></tr><tr><td>SUD</td><td>B</td><td>A</td></tr><tr><td>NORD</td><td>X</td><td>Y</td></tr><tr><td>OUEST</td><td>Y</td><td>X</td></tr><tr><td>L1 / R1</td><td>ZL / ZR</td><td>ZL / ZR</td></tr><tr><td>L2 / R2</td><td>L / R</td><td>L / R</td></tr><tr><td>SELECT / START</td><td>− / +</td><td>− / +</td></tr><tr><td>Sticks, croix directionnelle</td><td>Sticks, croix directionnelle</td><td>Sticks, croix directionnelle</td></tr></tbody></table>

### Accessoires

<table><thead><tr><th width="339">Mode</th><th>Commandes</th></tr></thead><tbody><tr><td><strong>WIIMOTE : Guitare</strong></td><td>Frettes : verte = SUD ou L2, rouge = L1 ou EST, jaune = R1, bleue = R2, orange = OUEST. Appuyer sur une frette gratte aussi la corde. Vibrato : sticks gauche / droite. Star Power : SELECT ou sticks haut / bas. + = START.</td></tr><tr><td><strong>WIIMOTE : Batterie (Rock Band)</strong></td><td>Rouge = L2 ou EST, jaune = L1 ou croix haut / gauche, bleu = R1 ou croix bas / droite, vert = R2 ou SUD, pédale = sticks gauche / droite.</td></tr><tr><td><strong>WIIMOTE : Batterie (Guitar Hero)</strong></td><td>Rouge = L2 ou EST, jaune = L1, bleu = R1, orange = R2, vert = SUD, pédale = sticks gauche / droite.</td></tr><tr><td><strong>WIIMOTE : TaikoDrum</strong></td><td>Centre du tambour (Don) = L2 / R2, bord (Ka) = L1 / R1.</td></tr><tr><td><strong>WIIMOTE : uDraw</strong> et <strong>WIIMOTE : tablette Drawsome</strong></td><td>Stylet = stick gauche, appuyer = SUD, lever = EST (uDraw : bascule = L1 / R1).</td></tr><tr><td><strong>WIIMOTE : PLATINE DJ</strong></td><td>Boutons verts / rouges / bleus = L1 / R1 / OUEST, platine = sticks, crossfader = L2 / R2, effets = L3 / R3.</td></tr></tbody></table>

### Choisir le mode avec le nom du fichier

Au lieu de régler l'option jeu par jeu, vous pouvez ajouter un code dans le nom du fichier du jeu, juste avant l'extension. Par exemple, `Super Mario Galaxy.ni.rvz` lance le jeu en mode WIIMOTE : NUNCHUK/CURSEUR.

<table><thead><tr><th width="301.5">Code</th><th>Mode</th></tr></thead><tbody><tr><td><code>.side.</code></td><td>Wiimote horizontale</td></tr><tr><td><code>.cc.</code></td><td>Manette classique</td></tr><tr><td><code>.is.</code> <code>.it.</code> <code>.in.</code></td><td>Curseur sur le stick gauche, puis balancement, inclinaison ou Nunchuk sur le stick droit</td></tr><tr><td><code>.si.</code> <code>.ti.</code> <code>.ni.</code></td><td>Balancement, inclinaison ou Nunchuk sur le stick gauche, curseur sur le stick droit</td></tr><tr><td><code>.st.</code> <code>.ts.</code> <code>.sn.</code> <code>.ns.</code> <code>.tn.</code> <code>.nt.</code></td><td>Autres combinaisons (s = balancement, t = inclinaison, n = Nunchuk)</td></tr><tr><td><code>.guitar.</code> <code>.drumsrb.</code> <code>.drumsgh.</code> <code>.tatacon.</code> <code>.udraw.</code> <code>.ds.</code> <code>.tt.</code></td><td>Guitare, batterie Rock Band, batterie Guitar Hero, tambour Taiko, uDraw, tablette Drawsome, platine DJ</td></tr></tbody></table>

### Autres réglages de la Wiimote émulée

* **NOMBRE DE WIIMOTES** : certains jeux passent en multijoueur dès que plusieurs manettes sont branchées. Réglez-le sur **1** pour les en empêcher.
* **ACTIVER LE MOTION INPUT** : avec une manette qui a un capteur de mouvement (DualShock 4, DualSense, Switch Pro…), bouger la manette remplace l'inclinaison et le secouement de la Wiimote.
* **CURSEUR IR RELATIF** : désactivez-le pour que le pointeur revienne au centre quand vous relâchez le stick.
* **MASQUER LE POINTEUR WIIMOTE** : le pointeur disparaît de l'écran quand vous ne le bougez plus.

### Vraies Wiimotes (DolphinBar)

La façon la plus simple d'utiliser de vraies Wiimotes est la **DolphinBar** de Mayflash, qui sert à la fois de récepteur et de Sensor Bar :

1. Réglez la DolphinBar en **mode 4**.
2. Appuyez sur le bouton de synchronisation de la DolphinBar, puis sur celui de la Wiimote.
3. Dans RetroBat, réglez **CONTRÔLES > TYPE DE WIIMOTE** sur **RÉELLE**.
4. Si besoin, réglez **POSITIONNEMENT DE LA SENSOR BAR** (**HAUT** ou **BAS**) selon l'endroit où est posée la DolphinBar, et **SENSIBILITÉ IR DE LA WIIMOTE**.



* Quand une DolphinBar est branchée, RetroBat désactive la recherche continue des Wiimotes. **DÉSACTIVER LA RECHERCHE CONTINUE DES WIIMOTES** permet de forcer ce réglage même lorsqu'aucune DolphinBar n'est branchée..
* **BALANCE BOARD** : à activer seulement si vous utilisez une vraie Balance Board.
* **BLUETOOTH PASSTHROUGH** : pour les utilisateurs avancés, qui donnent un adaptateur Bluetooth dédié à Dolphin.

#### Manettes GameCube en mode RÉELLE

Avec **TYPE DE WIIMOTE** sur **RÉELLE**, vos manettes jouent le rôle de manettes GameCube, pour les jeux Wii qui les acceptent (Super Smash Bros. Brawl, Mario Kart Wii…). **DISPOSITION DES BOUTONS (MANETTE GAMECUBE)** fonctionne comme sur la page GameCube.

**UTILISER DES MANETTES GAMECUBE** utilise à la place de vraies manettes GameCube, branchées sur un adaptateur (pilote Zadig, voir la [page GameCube](gamecube.md#utiliser-une-vraie-manette-gamecube-adaptateur)).

#### Mode RÉELLE COMME ÉMULÉE

Ce mode utilise de vraies Wiimotes, mais lues par Dolphin comme une Wiimote émulée. Les raccourcis se font alors depuis la Wiimote :

<table><thead><tr><th width="421.5">Action</th><th>Wiimote</th></tr></thead><tbody><tr><td>Quitter le jeu</td><td>− + HOME</td></tr><tr><td>Pause</td><td>− + B</td></tr><tr><td>Plein écran</td><td>− + A</td></tr><tr><td>Sauvegarde d'état (avec capture d'écran) / Chargement d'état</td><td>− + 1 / − + 2</td></tr><tr><td>Emplacement de sauvegarde suivant / précédent</td><td>− + HAUT / − + BAS</td></tr></tbody></table>

### Pistolets

Avec **PISTOLETS > ACTIVER LES PISTOLETS**, Dolphin utilise votre pistolet (Sinden, Gun4IR…) comme la Wiimote du joueur 1 : le pistolet vise l'écran, la gâchette appuie sur **B**, le clic droit sur **A** et le clic central secoue la Wiimote.

Pour les jeux reconnus, RetroBat adapte les boutons grâce au fichier `system\resources\gamesdb.xml`. Voir la [page **Contrôles des pistolets**](../../../../controleurs/pistolets_controles.md).

Pour utiliser une Wiimote comme pistolet, voir la [page **Wiimote & DolphinBar**](../../../../controleurs/supported-controllers/lightguns/wiimotedolphinbar.md).

### lr-dolphin

lr-dolphin propose moins de modes. Choisissez la manette de chaque joueur avec **CONTRÔLES > TYPE DE CONTRÔLEUR JOUEUR 1** (à 4) : **WIIMOTE** (par défaut), **WIIMOTE À L'HORIZONTALE**, **WIIMOTE + NUNCHUK**, **CLASSIC CONTROLLER**, **MANETTE CLASSIQUE PRO**, **VRAIE WIIMOTE** ou **MANETTE GAMECUBE**.

En mode **WIIMOTE** :

<table><thead><tr><th width="326.5">Manette RetroBat</th><th>Wiimote</th></tr></thead><tbody><tr><td>SUD / EST</td><td>B / A</td></tr><tr><td>NORD / OUEST</td><td>1 / 2</td></tr><tr><td>R2</td><td>Secouer</td></tr><tr><td>SELECT / START</td><td>− / +</td></tr><tr><td>R3</td><td>HOME</td></tr><tr><td>Stick gauche</td><td>Inclinaison</td></tr><tr><td>Stick droit</td><td>Pointeur (voir <strong>MODE IR</strong>)</td></tr></tbody></table>

Le détail des autres modes s'affiche dans le menu de RetroArch (**Contrôles > Contrôles du port 1**).

### Raccourcis

Avec une manette, **Dolphin** utilise les mêmes raccourcis que sur GameCube :

<table><thead><tr><th width="362.75">Action</th><th>Manette</th></tr></thead><tbody><tr><td>Quitter le jeu</td><td>HOTKEY + START</td></tr><tr><td>Pause</td><td>HOTKEY + EST</td></tr><tr><td>Sauvegarde d'état (avec capture d'écran) / Chargement d'état</td><td>HOTKEY + OUEST / HOTKEY + NORD</td></tr><tr><td>Emplacement de sauvegarde suivant / précédent</td><td>HOTKEY + HAUT / HOTKEY + BAS</td></tr><tr><td>Accélérer / ralentir</td><td>HOTKEY + DROITE / HOTKEY + GAUCHE</td></tr><tr><td>Changer de disque / éjecter</td><td>HOTKEY + L2 / HOTKEY + L1</td></tr><tr><td>Plein écran</td><td>HOTKEY + L3</td></tr></tbody></table>

**lr-dolphin** utilise les raccourcis de RetroArch (voir la [page Raccourcis](../../../../navigation/hotkeys.md)).

## Dossiers

### Sauvegardes

La Wii sauvegarde dans sa mémoire interne (la **NAND**). Dolphin et lr-dolphin utilisent la même :

<table><thead><tr><th width="297.75">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Sauvegardes (NAND Wii)</td><td><code>saves\wii\dolphin-emu\User\Wii</code></td></tr><tr><td>Sauvegardes d'état Dolphin</td><td><code>saves\wii\dolphin</code></td></tr><tr><td>Sauvegardes d'état lr-dolphin</td><td><code>saves\wii\libretro.dolphin</code></td></tr></tbody></table>

### Autres dossiers utiles

| Contenu                                   | Dossier                                       |
| ----------------------------------------- | --------------------------------------------- |
| Carte SD virtuelle                        | `saves\wii\dolphin-emu\User\Load\WiiSD.raw`   |
| Dossier synchronisé avec la carte SD      | `saves\wii\dolphin-emu\User\Load\WiiSDSync`   |
| Packs de textures                         | `saves\wii\dolphin-emu\User\Load\Textures`    |
| Patchs Riivolution                        | `saves\wii\dolphin-emu\User\Load\Riivolution` |
| Resource packs                            | `saves\wii\dolphin-emu\User\ResourcePacks`    |
| Captures (dumps) de textures et de vidéos | `saves\wii\dolphin-emu\User\Dump`             |
| Profils de manette et réglages de Dolphin | `emulators\dolphin-emu\User\Config`           |
| Réglages des pistolets par jeu            | `system\resources\gamesdb.xml`                |

**ÉMULATION > CHEMIN DE LA CARTE SD** permet d'utiliser une autre image de carte SD.

## Guides

### Succès (RetroAchievements) et jeux en .rvz

Comme sur GameCube, RetroBat ne reconnaît pas les jeux Wii au format .rvz lors de l'indexation des succès. L'outil `system\tools\indexcheevosrvz.bat` traite aussi `roms\wii` : voir la [page **GameCube**](gamecube.md#succes-retroachievements-et-jeux-en-.rvz).

### Textures personnalisées et jeux modifiés (Riivolution)

Même procédure que sur GameCube (voir la [page **GameCube**](gamecube.md#textures-personnalisees-dolphin)), avec les dossiers Wii :

* packs de textures dans `saves\wii\dolphin-emu\User\Load\Textures` ;
* patchs Riivolution dans `saves\wii\dolphin-emu\User\Load\Riivolution`, préréglages .json dans `roms\wii`.

Pour les jeux modifiés, lancez d'abord un jeu **Wii** depuis RetroBat avant d'ouvrir Dolphin, pour qu'il utilise les dossiers Wii.

### Utiliser le menu Wii

1. Ouvrez Dolphin (`emulators\dolphin-emu\Dolphin.exe`) et installez le menu Wii avec **Tools > Perform Online System Update** (Outils > Effectuer une mise à jour du système en ligne), en choisissant votre région.
2. Dans RetroBat, activez **ÉMULATION > LANCER LE MENU WII** dans les options d'un jeu : le menu Wii s'ouvre à la place du jeu.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (515).png" alt="" width="563"><figcaption></figcaption></figure></div>

Le menu Wii est installé dans la NAND (`saves\wii\dolphin-emu\User\Wii`). Pour qu'il soit trouvé, lancez au préalable un jeu Wii depuis RetroBat avant d'ouvrir Dolphin.

Pour vérifier si le menu Wii est bien installé dans Dolphin, tenter de le lancer directement depuis l'émulateur:

<div align="left"><figure><img src="../../../../.gitbook/assets/image (516).png" alt=""><figcaption></figcaption></figure></div>

### Jeux WiiWare et Console Virtuelle

Placez les fichiers .wad dans `roms\wii` : ils se lancent comme les autres jeux.

## Problèmes connus

<table><thead><tr><th width="346.5">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Le jeu ne réagit pas aux commandes, ou demande de brancher un Nunchuk</td><td>Le jeu attend une autre manette : réglez <strong>TYPE DE WIIMOTE ÉMULÉE</strong> dans les options du jeu (voir <a href="wii.md#controles">Contrôles</a>).</td></tr><tr><td>Le bouton HOME ne répond pas</td><td>En mode Nunchuk ou manette classique, SELECT et START servent aux boutons − et + : le bouton HOME n'est pas disponible.</td></tr><tr><td>Le jeu passe en multijoueur tout seul</td><td>Réglez <strong>NOMBRE DE WIIMOTES</strong> sur <strong>1</strong>.</td></tr><tr><td>La langue ne change pas</td><td>Elle s'applique à partir du deuxième lancement d'un jeu Wii (voir <a href="wii.md#bios">BIOS</a>).</td></tr><tr><td>Les vraies Wiimotes ne sont pas détectées</td><td>Vérifiez que la DolphinBar est en <strong>mode 4</strong>, que les Wiimotes sont synchronisées et que <strong>TYPE DE WIIMOTE</strong> est réglé sur <strong>RÉELLE</strong>.</td></tr><tr><td>lr-dolphin ne lance pas le jeu</td><td>lr-dolphin ne lit pas les jeux en .zip, .7z ou .json : décompressez-les, ou utilisez Dolphin.</td></tr></tbody></table>

