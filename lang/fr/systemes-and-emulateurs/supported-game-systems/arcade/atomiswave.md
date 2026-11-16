---
description: Sammy Corporation
---

# Atomiswave

<div align="left"><figure><img src="../../../.gitbook/assets/image (622).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Présentation

L'**Atomiswave** est une carte d'arcade de Sammy, sortie en 2003. Elle reprend l'architecture de la Dreamcast (processeur SH-4, puce graphique PowerVR2) : ses jeux sont sur cartouches et le panneau de commandes s'échange selon le jeu (joysticks, pistolets, volant). Bon marché, elle prend la suite du Neo Geo MVS chez SNK, qui y publie ses derniers jeux de combat. Les derniers titres sortent en 2009.

Parmi ses jeux : **The King of Fighters XI**, **The King of Fighters Neowave**, **NeoGeo Battle Coliseum**, **Metal Slug 6**, **Samurai Shodown VI** (Samurai Spirits Tenkaichi Kenkakuden), **Guilty Gear Isuka**, **Fist of the North Star**, **The Rumble Fish 2**, **Dolphin Blue**, **Demolish Fist**, **Faster Than Speed**, **Maximum Speed**, et des jeux au pistolet (**Sports Shooting USA**, **Extreme Hunting**, **Ranger Mission**).

RetroBat propose trois émulateurs : le core libretro **flycast** (par défaut), **Flycast** en version autonome et **Demul**.

{% embed url="https://fr.wikipedia.org/wiki/Atomiswave" %}

## En bref

<table><thead><tr><th width="282.75"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\atomiswave</code></td></tr><tr><td><strong>Extensions</strong></td><td>.bin .lst .zip .7z</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: flycast</td></tr><tr><td><strong>BIOS</strong></td><td><code>awbios.zip</code> dans <code>bios\dc</code></td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs (mappage par jeu pour les cores flycast)</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>core flycast, Flycast (gérées par RetroBat) ; Demul par raccourcis</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non (Flycast : jeu en ligne GGPO, propre à l'émulateur)</td></tr><tr><td><strong>Pistolets</strong></td><td>core flycast, Flycast, Demul</td></tr><tr><td><strong>Volants</strong></td><td>Flycast</td></tr><tr><td><strong>BIOS optionnels</strong></td><td>—</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="190.75">Émulateur</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>libretro: flycast</strong> (défaut)</td><td>Très bonne compatibilité, boutons placés comme sur la borne pour chaque jeu, sauvegardes instantanées, jusqu'à 4 pistolets, shaders et raccourcis de RetroArch.</td><td>Pas de fichier de mappage fourni pour les volants.</td></tr><tr><td><strong>flycast</strong></td><td>Même base que le core, avec ses propres menus. Mappage par jeu, sauvegardes instantanées, volants (Maximum Speed, Faster Than Speed), pistolets avec DemulShooter, jeu en ligne GGPO.</td><td>—</td></tr><tr><td><strong>demul</strong></td><td>Émulateur historique, aussi utilisé pour la Naomi et la Dreamcast.</td><td>Compatibilité plus faible. Disposition des boutons identique pour tous les jeux. Sauvegardes instantanées non gérées par RetroBat. Ne lit pas les <code>.bin</code> / <code>.lst</code>.</td></tr></tbody></table>

## BIOS

<table><thead><tr><th width="204.5">Fichier</th><th width="204.75">Dossier</th><th>Utilisé par</th></tr></thead><tbody><tr><td><code>awbios.zip</code></td><td><code>bios\dc</code></td><td>Tous les émulateurs</td></tr></tbody></table>

`awbios.zip` est le BIOS de l'Atomiswave au format MAME. Le core flycast et Flycast autonome le cherchent tous les deux dans `bios\dc` ; Demul le trouve dans `bios\dc`, `bios` ou le dossier des jeux. Son contenu dépend de la version de MAME (md5 de référence : `0ec5ae5b5a5c4959fa8b43fcf8687f7c`).

## Quel format de jeu ?

<table><thead><tr><th width="154">Format</th><th>Remarques</th></tr></thead><tbody><tr><td><strong>.zip</strong>, <strong>.7z</strong></td><td>Jeux au format MAME, à garder sans les décompresser et sans les renommer (<code>kofxi.zip</code>, <code>mslug6.zip</code>, <code>ngbc.zip</code>…). Les clones (<code>kofnwj</code>, <code>ngbcj</code>…) ont besoin du jeu parent dans le même dossier.</td></tr><tr><td><strong>.bin</strong>, <strong>.lst</strong></td><td>Ancien format NullDC (une image <code>.bin</code> et sa liste <code>.lst</code>) : cores flycast et Flycast uniquement.</td></tr></tbody></table>

## Contrôles

### Configuration automatique

RetroBat configure les manettes pour les trois émulateurs. Les commandes communes à tous les jeux :

<table><thead><tr><th width="237.75">Borne</th><th>Manette</th></tr></thead><tbody><tr><td>Joystick</td><td>Croix directionnelle, stick gauche</td></tr><tr><td>Start</td><td>START</td></tr><tr><td>Crédit</td><td>SELECT</td></tr><tr><td>Test</td><td>R3 (avec le menu service activé, voir <a href="atomiswave.md#menu-service-et-menu-de-test"><strong>Guides</strong></a>)</td></tr><tr><td>Service</td><td>L3 (avec le menu service activé, voir <a href="atomiswave.md#menu-service-et-menu-de-test"><strong>Guides</strong></a>)</td></tr></tbody></table>

* **Core flycast** et **Flycast** : la position des boutons d'action est définie jeu par jeu, pour retrouver la disposition de la borne. Les fichiers utilisés sont `libretro_flycast_atomiswave.yml` (core) et `flycast_Arcade.yml` (Flycast), voir la page [**Configuration des touches par émulateur**](../../../controleurs/controller-configuration.md#adapter-les-controles-sans-desactiver-lautoconfiguration). **CONTRÔLES > DISPOSITION DES BOUTONS** choisit une autre disposition quand le fichier en propose une.
* **Flycast** : **CONTRÔLES > UTILISER PAD DIRECTIONNEL** déplace les commandes analogiques sur la croix.
* **Demul** : même disposition pour tous les jeux : boutons 1 à 4 sur SUD, EST, OUEST, NORD, boutons 5 à 8 sur L1, R1, L2, R2.

### Pistolets

Les jeux au pistolet (**Sports Shooting USA**, **Extreme Hunting**, **Extreme Hunting 2**, **Ranger Mission**, **Sega Clay Challenge**) fonctionnent avec le core flycast (jusqu'à 4 pistolets), Flycast (2 pistolets, 4 avec DemulShooter) et Demul (1 pistolet, 2 avec DemulShooter). Pour les options et les boutons, voir la page [**Contrôle des pistolets**](../../../controleurs/pistolets_controles.md).

### Volants

Flycast gère les volants pour **Maximum Speed** et **Faster Than Speed** (**VOLANTS DE COURSE > ACTIVER LES VOLANTS**, **DISPOSITION DES BOUTONS DU VOLANT**). Le core flycast gère aussi les volants, mais RetroBat ne fournit pas encore son fichier de mappage. Pour les volants pris en charge, voir la page [**Volants**](../../../controleurs/supported-controllers/volants.md).

### Raccourcis

Le core flycast utilise les raccourcis standards de RetroArch (voir la page [**Raccourcis**](../../../navigation/hotkeys.md)).

**Flycast**

<table><thead><tr><th width="194.5">Raccourci</th><th>Action</th><th>Clavier</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quitter</td><td>Échap</td></tr><tr><td><strong>HOTKEY + SUD</strong></td><td>Menu de Flycast</td><td>F1</td></tr><tr><td><strong>HOTKEY + OUEST</strong></td><td>Sauvegarde instantanée</td><td>F2</td></tr><tr><td><strong>HOTKEY + NORD</strong></td><td>Chargement instantané</td><td>F4</td></tr><tr><td><strong>HOTKEY + DROITE</strong></td><td>Avance rapide (maintenir)</td><td>L</td></tr><tr><td><strong>HOTKEY + R3</strong></td><td>Capture d'écran</td><td>F8</td></tr></tbody></table>

**Demul**

<table><thead><tr><th width="204.5">Raccourci</th><th>Action</th><th>Clavier</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quitter</td><td></td></tr><tr><td><strong>HOTKEY + OUEST</strong></td><td>Sauvegarde instantanée de Demul</td><td>F2</td></tr><tr><td><strong>HOTKEY + NORD</strong></td><td>Chargement instantané de Demul</td><td>F4</td></tr></tbody></table>

Les sauvegardes instantanées de Demul restent dans Demul : elles n'apparaissent pas dans le gestionnaire de sauvegardes.

## Dossiers

<table><thead><tr><th width="354">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>BIOS</td><td><code>bios\dc</code></td></tr><tr><td>Core flycast : sauvegardes instantanées</td><td><code>saves\atomiswave\libretro.flycast</code></td></tr><tr><td>Flycast : sauvegardes des jeux (NVRAM)</td><td><code>saves\atomiswave\reicast</code></td></tr><tr><td>Flycast : sauvegardes instantanées</td><td><code>saves\atomiswave\flycast\sstates</code> (copiées depuis <code>saves\atomiswave\reicast\states</code>)</td></tr><tr><td>Flycast : configuration</td><td><code>emulators\flycast\emu.cfg</code></td></tr><tr><td>Demul : sauvegardes des jeux (NVRAM)</td><td><code>saves\atomiswave\demul</code></td></tr><tr><td>Demul : configuration</td><td><code>emulators\demul\Demul.ini</code>, <code>emulators\demul\padDemul.ini</code></td></tr><tr><td>Mappage par jeu (core flycast, Flycast)</td><td><code>system\resources\inputmapping</code> (copie modifiable dans <code>user\inputmapping</code>)</td></tr></tbody></table>

## Guides

### Menu service et menu de test

Le menu de test de la borne permet de régler le nombre de crédits, la difficulté, le nombre de rounds, et de vérifier les commandes.

1. Activez **ÉMULATION > MODE SERVICE** (core flycast) ou **ÉMULATION > ACTIVER LE MENU SERVICE** (Flycast). Avec Demul, les boutons sont toujours actifs.
2. En jeu, appuyez sur **R3** (Test) pour ouvrir le menu, puis naviguez avec les boutons de la borne. **L3** (Service) ajoute un crédit de service.

<div align="left"><figure><img src="../../../.gitbook/assets/image (623).png" alt="" width="563"><figcaption></figcaption></figure></div>

### Crédits

Les jeux Atomiswave n'ont pas de mode jeu gratuit réglable par l'émulateur : ajoutez des crédits avec **SELECT**, ou réglez le jeu gratuit dans le menu de test du jeu quand il le propose.

### Autres options utiles

<table><thead><tr><th width="337.75">Option</th><th>Effet</th></tr></thead><tbody><tr><td><strong>RÉSOLUTION INTERNE</strong></td><td>Augmente la résolution de rendu (les trois émulateurs).</td></tr><tr><td><strong>RAPPORT D'ASPECT</strong></td><td>Flycast, Demul : 4:3, 16:9 ou étiré.</td></tr><tr><td><strong>RENDU VISUEL > HACK ÉCRAN LARGE</strong> (core flycast)</td><td>Étend l'image en 16:9, avec des défauts sur certains jeux.</td></tr><tr><td><strong>VIDÉO > MODE TATÉ</strong></td><td>Affichage vertical (core flycast, Flycast).</td></tr><tr><td><strong>RÉSEAU > DIFFUSER LES SORTIES NUMÉRIQUES</strong></td><td>Envoie les sorties de la borne (lampes…) vers MameHooker (core flycast, Flycast).</td></tr></tbody></table>

## Problèmes connus

<table><thead><tr><th width="326.5">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Le jeu ne démarre pas</td><td>Vérifiez <code>awbios.zip</code> dans <code>bios\dc</code>, et le jeu parent pour un clone.</td></tr><tr><td>Le jeu demande des crédits</td><td>Appuyez sur <strong>SELECT</strong> pour ajouter un crédit.</td></tr><tr><td>Les boutons ne sont pas à la bonne place</td><td>Avec Demul, la disposition est la même pour tous les jeux : utilisez le core flycast ou Flycast.</td></tr><tr><td>Un jeu <code>.bin</code> / <code>.lst</code> ne démarre pas avec Demul</td><td>Demul ne lit que les jeux au format MAME : utilisez le core flycast ou Flycast.</td></tr><tr><td>Le jeu au pistolet ne réagit pas</td><td>Activez <strong>PISTOLETS > ACTIVER LES PISTOLETS</strong>, puis consultez la page <a href="../../../controleurs/pistolets_controles.md"><strong>Contrôle des pistolets</strong></a>.</td></tr></tbody></table>
