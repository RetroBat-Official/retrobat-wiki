# PrBoom

<div align="left">

<figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/52ff37c9e265587d006945a2ba695b5a962b3a3d/art/logos/prboom.svg" alt=""><figcaption></figcaption></figure>

</div>

Moteur de jeu permettant de jouer à Doom, Doom II, Doom Ultimate, Final Doom et d'autres mods.

{% embed url="https://docs.libretro.com/library/prboom/" %}

## Informations

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Émulateur</strong></td><td><ul><li>Libretro : prboom</li></ul></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> prboom</td></tr><tr><td><strong>Extensions</strong></td><td>.wad .iwad .pwad</td></tr></tbody></table>

## Bios

Aucun BIOS nécessaire.

## Contrôles

PrBoom permet de sélectionner 2 schémas de contrôles.

| Retrobat                                       | Classic                     | Modern                                                      |
| ---------------------------------------------- | --------------------------- | ----------------------------------------------------------- |
| START                                          | Afficher / masquer le menu  | Afficher / masquer le menu                                  |
| SELECT                                         | Afficher / masquer la carte | Afficher / masquer la carte                                 |
| D-PAD                                          | D-PAD                       | D-PAD                                                       |
| Left analog stick                              |                             | <p>X-axe: déplacement latéral<br>Y-axe: Avancer/reculer</p> |
| Right analog stick                             |                             | X-axe: regarder à gauche et droite                          |
| ![](<../../../.gitbook/assets/image (32).png>) | Courir                      | Sauvegarde rapide                                           |
| ![](<../../../.gitbook/assets/image (19).png>) | Utiliser                    | Menu : annuler                                              |
| ![](<../../../.gitbook/assets/image (6).png>)  | Tirer                       | Menu : sélectionner                                         |
| ![](<../../../.gitbook/assets/image (34).png>) | Mitrailler                  | Chargement rapide                                           |
| L1                                             | Mitrailler à gauche         | Arme précédente                                             |
| R1                                             | Mitrailler à droite         | Arme suivante                                               |
| L2                                             | Arme précédente             | Utiliser                                                    |
| R2                                             | Arme suivante               | Tirer                                                       |
| L3                                             |                             | Courir                                                      |
| R3                                             |                             | Se retourner (180°)                                         |

## Information spécifique au système

### Organisation des fichiers de jeux

PrBoom fonctionne avec des fichiers wad, iwad et pwad.&#x20;

Les fichiers WAD et IWAD sont les fichiers utilisés pour lancer les jeux ("`Internal Where's All the Data`").

Les fichiers PWAD sont des patchs, ils nécessitent la présence du fichier WAD/IWAD pour fonctionner.

Ci-dessous la structure recommandée pour l'organisation du dossier `\roms\prboom` :

<pre><code>└── roms\
    └── prboom\
        ├── doom\
<strong>        │   └── doom.wad
</strong>        └── doom 2\
        │   └── doom2.wad
        └── Doom Ultimate\
        │   └── doomu.wad
</code></pre>

Pour utiliser des fichiers pwad, il est nécessaire de les placer au sein de leur propre sous-dossier dans le dossier du jeu principal :

<pre><code>└── roms\
    └── prboom\
        ├── doom\
<strong>        │   └── doom.wad
</strong>        │   └── Episode 5 - Sigil\
        │           └── SIGIL.pwad
        └── Doom 2\
            └── doom2.wad
            └── Goldeneye\
                    └── goldeneye.pwad        
</code></pre>
