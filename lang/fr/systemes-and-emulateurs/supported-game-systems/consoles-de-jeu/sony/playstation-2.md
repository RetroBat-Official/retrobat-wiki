---
description: Sony
---

# PlayStation 2

<div align="left"><figure><img src="../../../../.gitbook/assets/image (421).png" alt=""><figcaption></figcaption></figure></div>

## Présentation

La PlayStation 2 est la deuxième console de salon de Sony, après la première PlayStation (1994). Elle sort au Japon le 4 mars 2000, puis en Amérique du Nord en octobre et en Europe en novembre de la même année. Son lancement est un véritable événement : les stocks partent en quelques jours, et la console reste difficile à trouver pendant des mois.

À l'intérieur, la PS2 repose sur l'**Emotion Engine**, un processeur conçu avec Toshiba, et sur le **Graphics Synthesizer**, sa puce graphique. C'est aussi l'une des premières consoles à lire les **DVD** : à une époque où les lecteurs DVD coûtent encore cher, beaucoup l'achètent aussi pour regarder des films. Elle lit également les **jeux PlayStation**, ce qui permet de garder son ancienne ludothèque. Des accessoires ajoutent ensuite le jeu en ligne (adaptateur réseau, disque dur pour Final Fantasy XI), la caméra EyeToy, les micros SingStar ou les guitares Guitar Hero. En 2004, un modèle **Slim** beaucoup plus compact remplace le modèle d'origine.

Avec plus de 155 millions d'exemplaires vendus, la PS2 est la console de salon la plus vendue de l'histoire. Produite jusqu'à fin 2012, elle possède l'une des ludothèques les plus riches jamais vues : Gran Turismo 3 et 4, Final Fantasy X et XII, Metal Gear Solid 2 et 3, Grand Theft Auto III, Vice City et San Andreas, Kingdom Hearts, Shadow of the Colossus, God of War, Ratchet & Clank, Jak and Daxter, Silent Hill 2, Devil May Cry, Tekken 5…

{% embed url="https://fr.wikipedia.org/wiki/PlayStation_2" %}

{% hint style="info" %}
**Les jeux PlayStation (PS1) vont dans le système PlayStation** (`roms\psx`), pas dans le système PlayStation 2, même si la PS2 savait les lire.
{% endhint %}

## En bref

<table><thead><tr><th width="215.25"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\ps2</code></td></tr><tr><td><strong>Extensions</strong></td><td>.iso .cso .bin .mdf .gz .chd .m3u .zip .7z .squashfs .decomp</td></tr><tr><td><strong>Émulateurs</strong></td><td><strong>pcsx2</strong> (par défaut), Libretro : pcsx2, play, pcsx2-16</td></tr><tr><td><strong>BIOS</strong></td><td>Nécessaire pour pcsx2, lr-pcsx2 et pcsx2-16 (pas pour play)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>pcsx2, lr-pcsx2</td></tr><tr><td><strong>Netplay</strong></td><td>Non</td></tr><tr><td><strong>Pistolets</strong></td><td>pcsx2 (GunCon 2)</td></tr><tr><td><strong>Volants</strong></td><td>pcsx2</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="172.75">Émulateur</th><th width="175">Pour qui ?</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>pcsx2</strong> (par défaut)</td><td>Tout le monde</td><td>Le plus compatible. HD, patchs écran large, packs de textures, pistolets, volants, guitares, jusqu'à 8 joueurs.</td><td>Demande un PC assez récent pour la HD.</td></tr><tr><td><strong>lr-pcsx2</strong></td><td>Utilisateurs de RetroArch</td><td>Fonctions de RetroArch (shaders, menu RetroArch), moteur de rendu paraLLEl-GS.</td><td>Pas de retour arrière, 2 joueurs, ni pistolet ni volant.</td></tr><tr><td><strong>play</strong></td><td>Utilisateurs sans BIOS</td><td>Fonctionne sans aucun BIOS.</td><td>Compatibilité plus faible, 2 joueurs, peu d'options.</td></tr><tr><td><strong>pcsx2-16</strong></td><td>Cas particuliers</td><td>Ancienne version (1.6), gardée pour les rares jeux qui y tournent mieux.</td><td>Pas de .chd, pas de configuration automatique des manettes.</td></tr></tbody></table>

**Dans le doute, gardez pcsx2.**

## BIOS

**Un seul de ces fichiers suffit** pour pcsx2, lr-pcsx2 et pcsx2-16 :

<table><thead><tr><th width="244.5">Fichier BIOS</th><th width="103.25">Région</th><th>MD5</th></tr></thead><tbody><tr><td>ps2-0230a-20080220.bin</td><td>USA</td><td>21038400dc633070a78ad53090c53017</td></tr><tr><td>ps2-0230e-20080220.bin</td><td>Europe</td><td>dc69f0643a3030aaa4797501b483d6c4</td></tr><tr><td>ps2-0230j-20080220.bin</td><td>Japon</td><td>80ac46fa7e77b8ab4366e86948e54f83</td></tr><tr><td>ps2-0250e-20100415.bin</td><td>Europe</td><td>93ea3bcee4252627919175ff1b16a1d9</td></tr><tr><td>SCPH30004R.bin</td><td>Europe</td><td>28922c703cc7d2cf856f177f2985b3a9</td></tr><tr><td>scph39001.bin</td><td>USA</td><td>d5ce2c7d119f563ce04bc04dbc3a323e</td></tr></tbody></table>

Autres noms acceptés par pcsx2 : `ps3_ps2_emu_bios.bin`, `SCPH-39004_BIOS_V7_EUR_160.BIN`, `SCPH-39001_BIOS_V7_USA_160.BIN`, `SCPH-70000_BIOS_V12_JAP_200.BIN`.

{% hint style="info" %}
* **lr-pcsx2** accepte n'importe quel BIOS PS2 placé dans `bios\pcsx2\bios`, quel que soit son nom.
* Quand plusieurs BIOS sont présents, pcsx2 et lr-pcsx2 utilisent d'abord `ps2-0230a-20080220.bin`, sinon le premier fichier trouvé.
* Un BIOS de n'importe quelle région lance les jeux de toutes les régions. Choisissez-le plutôt pour la **langue** (voir plus bas).
{% endhint %}

### Choisir le BIOS

Pour utiliser un BIOS précis, réglez **ÉMULATION > FORCER LE FIRMWARE** (pcsx2 et lr-pcsx2) dans les options du système ou du jeu. La liste propose USA 230, EUR 230, EUR 250, JAP 230 et PS3 PS2 FIRMWARE.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (422).png" alt=""><figcaption></figcaption></figure></div>

### Changer la langue de la console (BIOS)

Sur une vraie PS2, la langue se règle dans les paramètres de la console, et beaucoup de jeux s'en servent pour choisir leur propre langue. Avec pcsx2, c'est pareil :

1. Ouvrez **START** > **PARAMÈTRES DES JEUX** > **CONFIGURATION AVANCÉE PAR SYSTÈME** > **PLAYSTATION 2**, vérifiez que l'émulateur est **pcsx2**, puis activez **ÉMULATION > LANCER LE BIOS**.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (423).png" alt=""><figcaption></figcaption></figure></div>

2. Lancez n'importe quel jeu PS2 : le menu de la console s'ouvre à la place du jeu.
3. Avec la croix directionnelle, choisissez **System Configuration** (Configuration du système), puis validez avec **SUD** (✕). Les BIOS japonais valident avec **EST** (○).
4. Choisissez **Language** (ou **Language Settings**), puis **System Language**, et sélectionnez votre langue.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (424).png" alt=""><figcaption></figcaption></figure></div>

5. Quittez avec **HOTKEY + START**.
6. Retournez dans les options et désactivez **LANCER LE BIOS**.

La langue est enregistrée à côté du BIOS, dans un fichier `.nvm` du même nom (par exemple `bios\pcsx2\bios\ps2-0230e-20080220.nvm`). **lr-pcsx2 et pcsx2-16 utilisent le même fichier** : la langue réglée avec pcsx2 s'applique aussi à eux s'ils utilisent le même BIOS.

{% hint style="warning" %}
La langue ne change que dans les jeux qui la contiennent. Les jeux européens (PAL) sont souvent multilingues. La plupart des jeux américains (NTSC-U) ne contiennent que l'anglais, et les jeux japonais le japonais.
{% endhint %}

Autres émulateurs :

* **lr-pcsx2 :** **ÉMULATION > DÉBLOCAGE DES LANGUES** débloque d'autres langues dans certains jeux.
* **play :** play n'a pas de BIOS. Choisissez la langue dans **ÉMULATION > LANGUE** (anglais par défaut).

## Quel format de jeu ?

<table><thead><tr><th width="201">Format</th><th align="center">pcsx2</th><th align="center">lr-pcsx2</th><th align="center">play</th><th align="center">pcsx2-16</th></tr></thead><tbody><tr><td>.chd (conseillé)</td><td align="center">✔</td><td align="center">✔</td><td align="center">✔</td><td align="center">✘</td></tr><tr><td>.iso</td><td align="center">✔</td><td align="center">✔</td><td align="center">✔</td><td align="center">✔</td></tr><tr><td>.cso</td><td align="center">✔</td><td align="center">✔</td><td align="center">✔</td><td align="center">✔</td></tr><tr><td>.zip / .7z / .squashfs</td><td align="center">✔ (décompressé au lancement)</td><td align="center"></td><td align="center"></td><td align="center"></td></tr></tbody></table>

* **.chd** est le meilleur choix : le jeu est compressé (souvent 30 à 50 % plus petit) et lu directement, sans décompression.
* Les jeux en **.zip / .7z / .squashfs** sont décompressés par RetroBat avant chaque lancement avec pcsx2. Ça fonctionne, mais le chargement est plus lent.

### Jeux multi-disques

Certains jeux utilisent deux disques (Xenosaga Episode III, Metal Gear Solid 3: Subsistence…). Créez un fichier texte nommé `Jeu.m3u` dans `roms\ps2`, avec un disque par ligne :

```
Jeu (Disc 1).chd
Jeu (Disc 2).chd
```

* **pcsx2** démarre sur le premier disque. Quand le jeu demande le disque suivant, ouvrez le menu pause (**HOTKEY + SUD**), choisissez **Change Disc**, puis le disque suivant.
* **lr-pcsx2** utilise le contrôle des disques de RetroArch (**HOTKEY + L1** éjecter, **HOTKEY + R2** disque suivant, **HOTKEY + L1** insérer).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (425).png" alt="" width="327"><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../../../../.gitbook/assets/image (426).png" alt=""><figcaption></figcaption></figure></div>

## Contrôles

### Configuration automatique

RetroBat configure vos manettes automatiquement : vous n'avez rien à faire.

<table><thead><tr><th width="116.5">Émulateur</th><th width="153">Autoconfiguration RetroBat</th><th width="115.25">Joueurs</th><th>Remarques</th></tr></thead><tbody><tr><td>pcsx2</td><td>✔</td><td>Jusqu'à 8</td><td>Manettes XInput et SDL (DualShock 4, DualSense, Switch Pro, 8BitDo…). Le multitap (adaptateur multijoueur PS2) est activé automatiquement au-delà de 2 manettes.</td></tr><tr><td>lr-pcsx2</td><td>✔ (RetroArch)</td><td>2</td><td></td></tr><tr><td>play</td><td>✔</td><td>2</td><td></td></tr><tr><td>pcsx2-16</td><td>✘</td><td></td><td>Configuration manuelle dans l'émulateur (voir plus bas).</td></tr></tbody></table>

Les boutons sont associés par **position**, comme sur une manette DualShock 2 :

<table><thead><tr><th width="325.25">Manette RetroBat</th><th>Manette PS2</th></tr></thead><tbody><tr><td>SUD / EST / OUEST / NORD</td><td>✕ / ○ / □ / △</td></tr><tr><td>L1 / R1</td><td>L1 / R1</td></tr><tr><td>L2 / R2</td><td>L2 / R2</td></tr><tr><td>Stick gauche / droit (appui)</td><td>L3 / R3</td></tr><tr><td>SELECT / START</td><td>SELECT / START</td></tr></tbody></table>

<div align="left"><figure><img src="../../../../.gitbook/assets/image (427).png" alt="" width="225"><figcaption></figcaption></figure></div>

Pour utiliser votre propre configuration faite dans l'émulateur, réglez **AUTOCONFIGURER LES MANETTES** sur **OFF** (pcsx2, lr-pcsx2, play). Avec play, le profil `emulators\play\Play Data Files\inputprofiles\<nom du jeu>.xml` est alors utilisé s'il existe, sinon le profil par défaut.

### Raccourcis

**pcsx2** utilise les raccourcis standards de RetroBat :

| Action                                    | Manette             | Clavier        |
| ----------------------------------------- | ------------------- | -------------- |
| Quitter le jeu                            | HOTKEY + START      | Échap          |
| Menu pause (changer de disque, réglages…) | HOTKEY + SUD        | F1             |
| Sauvegarde d'état                         | HOTKEY + OUEST      | F2             |
| Chargement d'état                         | HOTKEY + NORD       | F4             |
| Emplacement précédent / suivant           | HOTKEY + Bas / Haut | F6 / F7        |
| Ralenti                                   | HOTKEY + Gauche     | Retour arrière |
| Avance rapide (maintenir)                 | HOTKEY + Droite     | L              |
| Capture d'écran                           | HOTKEY + R3         | F8             |
| Pause                                     | HOTKEY + L3         | P              |
| Avance rapide (bascule)                   |                     | Espace         |
| Plein écran                               |                     | F              |

* **lr-pcsx2** utilise les raccourcis de RetroArch (même tableau sur la page Raccourcis), sans retour arrière.
* **play** et **pcsx2-16** : seulement **HOTKEY + START** (quitter).

### Options des manettes pcsx2

Dans les options, sous-menu **CONTRÔLES** :

<table><thead><tr><th width="285.25">Option</th><th>Utilité</th></tr></thead><tbody><tr><td>ADAPTATEUR MULTIJOUEURS</td><td>Force le multitap sur le port 1, le port 2 ou les deux. Sinon, c'est automatique.</td></tr><tr><td>UTILISER LES GÂCHETTES POUR LES JEUX DE COURSE</td><td>Jeux de course (Gran Turismo…) : les gâchettes analogiques sont associées à □/✕ ou à un stick, pour une accélération progressive. Réglez ensuite l'accélération et le frein sur ces boutons dans les options du jeu.</td></tr><tr><td>BOUTON MODIFICATEUR DE PRESSION</td><td>Les boutons de la PS2 sont sensibles à la pression, et certains jeux s'en servent (Metal Gear Solid 2 et 3 : viser sans tirer). Maintenir le bouton de stick choisi rend les appuis suivants « légers ». <strong>VALEUR DU MODIFICATEUR DE PRESSION</strong> règle la force.</td></tr><tr><td>UTILISER LE STICK GAUCHE COMME D-PAD</td><td>Déplacement au stick gauche dans les jeux qui n'utilisent que la croix.</td></tr><tr><td>ZONE MORTE JOYSTICK / SENSIBILITÉ ANALOGIQUE / ZONE MORTE DES GÂCHETTES</td><td>Réglages fins des sticks et des gâchettes.</td></tr><tr><td>PUISSANCE DES VIBRATIONS</td><td>Force des vibrations.</td></tr><tr><td>UTILISER UNE GUITARE</td><td>Guitar Hero / Rock Band : utilise une guitare compatible (CRKD Guitar XP).</td></tr></tbody></table>

#### Schémas alternatifs:

Afin de pouvoir utiliser les gâchettes analogiques pour les jeux de course, il est possible d'utiliser un des schémas de contrôles alternatifs en activant cette option:

<div align="left"><figure><img src="../../../../.gitbook/assets/image (428).png" alt=""><figcaption></figcaption></figure></div>

<table><thead><tr><th width="276.5">Option</th><th>Schéma de contrôles</th></tr></thead><tbody><tr><td>SIMULER CARRE ET CROIX</td><td><img src="../../../../.gitbook/assets/image (429).png" alt="" data-size="original"></td></tr><tr><td>SIMULER LE STICK DROIT</td><td><img src="../../../../.gitbook/assets/image (430).png" alt="" data-size="original"></td></tr><tr><td>SIMULER LE STICK GAUCHE</td><td><img src="../../../../.gitbook/assets/image (431).png" alt="" data-size="original"></td></tr></tbody></table>

{% hint style="info" %}
Afin de pouvoir utiliser les gâchettes, il est nécessaire de changer le schéma de contrôle dans le jeu, en passant l'accélération et le freinage sur les bons boutons/sticks.
{% endhint %}

### Options des manettes lr-pcsx2

<table><thead><tr><th width="301.5">Option</th><th>Utilité</th></tr></thead><tbody><tr><td>DÉMARRER EN MODE ANALOGIQUE</td><td>Démarre la manette en mode analogique (le bouton ANALOG de la DualShock 2). Désactivez-le pour les jeux qui ne fonctionnent qu'en mode numérique.</td></tr><tr><td>SENSIBILITÉ ANALOGIQUE (CORE) / ZONE MORTE ANALOGIQUE (CORE)</td><td>Sensibilité et zone morte des sticks.</td></tr><tr><td>ACTIVER LES VIBRATIONS</td><td>Vibrations.</td></tr></tbody></table>

### Options des manettes play

<table><thead><tr><th width="299">Option</th><th>Utilité</th></tr></thead><tbody><tr><td>DÉSACTIVER LES VIBRATIONS</td><td>Désactive les vibrations.</td></tr></tbody></table>

### pcsx2-16 : configuration manuelle

pcsx2-16 n'est pas configuré par RetroBat :

1. Ouvrez `emulators\pcsx2-16` et lancez `pcsx2.exe`.
2. Menu **Config** > **Controllers (PAD)** > **Plugin Settings**.
3. Dans l'onglet **Pad 1**, cliquez sur chaque bouton puis appuyez sur le bouton correspondant de votre manette.
4. Fermez la fenêtre : la configuration est gardée pour vos prochaines parties.

### Pistolets (pcsx2)

pcsx2 émule le **GunCon 2** (Time Crisis 2 et 3, Vampire Night, Ninja Assault…).

1. Activez **CONTRÔLES > ACTIVER LES PISTOLETS** dans les options du système ou du jeu.
2. Vérifiez votre modèle de pistolet sur les pages Pistolets et Gun controls.
3. Réglages facultatifs du sous-menu **PISTOLETS** :
   * **PORT USB DU GUNCON POUR LE JOUEUR 1** : port USB du pistolet, USB 1 ou USB 2. Certains jeux attendent le pistolet sur le deuxième port.
   * **MAPPING DES BOUTONS GUNCON** : où vont les boutons A, B et START du GunCon (souris et clavier, ou manette).
   * **INVERSER GÂCHETTE ET RECHARGE**, **BOUTON DE CALIBRATION**.
   * **CIBLE** : aucun viseur, curseur de la souris, ou image personnalisée. Pour un viseur personnalisé, placez un fichier `crosshair.png` dans `emulators\pcsx2\cross`, ou choisissez un fichier avec **FICHIER DE VISEUR PERSONNALISÉ**. **TAILLE DE LA CIBLE CUSTOM** règle sa taille.

### Volants (pcsx2)

1. Activez **VOLANTS DE COURSE > ACTIVER LES VOLANTS**.
2. Vérifiez que votre volant est pris en charge sur la page Volants.
3. Réglages utiles : **TYPE DE VOLANT JOUEUR 1** (Driving Force, Driving Force Pro, GT Force : Gran Turismo 4 reconnaît le Driving Force Pro), **ACTIVER LE RETOUR DE FORCE**, **ZONE MORTE DE LA DIRECTION**…
4. Sans volant, **SIMULER LE VOLANT AVEC LA MANETTE** fait croire au jeu qu'un volant est branché.

## Dossiers

Tous les chemins partent de votre dossier RetroBat.

### Sauvegardes

Sur PS2, les jeux sauvegardent sur une **carte mémoire**. Les émulateurs la créent pour vous : vous n'avez rien à formater.

<table><thead><tr><th width="111.5">Émulateur</th><th width="258.75">Cartes mémoire</th><th>Sauvegardes d'état</th><th>Captures d'écran</th></tr></thead><tbody><tr><td>pcsx2</td><td><code>saves\ps2\pcsx2\memcards</code></td><td><code>saves\ps2\pcsx2</code></td><td><code>screenshots\pcsx2</code></td></tr><tr><td>lr-pcsx2</td><td><code>bios\pcsx2\memcards</code> (cartes partagées, par défaut) ou <code>saves\ps2</code> (une carte par jeu)</td><td><code>saves\ps2\libretro.pcsx2</code></td><td><code>screenshots</code></td></tr><tr><td>play</td><td><code>emulators\play\Play Data Files\vfs\mc0</code></td><td><code>emulators\play\Play Data Files\states</code></td><td></td></tr><tr><td>pcsx2-16</td><td><code>saves\ps2\pcsx2-16\memcards</code></td><td><code>saves\ps2\pcsx2-16\sstates</code></td><td><code>screenshots\pcsx2</code></td></tr></tbody></table>

{% hint style="warning" %}
Chaque émulateur a ses propres cartes mémoire. Si vous changez d'émulateur, votre progression ne suit pas. Gardez le même émulateur pour un jeu, ou copiez la carte mémoire vous-même (pcsx2, lr-pcsx2 et pcsx2-16 utilisent le même format `.ps2`).
{% endhint %}

* Pour récupérer la carte mémoire d'une autre installation de PCSX2, copiez son fichier `Mcd001.ps2` dans `saves\ps2\pcsx2\memcards` (en remplaçant le fichier existant, après en avoir fait une copie).
* Les sauvegardes d'état de pcsx2 et lr-pcsx2 apparaissent aussi dans le menu des sauvegardes d'état de RetroBat : voir la page Sauvegardes d'état.

### Autres dossiers utiles

<table><thead><tr><th width="374">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>BIOS et langue de la console (<code>.nvm</code>)</td><td><code>bios\pcsx2\bios</code></td></tr><tr><td>Packs de textures (pcsx2)</td><td><code>bios\pcsx2\textures</code></td></tr><tr><td>Codes de triche (pcsx2)</td><td><code>cheats\pcsx2\cheats</code></td></tr><tr><td>Viseur personnalisé (pcsx2)</td><td><code>emulators\pcsx2\cross</code></td></tr><tr><td>Configuration et profils de manettes de play</td><td><code>emulators\play\Play Data Files</code></td></tr></tbody></table>

## Guides

### Jouer en HD (résolution interne)

La PS2 affiche ses jeux en environ 480 lignes, ce qui paraît flou sur un écran moderne. La **RÉSOLUTION INTERNE** calcule la 3D dans une résolution plus élevée :

* pcsx2 et lr-pcsx2 : 2x ≈ 720p, 3x ≈ 1080p, 4x ≈ 1440p, 6x ≈ 4K.
* play : x2, x4…

Commencez par **3x** (1080p). Si le jeu ralentit, revenez à 2x. Certains jeux affichent des lignes ou une image décalée en HD : essayez le sous-menu **HACKS MANUELS**, ou revenez à la résolution native.

### Jouer en écran large (16:9)

Les jeux PS2 ont été conçus pour des téléviseurs 4:3. Beaucoup peuvent être passés en 16:9 grâce à des patchs :

* **pcsx2 :** **VIDÉO > PATCH ÉCRAN LARGE** est activé par défaut. Quand un patch existe pour le jeu, pcsx2 passe en 16:9 de lui-même. **VIDÉO > PATCH DE DÉSENTRELACEMENT** supprime le scintillement des jeux entrelacés qui ont un patch.
* **lr-pcsx2 :** **VIDÉO > PATCH ÉCRAN LARGE** (16:9, 16:10, 21:9, 32:9).
* **play :** **VIDÉO > HACK ÉCRAN LARGE** (meilleur résultat avec les jeux entièrement en 3D).
* **pcsx2-16 :** **RAPPORT D'ASPECT** réglé sur 16/9 (étire l'image).

{% hint style="info" %}
Avec pcsx2, les **décorations** (bezels) sont masquées en mode AUTO, car un jeu peut passer en 16:9 de lui-même. Pour les afficher, réglez le **RAPPORT D'ASPECT** sur 4:3, ou désactivez le **PATCH ÉCRAN LARGE**.
{% endhint %}

### Textures personnalisées (pcsx2)

Pour utiliser un pack de textures:

1. **Trouvez le numéro de série du jeu.** Il est écrit sur le disque et sur la boîte (par exemple `SLES-52725` ou `SLUS-20946`). Il est aussi affiché dans la liste des jeux de pcsx2.
2. **Créez le dossier** `bios\pcsx2\textures\<NUMÉRO DE SÉRIE>\replacements` (par exemple `bios\pcsx2\textures\SCES-51719\replacements`).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (432).png" alt=""><figcaption></figcaption></figure></div>

3. **Copiez le contenu du pack** dans `replacements`. Si le pack contient déjà un dossier au nom du numéro de série, copiez directement ce dossier dans `bios\pcsx2\textures`.
4. **Activez l'option** **RENDU VISUEL > TEXTURES PERSONNALISÉES** dans les options du jeu :
   * **OUI (PRÉCACHE)** : charge tout le pack au démarrage. Plus fluide en jeu, mais utilise beaucoup de mémoire.
   * **OUI (SANS PRÉCACHE)** : charge les textures au besoin. Pour les très gros packs ou les PC avec peu de mémoire.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (433).png" alt=""><figcaption></figcaption></figure></div>

5. Lancez le jeu. Pour un bon résultat, augmentez aussi la **RÉSOLUTION INTERNE**.

### Options des cartes mémoire

**pcsx2 :** **ÉMULATION > TYPE DE CARTE MÉMOIRE SLOT 1** :

* **CARTE MÉMOIRE STANDARD** : une seule carte (`Mcd001.ps2`) pour tous les jeux (par défaut). Comme sur une vraie console, elle peut être pleine (8 Mo).
* **CARTE MÉMOIRE PAR JEU** : une carte par jeu, au nom du jeu.
* **DOSSIER** : une carte « dossier » qui n'est jamais pleine.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (434).png" alt=""><figcaption></figcaption></figure></div>

**lr-pcsx2 :** **ÉMULATION > CARTES MÉMOIRES PARTAGÉES** est activé par défaut (une carte pour tous les jeux). Désactivez-le pour avoir une carte par jeu dans `saves\ps2`.

{% hint style="warning" %}
Changer de type de carte mémoire ne déplace pas vos sauvegardes : les jeux ne voient plus l'ancienne carte. Choisissez avant de commencer à jouer.
{% endhint %}

### Codes de triche

* **pcsx2 :** placez les fichiers de triche (`.pnach`) dans `cheats\pcsx2\cheats`, puis activez **ÉMULATION > ACTIVER LA TRICHE**.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (435).png" alt=""><figcaption></figcaption></figure></div>

* **lr-pcsx2 :** **ÉMULATION > ACTIVER LA TRICHE**.

La triche est désactivée en mode hardcore RetroAchievements.

### Écran du BIOS et démarrage

* **SAUTER LE BIOS** (pcsx2, lr-pcsx2, pcsx2-16) est activé par défaut : le jeu démarre directement, sans l'animation Sony. Désactivez-le pour voir l'animation de démarrage.
* **LANCER LE BIOS** (pcsx2) ouvre le menu de la console à la place du jeu (pour changer la langue, gérer les cartes mémoire…).

### Performances et problèmes d'affichage

* **PILOTES > VIDÉO** (pcsx2), **PILOTES > PILOTE VIDÉO DU CORE** (lr-pcsx2), **PILOTES > VIDÉO** (play) : moteur de rendu utilisé. Vulkan ou Direct3D 11/12 sont en général les plus rapides. Essayez-en un autre si un jeu affiche des défauts ou un écran noir.
* **pcsx2-16 :** **ÉMULATION > PLUGINS GRAPHIQUES** : choisissez AVX2 si votre processeur le prend en charge, sinon SSE4 ou SSE2.
* **lr-pcsx2 :** le moteur de rendu **paraLLEl-GS** reproduit très fidèlement l'image de la PS2. Son sous-menu **PARALLEL-GS** propose un suréchantillonnage pour une image plus nette.
* **CORRECTIFS** (pcsx2) : correctifs pour des jeux précis. pcsx2 applique déjà automatiquement les bons correctifs aux jeux connus : ne les changez que si un guide vous le demande.

## Problèmes connus

<table><thead><tr><th width="326.5">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>« No BIOS found in bios/pcsx2/bios folder »</td><td>Le BIOS manque ou, avec pcsx2, son nom n'est pas dans la liste. Voir BIOS.</td></tr><tr><td>« ATTENTION : LE SYSTÈME A UN BIOS MANQUANT… » au lancement</td><td>Aucun BIOS accepté n'a été trouvé dans <code>bios\pcsx2\bios</code>. Vérifiez le nom et le dossier du fichier. Avec play, choisissez OUI. Voir Vérifier le BIOS.</td></tr><tr><td>Le jeu reste en anglais</td><td>Le jeu ne contient que l'anglais (version US), ou la langue de la console n'est pas réglée. Voir Changer la langue de la console.</td></tr><tr><td>Le jeu ne démarre pas avec pcsx2-16</td><td>pcsx2-16 ne lit pas les .chd. Utilisez pcsx2, ou un .iso.</td></tr><tr><td>La manette ne répond pas avec pcsx2-16</td><td>pcsx2-16 n'est pas configuré par RetroBat. Voir pcsx2-16 : configuration manuelle.</td></tr><tr><td>Les jeux .zip / .7z sont longs à démarrer</td><td>Ils sont décompressés avant chaque lancement. Convertissez-les en .chd.</td></tr><tr><td>Le jeu demande le disque 2</td><td>Utilisez un fichier .m3u et changez de disque depuis le menu pause. Voir Jeux multi-disques.</td></tr><tr><td>Lignes, flou ou image décalée en HD</td><td>Revenez à la résolution native, ou essayez les options <strong>HACKS MANUELS</strong> du jeu.</td></tr><tr><td>Le jeu est lent</td><td>Baissez la résolution interne, essayez un autre moteur de rendu, ou désactivez les textures personnalisées.</td></tr><tr><td>Pas de décoration avec pcsx2</td><td>Normal en mode AUTO : voir Jouer en écran large.</td></tr></tbody></table>
