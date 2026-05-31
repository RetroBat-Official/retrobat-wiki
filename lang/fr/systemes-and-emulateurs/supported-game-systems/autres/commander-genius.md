# Commander Genius

<div align="left"><figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/421cec038116fe7b6711fa35683470884a28ed55/art/logos/cgenius.svg" alt=""><figcaption></figcaption></figure></div>

Moteur de jeu permettant de jouer à Commander Keen.

{% embed url="https://clonekeenplus.sourceforge.io/" %}

## Information

<table data-header-hidden><thead><tr><th width="297"></th><th></th></tr></thead><tbody><tr><td><strong>Émulateur</strong></td><td><ul><li>cgenius</li></ul></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> cgenius</td></tr><tr><td><strong>Extensions</strong></td><td>.cgenius</td></tr><tr><td><strong>Emplacement des sauvegardes</strong></td><td><em>emulators\cgenius\save</em><br>Copié dans <em>saves\cgenius</em></td></tr></tbody></table>

## BIOS

Aucun BIOS nécessaire.

## Contrôles

<table><thead><tr><th width="246">Retrobat</th><th>Commander Keen</th></tr></thead><tbody><tr><td>START</td><td>Aide</td></tr><tr><td>SELECT</td><td>Retour</td></tr><tr><td>D-PAD</td><td>Directions</td></tr><tr><td><img src="../../../.gitbook/assets/image (33).png" alt=""></td><td>Courir</td></tr><tr><td><img src="../../../.gitbook/assets/image (20) (1).png" alt=""></td><td>Sauter</td></tr><tr><td><img src="../../../.gitbook/assets/image (7) (1) (1).png" alt=""></td><td>Tirer</td></tr><tr><td><img src="../../../.gitbook/assets/image (35).png" alt=""></td><td>Pogo</td></tr><tr><td>L1</td><td>Statut</td></tr><tr><td>R1</td><td>Camlead</td></tr><tr><td>Hotkey + <img src="../../../.gitbook/assets/image (33).png" alt=""></td><td>Sauvegarde rapide</td></tr><tr><td>Hotkey + <img src="../../../.gitbook/assets/image (35).png" alt=""></td><td>Chargement rapide</td></tr></tbody></table>

## Information spécifique au système

### Fichiers de configuration

RetroBat utilise par défaut le fichier de configuration cgenius.cfg situé dans le dossier `\emulators\cgenius\` de l'installation RetroBat.

Cependant, si vous utilisiez précédemment cgenius en dehors de RetroBat, il est possible que des fichiers cgenius soient localisées dans votre dossier "Documents". Si tel est le cas, RetroBat ne fonctionnera pas correctement, car cgenius priorisera ces fichiers et non ceux fournis avec RetroBat.

Pour corriger ce problème, il suffit simplement de supprimer les fichiers existants dans votre dossier "Documents".

### Organisation des fichiers de jeux

Les jeux doivent être copiés dans lesous-dossier "**games**" du dossier `roms\cgenius`.

Pour que RetroBat détecte le jeu, ajouter un fichier texte dans le dossier du jeu et remplacer l'extension par ".cgenius".

Exemple d'organisation de dossier:

```
└── roms\
    └── cgenius\
        └── games\
            ├── keen1\
            │   └── ...
            │   └── Commander Keen.cgenius
            └── keen2\
            │   └── ...
            │   └── Commander Keen 2.cgenius
            └── keen7\
            │   └── ...
            │   └── Commander Keen 7.cgeni
```

### Ajout de jeux

Les jeux peuvent être ajoutés depuis l'émulateur:

#### **Démarrer l'exécutable cgenius.exe dans le dossier emulators\cgenius :**

<div align="left"><figure><img src="https://i.imgur.com/AzAGLU1.png" alt="" width="375"><figcaption></figcaption></figure></div>

#### Cliquer "+ MORE":

<div align="left"><figure><img src="https://i.imgur.com/kytdlOg.png" alt="" width="375"><figcaption></figcaption></figure></div>

#### Sélectionner le jeu à télécharger et cliquer sur "download"

Le jeu est téléchargé dans le dossier emulators\cgenius\games:

<div align="left"><figure><img src="https://i.imgur.com/ZZdiAKJ.png" alt=""><figcaption></figcaption></figure></div>

#### Copier/coller le dernier dossier (KeenDreams dans l'exemple) vers le dossier roms\cgenius\games:

<div align="left"><figure><img src="https://i.imgur.com/tqAORuQ.png" alt=""><figcaption></figcaption></figure></div>

#### Créer un fichier .cgenius dans le dossier du jeu:

<div align="left"><figure><img src="https://i.imgur.com/DYoPbqt.png" alt=""><figcaption></figcaption></figure></div>
