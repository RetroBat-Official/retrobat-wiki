# Sonic Retro

<div align="left"><figure><img src="../../../../.gitbook/assets/image (691).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Présentation

Ce système lance les versions remasterisées de **Sonic the Hedgehog** (1991), **Sonic the Hedgehog 2** (1992) et **Sonic CD** (1993), sorties sur mobiles puis sur PC (Sonic CD en 2011, Sonic 1 et 2 en 2013, puis dans **Sonic Origins** en 2022). Elles tournent sur le Retro Engine de Christian Whitehead ; RetroBat utilise les décompilations du projet RSDKModding :

* **RSDKv4** (émulateur `sonicretro`) pour Sonic 1 et Sonic 2 ;
* **RSDKv3** (émulateur `sonicretrocd`) pour Sonic CD.

Les jeux ne sont pas fournis : il faut le fichier de données `Data.rsdk` de votre propre version de chaque jeu.

{% embed url="https://github.com/Rubberduckycooly/Sonic-1-2-2013-Decompilation" %}

{% embed url="https://github.com/Rubberduckycooly/Sonic-CD-11-Decompilation" %}

## En bref

<table><thead><tr><th width="276.5"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\sonicretro</code></td></tr><tr><td><strong>Extensions</strong></td><td>.rsdk</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>sonicretro (sonicretrocd pour Sonic CD, choisi automatiquement)</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (<code>Data.rsdk</code> de chaque jeu à fournir)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Gérée par le jeu</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non (sauvegardes du jeu)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="217.75">Émulateur</th><th>Jeux</th></tr></thead><tbody><tr><td><strong>sonicretro</strong> (RSDKv4)</td><td>Sonic the Hedgehog, Sonic the Hedgehog 2</td></tr><tr><td><strong>sonicretrocd</strong> (RSDKv3)</td><td>Sonic CD</td></tr></tbody></table>

RetroBat lance Sonic CD avec sonicretrocd quand le dossier du jeu s'appelle `soniccd` (majuscules et espaces ignorés : `SonicCD`, `Sonic CD` conviennent). Sinon, activez **ÉMULATION > FORCER SONIC CD**.

## BIOS

Aucun BIOS n'est nécessaire.

## Quel format de jeu ?

Un dossier par jeu dans `roms\sonicretro`, avec le fichier **Data.rsdk** du jeu dedans :

```
roms\
└── sonicretro\
    ├── sonic1\
    │   └── Data.rsdk
    ├── sonic2\
    │   └── Data.rsdk
    └── soniccd\
        └── Data.rsdk
```

D'où viennent les fichiers :

* Sonic 1 et Sonic 2 : versions mobiles (iOS, Android) ou Sonic Origins (Steam, Epic Games Store) ;
* Sonic CD : version Steam de 2011, versions mobiles ou Sonic Origins.

Avec des données de **Sonic Origins**, choisissez **ÉMULATION > TYPE DE JEU > VERSION ORIGINS**.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (692).png" alt=""><figcaption></figcaption></figure></div>

## Contrôles

La manette est reconnue directement par le moteur : RetroBat ne la configure pas. Croix ou stick gauche = déplacement, boutons de façade = saut, START = pause.

### Raccourcis

<table><thead><tr><th width="196.5">Action</th><th>Manette</th></tr></thead><tbody><tr><td>Quitter</td><td>HOTKEY + START</td></tr></tbody></table>

Pas de sauvegardes instantanées : la progression est enregistrée par le jeu.

## Dossiers

<table><thead><tr><th width="272.75">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Sauvegardes du jeu</td><td>dossier du jeu (<code>SData.bin</code>), copiées par RetroBat dans <code>saves\sonicretro\&#x3C;dossier du jeu></code></td></tr><tr><td>Réglages (écrits par RetroBat)</td><td>dossier du jeu (<code>Settings.ini</code>)</td></tr><tr><td>Mods</td><td>dossier du jeu, sous-dossier <code>mods</code></td></tr></tbody></table>

## Guides

### Mods

Les mods prévus pour les décompilations (RSDKv4 pour Sonic 1 et 2, RSDKv3 pour Sonic CD) se placent dans le dossier `mods` du jeu, un dossier par mod, avec un fichier `mod.ini` dedans :

```
roms\
└── sonicretro\
    └── sonic2\
        ├── Data.rsdk
        └── mods\
            └── MonMod\
                └── mod.ini
```

Avec **ÉMULATION > ACTIVER LES MODS** (activé par défaut), RetroBat active tous les mods du dossier ; désactivé, le jeu se lance sans mods. Pour ne pas charger un mod, sortez son dossier de `mods`. Les mods sont chargés dans l'ordre du fichier `mods\modconfig.ini` ; les nouveaux mods sont ajoutés à la fin.

Un mod qui a ses propres sauvegardes les garde dans son dossier : RetroBat ne les copie pas dans `saves`.

### Options utiles

<table><thead><tr><th width="266.5">Option</th><th>Effet</th></tr></thead><tbody><tr><td><strong>ÉMULATION > LANGUE</strong></td><td>Langue du jeu (Sonic CD : anglais, français, italien, allemand, espagnol, japonais).</td></tr><tr><td><strong>ÉMULATION > TYPE DE JEU</strong></td><td><strong>VERSION ORIGINS</strong> pour les données de Sonic Origins.</td></tr></tbody></table>

## Problèmes connus

<table><thead><tr><th width="255.25">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Sonic CD ne démarre pas</td><td>Nommez son dossier <code>soniccd</code>, ou activez <strong>FORCER SONIC CD</strong>.</td></tr><tr><td>Le jeu ne démarre pas</td><td>Vérifiez que le dossier du jeu contient bien <code>Data.rsdk</code>.</td></tr><tr><td>Un mod n'est pas chargé</td><td>Vérifiez qu'il a un <code>mod.ini</code> dans son dossier, qu'il est fait pour le bon moteur (RSDKv4 ou RSDKv3) et que <strong>ACTIVER LES MODS</strong> n'est pas désactivé.</td></tr></tbody></table>
