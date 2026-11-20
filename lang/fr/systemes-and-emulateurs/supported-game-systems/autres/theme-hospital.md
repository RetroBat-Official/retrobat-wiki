---
description: Corsixth
---

# Theme Hospital

<div align="left"><figure><img src="../../../.gitbook/assets/image (689).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Présentation

**Theme Hospital** (Bullfrog, 1997) est un jeu de gestion : construire et faire tourner un hôpital, soigner des maladies imaginaires et garder les patients satisfaits.

RetroBat utilise **CorsixTH**, une version libre du moteur : haute résolution, corrections, nombreuses langues.

Les fichiers du jeu ne sont pas fournis : utilisez ceux de votre propre exemplaire (CD, GOG).

{% embed url="https://corsixth.com/" %}

## En bref

<table><thead><tr><th width="299"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\corsixth</code></td></tr><tr><td><strong>Extensions</strong></td><td>.game</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>corsixth</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (fichiers du jeu à fournir)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique (manette transformée en souris et clavier)</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non : sauvegardes du jeu</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr><tr><td><strong>Pistolets</strong></td><td>—</td></tr><tr><td><strong>Volants</strong></td><td>—</td></tr><tr><td><strong>BIOS optionnels</strong></td><td>—</td></tr></tbody></table>

## BIOS

Aucun BIOS n'est nécessaire. Il faut le contenu du dossier `HOSP` du jeu.

## Quel format de jeu ?

Le jeu est un dossier `.game` qui contient les fichiers du dossier `HOSP`.

<div align="left"><figure><img src="../../../.gitbook/assets/image (690).png" alt=""><figcaption></figcaption></figure></div>

## Contrôles

Theme Hospital se joue à la souris et au clavier. RetroBat transforme la manette du joueur 1 en souris et en touches du clavier (fichier `system\padtokey\corsixth.keys`) :

<table><thead><tr><th width="251.5">Manette RetroBat</th><th>Action</th></tr></thead><tbody><tr><td>Stick gauche</td><td>Déplacer le pointeur</td></tr><tr><td>SUD</td><td>Clic gauche</td></tr><tr><td>EST</td><td>Clic droit</td></tr><tr><td>NORD</td><td>Tourner l'objet (Espace)</td></tr><tr><td>OUEST</td><td>Échap</td></tr><tr><td>Croix</td><td>Faire défiler la carte</td></tr><tr><td>L1 / R1</td><td>Zoom arrière / avant</td></tr><tr><td>L2 (maintenu)</td><td>Murs transparents</td></tr><tr><td>R2 (maintenu)</td><td>Accélérer le temps</td></tr><tr><td>START</td><td>Pause</td></tr></tbody></table>

**CONTRÔLES > VEROUILLER LA SOURIS** (activé par défaut) garde la souris dans la fenêtre du jeu.

{% hint style="info" %}
Pour la manette, le zoom, les murs transparents et l'accélération passent sur le pavé numérique (`-`, `+`, `/`, `*`) au lieu de `-`, `=`, `x` et `z`. Avec **AUTOCONFIGURER LES MANETTES** désactivé, les touches d'origine du jeu sont remises.
{% endhint %}

### Raccourcis

<table><thead><tr><th width="240.25">Raccourci</th><th>Action</th></tr></thead><tbody><tr><td>HOTKEY + START</td><td>Quitter</td></tr></tbody></table>

## Dossiers

<table><thead><tr><th width="220.25">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Jeu</td><td><code>roms\corsixth\&#x3C;jeu>.game</code></td></tr><tr><td>Sauvegardes</td><td><code>saves\corsixth</code></td></tr><tr><td>Captures d'écran</td><td><code>screenshots\corsixth</code></td></tr><tr><td>Configuration</td><td><code>emulators\corsixth\config.txt</code>, <code>emulators\corsixth\hotkeys.txt</code></td></tr></tbody></table>

## Guides

### Organisation des fichiers

Copiez le contenu du dossier `HOSP` (CD d'origine ou version GOG) dans un dossier de `roms\corsixth`, puis ajoutez `.game` à la fin du nom du dossier :

### Options

* **RÉSOLUTION INTERNE DU JEU** : une résolution plus grande montre une plus grande partie de l'hôpital.
* **INTERFACE UTILISATEUR > ÉCHELLE DE L'INTERFACE** agrandit les menus et les panneaux.
* **ÉMULATION > LANGUE** : par défaut, la langue d'EmulationStation.
