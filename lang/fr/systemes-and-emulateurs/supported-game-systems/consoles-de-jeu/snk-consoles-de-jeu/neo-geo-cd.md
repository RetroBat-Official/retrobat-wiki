---
description: SNK
---

# Neo Geo CD

<div align="left"><figure><img src="../../../../.gitbook/assets/image (669).png" alt="" width="540"><figcaption></figcaption></figure></div>

## Présentation

La **Neo Geo CD** est la version CD de la console Neo Geo de SNK, sortie en 1994. Les jeux, sur CD-ROM, coûtaient bien moins cher que les cartouches de l'AES, mais le lecteur simple vitesse imposait de longs temps de chargement.

Trois modèles se sont succédé :

* le **Front Loader** (1994), à tiroir ;
* le **Top Loader** (1995), à capot ;
* le **CDZ** (1996, Japon), au lecteur plus rapide.

La ludothèque compte une centaine de jeux, surtout des adaptations des jeux Neo Geo (The King of Fighters, Samurai Shodown, Metal Slug…), souvent avec des musiques CD réenregistrées, et quelques exclusivités.

Les jeux en cartouche Neo Geo ont leur propre système (voir la page [**Neo Geo**](neo-geo.md)).

{% embed url="https://fr.wikipedia.org/wiki/Neo-Geo_CD" %}

## En bref

<table><thead><tr><th width="269"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\neogeocd</code></td></tr><tr><td><strong>Extensions</strong></td><td>.cue .chd .iso .zip .7z</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: neocd</td></tr><tr><td><strong>BIOS</strong></td><td>BIOS Neo Geo CD (voir BIOS)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro ; Raine par raccourcis</td></tr><tr><td><strong>RetroAchievements</strong></td><td>cores libretro (neocd conseillé)</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>cores libretro</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="147.75">Émulateur</th><th width="151.75">Pour qui ?</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>libretro: neocd</strong> (défaut)</td><td>Tout le monde</td><td>Émulateur dédié à la Neo Geo CD. Reconnaît tout seul les BIOS du dossier <code>bios\neocd</code>, passe les écrans de chargement par défaut. RetroAchievements, jeu en réseau.</td><td>Images <code>.cue</code> et <code>.chd</code> seulement.</td></tr><tr><td><strong>libretro: geolith</strong></td><td>Puristes</td><td>Émulation très précise, compatible avec tous les jeux du commerce.</td><td>Images <code>.cue</code> et <code>.chd</code> seulement. BIOS de MAME (<code>neocdz.zip</code>, et <code>neocd.zip</code> pour le Front / Top Loader).</td></tr><tr><td><strong>libretro: fbneo</strong></td><td>Utilisateurs de FBNeo</td><td>Même core et mêmes réglages que les jeux Neo Geo (dispositions de boutons).</td><td>Modèle CDZ uniquement. Images <code>.cue</code>, <code>.ccd</code> et <code>.chd</code> seulement.</td></tr><tr><td><strong>raine</strong></td><td>Images <code>.iso</code> ou compressées</td><td>Lit les images <code>.iso</code>, <code>.zip</code> et <code>.7z</code>. Volumes de la musique et des effets réglables.</td><td>Ne lit pas le <code>.chd</code>. Pas de RetroAchievements ni de jeu en réseau.</td></tr></tbody></table>

**En cas de doute, gardez libretro: neocd.**

## BIOS

**Core neocd** : placez au moins un de ces BIOS dans `bios\neocd`. Le core reconnaît les fichiers par leur contenu, leur nom n'a donc pas d'importance. Il les cherche aussi dans les sous-dossiers et dans les fichiers `.zip`.

<table><thead><tr><th width="155.75">Fichier</th><th width="191">Modèle</th><th>SHA-1</th></tr></thead><tbody><tr><td><code>neocd_z.rom</code></td><td>CDZ (choix par défaut de RetroBat)</td><td>b0f1c4fa8d4492a04431805f6537138b842b549f</td></tr><tr><td><code>neocd_sz.rom</code></td><td>CDZ (patch SMKDAN)</td><td>6a947457031dd3a702a296862446d7485aa89dbb</td></tr><tr><td><code>neocd_f.rom</code></td><td>Front Loader</td><td>a5f4a7a627b3083c979f6ebe1fabc5d2df6d083b</td></tr><tr><td><code>neocd_sf.rom</code></td><td>Front Loader (patch SMKDAN)</td><td>4a94719ee5d0e3f2b981498f70efc1b8f1cef325</td></tr><tr><td><code>neocd_t.rom</code></td><td>Top Loader</td><td>cc92b54a18a8bff6e595aabe8e5c360ba9e62eb5</td></tr><tr><td><code>neocd_st.rom</code></td><td>Top Loader (patch SMKDAN)</td><td>19729b51bdab60c42aafef6e20ea9234c7eb8410</td></tr><tr><td><code>neocd.bin</code></td><td>CDZ (MAME)</td><td>7bb26d1e5d1e930515219cb18bcde5b7b23e2eda</td></tr><tr><td><code>front-sp1.bin</code></td><td>Front Loader (MAME)</td><td>53bc1f283cdf00fa2efbb79f2e36d4c8038d743a</td></tr><tr><td><code>top-sp1.bin</code></td><td>Top Loader (MAME)</td><td>235f4d1d74364415910f73c10ae5482d90b4274f</td></tr><tr><td><code>uni-bioscd.rom</code></td><td>CDZ, BIOS Universe 3.3</td><td>5142f205912869b673a71480c5828b1eaed782a8</td></tr></tbody></table>

Sans aucun BIOS, le core neocd démarre avec un BIOS de remplacement intégré. Il reste incomplet : un BIOS d'origine est conseillé.

**Autres émulateurs** : ils utilisent les sets de MAME, à placer dans `bios`.

| Émulateur         | Fichiers                                                                                     |
| ----------------- | -------------------------------------------------------------------------------------------- |
| libretro: geolith | `neocdz.zip` (CDZ). Pour le Front Loader ou le Top Loader : `neocd.zip` **et** `neocdz.zip`. |
| libretro: fbneo   | `neocdz.zip` et `neogeo.zip` (dans `bios` ou `bios\fbneo`)                                   |
| raine             | `neocdz.zip`                                                                                 |

La vérification des BIOS de RetroBat demande au moins un BIOS dans `bios\neocd`, et liste `neocdz.zip`, `neocd.zip` et `neogeo.zip` comme optionnels.

**Quel modèle est émulé ?**

<table><thead><tr><th width="148.25">Émulateur</th><th>Option</th><th>Défaut RetroBat</th></tr></thead><tbody><tr><td>libretro: neocd</td><td><strong>ÉMULATION > BIOS</strong> : <strong>CDZ</strong>, <strong>CDZ (MAME)</strong>, <strong>FRONT LOADER</strong>, <strong>TOP LOADER</strong>, <strong>FRONT LOADER (MAME)</strong>, <strong>TOP LOADER (MAME)</strong>, <strong>UNIVERSE</strong></td><td><strong>CDZ</strong> (<code>neocd_z.rom</code>). S'il manque, le premier BIOS trouvé.</td></tr><tr><td>libretro: geolith</td><td><strong>ÉMULATION > BIOS</strong> : <strong>CDZ</strong>, <strong>FRONT LOADER</strong>, <strong>TOP LOADER</strong>, <strong>CDZ (UNIVERSE BIOS)</strong></td><td><strong>CDZ</strong></td></tr><tr><td>libretro: fbneo</td><td>—</td><td>CDZ</td></tr><tr><td>raine</td><td>—</td><td>CDZ (<code>neocdz.zip</code>)</td></tr></tbody></table>

Le modèle **CDZ** charge plus vite. Le Front Loader et le Top Loader servent surtout aux jeux qui fonctionnent mal sur CDZ.

## Quel format de jeu ?

| Format                            | neocd | geolith | fbneo | raine |
| --------------------------------- | ----- | ------- | ----- | ----- |
| `.cue` + `.bin`                   | oui   | oui     | oui   | oui   |
| `.chd`                            | oui   | oui     | oui   | non   |
| `.iso`                            | non   | non     | non   | oui   |
| `.zip` / `.7z` (image compressée) | non   | non     | non   | oui   |

* **Le `.chd` est conseillé** : un seul fichier, compressé, avec les pistes audio.
* Pour un jeu en `.cue`, gardez le `.cue` et ses fichiers (`.bin`, ou `.iso` avec des pistes audio `.wav`, `.flac`, `.ogg`, `.mp3`) dans le même dossier. Le core neocd lit ces deux sortes de `.cue`.
* Seuls les émulateurs compatibles avec le format du jeu sont proposés.

Pour convertir une image `.cue` en `.chd`, utilisez l'outil `chdman.exe` fourni avec MAME (dossier `emulators\mame`) : `chdman createcd -i jeu.cue -o jeu.chd`.

## Contrôles

RetroBat configure automatiquement les manettes. **START** et **SELECT** correspondent à ceux de la manette Neo Geo CD. Le stick gauche et la croix déplacent le joueur.

La Neo Geo CD a 4 boutons, **A**, **B**, **C** et **D**. Les cores libretro ajoutent des combinaisons de boutons sur les gâchettes, pratiques pour les coups spéciaux.

| Manette RetroBat | neocd     | geolith   | fbneo (CLASSIQUE, défaut) | raine |
| ---------------- | --------- | --------- | ------------------------- | ----- |
| SUD              | A         | A         | A                         | A     |
| EST              | B         | B         | B                         | B     |
| OUEST            | C         | C         | C                         | C     |
| NORD             | D         | D         | D                         | D     |
| L1               | C + D     | C + D     | C + D                     | —     |
| R1               | A + B     | A + B     | A + B                     | —     |
| L2               | B + C + D | B + C     | B + C + D                 | —     |
| R2               | A + B + C | A + B + C | A + B + C                 | —     |

Avec le core fbneo, **CONTRÔLES > TYPE DE CONTRÔLEUR** propose les mêmes dispositions que pour la Neo Geo (voir la page [**Neo Geo**](neo-geo.md)).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (670).png" alt="" width="225"><figcaption><p>NeoCD standard layout</p></figcaption></figure></div>

### Raccourcis

Les cores libretro utilisent les raccourcis standards de RetroArch (voir la page [**Raccourcis**](../../../../navigation/hotkeys.md)).

**Raine**

<table><thead><tr><th width="225.75">Raccourci</th><th>Action</th><th>Clavier</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quitter</td><td>ÉCHAP</td></tr><tr><td>HOTKEY + OUEST</td><td>Sauvegarde instantanée</td><td>F2</td></tr><tr><td>HOTKEY + NORD</td><td>Chargement instantané</td><td>F4</td></tr><tr><td>HOTKEY + HAUT / BAS</td><td>Emplacement de sauvegarde suivant</td><td>F6</td></tr><tr><td>HOTKEY + R3</td><td>Capture d'écran</td><td>F8</td></tr><tr><td>HOTKEY + EST</td><td>Menu de Raine</td><td>F1</td></tr><tr><td>HOTKEY + L3</td><td>Pause</td><td>P</td></tr><tr><td>HOTKEY + GAUCHE</td><td>Image par image</td><td>K</td></tr><tr><td>—</td><td>Plein écran / fenêtre</td><td>F</td></tr><tr><td>—</td><td>Réinitialiser le jeu</td><td>F9</td></tr></tbody></table>

Les touches se changent dans le fichier `kb_hotkeys.yml` (voir la page [**Raccourcis**](../../../../navigation/hotkeys.md)).

## Dossiers

| Contenu                                                                              | Dossier                          |
| ------------------------------------------------------------------------------------ | -------------------------------- |
| Jeux                                                                                 | `roms\neogeocd`                  |
| BIOS (core neocd)                                                                    | `bios\neocd`                     |
| BIOS (geolith, fbneo, raine)                                                         | `bios`                           |
| Core neocd : sauvegardes des jeux (mémoire de la console, un fichier `.srm` par jeu) | `saves\neogeocd`                 |
| Core geolith : sauvegardes des jeux                                                  | `saves\neogeocd`                 |
| Core fbneo : sauvegardes des jeux                                                    | `saves\neogeocd\fbneo`           |
| Cores libretro : sauvegardes instantanées                                            | `saves\neogeocd\libretro.<core>` |
| Raine : sauvegardes instantanées et sauvegardes des jeux                             | `emulators\raine\savegame`       |
| Raine : captures d'écran                                                             | `screenshots\raine`              |

## Guides

### Temps de chargement

Les chargements sont la principale gêne de la Neo Geo CD. Plusieurs options les réduisent :

<table><thead><tr><th width="150.75">Émulateur</th><th>Option</th><th>Effet</th></tr></thead><tbody><tr><td>neocd, geolith</td><td><strong>ÉMULATION > PASSER LES CHARGEMENTS CD</strong></td><td>Avance rapide automatique pendant les chargements. Activé par défaut avec neocd, désactivé avec geolith.</td></tr><tr><td>neocd, geolith</td><td><strong>ÉMULATION > VITESSE DE LECTURE CD</strong></td><td>Remplace l'attente du lecteur dans le BIOS, pour charger plus vite. Désactivé par défaut. Sans effet avec le BIOS Universe sur geolith.</td></tr><tr><td>raine</td><td><strong>ÉMULATION > AMÉLIORER LE TEMPS DE CHARGEMENT CD</strong></td><td>Vitesse du lecteur émulé, de 1X à 48X (8X par défaut), ou <strong>NON</strong> pour la vitesse d'origine.</td></tr><tr><td>raine</td><td><strong>ÉMULATION > MODE PERFORMANCE</strong></td><td>Accélère l'émulation au prix de la précision (activé par défaut).</td></tr></tbody></table>

### Sauvegardes des jeux

La Neo Geo CD enregistre les parties dans sa mémoire interne. Avec le core neocd, RetroBat crée une mémoire par jeu (un fichier `.srm` dans `saves\neogeocd`) : les sauvegardes d'un jeu ne remplissent pas la mémoire des autres.

Avec le core neocd, une sauvegarde instantanée garde le type de BIOS utilisé. Une sauvegarde faite avec le BIOS intégré ne se charge pas correctement avec un BIOS d'origine, et inversement.

### Le BIOS Universe

Le BIOS Universe CD permet de changer de région et donne accès à des codes de triche. Il se choisit avec **ÉMULATION > BIOS** : **UNIVERSE** (neocd, fichier `uni-bioscd.rom`) ou **CDZ (UNIVERSE BIOS)** (geolith). Ses menus s'ouvrent comme sur la Neo Geo (voir la page [**Neo Geo**](neo-geo.md)).

En mode hardcore des RetroAchievements, le core neocd refuse le BIOS Universe : gardez un autre BIOS pour jouer en hardcore.

### RetroAchievements

La Neo Geo CD a sa propre catégorie sur RetroAchievements. Le core neocd est conseillé. Pour plus de détails, voir la page [**RetroAchievements**](../../../../utilisation-avancee/retroachievements.md).

### Autres options utiles

<table><thead><tr><th width="139.5">Émulateur</th><th>Option</th><th>Effet</th></tr></thead><tbody><tr><td>neocd, geolith</td><td><strong>ÉMULATION > RÉGION</strong></td><td>Japon, USA (défaut), Europe (et Asie avec geolith). Certains jeux changent selon la région.</td></tr><tr><td>geolith</td><td><strong>VIDÉO > RAPPORT D'ASPECT DU CORE</strong></td><td><strong>1:1 (PIXELS CARRÉS)</strong> (défaut), <strong>45:44 (NTSC PRÉCIS)</strong> ou <strong>4:3 (NTSC TRADITIONNEL)</strong>. Utilisé quand <strong>RAPPORT D'ASPECT</strong> est sur AUTO.</td></tr><tr><td>raine</td><td><strong>AUDIO > VOLUME MUSIQUE CD</strong> / <strong>VOLUME EFFETS SONORES</strong></td><td>Volume des musiques CD et des effets, de 0 à 200 (70 par défaut).</td></tr></tbody></table>

## Problèmes connus

| Problème                                                      | Solution                                                                                                                                             |
| ------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| Le core neocd démarre sans BIOS ou certains jeux plantent     | Aucun BIOS reconnu dans `bios\neocd` : le core utilise son BIOS intégré, incomplet. Ajoutez un BIOS d'origine (voir [**BIOS**](neo-geo-cd.md#bios)). |
| Geolith : le jeu ne démarre pas en Front Loader ou Top Loader | Ces modèles demandent `neocd.zip` **et** `neocdz.zip` dans `bios`.                                                                                   |
| fbneo ou Raine ne démarrent pas                               | `neocdz.zip` manque dans `bios` (et `neogeo.zip` pour fbneo).                                                                                        |
| Un jeu `.iso`, `.zip` ou `.7z` ne propose que Raine           | Les autres émulateurs ne lisent que le `.cue` et le `.chd`. Convertissez le jeu en `.chd`.                                                           |
| Un `.chd` ne se lance pas avec Raine                          | Raine ne lit pas le `.chd` : utilisez le core neocd.                                                                                                 |
| Metal Slug 2 : sons qui grésillent (neocd)                    | Utilisez un BIOS CDZ.                                                                                                                                |
| Cyber Lip demande de formater la mémoire                      | Comportement normal de la console : acceptez le formatage dans l'écran du BIOS.                                                                      |
| RetroAchievements passe en mode normal                        | Le BIOS Universe est choisi : choisissez un autre BIOS dans **ÉMULATION > BIOS**.                                                                    |
