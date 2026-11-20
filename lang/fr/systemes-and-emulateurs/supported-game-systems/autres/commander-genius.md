# Commander Genius

<div align="left"><figure><img src="../../../.gitbook/assets/image (683).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Présentation

**Commander Keen** (id Software / Apogee, 1990-1991) est une série de jeux de plates-formes sur PC. **Commander Genius** est un moteur moderne qui lance les épisodes 1 à 6, **Keen Dreams** et des jeux de fans.

Commander Genius ajoute la haute résolution, des filtres d'image, le jeu à la manette et la sauvegarde rapide.

Des jeux (Keen Dreams, jeux de fans…) se téléchargent depuis Commander Genius ; les épisodes de la série viennent de vos propres exemplaires.

{% embed url="https://clonekeenplus.sourceforge.io/" %}

## En bref

<table><thead><tr><th width="284"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\cgenius\games</code></td></tr><tr><td><strong>Extensions</strong></td><td>.cgenius</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>cgenius</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non : sauvegarde / chargement rapide aux raccourcis</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr><tr><td><strong>Pistolets</strong></td><td>—</td></tr><tr><td><strong>Volants</strong></td><td>—</td></tr><tr><td><strong>BIOS optionnels</strong></td><td>—</td></tr></tbody></table>

## Quel format de jeu ?

Chaque jeu est un dossier de `roms\cgenius\games`. Un fichier vide `.cgenius` placé dans le dossier du jeu le lance directement.

```
roms\cgenius\
└── games\
    ├── keen1\
    │   ├── ...
    │   └── Commander Keen.cgenius
    ├── keen2\
    │   ├── ...
    │   └── Commander Keen 2.cgenius
    └── keen7\
        ├── ...
        └── Commander Keen 7.cgenius
```

## Contrôles

### Configuration automatique

<table><thead><tr><th width="192.75">Manette RetroBat</th><th>Commander Keen</th></tr></thead><tbody><tr><td>Croix</td><td>Directions</td></tr><tr><td>SUD</td><td>Sauter</td></tr><tr><td>EST</td><td>Tirer</td></tr><tr><td>OUEST</td><td>Courir</td></tr><tr><td>NORD</td><td>Pogo</td></tr><tr><td>L1</td><td>Statut</td></tr><tr><td>R1</td><td>Caméra (Camlead)</td></tr><tr><td>START</td><td>Aide</td></tr><tr><td>SELECT</td><td>Retour</td></tr></tbody></table>

**CONTRÔLES > TIR DOUBLE (2 BOUTONS)**, **SUPER POGO**, **POGO IMPOSSIBLE** et **TIR AUTOMATIQUE** modifient le jeu.

### Raccourcis

<table><thead><tr><th width="225.25">Raccourci</th><th>Action</th></tr></thead><tbody><tr><td>HOTKEY + START</td><td>Quitter</td></tr><tr><td>HOTKEY + OUEST</td><td>Sauvegarde rapide</td></tr><tr><td>HOTKEY + NORD</td><td>Chargement rapide</td></tr></tbody></table>

## Dossiers

<table><thead><tr><th width="192.75">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Jeux</td><td><code>roms\cgenius\games</code></td></tr><tr><td>Sauvegardes</td><td><code>emulators\cgenius\save</code> (copiées dans <code>saves\cgenius</code>)</td></tr><tr><td>Configuration</td><td><code>emulators\cgenius\cgenius.cfg</code></td></tr></tbody></table>

{% hint style="info" %}
Si Commander Genius a été utilisé en dehors de RetroBat, son fichier `Documents\Commander Genius\cgenius.cfg` serait prioritaire : RetroBat le renomme pendant la partie, puis le remet en place.
{% endhint %}

## Guides

### Télécharger des jeux depuis Commander Genius

1. Lancez `CGenius.exe` dans `emulators\cgenius` :

<div align="left"><figure><img src="../../../.gitbook/assets/image (684).png" alt="" width="375"><figcaption></figcaption></figure></div>

2. Cliquez sur **+ MORE** :

<div align="left"><figure><img src="../../../.gitbook/assets/image (685).png" alt="" width="375"><figcaption></figcaption></figure></div>

3. Choisissez le jeu et cliquez sur **Download**. Le jeu est téléchargé dans `emulators\cgenius\games` :

<div align="left"><figure><img src="../../../.gitbook/assets/image (686).png" alt=""><figcaption></figcaption></figure></div>

4. Copiez le dossier du jeu (KeenDreams dans l'exemple) dans `roms\cgenius\games` :

<div align="left"><figure><img src="../../../.gitbook/assets/image (687).png" alt=""><figcaption></figcaption></figure></div>

5. Créez un fichier `.cgenius` dans le dossier du jeu :

<div align="left"><figure><img src="../../../.gitbook/assets/image (688).png" alt=""><figcaption></figcaption></figure></div>

### Options

* **SHADERS** (SCALE2X à SCALE4X) lisse l'image, **RÉSOLUTION INTERNE DU JEU** élargit la vue.
* Le cadre décoratif s'affiche seulement avec le **RAPPORT D'ASPECT** 4/3.

## Problèmes connus

<table><thead><tr><th width="305.25">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Le jeu ne démarre pas directement</td><td>Le jeu doit être dans un sous-dossier de <code>roms\cgenius\games</code>.</td></tr></tbody></table>
