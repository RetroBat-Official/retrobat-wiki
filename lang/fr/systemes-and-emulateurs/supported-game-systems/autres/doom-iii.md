---
description: Boom3
---

# Doom III

<div align="left"><figure><img src="../../../.gitbook/assets/image (629).png" alt="" width="375"><figcaption></figcaption></figure></div>

## Présentation

**Doom 3** (id Software, 2004) reprend la base martienne de Doom en jeu de tir et d'horreur, avec un éclairage dynamique et des ombres en temps réel. Son extension **Resurrection of Evil** (2005) ajoute une nouvelle campagne et de nouvelles armes.

RetroBat lance ces jeux avec deux portages modernes du moteur : le core libretro **boom3** (par défaut) et **dhewm3**.

Les fichiers des jeux ne sont pas fournis : utilisez ceux de votre propre exemplaire (CD, Steam, GOG).

{% embed url="https://dhewm3.org/" %}

{% embed url="https://docs.libretro.com/library/boom3/" %}

## En bref

<table><thead><tr><th width="269"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\doom3</code></td></tr><tr><td><strong>Extensions</strong></td><td>.boom3 .game</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: boom3</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (fichiers du jeu à fournir)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non (sauvegardes du jeu)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr><tr><td><strong>Pistolets</strong></td><td>—</td></tr><tr><td><strong>Volants</strong></td><td>—</td></tr><tr><td><strong>BIOS optionnels</strong></td><td>—</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="163.25">Émulateur</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>libretro: boom3</strong> (défaut)</td><td>Raccourcis de RetroArch, rendu OpenGL ou Vulkan, fréquence d'images au-delà de 60 images par seconde, accepte aussi les données non patchées (1.0, 1.1).</td><td>Pas de mods dans RetroBat. Dispositions de manette du core moins pratiques que celle de dhewm3.</td></tr><tr><td><strong>dhewm3</strong></td><td>Moteur de référence du core, mods, manette configurée comme Doom 3 BFG, nombreuses options (qualité, luminosité, son surround).</td><td>Données du jeu en version 1.3.1 obligatoires.</td></tr></tbody></table>

## BIOS

Aucun BIOS n'est nécessaire. Il faut en revanche les fichiers du jeu (`.pk4`) :

<table><thead><tr><th width="188.25">Jeu</th><th width="182.75">Dossier</th><th>Fichiers</th></tr></thead><tbody><tr><td>Doom 3</td><td><code>roms\doom3\base</code></td><td><code>pak000.pk4</code> à <code>pak008.pk4</code></td></tr><tr><td>Resurrection of Evil</td><td><code>roms\doom3\d3xp</code></td><td><code>pak000.pk4</code>, <code>pak001.pk4</code></td></tr></tbody></table>

Resurrection of Evil a aussi besoin du dossier `base` de Doom 3.

Ces fichiers se trouvent dans le dossier d'installation du jeu : CD patché en 1.3.1, ou versions Steam et GOG (« DOOM 3 », pas « DOOM 3: BFG Edition »). dhewm3 exige la version 1.3.1 ; le core boom3 accepte aussi les CD non patchés (1.0, 1.1).

## Quel format de jeu ?

<table><thead><tr><th width="189">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.boom3</strong> / <strong>.game</strong></td><td>Fichier texte de lancement : sa première ligne donne le chemin du <code>pak000.pk4</code> du jeu (voir <a href="doom-iii.md#creer-les-fichiers-de-lancement"><strong>Guides</strong></a>).</td></tr></tbody></table>

Organisation de `roms\doom3` :

```
roms\doom3\
├── Doom 3.boom3
├── Doom 3 - Resurrection of Evil.boom3
├── base\
│   ├── pak000.pk4
│   ├── …
│   └── pak008.pk4
└── d3xp\
    ├── pak000.pk4
    └── pak001.pk4
```

## Contrôles

### Configuration automatique

**dhewm3** : RetroBat associe les boutons de la manette d'après la disposition de Doom 3 BFG (fichiers `gamepad.cfg` et `gamepad-d3xp.cfg` de dhewm3), PDA sur NORD.

<table><thead><tr><th width="297.75">Manette RetroBat</th><th>Action</th></tr></thead><tbody><tr><td>Stick gauche</td><td>Avancer, reculer, pas de côté</td></tr><tr><td>Stick droit</td><td>Tourner, regarder en haut et en bas</td></tr><tr><td>R2</td><td>Tirer</td></tr><tr><td>L2</td><td>Lampe torche</td></tr><tr><td>SUD</td><td>Sauter</td></tr><tr><td>EST</td><td>S'accroupir</td></tr><tr><td>OUEST</td><td>Recharger</td></tr><tr><td>NORD</td><td>PDA</td></tr><tr><td>L1 / R1</td><td>Arme précédente / arme suivante</td></tr><tr><td>L3</td><td>Courir (maintenir)</td></tr><tr><td>R3</td><td>S'accroupir</td></tr><tr><td>Croix : haut / bas / gauche / droite</td><td>Grenades / BFG / Soul Cube / poings</td></tr><tr><td>START</td><td>Menu</td></tr></tbody></table>

Pour Resurrection of Evil, la croix et L2 suivent la disposition `gamepad-d3xp.cfg` de dhewm3 (armes de l'extension). Les commandes se changent dans le menu de dhewm3 (**Settings > Controls**), mais RetroBat réécrit les boutons de la manette à chaque lancement : pour garder vos réglages, réglez **AUTOCONFIGURER LES MANETTES** sur OFF.

**Core boom3** : **CONTRÔLES > TYPE DE CONTRÔLEUR** choisit la disposition, MANETTE CLASSIQUE (par défaut), MANETTE CLASSIQUE ALT ou MANETTE MODERNE. CLAVIER ET SOURIS joue au clavier et à la souris.

<table><thead><tr><th width="159">Manette RetroBat</th><th width="175.25">Manette classique</th><th width="220.75">Manette classique alt</th><th>Manette moderne</th></tr></thead><tbody><tr><td>Stick gauche</td><td>Avancer, reculer, pas de côté</td><td>Avancer, reculer, pas de côté</td><td>Avancer, reculer, pas de côté</td></tr><tr><td>Stick droit</td><td>Regarder</td><td>Regarder</td><td>Regarder</td></tr><tr><td>Croix</td><td>Avancer, reculer, pas de côté</td><td>Avancer, reculer, pas de côté</td><td>Avancer, reculer, pas de côté</td></tr><tr><td>SUD</td><td>Sauter</td><td>Regarder en bas</td><td>S'accroupir</td></tr><tr><td>EST</td><td>Arme suivante</td><td>Tourner à droite</td><td>Pas de côté droite</td></tr><tr><td>OUEST</td><td>Tirer</td><td>Tourner à gauche</td><td>Sauter</td></tr><tr><td>NORD</td><td>Vue libre (maintenir)</td><td>Regarder en haut</td><td>Pas de côté gauche</td></tr><tr><td>L1 / R1</td><td>Pas de côté gauche / droite</td><td>Sauter / tirer</td><td>Arme précédente / suivante</td></tr><tr><td>L2 / R2</td><td>—</td><td>Courir / arme suivante</td><td>Sauter / tirer</td></tr><tr><td>L3</td><td>S'accroupir</td><td>S'accroupir</td><td>—</td></tr><tr><td>R3</td><td>PDA</td><td>Arme précédente</td><td>—</td></tr><tr><td>START</td><td>Menu</td><td>Menu</td><td>Menu</td></tr><tr><td>SELECT</td><td>PDA</td><td>PDA</td><td>PDA</td></tr></tbody></table>

### Raccourcis

* **dhewm3** :

<table><thead><tr><th width="245.25">Raccourci</th><th>Action</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quitter</td></tr><tr><td><strong>HOTKEY + SUD</strong></td><td>Menu</td></tr><tr><td><strong>HOTKEY + OUEST</strong></td><td>Sauvegarde rapide</td></tr><tr><td><strong>HOTKEY + NORD</strong></td><td>Chargement rapide</td></tr><tr><td><strong>HOTKEY + R3</strong></td><td>Capture d'écran</td></tr></tbody></table>

* **Core boom3** : raccourcis de RetroArch (menu, avance rapide, capture…), sans les sauvegardes instantanées. Les sauvegardes passent par le menu du jeu, ou par les touches de Doom 3 : `F5` sauvegarde rapide, `F9` chargement rapide.

Pour plus de détails, voir la page [**Raccourcis**](../../../navigation/hotkeys.md).

## Dossiers

<table><thead><tr><th width="350.25">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Jeux</td><td><code>roms\doom3</code></td></tr><tr><td>dhewm3 : sauvegardes</td><td><code>saves\doom3\dhewm3\base\savegames</code> (Resurrection of Evil : <code>d3xp\savegames</code>)</td></tr><tr><td>dhewm3 : captures d'écran (format TGA)</td><td><code>saves\doom3\dhewm3\base\screenshots</code></td></tr><tr><td>dhewm3 : configuration</td><td><code>emulators\dhewm3\base\dhewm.cfg</code> (Resurrection of Evil : <code>d3xp\dhewm.cfg</code>)</td></tr><tr><td>Core boom3 : sauvegardes</td><td><code>roms\doom3\base\savegames</code> (Resurrection of Evil : <code>d3xp\savegames</code>)</td></tr><tr><td>Core boom3 : configuration</td><td><code>roms\doom3\base\dhewm.cfg</code></td></tr></tbody></table>

## Guides

### Créer les fichiers de lancement

1. Copiez les dossiers `base` et `d3xp` du dossier d'installation du jeu dans `roms\doom3`.
2. Dans `roms\doom3`, créez un fichier texte et renommez-le `Doom 3.boom3` (l'extension `.txt` doit disparaître).
3. Ouvrez-le avec le Bloc-notes et écrivez sur la première ligne : `base\pak000.pk4`.
4. Pour Resurrection of Evil, créez de la même façon `Doom 3 - Resurrection of Evil.boom3` avec la ligne `d3xp\pak000.pk4`.

Le nom du fichier est celui qui apparaît dans la liste des jeux.

<div align="left"><figure><img src="../../../.gitbook/assets/image (630).png" alt=""><figcaption></figcaption></figure></div>

### Lancer un mod (dhewm3)

1. Placez le dossier du mod dans `roms\doom3`, à côté de `base` (par exemple `roms\doom3\sikkmod`).
2. Créez un fichier `.boom3` dont la première ligne commence par le nom de ce dossier, par exemple `sikkmod\pak000.pk4` : RetroBat lance dhewm3 avec ce dossier comme jeu (`fs_game`).
3. Les lignes suivantes sont ajoutées à la ligne de commande de dhewm3. Pour un mod de Resurrection of Evil, ajoutez par exemple :

```
+set fs_game_base d3xp
```

Autre exemple, pour ouvrir la console et régler le mod :

```
+set com_allowconsole 1 +set g_gib_power 100
```

Liste de mods compatibles : [mods dhewm3](https://dhewm3.org/mods.html). \
Choisissez **dhewm3** comme émulateur pour ces jeux : avec le core boom3, RetroBat ne gère pas les mods.

### Jeu en français

Un patch de traduction française existe pour dhewm3 : [Doom 3 Patch French](https://www.moddb.com/games/doom-iii/addons/doom-3-patch-french).

### Options utiles

* **dhewm3** : **RÉSOLUTION D'ÉCRAN** (résolution du bureau par défaut), **SYNCHRONISATION VERTICALE**, **VIDÉO > QUALITÉ**, **RENDU VISUEL > ANTICRÉNELAGE (MSAA)**, **RENDU VISUEL > LUMINOSITÉ** (Doom 3 est très sombre), **AUDIO > NOMBRE DE CANAUX AUDIO** (STÉRÉO ou SURROUND), **AUDIO > ACTIVER EAX**, **INTERFACE UTILISATEUR > MASQUER ATH**, **INTERFACE UTILISATEUR > AFFICHER LES FPS**, **CONTRÔLES > TOUJOURS COURIR**, **CONTRÔLES > INVERSER L'AXE Y**, **CONTRÔLES > ZONE MORTE JOYSTICK**.
* **Core boom3** : **RÉSOLUTION INTERNE** (1920x1080 par défaut), **VIDÉO > QUALITÉ**, **VIDÉO > FRÉQUENCE D'IMAGES** (au-delà de 60, les images sont interpolées), **CONTRÔLES > TYPE DE CONTRÔLEUR**, **CONTRÔLES > INVERSER L'AXE Y**.

## Problèmes connus

<table><thead><tr><th width="350.25">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Le jeu ne démarre pas</td><td>Vérifiez la ligne du fichier <code>.boom3</code> (<code>base\pak000.pk4</code> ou <code>d3xp\pak000.pk4</code>) et l'emplacement des dossiers <code>base</code> et <code>d3xp</code> dans <code>roms\doom3</code>.</td></tr><tr><td>Resurrection of Evil ne démarre pas</td><td>Le dossier <code>base</code> de Doom 3 doit être présent à côté de <code>d3xp</code>.</td></tr><tr><td>dhewm3 ne démarre pas avec les fichiers d'un CD</td><td>dhewm3 demande la version 1.3.1 : installez le patch officiel, ou utilisez le core boom3.</td></tr><tr><td>Doom 3 BFG Edition ne fonctionne pas</td><td>Cette version n'est pas prise en charge : utilisez la version d'origine (« DOOM 3 » sur Steam, GOG).</td></tr><tr><td>Le jeu est trop sombre</td><td>dhewm3 : augmentez <strong>RENDU VISUEL > LUMINOSITÉ</strong>.</td></tr><tr><td>Pas de sauvegardes instantanées</td><td>Sauvegardez depuis le menu du jeu, ou avec la sauvegarde rapide (voir <a href="../../../navigation/hotkeys.md"><strong>Raccourcis</strong></a>).</td></tr><tr><td>Un mod ne démarre pas</td><td>Utilisez dhewm3 ; pour un mod de Resurrection of Evil, ajoutez <code>+set fs_game_base d3xp</code> dans le fichier <code>.boom3</code>.</td></tr></tbody></table>
