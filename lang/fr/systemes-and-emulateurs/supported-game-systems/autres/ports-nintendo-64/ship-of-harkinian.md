# Ship Of Harkinian

<div align="left"><figure><img src="../../../../.gitbook/assets/image (644).png" alt="" width="403"><figcaption></figcaption></figure></div>

## Présentation

**Ship of Harkinian** (SoH) est un portage PC de **The Legend of Zelda: Ocarina of Time** (Nintendo, 1998), réalisé par l'équipe HarbourMasters à partir de la décompilation du jeu. Il ajoute la haute résolution, l'écran large, une fréquence d'images jusqu'à 360 images par seconde, de nombreuses améliorations, des packs de textures et un mode Randomizer.

Le jeu n'est pas fourni : SoH extrait les données de votre propre ROM du jeu (Nintendo 64 ou GameCube), version originale ou **Master Quest**.

{% embed url="https://www.shipofharkinian.com" %}

## En bref

<table><thead><tr><th width="284"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\soh</code></td></tr><tr><td><strong>Extensions</strong></td><td>.z64 .n64 .v64</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>soh</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (ROM du jeu à fournir)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique (joueur 1)</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non (sauvegardes du jeu)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr></tbody></table>

## BIOS

Aucun BIOS n'est nécessaire.

## Quel format de jeu ?

SoH lit les ROM Nintendo 64 aux formats **.z64**, **.n64** et **.v64** (les ROM GameCube sont des ROM N64 extraites du disque). Les archives `.zip` ne sont pas acceptées.

Versions compatibles :

<table><thead><tr><th width="352.25">Version</th><th width="134.5">Quête</th><th>Langues du jeu</th></tr></thead><tbody><tr><td>Nintendo 64 NTSC 1.0, 1.1, 1.2 (USA, Japon)</td><td>Originale</td><td>Anglais, japonais</td></tr><tr><td>Nintendo 64 PAL 1.0, 1.1</td><td>Originale</td><td>Anglais, allemand, français</td></tr><tr><td>GameCube NTSC (USA, Japon, Collector's Edition)</td><td>Originale</td><td>Anglais, japonais</td></tr><tr><td>GameCube PAL</td><td>Originale</td><td>Anglais, allemand, français</td></tr><tr><td>GameCube Master Quest NTSC (USA, Japon)</td><td>Master Quest</td><td>Anglais, japonais</td></tr><tr><td>GameCube Master Quest PAL</td><td>Master Quest</td><td>Anglais, allemand, français</td></tr><tr><td>GameCube PAL de débogage (originale et Master Quest)</td><td>Les deux</td><td>Anglais, allemand, français</td></tr></tbody></table>

Pour vérifier votre ROM, chargez-la dans le vérificateur de compatibilité ci-dessous : il indique si elle est prise en charge, sa région et s'il s'agit de Master Quest.

{% embed url="https://ship.equipment/" %}

Une seule entrée suffit dans `roms\soh` : une fois les données extraites, toutes les ROM du dossier lancent le même jeu.

## Contrôles

### Configuration automatique

RetroBat configure la manette du joueur 1 à chaque lancement :

<table><thead><tr><th width="231.5">Manette RetroBat</th><th>Nintendo 64</th></tr></thead><tbody><tr><td>Stick gauche</td><td>Stick</td></tr><tr><td>SUD</td><td>A</td></tr><tr><td>OUEST</td><td>B</td></tr><tr><td>L2</td><td>Z</td></tr><tr><td>L1</td><td>L</td></tr><tr><td>R1</td><td>R</td></tr><tr><td>Stick droit</td><td>Boutons C</td></tr><tr><td>Croix</td><td>Croix</td></tr><tr><td>START</td><td>START</td></tr><tr><td>SELECT</td><td>Ouvrir / fermer le menu de SoH</td></tr></tbody></table>

<div align="left"><figure><img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/n64-standalone.png?raw=true" alt="" width="375"><figcaption></figcaption></figure></div>

Pour placer Z sur la gâchette droite, réglez **CONTRÔLES > DISPOSITION DES CONTRÔLES** sur **STANDARD (Z GÂCHETTE DROITE)**.

Les autres options de **CONTRÔLES** : **ZONE MORTE ANALOGIQUE**, **ACTIVER LES VIBRATIONS** et **PUISSANCE DES VIBRATIONS**, **ACTIVER LE MOTION CONTROL** et **SENSIBILITÉ DU GYROSCOPE** (manettes avec gyroscope).

Pour garder une configuration faite dans le menu de SoH, désactivez **AUTOCONFIGURER LES MANETTES**.

### Manettes N64

RetroBat reconnaît la manette N64 Nintendo Switch Online et les adaptateurs N64 Mayflash et Raphnet, et leur applique une configuration dédiée.

{% hint style="info" %}
Avec l'adaptateur Mayflash, branchez les manettes en ordre inverse : le joueur 1 est la manette branchée sur le dernier port de l'adaptateur.
{% endhint %}

Pour plus de détails, voir la page [**Contrôleurs spéciaux**](../../../../controleurs/supported-controllers/gamepads/controleurs-speciaux.md).

### Raccourcis

<table><thead><tr><th width="217.75">Raccourci</th><th>Action</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quitter</td></tr><tr><td><strong>SELECT</strong></td><td>Ouvrir / fermer le menu de SoH</td></tr></tbody></table>

Au clavier :

<table><thead><tr><th width="147.75">Touche</th><th>Action</th></tr></thead><tbody><tr><td><strong>Échap</strong> ou <strong>F1</strong></td><td>Ouvrir / fermer le menu</td></tr><tr><td><strong>F11</strong></td><td>Plein écran</td></tr><tr><td><strong>Tab</strong></td><td>Activer / désactiver les textures personnalisées</td></tr><tr><td><strong>Ctrl + R</strong></td><td>Redémarrer le jeu</td></tr><tr><td><strong>F5</strong> / <strong>F6</strong> / <strong>F7</strong></td><td>Sauvegarde instantanée / changer d'emplacement / chargement (expérimental, non géré par RetroBat)</td></tr></tbody></table>

Quand le menu est ouvert, la manette sert à s'y déplacer : la croix pour choisir, SUD pour valider, EST pour revenir en arrière. Le jeu ne reçoit plus les commandes de la manette tant que le menu est affiché.

## Dossiers

<table><thead><tr><th width="236.5">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Sauvegardes</td><td><code>emulators\soh\Save</code></td></tr><tr><td>Données extraites du jeu</td><td><code>emulators\soh\oot.o2r</code> (Master Quest : <code>oot-mq.o2r</code>)</td></tr><tr><td>Mods et packs de textures</td><td><code>emulators\soh\mods</code></td></tr><tr><td>Journaux du Randomizer</td><td><code>emulators\soh\Randomizer</code></td></tr><tr><td>Configuration</td><td><code>emulators\soh\shipofharkinian.json</code></td></tr></tbody></table>

## Guides

### Premier lancement

Au premier lancement, RetroBat transmet la ROM à SoH, qui en extrait les données dans `oot.o2r` (ou `oot-mq.o2r` pour une ROM Master Quest). L'extraction prend quelques minutes, puis SoH demande **Run Ship of Harkinian?** : répondez **Yes** pour lancer le jeu.

Les lancements suivants démarrent directement. Après une mise à jour de SoH qui change le format des données, RetroBat supprime l'ancienne archive et SoH refait l'extraction.

### Jouer à Master Quest

Pour avoir les deux quêtes, placez aussi la ROM Master Quest dans `roms\soh` : son nom doit contenir « Master Quest », comme les noms No-Intro (par exemple `Legend of Zelda, The - Ocarina of Time - Master Quest (USA) (GameCube Edition).z64`). Lancez-la une fois depuis RetroBat : SoH crée `oot-mq.o2r` à côté de `oot.o2r`.

Avec les deux archives, l'écran de sélection des fichiers propose de choisir la quête (originale ou Master Quest) en créant une nouvelle sauvegarde. Le Randomizer peut aussi mélanger les donjons des deux versions.

### Jouer en français

Réglez **ÉMULATION > LANGUE** sur **FRANÇAIS**. Les textes en français (et en allemand) ne se trouvent que dans les versions **PAL** du jeu : avec une version NTSC, le jeu reste en anglais. À l'inverse, **JAPONAIS** demande une version NTSC.

### Mods et packs de textures

Placez les mods (fichiers `.o2r` ou `.otr` : textures, modèles, musiques) dans `emulators\soh\mods`, puis lancez le jeu. **Tab** active ou désactive les textures personnalisées en jeu.

### Randomizer

Le Randomizer se règle dans le menu de SoH (**SELECT** ou **Échap**) : choisissez les réglages, générez une graine, puis créez une nouvelle sauvegarde de type Randomizer sur l'écran de sélection des fichiers.

### Autres options utiles

<table><thead><tr><th width="332.75">Option</th><th>Effet</th></tr></thead><tbody><tr><td><strong>RÉSOLUTION INTERNE</strong></td><td>Résolution de rendu, de NATIF (240 lignes) à 4K. Par défaut : <strong>2X(480)</strong>.</td></tr><tr><td><strong>RAPPORT D'ASPECT</strong></td><td>Par défaut, l'image remplit l'écran. <strong>NATIF (4:3)</strong> garde les proportions d'origine, <strong>ÉCRAN LARGE (16:9)</strong>, <strong>3DS (5:3)</strong>, <strong>16:10</strong> ou <strong>ULTRA LARGE (21:9)</strong> élargissent le champ de vision.</td></tr><tr><td><strong>DÉCORATIONS</strong></td><td>Les décorations ne s'affichent qu'avec <strong>RAPPORT D'ASPECT</strong> réglé sur <strong>NATIF (4:3)</strong>.</td></tr><tr><td><strong>MISE À L'ÉCHELLE (NOMBRE ENTIER)</strong></td><td>Agrandit l'image d'un nombre entier de fois, pour des pixels nets.</td></tr><tr><td><strong>ÉMULATION > FPS CIBLE</strong></td><td>Fréquence d'images, de 20 (fréquence d'origine, par défaut) à 360 images par seconde. Les images intermédiaires sont interpolées.</td></tr><tr><td><strong>ÉMULATION > CALER LES FPS SUR LA FRÉQUENCE DE L'ÉCRAN</strong></td><td>Suit la fréquence de l'écran (60 Hz, 144 Hz…) au lieu de <strong>FPS CIBLE</strong>.</td></tr><tr><td><strong>RENDU VISUEL > FILTRAGE DES TEXTURES</strong></td><td><strong>TROIS POINTS</strong> (par défaut, comme la N64), <strong>LINÉAIRE</strong> ou <strong>AUCUN</strong>.</td></tr><tr><td><strong>RENDU VISUEL > ANTICRÉNELAGE (MSAA)</strong></td><td>Lisse les contours des polygones (1 à 8).</td></tr><tr><td><strong>PILOTES > VIDÉO</strong></td><td><strong>DIRECTX</strong> (par défaut) ou <strong>OPENGL</strong>.</td></tr><tr><td><strong>PILOTES > AUDIO</strong></td><td><strong>WASAPI</strong> (par défaut) ou <strong>SDL</strong>.</td></tr></tbody></table>

## Problèmes connus

<table><thead><tr><th width="356.5">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>SoH indique que la ROM n'est pas prise en charge</td><td>Vérifiez la ROM sur <strong>ship.equipment</strong> : seules les versions de la liste sont acceptées. Une ROM modifiée (traduction, hack) ne fonctionne pas.</td></tr><tr><td>SoH reste sur la fenêtre « Run Ship of Harkinian? »</td><td>Elle s'affiche une seule fois, après l'extraction : répondez <strong>Yes</strong>.</td></tr><tr><td>Le jeu reste en anglais avec la langue réglée sur <strong>FRANÇAIS</strong></td><td>Le français n'existe que dans les versions PAL du jeu (voir <a href="ship-of-harkinian.md#jouer-en-francais"><strong>Guides</strong></a>).</td></tr><tr><td>La ROM Master Quest lance la quête originale</td><td>Le nom du fichier doit contenir « Master Quest » pour que RetroBat la transmette à SoH (voir <a href="ship-of-harkinian.md#jouer-a-master-quest"><strong>Guides</strong></a>).</td></tr><tr><td>Le menu de SoH s'ouvre pendant la partie</td><td><strong>SELECT</strong> ouvre le menu : appuyez de nouveau sur <strong>SELECT</strong> pour le fermer.</td></tr><tr><td>Écran noir ou plantage au lancement</td><td>Réglez <strong>PILOTES > VIDÉO</strong> sur <strong>OPENGL</strong>.</td></tr><tr><td>Les décorations ne s'affichent pas</td><td>Réglez <strong>RAPPORT D'ASPECT</strong> sur <strong>NATIF (4:3)</strong>.</td></tr><tr><td>Un mod ne s'affiche pas</td><td>Vérifiez qu'il est dans <code>emulators\soh\mods</code> et qu'il est prévu pour la version de SoH livrée ; appuyez sur <strong>Tab</strong> pour activer les textures personnalisées.</td></tr></tbody></table>
