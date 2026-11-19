# Bermuda Syndrome

<div align="left"><figure><img src="../../../.gitbook/assets/image (672).png" alt="" width="514"><figcaption></figcaption></figure></div>

## Présentation

**Bermuda Syndrome** (Century Interactive / BMG, 1995) est un jeu d'aventure et d'action en 2D : le pilote Jack Thompson s'écrase dans un monde de dinosaures, au cœur du triangle des Bermudes.

RetroBat utilise **Bermuda**, une réécriture libre du moteur du jeu.

Les fichiers du jeu ne sont pas fournis : utilisez ceux de votre propre exemplaire.

{% embed url="https://github.com/cyxx/bermuda" %}

## En bref

<table><thead><tr><th width="296.5"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\bsyndrome</code></td></tr><tr><td><strong>Extensions</strong></td><td>.game</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>bsyndrome</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (fichiers du jeu à fournir)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Non : clavier</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non : sauvegardes du jeu (touches S / L)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr><tr><td><strong>Pistolets</strong></td><td>—</td></tr><tr><td><strong>Volants</strong></td><td>—</td></tr><tr><td><strong>BIOS optionnels</strong></td><td>—</td></tr></tbody></table>

## BIOS

Aucun BIOS n'est nécessaire. Les musiques (fichiers `.ogg`) se placent dans `bios\bsyndrome\MUSIC`.

## Quel format de jeu ?

Un fichier `.game` vide placé dans `roms\bsyndrome` lance le jeu du dossier `roms\bsyndrome\DATA`.

## Contrôles

Le jeu se joue au clavier :

<table><thead><tr><th width="224">Touche</th><th>Action</th></tr></thead><tbody><tr><td>Flèches</td><td>Déplacer Jack</td></tr><tr><td>Tab</td><td>Afficher le sac</td></tr><tr><td>Ctrl</td><td>Afficher la barre d'état</td></tr><tr><td>Maj / Espace</td><td>Utiliser l'arme</td></tr><tr><td>Entrée</td><td>Passer les dialogues</td></tr><tr><td>C</td><td>Capture d'écran (<code>.tga</code>)</td></tr><tr><td>S</td><td>Sauvegarder</td></tr><tr><td>L</td><td>Charger une sauvegarde</td></tr><tr><td>+ / -</td><td>Emplacement de sauvegarde suivant / précédent</td></tr><tr><td>F</td><td>Mode rapide</td></tr><tr><td>W</td><td>Plein écran / fenêtre</td></tr></tbody></table>

### Raccourcis

| Raccourci      | Action  |
| -------------- | ------- |
| HOTKEY + START | Quitter |

## Dossiers

| Contenu        | Dossier                |
| -------------- | ---------------------- |
| Données du jeu | `roms\bsyndrome\DATA`  |
| Musiques       | `bios\bsyndrome\MUSIC` |
| Sauvegardes    | `saves\bsyndrome`      |

## Guides

### Organisation des fichiers

```
roms\bsyndrome\
├── DATA\                    (fichiers du dossier BERMUDA du jeu)
│   ├── (sous-dossiers)
│   ├── BERMUDA.OVR
│   ├── BERMUDA.SPR
│   └── BERMUDA.WGP
└── Bermuda Syndrome.game    (fichier vide)

bios\bsyndrome\
└── MUSIC\                   (fichiers .ogg)
```

**RAPPORT D'ASPECT** passe l'image en 4/3 ou 16/9.

## Problèmes connus

<table><thead><tr><th width="300.25">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>« DATA folder not found in roms\bsyndrome\DATA. »</td><td>Copiez les fichiers du dossier <code>BERMUDA</code> du jeu dans <code>roms\bsyndrome\DATA</code>.</td></tr></tbody></table>
