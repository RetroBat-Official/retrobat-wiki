---
description: Fujitsu
---

# FM-TOWNS

<div align="left"><figure><img src="../../../../.gitbook/assets/image (747).png" alt="" width="479"><figcaption></figcaption></figure></div>

## Présentation

Le **FM Towns** est un ordinateur de Fujitsu sorti en 1989, au Japon uniquement. C'est l'un des premiers ordinateurs livrés avec un lecteur de CD-ROM de série. Il a un processeur 80386, 32 768 couleurs, un son FM et PCM, et sa propre interface graphique, Towns OS. Fujitsu en sort de nombreux modèles jusqu'en 1997, et en 1993 une console compatible, le **FM Towns Marty**.

Sa ludothèque compte surtout des jeux sur CD-ROM, souvent des versions améliorées de jeux d'autres machines : Super Street Fighter II, Splatterhouse, Rayxanber, Alltynex, Zak McKracken and the Alien Mindbenders (sa seule version en 256 couleurs), Alone in the Dark, Lemmings…

{% embed url="https://fr.wikipedia.org/wiki/FM_Towns" %}

## En bref

<table><thead><tr><th width="270.25"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\fmtowns</code></td></tr><tr><td><strong>Extensions</strong></td><td>.m3u .d88 .d77 .hdm .xdf .cue .iso .img .mfm .game .cd .chd .zip</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: geartowns</td></tr><tr><td><strong>BIOS</strong></td><td>Obligatoire (4 ROM du FM Towns)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique (Tsugaru : première manette détectée par Windows)</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro ; MAME par raccourcis</td></tr><tr><td><strong>RetroAchievements</strong></td><td>core geartowns</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>cores libretro geartowns et mame</td></tr></tbody></table>

## Quel émulateur choisir ?

| Émulateur                        | Pour qui ?           | Points forts                                                                                                                                                                                                                                                           | Limites                                                                                                                                                                                             |
| -------------------------------- | -------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **libretro: geartowns** (défaut) | Tout le monde        | Geartowns, émulateur dédié au FM Towns : base de jeux (modèle, vitesse et mémoire choisis automatiquement), CD-ROM et disquettes, changement de disque, manettes 2 et 6 boutons et Marty, souris au stick, RetroAchievements, jeu en réseau, sauvegardes instantanées. | —                                                                                                                                                                                                   |
| **tsugaru**                      | Puristes             | Tsugaru, émulateur très précis du FM Towns.                                                                                                                                                                                                                            | Ni `.chd`, ni `.m3u`, ni `.zip`. Une seule manette, sans configuration. Pas de sauvegardes instantanées ni de raccourcis RetroBat (seul HOTKEY + START, pour quitter). Pas d'options dans RetroBat. |
| **libretro: mame**               | Utilisateurs de MAME | MAME : FM Towns Model 1/2, II UX et Marty, listes de logiciels, jeu en réseau.                                                                                                                                                                                         | Plus lent et moins compatible que geartowns.                                                                                                                                                        |
| **mame64** (MAME autonome)       | Utilisateurs de MAME | Même émulation que le core libretro mame.                                                                                                                                                                                                                              | Mêmes limites.                                                                                                                                                                                      |

**En cas de doute, gardez libretro: geartowns.**

## BIOS

Le FM Towns a besoin de 4 ROM : système, OS, police et dictionnaire. Ce sont celles du FM Towns Model 1/2, le modèle de base, utilisé par défaut.

<table><thead><tr><th width="126.5">Fichier</th><th width="125">Nom MAME</th><th width="323">MD5</th><th>Utilisé par</th></tr></thead><tbody><tr><td><code>FMT_SYS.ROM</code></td><td><code>fmt_sys.rom</code></td><td>feaf8c5675151e00cfe3ad27673bff29</td><td>tous</td></tr><tr><td><code>FMT_DOS.ROM</code></td><td><code>fmt_dos.rom</code></td><td>0585b19930d4a7f4c71bcc8a33746588</td><td>tous</td></tr><tr><td><code>FMT_FNT.ROM</code></td><td><code>fmt_fnt.rom</code></td><td>eb44f2093f51eb7159f03e170b13af76</td><td>tous</td></tr><tr><td><code>FMT_DIC.ROM</code></td><td><code>fmt_dic.rom</code></td><td>34847786d7de94b5d1133c956ab1d75d</td><td>tous</td></tr><tr><td><code>FMT_F20.ROM</code></td><td><code>fmt_f20.rom</code></td><td>—</td><td>geartowns, facultatif (police 20 points)</td></tr></tbody></table>

Où les mettre ? Les noms sont acceptés en majuscules ou en minuscules.

<table><thead><tr><th>Emplacement</th><th width="102.75">geartowns</th><th width="113">Tsugaru</th><th width="83.75">MAME</th></tr></thead><tbody><tr><td><code>bios\fmtowns\</code> (les 4 fichiers)</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td><code>bios\fmtowns.zip</code> (jeu de ROM MAME)</td><td>✅</td><td>—</td><td>✅</td></tr><tr><td><code>bios\geartowns\</code> (les 4 fichiers)</td><td>✅</td><td>✅</td><td>—</td></tr><tr><td><code>bios\geartowns\fmtowns\</code> ou <code>bios\geartowns\fmtowns.zip</code></td><td>✅</td><td>dossier seulement</td><td>—</td></tr></tbody></table>

**Le plus simple : les 4 fichiers dans `bios\fmtowns\`**, qui marche avec les trois émulateurs. La vérification des BIOS de RetroBat accepte chacun de ces emplacements.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (748).png" alt=""><figcaption></figcaption></figure></div>

Les autres modèles demandent leur propre jeu de ROM :

<table><thead><tr><th width="221.75">Modèle</th><th>Jeu de ROM</th><th width="109">geartowns</th><th width="152">MAME</th></tr></thead><tbody><tr><td>FM Towns 1F/2F, 10F/20F, II CX, II UX, II UG</td><td><code>fmtownsux</code> (II UX)</td><td>✅</td><td>II UX seulement</td></tr><tr><td>FM Towns II HG</td><td><code>fmtownshr</code> (II HR), ou à défaut <code>fmtownsftv</code> (Fresh TV)</td><td>✅</td><td>—</td></tr><tr><td>FM Towns Marty</td><td><code>fmtmarty</code> (<code>mrom.m36</code>, <code>mrom.m37</code>)</td><td>✅</td><td>✅</td></tr></tbody></table>

Rangez-les en zip MAME dans `bios` (`bios\fmtownsux.zip`…) ou dans `bios\geartowns` (`bios\geartowns\fmtownsux\`…). La vérification des BIOS les liste comme optionnels.

Tsugaru enregistre les réglages de la machine (CMOS) dans un fichier `CMOS.DAT`, dans le dossier des ROM qu'il utilise.

## Quel format de jeu ?

<table><thead><tr><th width="172">Type</th><th width="240.5">Extensions</th><th>Remarques</th></tr></thead><tbody><tr><td>CD-ROM</td><td><code>.cue</code> (avec ses <code>.bin</code>), <code>.iso</code>, <code>.chd</code></td><td>La plupart des jeux. <code>.chd</code> : pas avec Tsugaru.</td></tr><tr><td>CD-ROM (dossier)</td><td><code>.game</code>, <code>.cd</code></td><td>Dossier qui contient le <code>.cue</code> et ses pistes, renommé en <code>Jeu.game</code> ou <code>Jeu.cd</code>. Tsugaru et MAME.</td></tr><tr><td>Disquette</td><td><code>.d88</code>, <code>.d77</code>, <code>.hdm</code>, <code>.xdf</code>, <code>.img</code>, <code>.mfm</code></td><td><code>.mfm</code> : pas avec Tsugaru.</td></tr><tr><td>Plusieurs disques</td><td><code>.m3u</code></td><td>Liste des CD ou disquettes d'un jeu. geartowns et MAME.</td></tr><tr><td>Archive</td><td><code>.zip</code></td><td>geartowns et MAME.</td></tr></tbody></table>

Quelques jeux sur CD demandent une disquette pour sauvegarder : voir [**Guides**](fm-towns.md#jeux-qui-demandent-une-disquette-de-sauvegarde).

## Contrôles

RetroBat configure automatiquement les manettes pour geartowns et MAME. La manette du FM Towns a deux boutons **A** et **B**, et les touches **RUN** et **SELECT**. La souris du PC sert de souris FM Towns, et le clavier du PC de clavier FM Towns.

| Manette RetroBat     | geartowns (manette d'origine)  | geartowns (manette 6 boutons) | tsugaru (manette XInput) |
| -------------------- | ------------------------------ | ----------------------------- | ------------------------ |
| Croix directionnelle | Croix                          | Croix                         | Croix                    |
| SUD                  | B                              | B                             | A                        |
| EST                  | A                              | C                             | B                        |
| OUEST                | —                              | A                             | RUN                      |
| NORD                 | —                              | Y                             | SELECT                   |
| START                | RUN                            | RUN                           | —                        |
| SELECT               | SELECT                         | SELECT                        | —                        |
| L1                   | —                              | X                             | —                        |
| R1                   | — (Zoom avec la manette Marty) | Z                             | —                        |

* Avec geartowns, **CONTRÔLES > TYPE DE CONTRÔLEUR JOUEUR 1 / JOUEUR 2** : **MANETTE D'ORIGINE** (défaut au port 1), **MANETTE MARTY**, **MANETTE 6 BOUTONS** (Super Street Fighter II), **SOURIS** (défaut au port 2), **CLAVIER**.
* Avec geartowns, **CONTRÔLES > SOURIS AU STICK ANALOGIQUE** déplace la souris au stick gauche ou droit (L2 / R2 = boutons). Un port doit être réglé sur **SOURIS**. **SENSIBILITÉ DE LA SOURIS** et **VITESSE DE LA SOURIS ANALOGIQUE** règlent la vitesse.
* Tsugaru utilise la première manette détectée par Windows (port 1) et la souris (port 2). Les boutons dépendent de la manette : avec une manette XInput, les 4 premiers boutons sont SUD, EST, OUEST, NORD.
* Avec MAME, **CONTRÔLES > TYPE DE JOYSTICK** choisit la manette émulée (**Manette FM Towns 2 boutons**, **Manette FM Towns 6 boutons**, **Manette FM Towns Marty**…). Les contrôles suivent la disposition de MAME : voir la page **MAME**.

Avec les cores libretro, appuyez sur `Arrêt défil` pour activer le **Game Focus** de RetroArch : toutes les touches du clavier vont au FM Towns. Pour mettre des touches du clavier sur la manette, voir la page [**Pad2Key**](../../../../controleurs/pad2key.md).

### Raccourcis

Les cores libretro utilisent les raccourcis standards de RetroArch. MAME autonome utilise les raccourcis communs de RetroBat. Avec Tsugaru, seul HOTKEY + START (quitter) marche ; `Arrêt défil` met en pause. Voir la page [**Raccourcis**](../../../../navigation/hotkeys.md).

## Dossiers

| Contenu                                   | Dossier                                                                             |
| ----------------------------------------- | ----------------------------------------------------------------------------------- |
| Jeux                                      | `roms\fmtowns`                                                                      |
| BIOS                                      | `bios\fmtowns`, `bios\geartowns`, `bios` (zips MAME)                                |
| geartowns : CMOS (réglages de la machine) | `saves\fmtowns\geartowns.geartowns.cmos` (un fichier par jeu avec **CMOS PAR JEU**) |
| geartowns : disquettes de sauvegarde      | `saves\fmtowns`                                                                     |
| Cores libretro : sauvegardes instantanées | `saves\fmtowns\libretro.<core>`                                                     |
| Tsugaru : CMOS                            | `CMOS.DAT` dans le dossier des ROM utilisé                                          |
| MAME : disque utilisateur                 | `saves\mame\fmtowns`                                                                |
| MAME autonome                             | Voir la page [**MAME**](../../arcade/mame.md)                                       |

## Guides

### Modèle, vitesse et mémoire

Avec geartowns, laissez **ÉMULATION > MODÈLE**, **VITESSE DU CPU** et **MÉMOIRE RAM** sur automatique : le core choisit d'après sa base de jeux. Quelques jeux profitent d'un processeur plus rapide (Super Street Fighter II, Alltynex) : **VITESSE DU CPU**. **RECOMPILATION DYNAMIQUE DU CPU** (activée par défaut) accélère la plupart des jeux.

Avec MAME, **ÉMULATION > MODÈLE DE MACHINE ÉMULÉE** : **FM TOWNS (MODEL 1/2) (par défaut)**, **FM TOWNS II UX** ou **FM TOWNS MARTY**. **TAILLE DE LA MÉMOIRE RAM** : 2 ou 4 Mo.

Tsugaru émule un FM Towns à 33 MHz avec 8 Mo de mémoire. Le modèle dépend des ROM utilisées.

### Jeux qui demandent une disquette de sauvegarde

Certains jeux sur CD sauvegardent sur une disquette, ou demandent une disquette système.

* geartowns : activez **ÉMULATION > DISQUETTE DE SAUVEGARDE**. Une disquette vierge est ajoutée à la liste des disques, puis gardée dans `saves\fmtowns`. Insérez-la depuis le menu de RetroArch (**Contrôle du disque**) quand le jeu la demande.
* MAME : **ÉMULATION > AJOUTER UN DISQUE UTILISATEUR** : **DISQUETTE VIERGE**, ou **DISQUETTE SYSTÈME** (placez la disquette système, au nom du jeu avec l'extension `.hdm`, dans `saves\mame\fmtowns`).

### Jeux sur plusieurs disques

Créez un fichier `.m3u` qui liste les CD ou disquettes, un par ligne, puis lancez le `.m3u`. Avec geartowns, changez de disque dans le menu de RetroArch (**Contrôle du disque**). **ÉMULATION > LECTEUR CIBLE DU CHANGEMENT DE DISQUE** choisit le lecteur de disquette, **MULTI-LECTEUR DE DISQUETTES** met aussi la disquette suivante dans le lecteur 2.

### RetroAchievements

Le core geartowns est compatible. Pour plus de détails, voir la page [**RetroAchievements**](../../../../utilisation-avancee/retroachievements.md).

### Autres options utiles

<table><thead><tr><th width="125.75">Émulateur</th><th>Option</th><th>Effet</th></tr></thead><tbody><tr><td>geartowns</td><td><strong>ÉMULATION > VITESSE DE LECTURE CD</strong>, <strong>PRÉCHARGER LE CD-ROM</strong></td><td>Chargements plus rapides. Certains jeux n'aiment pas un lecteur plus rapide.</td></tr><tr><td>geartowns</td><td><strong>ÉMULATION > CMOS PAR JEU</strong></td><td>Réglages de la machine séparés pour chaque jeu (conseillé pour le jeu en réseau).</td></tr><tr><td>geartowns</td><td><strong>ÉMULATION > PÉRIPHÉRIQUE DE DÉMARRAGE</strong></td><td>Force le démarrage sur le CD, une disquette ou un disque dur (modèles 1F/2F et suivants).</td></tr><tr><td>geartowns</td><td><strong>VIDÉO > RAPPORT D'ASPECT DU CORE</strong></td><td>4:3 (défaut), pixels carrés, 16:9, 16:10.</td></tr><tr><td>geartowns</td><td><strong>VIDÉO > SAUT D'IMAGE</strong></td><td>Évite les craquements du son sur un PC lent.</td></tr><tr><td>geartowns</td><td><strong>CONTRÔLES > AUTORISER LES DIRECTIONS OPPOSÉES</strong></td><td>Gauche + droite ou haut + bas en même temps.</td></tr></tbody></table>

## Problèmes connus

| Problème                                                        | Solution                                                                                                                                                            |
| --------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Le jeu ne démarre pas, message de firmware manquant (geartowns) | Les 4 ROM manquent, ou elles ne sont pas dans un emplacement lu (voir [**BIOS**](fm-towns.md#bios)). Pour un autre modèle que le Model 1/2, ajoutez son jeu de ROM. |
| Tsugaru ne démarre pas                                          | Les ROM ne sont pas dans un dossier (Tsugaru ne lit pas les zips), ou le jeu est en `.chd`, `.m3u` ou `.zip`.                                                       |
| Le jeu demande une disquette                                    | Voir [**Jeux qui demandent une disquette de sauvegarde**](fm-towns.md#jeux-qui-demandent-une-disquette-de-sauvegarde).                                              |
| Le jeu saccade ou le son craque                                 | Gardez **RECOMPILATION DYNAMIQUE DU CPU** activée. Sur un PC lent, activez **SAUT D'IMAGE**.                                                                        |
| Un jeu de combat n'a pas tous ses coups                         | Réglez **TYPE DE CONTRÔLEUR JOUEUR 1** sur **MANETTE 6 BOUTONS**.                                                                                                   |
| Les touches du clavier lancent des raccourcis de RetroArch      | Appuyez sur `Arrêt défil` (Game Focus).                                                                                                                             |
