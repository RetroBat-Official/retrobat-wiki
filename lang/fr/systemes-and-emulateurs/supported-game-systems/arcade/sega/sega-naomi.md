---
description: Sega
---

# Sega NAOMI

<div align="left"><figure><img src="../../../../.gitbook/assets/image (631).png" alt="" width="418"><figcaption></figcaption></figure></div>

## Présentation

La **NAOMI** (New Arcade Operation Machine Idea) est une carte d'arcade de Sega, sortie en 1998. Elle reprend l'architecture de la Dreamcast avec plus de mémoire, ce qui facilite les adaptations sur la console. Les jeux sont d'abord sur cartouches, puis sur GD-ROM à partir de 2000 (le disque est copié dans une carte mémoire au démarrage). Très répandue, elle accueille aussi des jeux de Capcom, SNK, Treasure ou Arc System Works, jusqu'à la fin des années 2000.

Parmi ses jeux : **Crazy Taxi**, **The House of the Dead 2**, **Marvel vs. Capcom 2**, **Capcom vs. SNK 2**, **Ikaruga**, **Guilty Gear XX**, **Virtua Tennis**, **Dead or Alive 2**, **Power Stone 2**, **18 Wheeler**, **Ferrari F355 Challenge**, **Zombie Revenge**, **Under Defeat**, **Confidential Mission**.

RetroBat propose trois émulateurs : le core libretro **flycast** (par défaut), **Flycast** en version autonome et **Demul**.

{% embed url="https://fr.wikipedia.org/wiki/Naomi_(syst%C3%A8me_d'arcade)" %}

## En bref

<table><thead><tr><th width="265.25"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\naomi</code></td></tr><tr><td><strong>Extensions</strong></td><td>.bin .dat .lst .zip .7z .decomp</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: flycast</td></tr><tr><td><strong>BIOS</strong></td><td><code>naomi.zip</code> dans <code>bios\dc</code></td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs (mappage par jeu pour les cores flycast)</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>core flycast, Flycast (gérées par RetroBat) ; Demul par raccourcis</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non (Flycast : GGPO et réseau NAOMI, propres à l'émulateur)</td></tr><tr><td><strong>Pistolets</strong></td><td>core flycast, Flycast, Demul</td></tr><tr><td><strong>Volants</strong></td><td>Flycast</td></tr><tr><td><strong>BIOS optionnels</strong></td><td><code>hod2bios.zip</code>, <code>f355bios.zip</code>, <code>f355dlx.zip</code>, <code>airlbios.zip</code> dans <code>bios\dc</code> (jeux qui ont leur propre <a href="sega-naomi.md#bios">BIOS</a>)</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="165.75">Émulateur</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>libretro: flycast</strong> (défaut)</td><td>Très bonne compatibilité, boutons placés comme sur la borne pour chaque jeu, sauvegardes instantanées, jusqu'à 4 pistolets, shaders et raccourcis de RetroArch.</td><td>Pas de fichier de mappage fourni pour les volants.</td></tr><tr><td><strong>flycast</strong></td><td>Même base que le core, avec ses propres menus. Mappage par jeu, sauvegardes instantanées, volants, pistolets avec DemulShooter, jeu en ligne GGPO et réseau NAOMI (bornes reliées).</td><td>—</td></tr><tr><td><strong>demul</strong></td><td>Émulateur historique, aussi utilisé pour l'Atomiswave et la Dreamcast.</td><td>Compatibilité plus faible. Disposition des boutons identique pour tous les jeux. Sauvegardes instantanées non gérées par RetroBat. Ne lit pas les <code>.bin</code> / <code>.dat</code> / <code>.lst</code>.</td></tr></tbody></table>

## BIOS

<table><thead><tr><th width="177">Fichier</th><th width="152.5">Dossier</th><th>Utilisé par</th></tr></thead><tbody><tr><td><code>naomi.zip</code></td><td><code>bios\dc</code></td><td>Tous les jeux, tous les émulateurs</td></tr><tr><td><code>hod2bios.zip</code></td><td><code>bios\dc</code></td><td>The House of the Dead 2</td></tr><tr><td><code>f355bios.zip</code></td><td><code>bios\dc</code></td><td>Ferrari F355 Challenge Twin</td></tr><tr><td><code>f355dlx.zip</code></td><td><code>bios\dc</code></td><td>Ferrari F355 Challenge (version deluxe)</td></tr><tr><td><code>airlbios.zip</code></td><td><code>bios\dc</code></td><td>Airline Pilots</td></tr></tbody></table>

Ces archives sont au format MAME. Le core flycast et Flycast autonome les cherchent tous les deux dans `bios\dc` ; Demul les trouve dans `bios\dc`, `bios` ou le dossier des jeux. Leur contenu dépend de la version de MAME (md5 de référence de `naomi.zip` : `eb4099aeb42ef089cfe94f8fe95e51f6`). Les jeux sur GD-ROM utilisent aussi `naomi.zip`.

## Quel format de jeu ?

<table><thead><tr><th width="171.5">Format</th><th>Remarques</th></tr></thead><tbody><tr><td><strong>.zip</strong>, <strong>.7z</strong></td><td>Jeux au format MAME, à garder tels quels, sans les décompresser ni les renommer (<code>crzytaxi.zip</code>, <code>mvsc2.zip</code>, <code>hotd2.zip</code>…). Les clones ont besoin du jeu parent dans le même dossier. Les jeux sur GD-ROM ont aussi un fichier <code>.chd</code> (voir <a href="sega-naomi.md#jeux-sur-gd-rom-fichiers-chd"><strong>Guides</strong></a>).</td></tr><tr><td><strong>.bin</strong>, <strong>.dat</strong>, <strong>.lst</strong></td><td>Ancien format NullDC (images <code>.bin</code> / <code>.dat</code> et leur liste <code>.lst</code>) : cores flycast et Flycast uniquement.</td></tr><tr><td><strong>.decomp</strong></td><td>Portage PC, voir la page <a href="../../autres/recomp.md"><strong>Recompilations</strong></a>.</td></tr></tbody></table>

## Contrôles

### Configuration automatique

RetroBat configure les manettes pour les trois émulateurs. Les commandes communes à tous les jeux :

<table><thead><tr><th width="152.75">Borne</th><th>Manette</th></tr></thead><tbody><tr><td>Joystick</td><td>Croix directionnelle, stick gauche</td></tr><tr><td>Start</td><td>START</td></tr><tr><td>Crédit</td><td>SELECT</td></tr><tr><td>Test</td><td>R3 (avec le menu service activé, voir <a href="sega-naomi.md#menu-service-et-menu-de-test"><strong>Guides</strong></a>)</td></tr><tr><td>Service</td><td>L3 (avec le menu service activé, voir <a href="sega-naomi.md#menu-service-et-menu-de-test"><strong>Guides</strong></a>)</td></tr></tbody></table>

* **Core flycast** et **Flycast** : la position des boutons d'action est définie jeu par jeu, pour retrouver la disposition de la borne. Les fichiers utilisés sont `libretro_flycast_naomi.yml` (core) et `flycast_Arcade.yml` (Flycast), voir la page [**Configuration des touches par émulateur**](../../../../controleurs/controller-configuration.md#adapter-les-controles-sans-desactiver-lautoconfiguration). **CONTRÔLES > DISPOSITION DES BOUTONS** choisit une autre disposition quand le fichier en propose une (par exemple pour Dead or Alive 2).
* **Flycast** : **CONTRÔLES > UTILISER PAD DIRECTIONNEL** déplace les commandes analogiques sur la croix.
* **Demul** : même disposition pour tous les jeux : boutons 1 à 4 sur SUD, EST, OUEST, NORD, boutons 5 à 8 sur L1, R1, L2, R2.

### Pistolets

Les jeux au pistolet (**The House of the Dead 2**, **Confidential Mission**, **Death Crimson OX**, **Ninja Assault**, **Lupin the Third: The Shooting**) fonctionnent avec le core flycast (jusqu'à 4 pistolets), Flycast (2 pistolets, 4 avec DemulShooter) et Demul (1 pistolet, 2 avec DemulShooter). Pour les options et les boutons, voir la page [**Contrôle des pistolets**](../../../../controleurs/pistolets_controles.md).

### Volants

Flycast gère les volants (**VOLANTS DE COURSE > ACTIVER LES VOLANTS**) pour **18 Wheeler**, **Crazy Taxi**, **Ferrari F355 Challenge** (avec l'embrayage), **Tokyo Bus Guide** et **Wave Runner GP**. **VOLANTS DE COURSE > DISPOSITION DES BOUTONS DU VOLANT** adapte les boutons au jeu (par exemple la marche arrière sur B pour Crazy Taxi). Le core flycast gère aussi les volants, mais RetroBat ne fournit pas encore son fichier de mappage. Pour les volants pris en charge, voir la page [**Volants**](../../../../controleurs/supported-controllers/volants.md).

### Raccourcis

Le core flycast utilise les raccourcis standards de RetroArch (voir la page [**Raccourcis**](../../../../navigation/hotkeys.md)).

**Flycast**

| Raccourci           | Action                    | Clavier |
| ------------------- | ------------------------- | ------- |
| **HOTKEY + START**  | Quitter                   | Échap   |
| **HOTKEY + SUD**    | Menu de Flycast           | F1      |
| **HOTKEY + OUEST**  | Sauvegarde instantanée    | F2      |
| **HOTKEY + NORD**   | Chargement instantané     | F4      |
| **HOTKEY + DROITE** | Avance rapide (maintenir) | L       |
| **HOTKEY + R3**     | Capture d'écran           | F8      |

**Demul**

| Raccourci          | Action                          | Clavier |
| ------------------ | ------------------------------- | ------- |
| **HOTKEY + START** | Quitter                         |         |
| **HOTKEY + OUEST** | Sauvegarde instantanée de Demul | F2      |
| **HOTKEY + NORD**  | Chargement instantané de Demul  | F4      |

Les sauvegardes instantanées de Demul restent dans Demul : elles n'apparaissent pas dans le gestionnaire de sauvegardes.

## Dossiers

| Contenu                                        | Dossier                                                                     |
| ---------------------------------------------- | --------------------------------------------------------------------------- |
| BIOS                                           | `bios\dc`                                                                   |
| Core flycast : sauvegardes instantanées        | `saves\naomi\libretro.flycast`                                              |
| Flycast : sauvegardes des jeux (NVRAM, EEPROM) | `saves\naomi\reicast`                                                       |
| Flycast : sauvegardes instantanées             | `saves\naomi\flycast\sstates` (copiées depuis `saves\naomi\reicast\states`) |
| Flycast : configuration                        | `emulators\flycast\emu.cfg`                                                 |
| Demul : sauvegardes des jeux (NVRAM)           | `saves\naomi\demul`                                                         |
| Demul : configuration                          | `emulators\demul\Demul.ini`, `emulators\demul\padDemul.ini`                 |
| Mappage par jeu (core flycast, Flycast)        | `system\resources\inputmapping` (copie modifiable dans `user\inputmapping`) |

## Guides

### Jeux sur GD-ROM (fichiers CHD)

Les jeux sur GD-ROM (**Ikaruga**, **Capcom vs. SNK 2**, **Guilty Gear XX**…) ont besoin, en plus de leur `.zip`, de l'image du disque au format `.chd`. Placez le `.chd` dans un dossier qui porte le nom du `.zip`, sans renommer ni l'un ni l'autre :

```
roms\
└─ naomi\
   ├─ ikaruga\
   │  └─ gdl-0010.chd
   └─ ikaruga.zip
```

Seul le `.zip` apparaît dans la liste des jeux.

### Menu service et menu de test

Le menu de test de la borne permet de régler le nombre de crédits, la difficulté, le nombre de rounds, et de vérifier les commandes.

1. Activez **ÉMULATION > MODE SERVICE** (core flycast) ou **ÉMULATION > ACTIVER LE MENU SERVICE** (Flycast). Avec Demul, les boutons sont toujours actifs.
2. En jeu, appuyez sur **R3** (Test) pour ouvrir le menu, puis naviguez avec les boutons de la borne. **L3** (Service) ajoute un crédit de service.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (632).png" alt="" width="563"><figcaption></figcaption></figure></div>

### Jeu gratuit et région

* **ÉMULATION > JEU GRATUIT** (core flycast, Flycast, activé par défaut) configure le jeu sans pièces : START suffit pour jouer. Désactivé, ajoutez des crédits avec **SELECT**.
* **ÉMULATION > RÉGION** (core flycast) choisit la région de la borne (Japon, USA, Europe) : elle change la langue et parfois le contenu du jeu.

Ces réglages sont écrits dans la mémoire de la borne au lancement. Si un jeu garde l'ancien réglage, changez-le aussi dans son menu de test.

### Autres options utiles

<table><thead><tr><th width="307.75">Option</th><th>Effet</th></tr></thead><tbody><tr><td><strong>RÉSOLUTION INTERNE</strong></td><td>Augmente la résolution de rendu (les trois émulateurs).</td></tr><tr><td><strong>RAPPORT D'ASPECT</strong></td><td>Flycast, Demul : 4:3, 16:9 ou étiré.</td></tr><tr><td><strong>RENDU VISUEL > PATCH ÉCRAN LARGE</strong> / <strong>HACK ÉCRAN LARGE</strong></td><td>Affichage en 16:9 : les patchs corrigent les jeux compatibles, le hack étend l'image de tous les jeux (avec des défauts).</td></tr><tr><td><strong>VIDÉO > MODE TATÉ</strong></td><td>Affichage vertical pour les shoot'em up (Ikaruga, Under Defeat…) sur un écran tourné (core flycast, Flycast).</td></tr><tr><td><strong>RÉSEAU > MODE RÉSEAU</strong> (Flycast)</td><td>GGPO pour les jeux de combat en ligne, ou <strong>NAOMI</strong> pour relier plusieurs bornes ; <strong>MODE HÔTE</strong> et <strong>SERVEUR</strong> indiquent qui héberge.</td></tr><tr><td><strong>RÉSEAU > DIFFUSER LES SORTIES NUMÉRIQUES</strong></td><td>Envoie les sorties de la borne (lampes…) vers MameHooker (core flycast, Flycast).</td></tr></tbody></table>

## Problèmes connus

<table><thead><tr><th width="311.5">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Le jeu ne démarre pas</td><td>Vérifiez <code>naomi.zip</code> dans <code>bios\dc</code> (ou le BIOS propre au jeu), et le jeu parent pour un clone.</td></tr><tr><td>Un jeu GD-ROM ne démarre pas</td><td>Vérifiez le <code>.chd</code> dans le dossier qui porte le nom du <code>.zip</code> (voir <a href="sega-naomi.md#jeux-sur-gd-rom-fichiers-chd"><strong>Guides</strong></a>).</td></tr><tr><td>The House of the Dead 2 ne démarre pas</td><td>Ajoutez <code>hod2bios.zip</code> dans <code>bios\dc</code>.</td></tr><tr><td>Les boutons ne sont pas à la bonne place</td><td>Avec Demul, la disposition est la même pour tous les jeux : utilisez le core flycast ou Flycast.</td></tr><tr><td>Un jeu <code>.bin</code> / <code>.dat</code> / <code>.lst</code> ne démarre pas avec Demul</td><td>Demul ne lit que les jeux au format MAME : utilisez le core flycast ou Flycast.</td></tr><tr><td>Le jeu au pistolet ne réagit pas</td><td>Activez <strong>PISTOLETS > ACTIVER LES PISTOLETS</strong>, puis consultez la page <a href="../../../../controleurs/pistolets_controles.md"><strong>Contrôle des pistolets</strong></a>.</td></tr></tbody></table>
