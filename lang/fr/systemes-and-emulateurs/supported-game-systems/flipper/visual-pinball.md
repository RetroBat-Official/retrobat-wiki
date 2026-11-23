# Visual Pinball

<div align="left"><figure><img src="../../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure></div>

## Présentation

**Visual Pinball** est un simulateur et un éditeur de tables de flipper, créé par **Randy Davis** en 2000 et aujourd'hui développé par la communauté sous le nom **Visual Pinball X** (VPX). Gratuit, il fait jouer des milliers de tables : des reproductions de vrais flippers (Williams, Bally, Stern, Gottlieb, Data East…) et des tables originales.

Pour les flippers électroniques, **VPinMAME** émule l'électronique de la vraie machine à partir de sa ROM : règles, sons et afficheur à points (DMD) d'origine. D'autres composants complètent la table : **backglass** (fronton animé, fichiers `.directb2s`), **FlexDMD / UltraDMD** (DMD des tables originales), **PinUP Player** (vidéos des « PuP packs ») et retours physiques **DOF** pour les bornes équipées.

RetroBat fournit Visual Pinball X 10.8 avec tous ces composants et les configure : écrans (1 à 3), DMD, backglass et manette.

{% embed url="https://en.wikipedia.org/wiki/Visual_Pinball" %}

{% embed url="https://www.vpforums.org/" %}

## En bref

<table><thead><tr><th width="280.25"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\vpinball</code></td></tr><tr><td><strong>Extensions</strong></td><td>.vpx .7z .zip .rar</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>vpinball (Visual Pinball X 10.8)</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (les ROM des flippers vont dans <code>roms\vpinball\roms</code>)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique (joueur 1)</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="220.75">Émulateur</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>vpinball</strong> (seul émulateur)</td><td>Visual Pinball X 10.8 avec VPinMAME, backglass, DMD et PuP packs. Écrans calculés automatiquement (1, 2 ou 3 écrans). Manette et clavier configurés.</td><td>Demandes d'autorisation de Windows au premier lancement (voir <a href="visual-pinball.md#problemes-connus"><strong>Problèmes connus</strong></a>). Une seule manette (joueur 1).</td></tr></tbody></table>

Les tables **Future Pinball** (`.fpt`) ont leur propre système : [**Future Pinball**](future-pinball.md) (`roms\fpinball`).

## BIOS

Aucun BIOS n'est nécessaire. Les tables de flippers électroniques ont besoin de la **ROM** de la vraie machine (voir ci-dessous).

## Quel format de jeu ?

<table><thead><tr><th width="155.25">Format</th><th>Remarques</th></tr></thead><tbody><tr><td><strong>.vpx</strong></td><td>Table Visual Pinball X.</td></tr><tr><td><strong>.zip</strong>, <strong>.7z</strong>, <strong>.rar</strong></td><td>Archive contenant la table (et ses fichiers). RetroBat l'extrait au lancement et lance le premier <code>.vpx</code> trouvé.</td></tr></tbody></table>

Les tables `.vpt` de Visual Pinball 9 ne sont pas listées.

Selon la table, d'autres fichiers sont nécessaires. Ils sont indiqués là où la table a été téléchargée :

| Fichier                                    | Rôle                                           | Où le mettre                                                                                            |
| ------------------------------------------ | ---------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| `.directb2s`                               | Backglass (fronton animé)                      | À côté de la table, **avec le même nom** que le `.vpx`.                                                 |
| ROM `.zip`                                 | Électronique de la vraie machine (VPinMAME)    | `roms\vpinball\roms`, sans renommer le `.zip`.                                                          |
| Dossier `.UltraDMD` ou de la table         | DMD des tables originales (FlexDMD / UltraDMD) | À côté de la table, sans renommer le dossier.                                                           |
| Musiques (`.mp3`, `.ogg`)                  | Musique de certaines tables originales         | `emulators\vpinball\Music` ou dossier `music` à côté de la table, en gardant les sous-dossiers fournis. |
| PuP pack                                   | Vidéos et sons supplémentaires                 | `emulators\vpinball\PinUPSystem\PUPVideos\<nom du pack>`                                                |
| Coloration du DMD (`.pal`, `.vni`, `.cRZ`) | DMD en couleurs                                | `emulators\vpinball\VPinMAME\altcolor\<nom de la ROM>`                                                  |
| Sons alternatifs                           | Sons remplacés de la ROM                       | `emulators\vpinball\VPinMAME\altsound\<nom de la ROM>`                                                  |

```
roms\
└─ vpinball\
   ├─ Ma table.vpx
   ├─ Ma table.directb2s
   ├─ Ma table.UltraDMD\      (si fourni)
   ├─ music\                  (si fourni)
   └─ roms\
      └─ afm_113b.zip
```

Les ROM sont aussi cherchées dans un dossier `roms` placé à côté de la table, puis dans `emulators\vpinball\VPinMAME\roms`. Une table en archive (`.zip`, `.7z`, `.rar`) peut contenir son dossier `roms`, sinon `roms\vpinball\roms` est utilisé.

**Nom de la ROM** : il est écrit dans le script de la table (`cGameName = "…"`). RetroBat le lit au lancement et l'indique dans `emulationstation\emulatorLauncher.log` (ligne `VPinMAME rom name read from table`).

<div align="left"><figure><img src="../../../.gitbook/assets/image (737).png" alt=""><figcaption><p>Backglass avec le même nom que la table</p></figcaption></figure></div>

<div align="left"><figure><img src="../../../.gitbook/assets/image (738).png" alt=""><figcaption><p>ROM dans roms\vpinball\roms</p></figcaption></figure></div>

<div align="left"><figure><img src="../../../.gitbook/assets/image (739).png" alt=""><figcaption></figcaption></figure></div>

Au lancement, RetroBat affiche le backglass de la table (s'il existe) pendant le chargement.

## Contrôles

RetroBat configure la manette du joueur 1 et le clavier à chaque lancement :

<table><thead><tr><th width="242.75">Manette RetroBat</th><th>Visual Pinball</th></tr></thead><tbody><tr><td>L1 / R1</td><td>Flipper gauche / droit</td></tr><tr><td>SUD</td><td>Lanceur (maintenir puis relâcher)</td></tr><tr><td>R2</td><td>Lanceur analogique</td></tr><tr><td>Croix haut</td><td>Secouer la table vers l'avant</td></tr><tr><td>Croix gauche / droite</td><td>Secouer la table à gauche / à droite</td></tr><tr><td>Croix bas</td><td>Tilt mécanique</td></tr><tr><td>Stick gauche</td><td>Secouer la table (analogique), avec <strong>CONTRÔLES > ACTIVER LE NUDGE ANALOGIQUE</strong></td></tr><tr><td>EST</td><td>Bouton d'action (lockbar)</td></tr><tr><td>OUEST / NORD</td><td>MagnaSave gauche / droit</td></tr><tr><td>SELECT</td><td>Insérer un crédit</td></tr><tr><td>START</td><td>Démarrer la partie</td></tr><tr><td>L3</td><td>Pause</td></tr></tbody></table>

L2 et le stick droit ne sont pas utilisés. Le bouton d'action sert à lancer la bille ou à tirer sur beaucoup de tables récentes, les MagnaSave retiennent la bille sur certaines tables (Black Knight, Jungle Lord…).

<table><thead><tr><th width="277.75">Clavier</th><th>Visual Pinball</th></tr></thead><tbody><tr><td><code>Maj gauche</code> / <code>Maj droite</code></td><td>Flipper gauche / droit</td></tr><tr><td><code>Windows gauche</code> / <code>Alt Gr</code></td><td>2e niveau du flipper gauche / droit (tables qui l'utilisent)</td></tr><tr><td><code>Entrée</code></td><td>Lanceur</td></tr><tr><td><code>Espace</code></td><td>Secouer vers l'avant</td></tr><tr><td><code>W</code> / <code>!</code></td><td>Secouer à gauche / à droite</td></tr><tr><td><code>T</code></td><td>Tilt mécanique</td></tr><tr><td><code>Ctrl gauche</code> / <code>Ctrl droit</code></td><td>MagnaSave gauche / droit</td></tr><tr><td><code>Alt gauche</code></td><td>Bouton d'action (lockbar)</td></tr><tr><td><code>5</code> / <code>4</code></td><td>Insérer un crédit (monnayeur 1 / 2)</td></tr><tr><td><code>1</code></td><td>Démarrer la partie</td></tr><tr><td><code>P</code></td><td>Pause</td></tr><tr><td><code>)</code> / <code>=</code></td><td>Volume - / +</td></tr><tr><td><code>X</code></td><td>Menu de la table (appui long : quitter)</td></tr><tr><td><code>F10</code></td><td>Réglages de la table en jeu (vue, éclairage…)</td></tr><tr><td><code>F11</code></td><td>Images par seconde</td></tr></tbody></table>

Touches données pour un clavier AZERTY : Visual Pinball lit la position des touches (sur un clavier QWERTY, `W` est `Z`, `!` est `/` et `)` est `-`). `Échap` est désactivée.

Pour garder vos propres réglages de Visual Pinball (manette et clavier), désactivez **AUTOCONFIGURER LES MANETTES**. **PILOTES > MANETTES** choisit DIRECTINPUT ou XINPUT (par défaut selon la manette), ou **UTILISER** [**PAD2KEY**](../../../controleurs/pad2key.md) (la manette simule le clavier, avec les mêmes boutons).

### Raccourcis

<table><thead><tr><th width="185.75">Action</th><th>Manette</th><th>Clavier</th></tr></thead><tbody><tr><td>Quitter</td><td>HOTKEY + START</td><td><code>X</code> (appui long)</td></tr><tr><td>Capture d'écran</td><td>HOTKEY + R3</td><td><code>Impr. écran</code></td></tr></tbody></table>

La capture devient l'image du jeu dans RetroBat s'il n'en a pas, sinon elle est enregistrée dans `screenshots`.

Avec **ÉMULATION > UTILISER EXIT TABLE POUR QUITTER**, HOTKEY + START envoie `X` à Visual Pinball au lieu de fermer sa fenêtre : son menu s'ouvre (choisir **Quit**). Avec **ÉMULATION > DÉSACTIVER LE MENU**, `X` quitte la table directement.

## Dossiers

| Contenu                                      | Dossier                                                                                |
| -------------------------------------------- | -------------------------------------------------------------------------------------- |
| Tables, backglass, `ScreenRes.txt`           | `roms\vpinball`                                                                        |
| ROM                                          | `roms\vpinball\roms`                                                                   |
| Scores et réglages des flippers (NVRAM)      | `emulators\vpinball\VPinMAME\nvram`                                                    |
| Coloration du DMD, sons alternatifs          | `emulators\vpinball\VPinMAME\altcolor`, `emulators\vpinball\VPinMAME\altsound`         |
| Musiques                                     | `emulators\vpinball\Music`                                                             |
| PuP packs                                    | `emulators\vpinball\PinUPSystem\PUPVideos`                                             |
| Réglages de Visual Pinball                   | `emulators\vpinball\VPinballX.ini`                                                     |
| Réglages du DMD externe et des DMD matériels | `emulators\vpinball\VPinMAME\DmdDevice.ini`                                            |
| Réglages du backglass                        | `emulators\vpinball\BackglassServer\B2STableSettings.xml` (copié dans `roms\vpinball`) |
| Captures d'écran                             | `screenshots`                                                                          |

RetroBat réécrit à chaque lancement une partie de `VPinballX.ini`, `ScreenRes.txt` et `DmdDevice.ini` d'après ses options.

## Guides

### Configurer les écrans (1, 2 ou 3 écrans)

Sur un PC avec un seul écran, rien n'est à régler. Pour une borne ou plusieurs écrans, réglez **ÉCRANS > CONFIGURATION DES ÉCRANS** : RetroBat place alors le plateau, le backglass et le DMD tout seul.

| Option                                          | Effet                                                                                                                                                                                                       |
| ----------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **ÉCRANS > CONFIGURATION DES ÉCRANS**           | **DÉTECTER LES ÉCRANS CONNECTÉS** (jusqu'à 3), **1 ÉCRAN**, **2 ÉCRANS (PLATEAU + BACKGLASS)** ou **3 ÉCRANS (PLATEAU + BACKGLASS + DMD)**.                                                                 |
| **VIDÉO > INDEX DE L'ÉCRAN**                    | Écran du plateau. Sans réglage, l'écran principal.                                                                                                                                                          |
| **ÉCRANS > ÉCRAN DU BACKGLASS**                 | Sans réglage, le plus grand des autres écrans.                                                                                                                                                              |
| **ÉCRANS > EMPLACEMENT DU DMD**                 | Sans réglage : sur le plateau avec 1 écran, en bas de l'écran du backglass avec 2 écrans, sur son propre écran avec 3 écrans. **DMD MATÉRIEL UNIQUEMENT** : seulement sur un DMD branché (ZeDMD, PIN2DMD…). |
| **ÉCRANS > ÉCRAN DU DMD**                       | Avec 3 écrans. Sans réglage, le plus petit écran restant.                                                                                                                                                   |
| **VIDÉO > VUE DU FLIPPER**                      | Sans réglage : **BUREAU** avec un écran horizontal, **PLEIN ÉCRAN SUR UN SEUL ÉCRAN** avec un écran vertical, **BORNE** avec plusieurs écrans.                                                              |
| **VIDÉO > ACTIVER BACKGLASS**                   | Sans réglage, le backglass s'affiche s'il a un écran (pas avec 1 écran).                                                                                                                                    |
| **VIDÉO > ROTATION DE L'ÉCRAN**                 | Fait pivoter l'écran du plateau pendant la partie (écran couché dans une borne), puis le remet comme avant.                                                                                                 |
| **ÉCRANS > IGNORER LE FICHIER .RES DU FLIPPER** | Ignore le placement du backglass propre à la table (fichier `.res` à côté de la table) pendant la partie.                                                                                                   |

Les écrans sont numérotés comme pour **INDEX DE L'ÉCRAN** (0 = premier écran).

<div align="left"><figure><img src="../../../.gitbook/assets/image (740).png" alt=""><figcaption></figcaption></figure></div>

Sans **CONFIGURATION DES ÉCRANS**, RetroBat garde l'ancien fonctionnement : les valeurs du menu **SCREENRES** (taille et position du backglass et du DMD), sinon le plateau sur l'écran principal et le backglass sur l'écran 2. L'outil `emulators\vpinball\BackglassServer\B2S_ScreenResIdentifier.exe` aide à trouver ces valeurs. Pour garder un `ScreenRes.txt` fait à la main, activez **SCREENRES > NE PAS ÉCRASER LE FICHIER SCREENRES**.

### DMD (afficheur à points)

<table><thead><tr><th width="379">Option</th><th>Effet</th></tr></thead><tbody><tr><td><strong>VPINMAME > DMD</strong></td><td><strong>INTERNE</strong> (par défaut) : fenêtre DMD de VPinMAME. <strong>EXTERNE</strong> : DMD de dmdext, qui gère aussi les DMD matériels. <strong>AUCUN</strong> : pas de DMD VPinMAME.</td></tr><tr><td><strong>VPINMAME > DMD VIRTUEL</strong></td><td>Fenêtre du DMD externe (activée par défaut).</td></tr><tr><td><strong>VPINMAME > ZEDMD</strong>, <strong>ZEDMDHD</strong>, <strong>PIN2DMD</strong></td><td>DMD matériels branchés en USB (avec <strong>DMD</strong> sur <strong>EXTERNE</strong>).</td></tr><tr><td><strong>VPINMAME > COLORISER LE DMD</strong></td><td>DMD en couleurs (VPinMAME).</td></tr><tr><td><strong>VPINMAME > ÉCHELLE DU DMD (ZOOM)</strong></td><td>Taille des points du DMD de VPinMAME.</td></tr></tbody></table>

### Autres options utiles

| Option                                                                            | Effet                                                                                                     |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| **SYNCHRONISATION VERTICALE**                                                     | **FRAME PACING** par défaut.                                                                              |
| **VIDÉO > RÉSOLUTION DE L'ÉCRAN**                                                 | Résolution de l'écran du plateau pendant la partie.                                                       |
| **VIDÉO > PLEIN ÉCRAN EXCLUSIF**                                                  | Visual Pinball change lui-même de résolution, au lieu de RetroBat.                                        |
| **RENDU VISUEL > ANTICRÉNELAGE**, **SURÉCHANTILLONNAGE**                          | Image plus lisse (le suréchantillonnage demande une carte graphique puissante).                           |
| **RENDU VISUEL > OCCLUSION AMBIANTE**, **IMAGE PLUS NETTE**, **NIVEAU DE DÉTAIL** | Qualité de l'image : à baisser sur un PC peu puissant.                                                    |
| **RENDU VISUEL > ÉCLAIRAGE D'AMBIANCE**                                           | Éclairage de la salle, du jour à la nuit.                                                                 |
| **AUDIO > NOMBRE DE CANAUX AUDIO**                                                | Sons en 2 canaux ou en surround (bornes avec haut-parleurs supplémentaires).                              |
| **AUDIO > DÉSACTIVER LA MUSIQUE**                                                 | Coupe la musique des tables originales.                                                                   |
| **RETOURS PHYSIQUES (DOF)**                                                       | Pour chaque élément (contacteurs, knocker, flippers…) : retour physique (DOF), effet sonore, ou les deux. |
| **BACKGLASS > MASQUER LA GRILLE**                                                 | Masque la grille du haut-parleur sous le backglass.                                                       |
| **CONTRÔLES > ZONE MORTE JOYSTICK**, **MODE DE VIBRATION**                        | Zone morte du stick, vibrations de la manette.                                                            |
| **CONTRÔLES > DÉSACTIVER LE STICK ANALOGIQUE**                                    | Stick et R2 ne sont plus utilisés.                                                                        |

## Problèmes connus

<table><thead><tr><th width="336.5">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Windows demande l'autorisation d'un administrateur au lancement</td><td>Normal au premier lancement, et après avoir déplacé RetroBat : RetroBat enregistre les composants (VPinMAME, backglass, DMD, PinUP Player). Acceptez, sinon les ROM, le backglass ou le DMD ne fonctionnent pas.</td></tr><tr><td>La table ne démarre pas ou VPinMAME ne trouve pas la ROM</td><td>Mettez la ROM dans <code>roms\vpinball\roms</code>, sans la renommer (voir <a href="visual-pinball.md#quel-format-de-jeu"><strong>Nom de la ROM</strong></a>). Certaines tables demandent une version précise de la ROM.</td></tr><tr><td>Pas de backglass</td><td>Le <code>.directb2s</code> doit avoir le même nom que la table. Avec 1 écran, le backglass est désactivé : forcez-le avec <strong>VIDÉO > ACTIVER BACKGLASS</strong>.</td></tr><tr><td>Backglass ou DMD mal placé</td><td>Réglez <strong>ÉCRANS > CONFIGURATION DES ÉCRANS</strong>. Si un fichier <code>.res</code> est à côté de la table, essayez <strong>IGNORER LE FICHIER .RES DU FLIPPER</strong>.</td></tr><tr><td>Le DMD de VPinMAME s'affiche au mauvais endroit, avec un écran à gauche ou au-dessus de l'écran principal</td><td>Dans Windows, placez l'écran du DMD à droite ou en dessous de l'écran principal, ou choisissez <strong>VPINMAME > DMD</strong> sur <strong>EXTERNE</strong>.</td></tr><tr><td>Pas de musique</td><td>Musiques dans <code>emulators\vpinball\Music</code> (ou <code>music</code> à côté de la table), avec les sous-dossiers fournis.</td></tr><tr><td>Problèmes d'affichage</td><td>Carte Intel : <strong>VIDÉO > PROCESSEUR VERTEX LOGICIEL</strong>. Autres cartes : <strong>VIDÉO > UTILISER TAMPON NVIDIA</strong>.</td></tr><tr><td>La table rame</td><td>Baissez <strong>SURÉCHANTILLONNAGE</strong>, <strong>OCCLUSION AMBIANTE</strong> et <strong>ANTICRÉNELAGE</strong>.</td></tr></tbody></table>
