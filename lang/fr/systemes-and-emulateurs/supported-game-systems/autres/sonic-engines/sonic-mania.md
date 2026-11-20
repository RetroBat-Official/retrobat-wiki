# Sonic Mania

<div align="left"><figure><img src="../../../../.gitbook/assets/image (693).png" alt="" width="269"><figcaption></figcaption></figure></div>

## Présentation

**Sonic Mania** (Sega, 2017) est un Sonic en 2D développé par Christian Whitehead, Headcannon et PagodaWest Games, dans l'esprit des épisodes Mega Drive. RetroBat le lance avec **RSDKv5U**, la version PC du moteur Retro Engine issue de la décompilation du jeu (projet RSDKModding).

Le jeu n'est pas fourni : il faut le fichier de données `Data.rsdk` de votre propre version du jeu.

{% embed url="https://github.com/Rubberduckycooly/Sonic-Mania-Decompilation" %}

## En bref

<table><thead><tr><th width="292.75"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\sonic-mania</code></td></tr><tr><td><strong>Extensions</strong></td><td>.rsdk</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>sonicmania</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (<code>Data.rsdk</code> du jeu à fournir)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Gérée par le jeu</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non (sauvegardes du jeu)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr></tbody></table>

## BIOS

Aucun BIOS n'est nécessaire.

## Quel format de jeu ?

Le fichier **Data.rsdk** de Sonic Mania (version PC, Steam ou Epic Games Store, avec ou sans Sonic Mania Plus). Copiez-le dans `roms\sonic-mania` :

```
roms\
└── sonic-mania\
    └── Data.rsdk
```

<div align="left"><figure><img src="../../../../.gitbook/assets/image (694).png" alt=""><figcaption></figcaption></figure></div>

## Contrôles

La manette est reconnue directement par le moteur : RetroBat ne la configure pas. Croix ou stick gauche = déplacement, boutons de façade = saut, START = pause.

### Raccourcis

<table><thead><tr><th width="194">Action</th><th>Manette</th></tr></thead><tbody><tr><td>Quitter</td><td>HOTKEY + START</td></tr></tbody></table>

Pas de sauvegardes instantanées : la progression est enregistrée par le jeu.

## Dossiers

<table><thead><tr><th width="277.75">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Sauvegardes du jeu</td><td><code>roms\sonic-mania</code> (<code>SaveData.bin</code>, <code>Achievements.bin</code>), copiées par RetroBat dans <code>saves\sonicmania</code></td></tr><tr><td>Réglages (écrits par RetroBat)</td><td><code>roms\sonic-mania\Settings.ini</code></td></tr><tr><td>Mods</td><td><code>roms\sonic-mania\mods</code></td></tr></tbody></table>

## Guides

### Mods

Les mods prévus pour la décompilation (RSDKv5) se placent dans `roms\sonic-mania\mods`, un dossier par mod, avec un fichier `mod.ini` dedans :

```
roms\
└── sonic-mania\
    ├── Data.rsdk
    └── mods\
        └── MonMod\
            └── mod.ini
```

Avec **ÉMULATION > ACTIVER LES MODS** (activé par défaut), RetroBat active tous les mods du dossier ; désactivé, le jeu se lance sans mods. Pour ne pas charger un mod, sortez son dossier de `mods`. Les mods sont chargés dans l'ordre du fichier `mods\modconfig.ini` ; les nouveaux mods sont ajoutés à la fin.

Les mods faits pour la version Steam d'origine (Mania Mod Loader) ne fonctionnent pas avec ce moteur.

### Options utiles

<table><thead><tr><th width="259">Option</th><th>Effet</th></tr></thead><tbody><tr><td><strong>ÉMULATION > LANGUE</strong></td><td>Langue du jeu.</td></tr><tr><td><strong>SHADERS</strong></td><td>Filtre d'image (net, CRT).</td></tr></tbody></table>

## Problèmes connus

<table><thead><tr><th width="269">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Le jeu ne démarre pas</td><td>Vérifiez que <code>Data.rsdk</code> est bien dans <code>roms\sonic-mania</code>.</td></tr><tr><td>Un mod n'est pas chargé</td><td>Vérifiez qu'il a un <code>mod.ini</code> dans son dossier, qu'il est fait pour la décompilation (RSDKv5) et que <strong>ACTIVER LES MODS</strong> n'est pas désactivé.</td></tr></tbody></table>
