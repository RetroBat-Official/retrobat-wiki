# 2 Ship 2 Harkinian

<div align="left"><figure><img src="../../../../.gitbook/assets/image (642).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Présentation

**2 Ship 2 Harkinian** (2Ship) est un portage PC de **The Legend of Zelda: Majora's Mask** (Nintendo, 2000), réalisé par l'équipe HarbourMasters, celle de Ship of Harkinian, à partir de la décompilation du jeu. Il ajoute la haute résolution, l'écran large, une fréquence d'images jusqu'à 360 images par seconde, de nombreuses améliorations, des packs de textures et un mode Randomizer.

Le jeu n'est pas fourni : 2Ship extrait les données de votre propre ROM du jeu (version américaine Nintendo 64 ou GameCube).

{% embed url="https://github.com/HarbourMasters/2ship2harkinian" %}

## En bref

<table><thead><tr><th width="264"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\2ship</code></td></tr><tr><td><strong>Extensions</strong></td><td>.z64 .n64 .v64</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>2ship</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (ROM du jeu à fournir)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique (joueur 1)</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non (sauvegardes du jeu)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr></tbody></table>

## BIOS

Aucun BIOS n'est nécessaire.

## Quel format de jeu ?

2Ship lit les ROM Nintendo 64 aux formats **.z64**, **.n64** et **.v64**. Les archives `.zip` ne sont pas acceptées.

Versions compatibles :

| Version                                                        | Langue du jeu |
| -------------------------------------------------------------- | ------------- |
| Nintendo 64 NTSC-U 1.0 (USA)                                   | Anglais       |
| GameCube NTSC-U (USA, version de la Zelda Collector's Edition) | Anglais       |

Les versions PAL et japonaises ne sont pas prises en charge : le jeu est donc en anglais. Pour vérifier votre ROM, chargez-la dans le vérificateur de compatibilité ci-dessous.

{% embed url="https://2ship.equipment/" %}

## Contrôles

### Configuration automatique

RetroBat configure la manette du joueur 1 à chaque lancement :

| Manette RetroBat | Nintendo 64                      |
| ---------------- | -------------------------------- |
| Stick gauche     | Stick                            |
| SUD              | A                                |
| OUEST            | B                                |
| L2               | Z                                |
| L1               | L                                |
| R1               | R                                |
| Stick droit      | Boutons C                        |
| Croix            | Croix                            |
| START            | START                            |
| SELECT           | Ouvrir / fermer le menu de 2Ship |

<div align="left"><figure><img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/n64-standalone.png?raw=true" alt="" width="375"><figcaption></figcaption></figure></div>

Pour placer Z sur la gâchette droite, réglez **CONTRÔLES > DISPOSITION DES CONTRÔLES** sur **STANDARD (Z GÂCHETTE DROITE)**.

Les autres options de **CONTRÔLES** : **ZONE MORTE ANALOGIQUE**, **ACTIVER LES VIBRATIONS** et **PUISSANCE DES VIBRATIONS**, **ACTIVER LE MOTION CONTROL** et **SENSIBILITÉ DU GYROSCOPE** (manettes avec gyroscope).

Pour garder une configuration faite dans le menu de 2Ship, désactivez **AUTOCONFIGURER LES MANETTES**.

### Manettes N64

RetroBat reconnaît la manette N64 Nintendo Switch Online et les adaptateurs N64 Mayflash et Raphnet, et leur applique une configuration dédiée.

{% hint style="info" %}
Avec l'adaptateur Mayflash, branchez les manettes en ordre inverse : le joueur 1 est la manette branchée sur le dernier port de l'adaptateur.
{% endhint %}

Pour plus de détails, voir la page [**Contrôleurs spéciaux**](../../../../controleurs/supported-controllers/gamepads/controleurs-speciaux.md).

### Raccourcis

<table><thead><tr><th width="225.25">Raccourci</th><th>Action</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quitter</td></tr><tr><td><strong>SELECT</strong></td><td>Ouvrir / fermer le menu de 2Ship</td></tr></tbody></table>

Au clavier :

<table><thead><tr><th width="202.75">Touche</th><th>Action</th></tr></thead><tbody><tr><td><strong>Échap</strong> ou <strong>F1</strong></td><td>Ouvrir / fermer le menu</td></tr><tr><td><strong>F11</strong></td><td>Plein écran</td></tr><tr><td><strong>Tab</strong></td><td>Activer / désactiver les textures personnalisées</td></tr><tr><td><strong>Ctrl + R</strong></td><td>Redémarrer le jeu</td></tr></tbody></table>

Quand le menu est ouvert, la manette sert à s'y déplacer : la croix pour choisir, SUD pour valider, EST pour revenir en arrière. Le jeu ne reçoit plus les commandes de la manette tant que le menu est affiché.

## Dossiers

<table><thead><tr><th width="259">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Sauvegardes</td><td><code>emulators\2ship\saves</code></td></tr><tr><td>Données extraites du jeu</td><td><code>emulators\2ship\mm.o2r</code></td></tr><tr><td>Mods et packs de textures</td><td><code>emulators\2ship\mods</code></td></tr><tr><td>Préréglages</td><td><code>emulators\2ship\presets</code></td></tr><tr><td>Configuration</td><td><code>emulators\2ship\2ship2harkinian.json</code></td></tr></tbody></table>

## Guides

### Premier lancement

Au premier lancement, RetroBat transmet la ROM à 2Ship, qui en extrait les données dans `mm.o2r` puis lance le jeu. L'extraction prend quelques minutes. Les lancements suivants démarrent directement.

Après une mise à jour de 2Ship qui change le format des données, RetroBat supprime l'ancienne archive et 2Ship refait l'extraction.

Une seule entrée suffit dans `roms\2ship` : une fois les données extraites, la ROM n'est plus lue.

### Mods et packs de textures

Placez les mods (fichiers `.o2r` ou `.otr` : textures, modèles, musiques) dans `emulators\2ship\mods`, puis lancez le jeu. **Tab** active ou désactive les textures personnalisées en jeu.

### Randomizer

Le Randomizer se règle dans le menu de 2Ship (**SELECT** ou **Échap**), avant de créer une nouvelle sauvegarde.

### Autres options utiles

<table><thead><tr><th width="329">Option</th><th>Effet</th></tr></thead><tbody><tr><td><strong>RÉSOLUTION INTERNE</strong></td><td>Résolution de rendu, de NATIF (240 lignes) à 4K. Par défaut : <strong>2X(480)</strong>.</td></tr><tr><td><strong>RAPPORT D'ASPECT</strong></td><td>Par défaut, l'image remplit l'écran. <strong>NATIF (4:3)</strong> garde les proportions d'origine, <strong>ÉCRAN LARGE (16:9)</strong>, <strong>3DS (5:3)</strong>, <strong>16:10</strong> ou <strong>ULTRA LARGE (21:9)</strong> élargissent le champ de vision.</td></tr><tr><td><strong>DÉCORATIONS</strong></td><td>Les décorations ne s'affichent qu'avec <strong>RAPPORT D'ASPECT</strong> réglé sur <strong>NATIF (4:3)</strong>.</td></tr><tr><td><strong>MISE À L'ÉCHELLE (NOMBRE ENTIER)</strong></td><td>Agrandit l'image d'un nombre entier de fois, pour des pixels nets.</td></tr><tr><td><strong>ÉMULATION > FPS CIBLE</strong></td><td>Fréquence d'images, de 20 (fréquence d'origine, par défaut) à 360 images par seconde. Les images intermédiaires sont interpolées.</td></tr><tr><td><strong>ÉMULATION > CALER LES FPS SUR LA FRÉQUENCE DE L'ÉCRAN</strong></td><td>Suit la fréquence de l'écran (60 Hz, 144 Hz…) au lieu de <strong>FPS CIBLE</strong>.</td></tr><tr><td><strong>RENDU VISUEL > FILTRAGE DES TEXTURES</strong></td><td><strong>TROIS POINTS</strong> (par défaut, comme la N64), <strong>LINÉAIRE</strong> ou <strong>AUCUN</strong>.</td></tr><tr><td><strong>RENDU VISUEL > ANTICRÉNELAGE (MSAA)</strong></td><td>Lisse les contours des polygones (1 à 8).</td></tr><tr><td><strong>PILOTES > VIDÉO</strong></td><td><strong>DIRECTX 11</strong> (par défaut) ou <strong>OPENGL</strong>.</td></tr><tr><td><strong>PILOTES > AUDIO</strong></td><td><strong>WASAPI</strong> (par défaut) ou <strong>SDL</strong>.</td></tr></tbody></table>

## Problèmes connus

| Problème                                           | Solution                                                                                                                                                          |
| -------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 2Ship indique que la ROM n'est pas prise en charge | Seules la version américaine N64 1.0 et la version GameCube américaine sont acceptées : vérifiez la ROM sur **2ship.equipment**.                                  |
| Le jeu est en anglais                              | 2Ship ne prend en charge que les versions américaines du jeu.                                                                                                     |
| Le menu de 2Ship s'ouvre pendant la partie         | **SELECT** ouvre le menu : appuyez de nouveau sur **SELECT** pour le fermer.                                                                                      |
| Écran noir ou plantage au lancement                | Réglez **PILOTES > VIDÉO** sur **OPENGL**.                                                                                                                        |
| Les décorations ne s'affichent pas                 | Réglez **RAPPORT D'ASPECT** sur **NATIF (4:3)**.                                                                                                                  |
| Un mod ne s'affiche pas                            | Vérifiez qu'il est dans `emulators\2ship\mods` et qu'il est prévu pour la version de 2Ship livrée ; appuyez sur **Tab** pour activer les textures personnalisées. |
