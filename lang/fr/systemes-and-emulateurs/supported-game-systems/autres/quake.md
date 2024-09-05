# Quake

<div align="left">

<figure><img src="https://github.com/fabricecaruso/es-theme-carbon/blob/master/art/logos/tyrquake.png?raw=true" alt=""><figcaption></figcaption></figure>

</div>

Moteur de jeu Quake 1

{% embed url="https://docs.libretro.com/library/tyrquake/" %}

## Informations

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Émulateurs</strong></td><td><ul><li>Libretro: tyrquake</li></ul></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> tyrquake</td></tr><tr><td><strong>Extension</strong></td><td>.pak</td></tr></tbody></table>

## Bios

Aucun BIOS nécessaire.

## Contrôles

Tyrquake permet de sélectionner 3 schémas de contrôles.

<table><thead><tr><th width="156">Retrobat</th><th>Classic</th><th>Classic Alt</th><th>Modern</th></tr></thead><tbody><tr><td>START</td><td>Menu</td><td>Menu</td><td>Menu</td></tr><tr><td>SELECT</td><td>Toggle Run Mode</td><td>Toggle Run Mode</td><td>Show scores</td></tr><tr><td>D-PAD</td><td>D-PAD</td><td>D-PAD</td><td>D-PAD</td></tr><tr><td>Stick gauche</td><td>X-axe : Strafe<br>Y-axe: d-pad haut/bas</td><td>X-axe : Strafe<br>Y-axe: d-pad haut/bas</td><td>X-axe : Strafe<br>Y-axe: d-pad haut/bas</td></tr><tr><td>Stick droit</td><td>X-axis : d-pad gauche et droite<br>Y-axis: Regarder en haut et en bas</td><td>X-axis : d-pad gauche et droite<br>Y-axis: Regarder en haut et en bas</td><td>Regarder</td></tr><tr><td><img src="../../../.gitbook/assets/image (33).png" alt=""></td><td>Tirer</td><td>Regarder à gauche</td><td>Nager vers le haut</td></tr><tr><td><img src="../../../.gitbook/assets/image (20).png" alt=""></td><td>Sauter</td><td>Regarder en bas</td><td>Nager vers le bas</td></tr><tr><td><img src="../../../.gitbook/assets/image (7).png" alt=""></td><td>Changer d'arme</td><td>Regarder à droite</td><td>Mitrailler à droite</td></tr><tr><td><img src="../../../.gitbook/assets/image (35).png" alt=""></td><td>Visualisation libre</td><td>Regarder en haut</td><td>Mitrailler à gauche</td></tr><tr><td>L1</td><td>Mitrailler à gauche</td><td>Sauter</td><td>Arme précédente</td></tr><tr><td>R1</td><td>Mitrailler à droite</td><td>Tirer</td><td>Arme suivante</td></tr><tr><td>L2</td><td>Regarder en haut</td><td>Courir</td><td>Sauter</td></tr><tr><td>R2</td><td>Regarder en bas</td><td>Arme suivante</td><td>Tirer</td></tr><tr><td>L3</td><td>Aller vers le bas</td><td>Nager vers le bas</td><td>Aller vers le bas</td></tr><tr><td>R3</td><td>Nager vers le haut</td><td>Arme précédente</td><td>Nager vers le haut</td></tr></tbody></table>

## Information spécifique au système

### Organisation des fichiers de jeu

Ci-dessous la structure recommandée pour l'organisation du dossier des jeux:

<pre><code>└── roms\
    └── tyrquake\
        ├── id1\
<strong>        │   └── pak0.pak
</strong><strong>        │   └── pak1.pak
</strong>        │   └── music\
        │       └── track02.ogg
        │       └── ...
        └── hipnotik\
        │   └── pak0.pak
        │   └── music\
        │       └── track02.ogg
        │       └── ...
        └── rogue\
<strong>        │   └── pak0.pak
</strong>        │   └── music\
        │       └── track02.ogg
        │       └── ...
        └── dopa\
            └── pak0.pak
</code></pre>
