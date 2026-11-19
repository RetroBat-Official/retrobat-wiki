---
description: SNK
---

# Neo Geo

<div align="left"><figure><img src="../../../../.gitbook/assets/image (665).png" alt="" width="425"><figcaption></figcaption></figure></div>

## Présentation

La **Neo Geo** est un système de SNK sorti en 1990, en deux versions qui lisent les mêmes jeux :

* le **MVS** (Multi Video System), une carte d'arcade qui peut accueillir jusqu'à 6 jeux dans une même borne ;
* l'**AES** (Advanced Entertainment System), la console de salon, vendue pour offrir « l'arcade à la maison ».

SNK y a publié environ 150 jeux jusqu'en 2004, surtout des jeux de combat et d'action : The King of Fighters, Metal Slug, Samurai Shodown, Fatal Fury, Garou: Mark of the Wolves…

Dans RetroBat, les jeux Neo Geo sont des **romsets** d'arcade (`mslug.zip` pour Metal Slug), accompagnés du BIOS `neogeo.zip`. L'émulateur Geolith utilise un autre format, le `.neo` (voir [**Quel format de jeu ?**](neo-geo.md#quel-format-de-jeu)).

Les jeux sur CD de la Neo Geo CD ont leur propre système (voir la page [**Neo Geo CD**](neo-geo-cd.md)).

{% embed url="https://fr.wikipedia.org/wiki/Neo-Geo_AES" %}

## En bref

<table><thead><tr><th width="246.5"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\neogeo</code></td></tr><tr><td><strong>Extensions</strong></td><td>.zip .7z .neo .wad</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: fbneo</td></tr><tr><td><strong>BIOS</strong></td><td><code>neogeo.zip</code> (et <code>aes.zip</code> pour geolith)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro ; FBNeo, Raine et MAME par raccourcis</td></tr><tr><td><strong>RetroAchievements</strong></td><td>cores libretro (fbneo conseillé)</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>cores libretro</td></tr></tbody></table>

## Quel émulateur choisir ?

| Émulateur                                  | Pour qui ?                        | Points forts                                                                                                                                                                    | Limites                                                                                                          |
| ------------------------------------------ | --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| **libretro: fbneo** (défaut)               | Tout le monde                     | FinalBurn Neo dans RetroArch : très compatible, BIOS Universe par défaut, dispositions de boutons Neo Geo, cartes mémoire par jeu, RetroAchievements, jeu en réseau.            | Romsets FBNeo uniquement.                                                                                        |
| **libretro: geolith**                      | Puristes                          | Émulation très précise de l'AES et du MVS, compatible avec tous les jeux du commerce. Prise en charge du multitap 4 joueurs, du V-Liner et du trackball de The Irritating Maze. | Lit seulement les fichiers `.neo` (à convertir, voir [**Quel format de jeu ?**](neo-geo.md#quel-format-de-jeu)). |
| **fbneo** (autonome)                       | Bornes, sticks arcade             | Le FBNeo officiel, boutons réglés jeu par jeu par RetroBat (voir la page [**FinalBurn Neo**](../../arcade/final-burn-neo.md)).                                                  | Pas de RetroAchievements ni de jeu en réseau. Sauvegardes instantanées par raccourcis.                           |
| **raine**                                  | Curieux                           | Émulateur historique Neo Geo et Neo Geo CD, avec son propre menu.                                                                                                               | Pas de RetroAchievements ni de jeu en réseau.                                                                    |
| **mame64** (MAME)                          | Utilisateurs de MAME              | Le MAME officiel, avec vos romsets MAME.                                                                                                                                        | Romsets MAME de la même version. Réglages dans le menu de MAME.                                                  |
| **libretro: fbalpha, fbalpha2012\_neogeo** | PC très modestes, romsets anciens | Anciennes versions de FB Alpha, plus légères.                                                                                                                                   | Romset de leur propre version, plus mis à jour.                                                                  |

**En cas de doute, gardez libretro: fbneo.**

## BIOS

<table><thead><tr><th width="129.5">Fichier</th><th>Utilisé par</th><th>Contenu</th></tr></thead><tbody><tr><td><code>neogeo.zip</code></td><td>Tous les émulateurs</td><td>BIOS MVS (toutes régions), BIOS AES et BIOS Universe</td></tr><tr><td><code>aes.zip</code></td><td>geolith (type de système AES, son défaut)</td><td>BIOS AES</td></tr><tr><td><code>irrmaze.zip</code></td><td>geolith</td><td>BIOS de The Irritating Maze (trackball), en MVS</td></tr></tbody></table>

* Placez ces fichiers dans le dossier `bios`. `neogeo.zip` peut aussi se placer à côté des jeux, dans `roms\neogeo`, sauf pour geolith qui ne lit que `bios`.
* Avec **libretro: fbalpha2012\_neogeo**, `neogeo.zip` doit se trouver dans `roms\neogeo` : ce core ne lit pas le dossier `bios`.
* Le `neogeo.zip` doit venir de la même version que vos jeux : celui de FBNeo pour fbneo, celui de MAME pour MAME. Pour geolith, `neogeo.zip`, `aes.zip` et `irrmaze.zip` doivent venir d'un set MAME récent.

La vérification des BIOS de RetroBat demande `neogeo.zip` (dans `bios` ou `roms\neogeo`) et liste `aes.zip` et `irrmaze.zip` comme optionnels.

**Quel BIOS est utilisé ?**

<table><thead><tr><th width="194.5">Émulateur</th><th>Option</th><th>Défaut RetroBat</th></tr></thead><tbody><tr><td>libretro: fbneo</td><td><strong>ÉMULATION > BIOS</strong></td><td><strong>BIOS UNIVERSE</strong> (<strong>DIPSWITCH</strong> en mode hardcore des RetroAchievements)</td></tr><tr><td>libretro: geolith</td><td><strong>ÉMULATION > TYPE DE SYSTÈME</strong> : <strong>AES (CONSOLE DE SALON)</strong>, <strong>MVS (ARCADE)</strong> ou <strong>BIOS UNIVERSE</strong></td><td>AES, région USA</td></tr><tr><td>libretro: fbalpha, fbalpha2012_neogeo</td><td><strong>ÉMULATION > MODE NEO-GEO</strong></td><td><strong>BIOS UNIVERSE</strong></td></tr><tr><td>raine</td><td><strong>ÉMULATION > BIOS</strong></td><td><strong>UNIVERSE BIOS V3.2</strong></td></tr><tr><td>fbneo (autonome)</td><td>Menu de FBNeo (<strong>F1</strong>), <strong>Input > Set dipswitches</strong>, réglage <strong>BIOS</strong></td><td>Réglage de FBNeo</td></tr><tr><td>mame64</td><td>Menu de MAME (<strong>TAB</strong>), <strong>BIOS Selection</strong></td><td>BIOS par défaut de MAME</td></tr></tbody></table>

## Quel format de jeu ?

**Romsets `.zip` / `.7z`** : gardez-les compressés et sous leur nom d'origine (`kof98.zip`, `mslug3.zip`…).

<table><thead><tr><th width="297.75">Émulateur</th><th>Version du romset</th></tr></thead><tbody><tr><td>libretro: fbneo, fbneo (autonome)</td><td>Dernière version de FBNeo</td></tr><tr><td>mame64</td><td>Version de MAME fournie par RetroBat</td></tr><tr><td>raine</td><td>Liste de jeux propre à Raine : un romset FBNeo ou MAME récent fonctionne en général, pas toujours</td></tr><tr><td>libretro: fbalpha</td><td>FB Alpha 0.2.97.44</td></tr><tr><td>libretro: fbalpha2012_neogeo</td><td>FB Alpha 0.2.97.29</td></tr></tbody></table>

Pour le détail des romsets (non-merged, split, merged), voir la page [**Le Guide Arcade**](../../../arcade-guide.md).

**Fichiers `.neo`** (geolith uniquement) : c'est le format de la cartouche NeoSD de TerraOnion, un fichier par jeu. Geolith ne lit pas les romsets MAME / FBNeo : convertissez-les avec l'outil **lithogen** (lien ci-dessous). Un `.neo` peut aussi être rangé dans un `.zip` ; RetroBat vérifie alors que le zip contient bien un `.neo`.

{% embed url="https://github.com/carmiker/lithogen" %}

Pour un fichier `.neo`, seul geolith est proposé. Inversement, geolith n'est pas proposé pour un `.7z`.

## Contrôles

RetroBat configure automatiquement les manettes. Sur tous les émulateurs, **SELECT** met une pièce et **START** lance la partie. Le stick gauche et la croix déplacent le joueur.

La Neo Geo a 4 boutons, **A**, **B**, **C** et **D**, alignés de gauche à droite sur le stick d'origine. Les cores libretro ajoutent des combinaisons de boutons sur les gâchettes, pratiques pour les coups spéciaux et les menus du BIOS.

| Manette RetroBat | fbneo (CLASSIQUE, défaut) | fbneo (MODERNE) | geolith   | raine   |
| ---------------- | ------------------------- | --------------- | --------- | ------- |
| SUD              | A                         | B               | A         | A       |
| EST              | B                         | D               | B         | B       |
| OUEST            | C                         | A               | C         | C       |
| NORD             | D                         | C               | D         | D       |
| L1               | C + D                     | B + C + D       | C + D     | —       |
| R1               | A + B                     | C + D           | A + B     | —       |
| L2               | B + C + D                 | A + B + C       | B + C     | —       |
| R2               | A + B + C                 | A + B           | A + B + C | —       |
| L3               | —                         | —               | Test      | Service |
| R3               | —                         | —               | Service   | Test    |

<div align="left"><figure><img src="../../../../.gitbook/assets/image (668).png" alt=""><figcaption></figcaption></figure></div>

**Core fbneo** : **CONTRÔLES > TYPE DE CONTRÔLEUR** propose aussi des dispositions faites pour le matériel Neo Geo : **4 BOUTONS - NEOGEO MINI**, **6 BOUTONS - VARIANTE NEOGEO** et les trois **8 BOUTONS - MVS**. L'option **TATTOO** de RetroBat peut afficher à côté du jeu un schéma des boutons, pour les dispositions CLASSIQUE, MODERNE et PANNEAU 6 BOUTONS.

**Core geolith** : **CONTRÔLES > MODE 4-JOUEURS** active le multitap NEO-FTC1B pour les quelques jeux à 4 joueurs. Il ne fonctionne qu'avec le type de système **MVS (ARCADE)** et la région **JAPON** ou **ASIE**.

**Raine** : **CONTRÔLES > UTILISER LE PAD DIRECTIONNEL** déplace aussi le joueur avec la croix (activé par défaut).

**FBNeo (autonome)** et **MAME** : voir les pages [**FinalBurn Neo**](../../arcade/final-burn-neo.md) et [**MAME**](../../arcade/mame.md).

### Raccourcis

Les cores libretro utilisent les raccourcis standards de RetroArch (voir la page [**Raccourcis**](../../../../navigation/hotkeys.md)). Pour FBNeo autonome, voir la page [**FinalBurn Neo**](../../arcade/final-burn-neo.md) ; pour MAME, la page [**MAME**](../../arcade/mame.md).

**Raine**

| Raccourci           | Action                            | Clavier |
| ------------------- | --------------------------------- | ------- |
| **HOTKEY + START**  | Quitter                           | ÉCHAP   |
| HOTKEY + OUEST      | Sauvegarde instantanée            | F2      |
| HOTKEY + NORD       | Chargement instantané             | F4      |
| HOTKEY + HAUT / BAS | Emplacement de sauvegarde suivant | F6      |
| HOTKEY + R3         | Capture d'écran                   | F8      |
| HOTKEY + EST        | Menu de Raine                     | F1      |
| HOTKEY + L3         | Pause                             | P       |
| HOTKEY + GAUCHE     | Image par image                   | K       |
| —                   | Plein écran / fenêtre             | F       |
| —                   | Réinitialiser le jeu              | F9      |

Les touches se changent dans le fichier `kb_hotkeys.yml` (voir la page [**Raccourcis**](../../../../navigation/hotkeys.md)).

## Dossiers

| Contenu                                                        | Dossier                                                                                                |
| -------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| Jeux                                                           | `roms\neogeo`                                                                                          |
| BIOS                                                           | `bios` (ou `roms\neogeo`, voir [**BIOS**](neo-geo.md#bios))                                            |
| Core fbneo : cartes mémoire, NVRAM, meilleurs scores           | `saves\neogeo\fbneo`                                                                                   |
| Core geolith : cartes mémoire et NVRAM (`.mcr`, `.nv`, `.srm`) | `saves\neogeo`                                                                                         |
| Cores libretro : sauvegardes instantanées                      | `saves\neogeo\libretro.<core>`                                                                         |
| Raine : sauvegardes instantanées et sauvegardes des jeux       | `emulators\raine\savegame`                                                                             |
| Raine : captures d'écran                                       | `screenshots\raine`                                                                                    |
| Raine : configuration                                          | `emulators\raine\config\raine32_sdl.cfg`                                                               |
| FBNeo, MAME                                                    | Voir les pages [**FinalBurn Neo**](../../arcade/final-burn-neo.md) et [**MAME**](../../arcade/mame.md) |

## Guides

### Le BIOS Universe

Le **BIOS Universe** (UniBIOS) est un BIOS amélioré, créé par des passionnés. Il permet de passer un jeu en version AES ou MVS, de changer de région (certains jeux sont différents au Japon) et donne accès à des codes de triche. C'est le BIOS par défaut de RetroBat avec les cores fbneo, fbalpha et fbalpha2012\_neogeo, et avec Raine.

* **Réglages du BIOS** : maintenez **A + B + C** pendant le démarrage du jeu.
* **Menu en jeu** (triche, réglages du jeu) : appuyez sur **START + A + B + C** pendant la partie.

Avec les cores libretro, **A + B + C** est sur **R2** (sur **L2** avec la disposition MODERNE du core fbneo) : maintenez R2 au démarrage, ou appuyez sur START + R2 en jeu.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (667).png" alt="" width="563"><figcaption><p>Menu de réglage du BIOS</p></figcaption></figure></div>

<div align="left"><figure><img src="../../../../.gitbook/assets/image (666).png" alt="" width="491"><figcaption><p>Menu en jeu</p></figcaption></figure></div>

### AES ou MVS ?

La plupart des jeux sont identiques sur les deux versions. Quelques différences :

* en **MVS** (arcade), il faut mettre des pièces (**SELECT**), et la difficulté ou le nombre de vies se règlent dans le menu de la borne ;
* en **AES** (console), il n'y a pas de pièces, et certains jeux ont des options ou du contenu différents ;
* selon la région, certains jeux changent (sang, textes, censure).

Avec le BIOS Universe, le choix se fait dans ses réglages. Avec geolith, utilisez **ÉMULATION > TYPE DE SYSTÈME**. Certains jeux, surtout des bootlegs et des hacks, demandent le MVS. **ÉMULATION > JEU GRATUIT** (geolith) évite d'avoir à mettre des pièces en MVS.

**INTERFACE UTILISATEUR > AFFICHER LE MENU DU JEU** (geolith) ouvre au démarrage le menu de réglage du système MVS.

### Cartes mémoire

L'AES et le MVS enregistrent les parties sur une carte mémoire.

* Le core fbneo crée une carte mémoire par jeu, dans `saves\neogeo\fbneo`.
* Geolith insère une carte mémoire par défaut et l'enregistre dans `saves\neogeo`.

### RetroAchievements

Les jeux Neo Geo sont classés dans la catégorie Arcade de RetroAchievements. Le core fbneo est le mieux suivi. Geolith est reconnu avec ses fichiers `.neo`.

En mode hardcore, RetroArch refuse le BIOS Universe avec le core fbneo. RetroBat règle tout seul le BIOS sur **DIPSWITCH** en hardcore : laissez **ÉMULATION > BIOS** sur son réglage par défaut. Pour plus de détails, voir la page [**RetroAchievements**](../../../../utilisation-avancee/retroachievements.md).

### Autres options utiles

**Core geolith**

| Option                                                | Effet                                                                                                                                      |
| ----------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| **ÉMULATION > RÉGION**                                | USA (défaut), Europe, Japon ou Asie.                                                                                                       |
| **ÉMULATION > OVERCLOCKING**                          | Accélère le processeur pour réduire les ralentissements d'origine. Peut créer des bugs.                                                    |
| **VIDÉO > RAPPORT D'ASPECT DU CORE**                  | **1:1 (PIXELS CARRÉS)** (défaut), **45:44 (NTSC PRÉCIS)** ou **4:3 (NTSC TRADITIONNEL)**. Utilisé quand **RAPPORT D'ASPECT** est sur AUTO. |
| **RENDU VISUEL > LIMITE DE SPRITES PAR LIGNE (HACK)** | Réduit les sprites qui clignotent quand il y en a trop sur une ligne. Au-delà de 96, peut créer des bugs.                                  |

**Core fbneo** : voir la page [**FinalBurn Neo**](../../arcade/final-burn-neo.md) (overclocking, menu de diagnostic, dip switches, meilleurs scores).

**Raine**

| Option                                        | Effet                                                                 |
| --------------------------------------------- | --------------------------------------------------------------------- |
| **ÉMULATION > LIMITER LES FPS**               | Activé par défaut. Désactivé, le jeu tourne aussi vite que possible.  |
| **VIDÉO > MAINTENIR LE RATIO D'AFFICHAGE**    | Garde les proportions de l'image (activé par défaut).                 |
| **VIDÉO > ROTATION DE L'ÉCRAN**               | Tourne l'image de 90°, 180° ou 270°.                                  |
| **RENDU VISUEL > FILTRE DE MISE À L'ÉCHELLE** | **PLUS PROCHE** (pixels nets, défaut) ou **LINÉAIRE** (image lissée). |
| **INTERFACE UTILISATEUR > AFFICHER LES FPS**  | Affiche le nombre d'images par seconde.                               |

## Problèmes connus

| Problème                                                                   | Solution                                                                                                                                                                                                      |
| -------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Le jeu ne démarre pas, ou un fichier manque                                | Le romset ne correspond pas à la version de l'émulateur, ou `neogeo.zip` manque ou vient d'une autre version (voir [**BIOS**](neo-geo.md#bios) et [**Quel format de jeu ?**](neo-geo.md#quel-format-de-jeu)). |
| Geolith : message « Geolith core requires a .neo file in the zip archive » | Le zip est un romset MAME / FBNeo : convertissez-le en `.neo` avec lithogen, ou utilisez le core fbneo.                                                                                                       |
| Geolith : le jeu ne démarre pas en AES                                     | `aes.zip` manque dans `bios`, ou le jeu demande le MVS : réglez **ÉMULATION > TYPE DE SYSTÈME** sur **MVS (ARCADE)**.                                                                                         |
| Écran noir avec du son                                                     | Le BIOS choisi manque dans `neogeo.zip` : utilisez le `neogeo.zip` de la même version que l'émulateur, ou choisissez un autre BIOS.                                                                           |
| RetroAchievements passe en mode normal                                     | Le BIOS Universe est choisi : remettez **ÉMULATION > BIOS** sur son réglage par défaut.                                                                                                                       |
| libretro: fbalpha2012\_neogeo ne trouve pas le BIOS                        | Placez `neogeo.zip` dans `roms\neogeo`.                                                                                                                                                                       |
| Geolith : le mode 4 joueurs ne marche pas                                  | Réglez **TYPE DE SYSTÈME** sur **MVS (ARCADE)** et **RÉGION** sur **JAPON** ou **ASIE**.                                                                                                                      |
