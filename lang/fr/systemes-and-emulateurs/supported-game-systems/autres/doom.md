# Doom

<div align="left"><figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/52ff37c9e265587d006945a2ba695b5a962b3a3d/art/logos/prboom.svg" alt=""><figcaption></figcaption></figure></div>

Moteur de jeu permettant de jouer la plupart des jeux utilisant le moteur de jeu Doom.

{% embed url="https://github.com/UZDoom/uzdoom" %}

{% embed url="https://zdoom.org/index" %}

## Informations

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Émulateur</strong></td><td><ul><li>uzdoom</li><li>gzdoom</li><li>libretro: prboom</li></ul></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> doom</td></tr><tr><td><strong>Extensions</strong></td><td>.wad .iwad .pwad .pk3 .ipk3 .gzdoom .uzdoom</td></tr></tbody></table>

## Bios

Aucun BIOS nécessaire.

## Contrôles

Les contrôles sont à configurer directement dans l'émulateur.

### PRBoom

| Retrobat                                           | Classic                     | Modern                                                      |
| -------------------------------------------------- | --------------------------- | ----------------------------------------------------------- |
| START                                              | Afficher / masquer le menu  | Afficher / masquer le menu                                  |
| SELECT                                             | Afficher / masquer la carte | Afficher / masquer la carte                                 |
| D-PAD                                              | D-PAD                       | D-PAD                                                       |
| Left analog stick                                  |                             | <p>X-axe: déplacement latéral<br>Y-axe: Avancer/reculer</p> |
| Right analog stick                                 |                             | X-axe: regarder à gauche et droite                          |
| ![](<../../../.gitbook/assets/image (33).png>)     | Courir                      | Sauvegarde rapide                                           |
| ![](<../../../.gitbook/assets/image (20) (1).png>) | Utiliser                    | Menu : annuler                                              |
| ![](<../../../.gitbook/assets/image (7) (1).png>)  | Tirer                       | Menu : sélectionner                                         |
| ![](<../../../.gitbook/assets/image (35).png>)     | Mitrailler                  | Chargement rapide                                           |
| L1                                                 | Mitrailler à gauche         | Arme précédente                                             |
| R1                                                 | Mitrailler à droite         | Arme suivante                                               |
| L2                                                 | Arme précédente             | Utiliser                                                    |
| R2                                                 | Arme suivante               | Tirer                                                       |
| L3                                                 |                             | Courir                                                      |
| R3                                                 |                             | Se retourner (180°)                                         |

## Information spécifique au système

### Jeux pris en charge

Les listes des jeux compatibles avec UZDoom et GZDoom sont disponibles ici:

{% embed url="https://zdoom.org/wiki/IWAD" %}

### Modifier les lignes de commande de lancement

RetroBat vous permet de lancer un jeu avec une ligne de commande personnalisée.

Pour cela, créer un fichier .txt et spécifier un argument par ligne:

<div align="left"><figure><img src="https://i.imgur.com/hr7OEao.png" alt=""><figcaption></figcaption></figure></div>

Sauver le fichier avec l'extension ".uzdoom" ou ".gzdoom" et placer le dans le dossier `roms\doom`.

### Lancer des mods

La méthode ci-dessus permet également de démarrer des "mods" du jeu.&#x20;

Pour cela, indiquer sur quel jeu principal (iwad) le mod est basé, puis le mod à lancer, en précisant les chemins vers chacun des fichiers.\
\
Un exemple, avec le mod "10 sectors" :\
\
![](<../../../.gitbook/assets/image (38).png>)\
\
Il ne reste plus qu'à démarrer le jeu en sélectionnant le jeu `"10sector.gzdoom"` depuis RetroBat.

### Organisation des fichiers de jeux (PRBoom)

PrBoom fonctionne avec des fichiers wad, iwad et pwad.&#x20;

Les fichiers WAD et IWAD sont les fichiers utilisés pour lancer les jeux ("`Internal Where's All the Data`").

Les fichiers PWAD sont des patchs, ils nécessitent la présence du fichier WAD/IWAD pour fonctionner.

Ci-dessous la structure recommandée pour l'organisation du dossier `\roms\doom`:

<pre><code>└── roms\
    └── doom\
        ├── doom\
<strong>        │   └── doom.wad
</strong>        └── doom 2\
        │   └── doom2.wad
        └── Doom Ultimate\
        │   └── doomu.wad
</code></pre>

Pour utiliser des fichiers pwad, il est nécessaire de les placer au sein de leur propre sous-dossier dans le dossier du jeu principal :

<pre><code>└── roms\
    └── doom\
        ├── doom\
<strong>        │   └── doom.wad
</strong>        │   └── Episode 5 - Sigil\
        │           └── SIGIL.pwad
        └── Doom 2\
            └── doom2.wad
            └── Goldeneye\
                    └── goldeneye.pwad        
</code></pre>
