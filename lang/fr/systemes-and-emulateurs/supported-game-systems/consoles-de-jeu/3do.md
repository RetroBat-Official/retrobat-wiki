---
description: The 3do Company
---

# 3DO

<div align="left"><figure><img src="../../../.gitbook/assets/image (611).png" alt=""><figcaption></figcaption></figure></div>

### Présentation

La **3DO Interactive Multiplayer** est une console de salon sortie en 1993. The 3DO Company, fondée par Trip Hawkins (créateur d'Electronic Arts), ne la fabrique pas elle-même : elle vend une licence à des constructeurs, comme Panasonic (FZ-1, FZ-10), Goldstar ou Sanyo. Elle repose sur un processeur ARM60 à 12,5 MHz et lit ses jeux sur CD-ROM. Vendue cher, elle disparaît en 1996.

Parmi ses jeux : **Gex**, **Road Rash**, **The Need for Speed**, **Star Control II**, **Super Street Fighter II Turbo**, **Return Fire**, **Wing Commander III**, **Samurai Shodown**, et des jeux au pistolet d'American Laser Games (**Mad Dog McCree**, **Crime Patrol**, **Who Shot Johnny Rock?**).

RetroBat propose deux émulateurs : le core libretro **opera** (par défaut) et **Phoenix**.

{% embed url="https://fr.wikipedia.org/wiki/3DO_Interactive_Multiplayer" %}

### En bref

<table><thead><tr><th width="270.25"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\3do</code></td></tr><tr><td><strong>Extensions</strong></td><td>.cue .iso .chd</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: opera</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun obligatoire (BIOS intégré au core opera)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>core libretro</td></tr><tr><td><strong>RetroAchievements</strong></td><td>core libretro</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>core libretro</td></tr><tr><td><strong>Pistolets</strong></td><td>core libretro (jusqu'à 4)</td></tr><tr><td><strong>BIOS optionnels</strong></td><td>BIOS des consoles (<code>panafz1.bin</code>, <code>panafz10.bin</code>…) et ROM Kanji dans <code>bios</code> ; <code>panafz10.bin</code> nécessaire à Phoenix</td></tr></tbody></table>

### Quel émulateur choisir ?

<table><thead><tr><th width="162">Émulateur</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>libretro: opera</strong> (défaut)</td><td>Fonctionne sans BIOS, sauvegardes instantanées, RetroAchievements, jeu en réseau, pistolets, souris et manche de vol, shaders et raccourcis de RetroArch.</td><td>—</td></tr><tr><td><strong>phoenix</strong></td><td>Émulateur autonome, plusieurs moteurs de rendu.</td><td>Demande <code>panafz10.bin</code>. Pas de sauvegardes instantanées gérées par RetroBat, pas de pistolets.</td></tr></tbody></table>

### BIOS

Le core opera intègre **Opera Boot**, un BIOS libre : aucun fichier n'est nécessaire.

Un BIOS d'origine reste le plus compatible : s'il est présent dans `bios`, RetroBat l'utilise automatiquement (dans l'ordre du tableau ci-dessous), sinon le core démarre avec Opera Boot. L'option **ÉMULATION > BIOS** force un BIOS.

<table><thead><tr><th width="197">Fichier</th><th width="235">Console</th><th>MD5</th></tr></thead><tbody><tr><td><code>panafz1.bin</code></td><td>Panasonic FZ-1 (États-Unis)</td><td>f47264dd47fe30f73ab3c010015c155b</td></tr><tr><td><code>panafz10.bin</code></td><td>Panasonic FZ-10 (États-Unis), <strong>nécessaire à Phoenix</strong></td><td>51f2f43ae2f3508a14d9f56597e2d3ce</td></tr><tr><td><code>panafz1j.bin</code></td><td>Panasonic FZ-1 (Japon)</td><td>a496cfdded3da562759be3561317b605</td></tr><tr><td><code>panafz10e-anvil.bin</code></td><td>Panasonic FZ-10 ANVIL (Europe)</td><td>a48e6746bd7edec0f40cff078f0bb19f</td></tr><tr><td><code>goldstar.bin</code></td><td>Goldstar GDO-101M</td><td>8639fd5e549bd6238cfee79e3e749114</td></tr><tr><td><code>sanyotry.bin</code></td><td>Sanyo TRY IMP-21J</td><td>35fa1a1ebaaeea286dc5cd15487c13ea</td></tr><tr><td><code>panafz10-norsa.bin</code></td><td>Panasonic FZ-10, vérification RSA désactivée</td><td>1477bda80dc33731a65468c1f5bcbee9</td></tr><tr><td><code>panafz1j-norsa.bin</code></td><td>Panasonic FZ-1 (Japon), vérification RSA désactivée</td><td>f6c71de7470d16abe4f71b1444883dc8</td></tr><tr><td><code>panafz10e-anvil-norsa.bin</code></td><td>Panasonic FZ-10 ANVIL, vérification RSA désactivée</td><td>cf11bbb5a16d7af9875cca9de9a15e09</td></tr><tr><td><code>3do_arcade_saot.bin</code></td><td>Borne Shootout at Old Tucson</td><td>8970fc987ab89a7f64da9f8a8c4333ff</td></tr></tbody></table>

Les versions « norsa » permettent de lancer des jeux non signés (homebrews).

Certains jeux japonais ont aussi besoin d'une ROM de police Kanji, à choisir avec **ÉMULATION > ROM DE POLICE KANJI** :

<table><thead><tr><th width="297.75">Fichier</th><th>MD5</th></tr></thead><tbody><tr><td><code>panafz1-kanji.bin</code></td><td>b8dc97f778a6245c58e064b0312e8281</td></tr><tr><td><code>panafz1j-kanji.bin</code></td><td>c23fb5d5e6bb1c240d02cf968972be37</td></tr><tr><td><code>panafz10ja-anvil-kanji.bin</code></td><td>428577250f43edc902ea239c50d2240d</td></tr></tbody></table>

Tous ces fichiers vont dans `bios`.

### Quel format de jeu ?

<table><thead><tr><th width="162.75">Format</th><th>Remarques</th></tr></thead><tbody><tr><td><strong>.cue</strong> / <strong>.bin</strong></td><td>Format le plus courant. Gardez le <code>.cue</code> et ses <code>.bin</code> ensemble.</td></tr><tr><td><strong>.iso</strong></td><td>Image d'une seule piste.</td></tr><tr><td><strong>.chd</strong></td><td>Format compressé, recommandé pour gagner de la place.</td></tr></tbody></table>

Le core opera ne gère pas les `.m3u` : chaque disque d'un jeu sur plusieurs disques se lance séparément (voir [**Jeux sur plusieurs disques**](3do.md#jeux-sur-plusieurs-disques) plus bas).

### Contrôles

#### Configuration automatique

RetroBat configure automatiquement les manettes pour les deux émulateurs. L'option **AUTOCONFIGURER LES MANETTES** permet de garder sa propre configuration.

<table><thead><tr><th width="272.75">Manette 3DO</th><th>Manette</th></tr></thead><tbody><tr><td>A</td><td>OUEST</td></tr><tr><td>B</td><td>SUD</td></tr><tr><td>C</td><td>EST</td></tr><tr><td>L / R</td><td>L1 / R1</td></tr><tr><td>P (Play / Pause)</td><td>START</td></tr><tr><td>X (Stop)</td><td>SELECT</td></tr><tr><td>Croix</td><td>Croix directionnelle ou stick gauche</td></tr></tbody></table>

<div align="left"><figure><img src="../../../.gitbook/assets/image (612).png" alt="" width="225"><figcaption></figcaption></figure></div>

Avec Phoenix, les directions sont sur le stick gauche ; activez **CONTRÔLES > UTILISER PAD DIRECTIONNEL** pour jouer avec la croix.

#### Core opera : périphériques

Le menu **CONTRÔLES** choisit le périphérique de chaque joueur avec **TYPE DE CONTRÔLEUR JOUEUR 1** (à 4) :

* **MANETTE 3DO** : manette standard (par défaut).
* **MANCHE DE VOL 3DO** : stick gauche = manche, stick droit = manette des gaz, R2 = tir, A / B / C et la croix comme la manette.
* **SOURIS 3DO** : pour les jeux à la souris.
* **PISTOLET 3DO** : pour les jeux au pistolet (voir **Pistolets**).

**NOMBRE DE CONTRÔLEURS CONNECTÉS** fixe le nombre de périphériques vus par la console (1 par défaut) : certains jeux plantent quand plusieurs périphériques sont branchés.

#### Manettes six boutons

Avec une manette de type Mega Drive (8BitDo M30, manettes Retro-bit 2.4 GHz), RetroBat place A, B et C sur la rangée du bas. Pour certaines de ces manettes, il faut activer **CONTRÔLES > UTILISER UNE MANETTE DE TYPE 3DO**.

#### Pistolets

Les jeux au pistolet (Mad Dog McCree, Crime Patrol, Corpse Killer, Drug Wars, Space Pirates, Who Shot Johnny Rock?…) fonctionnent avec le core opera, jusqu'à 4 pistolets. Activez **PISTOLETS > ACTIVER LES PISTOLETS**.

* Clic gauche : tir ; clic droit ou tir hors de l'écran : recharge.
* Au clavier : 1 = Start, 5 = Select.
* **AFFICHER CIBLE** affiche le viseur, **MAPPING DES BOUTONS A/B** choisit les boutons auxiliaires (souris, croix de la Wiimote ou clavier), **UN SEUL PISTOLET** ne configure qu'un pistolet.
* Avec le BIOS de la borne (`3do_arcade_saot.bin`), RetroBat utilise le pistolet arcade de la borne (pièces, Start, service).

Pour plus de détails sur les pistolets, voir la page [**Pistolets**](../../../controleurs/supported-controllers/lightguns/).

#### Raccourcis

**Core opera** : raccourcis RetroArch habituels (sauvegarde, chargement, rembobinage…). Pour plus de détails, voir la page [**Raccourcis**](../../../navigation/hotkeys.md).

**Phoenix**

<table><thead><tr><th width="220.25">Raccourci</th><th>Action</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quitter</td></tr></tbody></table>

RetroBat allume la console et passe Phoenix en plein écran automatiquement au lancement.

### Dossiers

<table><thead><tr><th width="381.5">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>BIOS et ROM Kanji</td><td><code>bios</code></td></tr><tr><td>Core opera : sauvegardes des jeux (NVRAM, une par jeu)</td><td><code>saves\3do\opera\per_game</code></td></tr><tr><td>Core opera : sauvegardes des jeux (NVRAM partagée)</td><td><code>saves\3do\opera\shared</code></td></tr><tr><td>Core opera : sauvegardes instantanées</td><td><code>saves\3do\libretro.opera</code></td></tr><tr><td>Captures d'écran</td><td><code>screenshots</code></td></tr><tr><td>Phoenix : configuration</td><td><code>emulators\phoenix\phoenix.config.xml</code></td></tr></tbody></table>

### Guides

#### Jeux sur plusieurs disques

Le core opera ne change pas de disque en cours de partie : lancez chaque disque séparément. Pour retrouver sa progression d'un disque à l'autre, les disques doivent partager la même NVRAM :

* Si le nom du fichier contient « Disc » (par exemple `Wing Commander III (Disc 1).cue`), RetroBat utilise automatiquement la NVRAM partagée.
* Sinon, réglez **ÉMULATION > STOCKAGE NVRAM** sur **PARTAGÉ** pour ce jeu.

#### Améliorer la fluidité

La 3DO affiche souvent peu d'images par seconde. **ÉMULATION > FRÉQUENCE DU PROCESSEUR** augmente la vitesse du processeur émulé (jusqu'à 4x) : de nombreux jeux deviennent plus fluides, au prix des performances, et quelques jeux peuvent présenter des bugs.

#### Autres options utiles (core opera)

<table><thead><tr><th width="334">Option</th><th>Effet</th></tr></thead><tbody><tr><td><strong>ÉMULATION > FORMAT VIDÉO ÉMULÉ</strong></td><td>NTSC (60 Hz) ou PAL (50 Hz). Certains jeux européens demandent un BIOS européen.</td></tr><tr><td><strong>ÉMULATION > VITESSE DE LECTURE CD</strong></td><td>Lecture plus rapide des disques (2x d'origine) ; certains jeux ne la supportent pas.</td></tr><tr><td><strong>ÉMULATION > HLE DE L'OS</strong></td><td>Émulation haut niveau de fonctions du système, peut améliorer les performances.</td></tr><tr><td><strong>ÉMULATION > DSP MULTITHREAD</strong></td><td>Le son est calculé sur un autre cœur du processeur (activé par défaut).</td></tr><tr><td><strong>VIDÉO > HAUTE RÉSOLUTION</strong></td><td>Rendu en résolution doublée (activé par défaut).</td></tr></tbody></table>

**Phoenix** : **PILOTES > VIDÉO** (logiciel approximatif, logiciel original ou matériel expérimental), **SYNCHRONISATION VERTICALE**, **RENDU VISUEL > FILTRAGE BILINÉAIRE**.

### Problèmes connus

<table><thead><tr><th width="347.75">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Un jeu ne démarre pas ou se bloque avec le BIOS intégré</td><td>Ajoutez un BIOS d'origine dans <code>bios</code> (par exemple <code>panafz10.bin</code>), ou choisissez-le avec <strong>ÉMULATION > BIOS</strong>.</td></tr><tr><td>Un jeu plante quand plusieurs manettes sont branchées</td><td>Laissez <strong>CONTRÔLES > NOMBRE DE CONTRÔLEURS CONNECTÉS</strong> sur 1.</td></tr><tr><td>Textes manquants dans un jeu japonais</td><td>Ajoutez une ROM Kanji dans <code>bios</code> et choisissez-la avec <strong>ÉMULATION > ROM DE POLICE KANJI</strong>.</td></tr><tr><td>Une sauvegarde instantanée ancienne ne se charge plus</td><td>Le core opera a changé de format de sauvegarde instantanée fin 2026 : les anciennes ne sont plus compatibles. Les sauvegardes des jeux (NVRAM) ne sont pas concernées.</td></tr><tr><td>Phoenix ne démarre pas</td><td>Placez <code>panafz10.bin</code> dans <code>bios</code>.</td></tr><tr><td>Avec Phoenix, la croix ne répond pas</td><td>Activez <strong>CONTRÔLES > UTILISER PAD DIRECTIONNEL</strong>.</td></tr></tbody></table>
