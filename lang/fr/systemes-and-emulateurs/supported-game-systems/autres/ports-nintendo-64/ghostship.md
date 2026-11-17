# Ghostship

<div align="left"><figure><img src="../../../../.gitbook/assets/image (643).png" alt="" width="375"><figcaption></figcaption></figure></div>

## Présentation

**Ghostship** est un portage PC de **Super Mario 64** (Nintendo, 1996), réalisé par l'équipe HarbourMasters à partir de la décompilation du jeu. Il ajoute la haute résolution, l'écran large, une fréquence d'images jusqu'à 360 images par seconde, de nombreuses améliorations et des packs de textures.

Le jeu n'est pas fourni : Ghostship extrait les données de votre propre ROM du jeu (version américaine ou japonaise).

{% embed url="https://github.com/HarbourMasters/Ghostship" %}

## En bref

<table><thead><tr><th width="275.25"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\ghostship</code></td></tr><tr><td><strong>Extensions</strong></td><td>.z64</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>ghostship</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (ROM du jeu à fournir)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique (joueur 1)</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non (sauvegardes du jeu)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr></tbody></table>

## BIOS

Aucun BIOS n'est nécessaire.

## Quel format de jeu ?

Ghostship ne lit que les ROM au format **.z64**. Une ROM `.n64` ou `.v64` doit d'abord être convertie en `.z64` (par exemple avec l'outil en ligne de hack64.net).

{% embed url="https://hack64.net/tools/swapper.php" %}

Versions compatibles :

<table><thead><tr><th width="207.75">Version</th><th>SHA-1</th></tr></thead><tbody><tr><td>Nintendo 64 USA</td><td><code>9bef1128717f958171a4afac3ed78ee2bb4e86ce</code></td></tr><tr><td>Nintendo 64 Japon</td><td><code>8a20a5c83d6ceb0f0506cfc9fa20d8f438cafe51</code></td></tr></tbody></table>

Une seule entrée suffit dans `roms\ghostship` : une fois les données extraites, la ROM n'est plus lue.

## Contrôles

### Configuration automatique

RetroBat configure la manette du joueur 1 à chaque lancement :

<table><thead><tr><th width="220.25">Manette RetroBat</th><th>Nintendo 64</th></tr></thead><tbody><tr><td>Stick gauche</td><td>Stick</td></tr><tr><td>SUD</td><td>A</td></tr><tr><td>OUEST</td><td>B</td></tr><tr><td>L2</td><td>Z</td></tr><tr><td>L1</td><td>L</td></tr><tr><td>R1</td><td>R</td></tr><tr><td>Stick droit</td><td>Boutons C</td></tr><tr><td>Croix</td><td>Croix</td></tr><tr><td>START</td><td>START</td></tr><tr><td>SELECT</td><td>Ouvrir / fermer le menu de Ghostship</td></tr></tbody></table>

<div align="left"><figure><img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/n64-standalone.png?raw=true" alt="" width="375"><figcaption></figcaption></figure></div>

Pour placer Z sur la gâchette droite, réglez **CONTRÔLES > DISPOSITION DES CONTRÔLES** sur **STANDARD (Z GÂCHETTE DROITE)**.

Les autres options de **CONTRÔLES** : **ZONE MORTE ANALOGIQUE**, **ACTIVER LES VIBRATIONS** et **PUISSANCE DES VIBRATIONS**, **ACTIVER LE MOTION CONTROL** et **SENSIBILITÉ DU GYROSCOPE** (manettes avec gyroscope).

Pour garder une configuration faite dans le menu de Ghostship, désactivez **AUTOCONFIGURER LES MANETTES**.

### Manettes N64

RetroBat reconnaît la manette N64 Nintendo Switch Online et les adaptateurs N64 Mayflash et Raphnet, et leur applique une configuration dédiée.

{% hint style="info" %}
Avec l'adaptateur Mayflash, branchez les manettes en ordre inverse : le joueur 1 est la manette branchée sur le dernier port de l'adaptateur.
{% endhint %}

Pour plus de détails, voir la page [**Contrôleurs spéciaux**](../../../../controleurs/supported-controllers/gamepads/controleurs-speciaux.md).

### Raccourcis

<table><thead><tr><th width="231.5">Raccourci</th><th>Action</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quitter</td></tr><tr><td><strong>SELECT</strong></td><td>Ouvrir / fermer le menu de Ghostship</td></tr></tbody></table>

Au clavier :

<table><thead><tr><th width="164">Touche</th><th>Action</th></tr></thead><tbody><tr><td><strong>Échap</strong></td><td>Ouvrir / fermer le menu</td></tr><tr><td><strong>F11</strong></td><td>Plein écran</td></tr><tr><td><strong>Tab</strong></td><td>Activer / désactiver les textures personnalisées</td></tr><tr><td><strong>Ctrl + R</strong></td><td>Redémarrer (dans un niveau)</td></tr></tbody></table>

Quand le menu est ouvert, la manette sert à s'y déplacer : la croix pour choisir, SUD pour valider, EST pour revenir en arrière. Le jeu ne reçoit plus les commandes de la manette tant que le menu est affiché.

## Dossiers

<table><thead><tr><th width="239">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Sauvegardes</td><td><code>emulators\ghostship\saves</code></td></tr><tr><td>Données extraites du jeu</td><td><code>emulators\ghostship\sm64.o2r</code></td></tr><tr><td>Mods et packs de textures</td><td><code>emulators\ghostship\mods</code></td></tr><tr><td>Configuration</td><td><code>emulators\ghostship\ghostship.cfg.json</code></td></tr></tbody></table>

## Guides

### Premier lancement

Au premier lancement, RetroBat transmet la ROM à Ghostship, qui en extrait les données dans `sm64.o2r` puis lance le jeu. L'extraction prend quelques minutes. Les lancements suivants démarrent directement.

Après une mise à jour de Ghostship qui change le format des données, RetroBat supprime l'ancienne archive et Ghostship refait l'extraction.

### Mods et packs de textures

Placez les mods (fichiers `.o2r` ou `.otr` : textures, modèles, musiques) dans `emulators\ghostship\mods`, puis lancez le jeu. La section **Mods** du menu de Ghostship permet de les gérer. **Tab** active ou désactive les textures personnalisées en jeu.

### Autres options utiles

<table><thead><tr><th width="341.5">Option</th><th>Effet</th></tr></thead><tbody><tr><td><strong>RÉSOLUTION INTERNE</strong></td><td>Résolution de rendu, de <strong>240p (NATIF)</strong> à <strong>2160p (4K)</strong>. Par défaut : <strong>720p</strong>.</td></tr><tr><td><strong>RAPPORT D'ASPECT</strong></td><td>Par défaut, l'image remplit l'écran. <strong>NATIF (4:3)</strong> garde les proportions d'origine, <strong>ÉCRAN LARGE (16:9)</strong>, <strong>3DS (5:3)</strong>, <strong>16:10</strong> ou <strong>ULTRA LARGE (21:9)</strong> élargissent le champ de vision.</td></tr><tr><td><strong>DÉCORATIONS</strong></td><td>Les décorations ne s'affichent qu'avec <strong>RAPPORT D'ASPECT</strong> réglé sur <strong>NATIF (4:3)</strong>.</td></tr><tr><td><strong>MISE À L'ÉCHELLE (NOMBRE ENTIER)</strong></td><td>Agrandit l'image d'un nombre entier de fois, pour des pixels nets.</td></tr><tr><td><strong>SYNCHRONISATION VERTICALE</strong></td><td>Activée par défaut.</td></tr><tr><td><strong>RENDU VISUEL > FPS CIBLE</strong></td><td>Fréquence d'images, de 30 (fréquence d'origine) à 360 images par seconde. Les images intermédiaires sont interpolées. Par défaut, le jeu suit la fréquence de l'écran (60 Hz, 144 Hz…).</td></tr><tr><td><strong>RENDU VISUEL > FILTRAGE DES TEXTURES</strong></td><td><strong>LINÉAIRE</strong> (par défaut), <strong>TROIS POINTS</strong> (comme la N64) ou <strong>AUCUN</strong>.</td></tr><tr><td><strong>RENDU VISUEL > ANTICRÉNELAGE (MSAA)</strong></td><td>Lisse les contours des polygones (1 à 8).</td></tr><tr><td><strong>PILOTES > VIDÉO</strong></td><td><strong>OPENGL</strong> (par défaut), <strong>DIRECTX 11</strong> ou <strong>VULKAN</strong>.</td></tr><tr><td><strong>PILOTES > AUDIO</strong></td><td><strong>WASAPI</strong> (par défaut) ou <strong>SDL</strong>.</td></tr></tbody></table>

## Problèmes connus

<table><thead><tr><th width="340.25">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Ghostship indique que la ROM n'est pas prise en charge</td><td>Seules les versions américaine et japonaise sont acceptées, au format <code>.z64</code> : vérifiez le SHA-1 de la ROM (voir <strong>Quel format de jeu ?</strong>).</td></tr><tr><td>Le menu de Ghostship s'ouvre pendant la partie</td><td><strong>SELECT</strong> ouvre le menu : appuyez de nouveau sur <strong>SELECT</strong> pour le fermer.</td></tr><tr><td>Écran noir ou plantage au lancement</td><td>Changez de pilote vidéo avec <strong>PILOTES > VIDÉO</strong> (<strong>DIRECTX 11</strong> ou <strong>VULKAN</strong>).</td></tr><tr><td>Les décorations ne s'affichent pas</td><td>Réglez <strong>RAPPORT D'ASPECT</strong> sur <strong>NATIF (4:3)</strong>.</td></tr><tr><td>Un mod ne s'affiche pas</td><td>Vérifiez qu'il est dans <code>emulators\ghostship\mods</code> et qu'il est prévu pour la version de Ghostship livrée ; appuyez sur <strong>Tab</strong> pour activer les textures personnalisées.</td></tr></tbody></table>
