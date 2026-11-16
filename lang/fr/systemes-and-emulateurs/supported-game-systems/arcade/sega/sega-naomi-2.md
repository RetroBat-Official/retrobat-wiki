---
description: Sega
---

# Sega NAOMI 2

<div align="left"><figure><img src="../../../../.gitbook/assets/image (633).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Présentation

La **NAOMI 2** est la version plus puissante de la NAOMI, sortie par Sega en 2000. Elle double les processeurs et les puces graphiques (deux SH-4, deux PowerVR2) et ajoute une puce de calcul géométrique, l'Elan, pour des scènes 3D bien plus riches. Ses jeux sont sur cartouches ou sur GD-ROM. Sa ludothèque est courte mais marquante, notamment des jeux de course reliés en réseau.

Parmi ses jeux : **Virtua Fighter 4** (et Evolution, Final Tuned), **Initial D Arcade Stage** (1 à 3), **Beach Spikers**, **Club Kart**, **Wild Riders**, **Soul Surfer**, **The King of Route 66**, **Virtua Striker 3**.

RetroBat propose trois émulateurs : le core libretro **flycast** (par défaut), **Flycast** en version autonome et **Demul**.

{% embed url="https://fr.wikipedia.org/wiki/Naomi_2" %}

## En bref

<table><thead><tr><th width="265.25"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\naomi2</code></td></tr><tr><td><strong>Extensions</strong></td><td>.zip .7z .decomp</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: flycast</td></tr><tr><td><strong>BIOS</strong></td><td><code>naomi2.zip</code> dans <code>bios\dc</code></td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs (mappage par jeu pour les cores flycast)</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>core flycast, Flycast (gérées par RetroBat) ; Demul par raccourcis</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non (Flycast : GGPO et réseau NAOMI, propres à l'émulateur)</td></tr><tr><td><strong>Pistolets</strong></td><td>—</td></tr><tr><td><strong>Volants</strong></td><td>Flycast</td></tr><tr><td><strong>BIOS optionnels</strong></td><td>—</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="167">Émulateur</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>libretro: flycast</strong> (défaut)</td><td>Très bonne compatibilité, boutons placés comme sur la borne pour chaque jeu, sauvegardes instantanées, shaders et raccourcis de RetroArch.</td><td>Pas de fichier de mappage fourni pour les volants.</td></tr><tr><td><strong>flycast</strong></td><td>Même base que le core, avec ses propres menus. Mappage par jeu, sauvegardes instantanées, volants (Initial D, Club Kart, The King of Route 66, Wild Riders), jeu en ligne GGPO et réseau NAOMI (bornes reliées).</td><td>—</td></tr><tr><td><strong>demul</strong></td><td>Émulateur historique, aussi utilisé pour la NAOMI et l'Atomiswave.</td><td>Compatibilité plus faible. Disposition des boutons identique pour tous les jeux. Sauvegardes instantanées non gérées par RetroBat.</td></tr></tbody></table>

## BIOS

<table><thead><tr><th width="164.5">Fichier</th><th width="151">Dossier</th><th>Utilisé par</th></tr></thead><tbody><tr><td><code>naomi2.zip</code></td><td><code>bios\dc</code></td><td>Tous les jeux, tous les émulateurs</td></tr></tbody></table>

`naomi2.zip` est le BIOS de la NAOMI 2 au format MAME, différent de celui de la NAOMI. Le core flycast et Flycast autonome le cherchent tous les deux dans `bios\dc` ; Demul le trouve dans `bios\dc`, `bios` ou le dossier des jeux. Son contenu dépend de la version de MAME.

<details>

<summary>Contenu de naomi2.zip</summary>

```
naomi2.zip
- 315-6146.bin "728bfe038ce280872057e365ebfc0fee"
- 315-6215.bin "baf83367044924067e09856ba164aa6f"
- epr-23605.ic27 "6f8ad6e3ab04c8ae1cbcaa652b91cf4e"
- epr-23605a.ic27 "f3f39513484df216d9979f6ae7577942"
- epr-23605b.ic27 "ab046e62c51d67fb89eade2b8d5f6a8d"
- epr-23605c.ic27 "096a5217ff6e6c6cafe65a03336760ab"
- epr-23605c_multi.ic27 "659d579ba9aef5b025d87323044e83f4"
- epr-23607.ic27 "cbe0984d03d73869c23da5a3dd2ce207"
- epr-23607b.ic27 "b624ec7b3b90fdf3be103cdfb1679d1d"
- epr-23607c.ic27 "a9d82db14b823a5a57885bea1a998eb7"
- epr-23608.ic27 "3b1315be24dc8d17f4fa18f3bfc5fe5c"
- epr-23608a.ic27 "0143cf852cb2a8a41f217bc688f62105"
- epr-23608b.ic27 "8b88c1f5a06e9b560e887c3b9f879237"
- epr-23608c.ic27 "b49702e4fadb3b5f9143a3d20afd04b5"
- epr-23609b.ic27 "ecadb008179ca1e6f4fe3fa091ab5df2"
- main_eeprom.bin "edeed38a9795e062a9af28c3eba22040"
- sp5001.bin "14e6bffff0d4dff6a5a547e7c43680ff"
- sp5001-a.bin "689d2228b00fb59781f82af6e8ecdb78"
- sp5001-b.bin "8373a11106c1c2fc21ac839f75ea488f"
- sp5002-a.bin "7eecfb8e8f82b47ffab92a0c5528100e"
- x76f100_eeprom.bin "960ece0dc22a7c5ff81c812a2993e7cc"
```

</details>

## Quel format de jeu ?

<table><thead><tr><th width="156.5">Format</th><th>Remarques</th></tr></thead><tbody><tr><td><strong>.zip</strong>, <strong>.7z</strong></td><td>Jeux au format MAME, à garder tels quels, sans les décompresser ni les renommer (<code>vf4.zip</code>, <code>initdv3e.zip</code>, <code>clubkrt.zip</code>…). Les clones ont besoin du jeu parent dans le même dossier. Les jeux sur GD-ROM ont aussi un fichier <code>.chd</code> (voir <a href="sega-naomi-2.md#jeux-sur-gd-rom-fichiers-chd"><strong>Guides</strong></a>).</td></tr><tr><td><strong>.decomp</strong></td><td>Portage PC, voir la page <a href="../../autres/recomp.md"><strong>Recompilations</strong></a>.</td></tr></tbody></table>

## Contrôles

### Configuration automatique

RetroBat configure les manettes pour les trois émulateurs. Les commandes communes à tous les jeux :

<table><thead><tr><th width="195.25">Borne</th><th>Manette</th></tr></thead><tbody><tr><td>Joystick</td><td>Croix directionnelle, stick gauche</td></tr><tr><td>Start</td><td>START</td></tr><tr><td>Crédit</td><td>SELECT</td></tr><tr><td>Test</td><td>R3 (avec le menu service activé, voir <a href="sega-naomi-2.md#menu-service-et-menu-de-test"><strong>Guides</strong></a>)</td></tr><tr><td>Service</td><td>L3 (avec le menu service activé, voir <a href="sega-naomi-2.md#menu-service-et-menu-de-test"><strong>Guides</strong></a>)</td></tr></tbody></table>

* **Core flycast** et **Flycast** : la position des boutons d'action est définie jeu par jeu, pour retrouver la disposition de la borne. Les fichiers utilisés sont `libretro_flycast_naomi2.yml` (core) et `flycast_Arcade.yml` (Flycast), voir la page [**Configuration des touches par émulateur**](../../../../controleurs/controller-configuration.md#adapter-les-controles-sans-desactiver-lautoconfiguration). **CONTRÔLES > DISPOSITION DES BOUTONS** choisit une autre disposition quand le fichier en propose une.
* **Flycast** : **CONTRÔLES > UTILISER PAD DIRECTIONNEL** déplace les commandes analogiques sur la croix.
* **Demul** : même disposition pour tous les jeux : boutons 1 à 4 sur SUD, EST, OUEST, NORD, boutons 5 à 8 sur L1, R1, L2, R2.

### Volants

Flycast gère les volants (**VOLANTS DE COURSE > ACTIVER LES VOLANTS**) pour **Initial D**, **Club Kart**, **The King of Route 66**, **Wild Riders** et **Sega Driving Simulator**. **VOLANTS DE COURSE > DISPOSITION DES BOUTONS DU VOLANT** adapte les boutons au jeu : vitesses sur A / B pour Initial D, marche arrière sur X pour The King of Route 66. Le core flycast gère aussi les volants, mais RetroBat ne fournit pas encore son fichier de mappage. Pour les volants pris en charge, voir la page [**Volants**](../../../../controleurs/supported-controllers/volants.md).

### Raccourcis

Le core flycast utilise les raccourcis standards de RetroArch (voir la page [**Raccourcis**](../../../../navigation/hotkeys.md)).

#### **Flycast**

| Raccourci           | Action                    | Clavier |
| ------------------- | ------------------------- | ------- |
| **HOTKEY + START**  | Quitter                   | Échap   |
| **HOTKEY + SUD**    | Menu de Flycast           | F1      |
| **HOTKEY + OUEST**  | Sauvegarde instantanée    | F2      |
| **HOTKEY + NORD**   | Chargement instantané     | F4      |
| **HOTKEY + DROITE** | Avance rapide (maintenir) | L       |
| **HOTKEY + R3**     | Capture d'écran           | F8      |

#### **Demul**

| Raccourci          | Action                          | Clavier |
| ------------------ | ------------------------------- | ------- |
| **HOTKEY + START** | Quitter                         |         |
| **HOTKEY + OUEST** | Sauvegarde instantanée de Demul | F2      |
| **HOTKEY + NORD**  | Chargement instantané de Demul  | F4      |

Les sauvegardes instantanées de Demul restent dans Demul : elles n'apparaissent pas dans le gestionnaire de sauvegardes.

## Dossiers

<table><thead><tr><th width="337.75">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>BIOS</td><td><code>bios\dc</code></td></tr><tr><td>Core flycast : sauvegardes instantanées</td><td><code>saves\naomi2\libretro.flycast</code></td></tr><tr><td>Flycast : sauvegardes des jeux (NVRAM, EEPROM)</td><td><code>saves\naomi2\reicast</code></td></tr><tr><td>Flycast : sauvegardes instantanées</td><td><code>saves\naomi2\flycast\sstates</code> (copiées depuis <code>saves\naomi2\reicast\states</code>)</td></tr><tr><td>Flycast : configuration</td><td><code>emulators\flycast\emu.cfg</code></td></tr><tr><td>Demul : sauvegardes des jeux (NVRAM)</td><td><code>saves\naomi2\demul</code></td></tr><tr><td>Demul : configuration</td><td><code>emulators\demul\Demul.ini</code>, <code>emulators\demul\padDemul.ini</code></td></tr><tr><td>Mappage par jeu (core flycast, Flycast)</td><td><code>system\resources\inputmapping</code> (copie modifiable dans <code>user\inputmapping</code>)</td></tr></tbody></table>

## Guides

### Jeux sur GD-ROM (fichiers CHD)

Les jeux sur GD-ROM (**Virtua Fighter 4**, **Initial D**…) ont besoin, en plus de leur `.zip`, de l'image du disque au format `.chd`. Placez le `.chd` dans un dossier qui porte le nom du `.zip`, sans renommer ni l'un ni l'autre :

```
roms\
└─ naomi2\
   ├─ vf4tuned\
   │  └─ gds-0036f.chd
   └─ vf4tuned.zip
```

Seul le `.zip` apparaît dans la liste des jeux.

### Menu service et menu de test

Le menu de test de la borne permet de régler le nombre de crédits, la difficulté, le nombre de rounds, et de vérifier les commandes.

1. Activez **ÉMULATION > MODE SERVICE** (core flycast) ou **ÉMULATION > ACTIVER LE MENU SERVICE** (Flycast). Avec Demul, les boutons sont toujours actifs.
2. En jeu, appuyez sur **R3** (Test) pour ouvrir le menu, puis naviguez avec les boutons de la borne. **L3** (Service) ajoute un crédit de service.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (634).png" alt="" width="563"><figcaption></figcaption></figure></div>

### Jeu gratuit et région

* **ÉMULATION > JEU GRATUIT** (core flycast, Flycast, activé par défaut) configure le jeu sans pièces : START suffit pour jouer. Désactivé, ajoutez des crédits avec **SELECT**.
* **ÉMULATION > RÉGION** (core flycast) choisit la région de la borne (Japon, USA, Europe) : elle change la langue et parfois le contenu du jeu.

Ces réglages sont écrits dans la mémoire de la borne au lancement. Si un jeu garde l'ancien réglage, changez-le aussi dans son menu de test.

### Autres options utiles

<table><thead><tr><th width="331.5">Option</th><th>Effet</th></tr></thead><tbody><tr><td><strong>RÉSOLUTION INTERNE</strong></td><td>Augmente la résolution de rendu (les trois émulateurs).</td></tr><tr><td><strong>RAPPORT D'ASPECT</strong></td><td>Flycast, Demul : 4:3, 16:9 ou étiré.</td></tr><tr><td><strong>RENDU VISUEL > PATCH ÉCRAN LARGE</strong> / <strong>HACK ÉCRAN LARGE</strong></td><td>Affichage en 16:9 : les patchs corrigent les jeux compatibles, le hack étend l'image de tous les jeux (avec des défauts).</td></tr><tr><td><strong>RÉSEAU > MODE RÉSEAU</strong> (Flycast)</td><td>GGPO pour les jeux de combat en ligne, ou <strong>NAOMI</strong> pour relier plusieurs bornes (Club Kart, Initial D, The King of Route 66) ; <strong>MODE HÔTE</strong> et <strong>SERVEUR</strong> indiquent qui héberge.</td></tr><tr><td><strong>RÉSEAU > DIFFUSER LES SORTIES NUMÉRIQUES</strong></td><td>Envoie les sorties de la borne (lampes…) vers MameHooker (core flycast, Flycast).</td></tr></tbody></table>

## Problèmes connus

<table><thead><tr><th width="319">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Le jeu ne démarre pas</td><td>Vérifiez <code>naomi2.zip</code> dans <code>bios\dc</code> (<code>naomi.zip</code> ne convient pas), et le jeu parent pour un clone.</td></tr><tr><td>Un jeu GD-ROM ne démarre pas</td><td>Vérifiez le <code>.chd</code> dans le dossier qui porte le nom du <code>.zip</code> (voir <a href="sega-naomi-2.md#jeux-sur-gd-rom-fichiers-chd"><strong>Guides</strong></a>).</td></tr><tr><td>Le jeu est lent ou mal affiché avec Demul</td><td>Utilisez le core flycast ou Flycast, plus compatibles pour la NAOMI 2.</td></tr><tr><td>Les boutons ne sont pas à la bonne place</td><td>Avec Demul, la disposition est la même pour tous les jeux : utilisez le core flycast ou Flycast.</td></tr></tbody></table>
