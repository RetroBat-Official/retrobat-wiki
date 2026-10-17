---
description: >-
  Portages PC natifs de jeux console : recompilations, décompilations et autres
  portages communautaires
---

# Recompilations

<div align="left"><figure><img src="../../../.gitbook/assets/image (202).png" alt="" width="375"><figcaption></figcaption></figure></div>

Les portages recompilés et décompilés sont des jeux console reconstruits en programmes Windows natifs (Majora's Mask, Banjo-Kazooie, Star Fox 64, Sonic Unleashed…). Aucun émulateur n'intervient : RetroBat lance directement l'exécutable du portage et attend sa fermeture.

RetroBat ne fournit pas ces portages. Ils s'installent avec **Quiver Launcher**, ou se téléchargent à la main depuis la page officielle de chaque projet. Chaque portage a ses propres instructions pour fournir les données du jeu original (ROM, ISO ou fichiers du jeu).

Ce système peut contenir :

* des jeux installés avec Quiver Launcher (raccourcis `.lnk`),
* des portages de décompilation avec un fichier `.decomp` (dans le sous-dossier roms\ du système original du jeu décompilé ou recompilé).

## Information

<table data-header-hidden><thead><tr><th width="240"></th><th></th></tr></thead><tbody><tr><td><strong>Émulateurs</strong></td><td><ul><li>quiverlauncher</li></ul></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> recomp</td></tr><tr><td><strong>Extensions</strong></td><td>.lnk</td></tr></tbody></table>

## Contrôles

RetroBat ne configure pas automatiquement les manettes pour ces portages. Configurez les contrôles dans chaque portage.

**HOTKEY + START** ferme le jeu lancé depuis RetroBat et revient dans RetroBat. Dans Quiver Launcher, ce raccourci ferme le lanceur.

{% hint style="info" %}
Un jeu lancé depuis Quiver Launcher doit être fermé depuis son propre menu. Laissez désactivée l'option **Close to tray** de Quiver Launcher, sinon la fermeture du lanceur le cache seulement et RetroBat continue d'attendre.
{% endhint %}

## Information spécifique au système

### Quiver Launcher

Quiver Launcher télécharge, installe et met à jour des portages communautaires à partir de leurs publications GitHub et GitLab.

{% embed url="https://github.com/tgeorgiadis/quiver-launcher" %}

#### Ouvrir Quiver Launcher

* Depuis les entrées du menu RetroBat, sélectionnez **Quiver Launcher**. RetroBat le télécharge à la première utilisation.
* Ou activez **RUN LAUNCHER** dans les options avancées d'un jeu de ce système : le lanceur s'ouvre à la place du jeu.

<div align="left"><figure><img src="../../../.gitbook/assets/image (203).png" alt=""><figcaption><p>Démarrer QuiverLauncher depuis le menu RetroBat...</p></figcaption></figure></div>

<div align="left"><figure><img src="../../../.gitbook/assets/image (204).png" alt=""><figcaption><p>... ou activer DEMARRER LE LAUNCHER depuis les options avancées du système ou du jeu.</p></figcaption></figure></div>

RetroBat ouvre Quiver Launcher en plein écran (sauf si RetroBat est en mode fenêtré), avec la navigation à la manette activée. Les statistiques d'utilisation sont désactivées par défaut.

#### Ajouter des jeux

1. Ouvrez Quiver Launcher et installez les jeux souhaités.
2. Suivez les instructions de chaque jeu pour fournir les données du jeu original.
3. Ajoutez les jeux dans RetroBat, automatiquement ou à la main :
   * **Automatiquement** : activez **MENU PRINCIPAL > PARAMÈTRES DES JEUX > SCAN RECOMPILATION (QUIVERLAUNCHER)**. À chaque démarrage, RetroBat crée un raccourci dans `roms\recomp` pour chaque jeu installé dans Quiver Launcher.
   * **À la main** : dans Quiver Launcher, créez un raccourci sur le bureau pour le jeu, puis déplacez ce raccourci du bureau vers `roms\recomp`.
4. Rafraîchissez la liste des jeux ou redémarrez RetroBat.

{% hint style="info" %}
Si le dossier d'un jeu contient plusieurs exécutables, choisissez d'abord l'exécutable à utiliser dans Quiver Launcher. Tant que ce n'est pas fait, le scan automatique ignore ce jeu.
{% endhint %}

#### Ce que fait RetroBat au lancement d'un jeu Quiver

* Le jeu est lancé directement, sans ouvrir Quiver Launcher.
* Le mode plein écran ou fenêtré suit les réglages de RetroBat.
* Le jeu enregistre sa configuration et ses sauvegardes dans son propre dossier (`emulators\quiverlauncher\Apps\<jeu>`), et non dans le dossier utilisateur de Windows.
* Si le dossier RetroBat a été déplacé, les raccourcis retrouvent quand même les jeux au nouvel&#x20;
* **Perfect Dark** : l'option **REGION** choisit l'exécutable Europe, USA ou Japon.

### Portages decomp (.decomp)

Un portage `.decomp` peut être placé dans le dossier de sa console d'origine, pour apparaître dans la même liste que les jeux de cette console (par exemple un portage de Star Fox 64 affiché avec les jeux Nintendo 64). Quel que soit l'émulateur choisi pour le système ou pour le jeu, un fichier `.decomp` est toujours lancé comme un portage decomp.

```
roms
└── n64
    ├── (jeux Nintendo 64)
    └── Starship
        ├── Starship.exe
        └── Star Fox 64.decomp
```

L'extension `.decomp` est actuellement acceptée par les systèmes suivants :

| Système          | Dossier         |
| ---------------- | --------------- |
| MAME             | `roms\mame`     |
| CPS-III          | `roms\cps3`     |
| Model 2          | `roms\model2`   |
| Model 3          | `roms\model3`   |
| Naomi            | `roms\naomi`    |
| Naomi 2          | `roms\naomi2`   |
| Super Nintendo   | `roms\snes`     |
| Nintendo 64      | `roms\n64`      |
| GameCube         | `roms\gamecube` |
| Wii              | `roms\wii`      |
| Switch           | `roms\switch`   |
| Game Boy Advance | `roms\gba`      |
| PlayStation      | `roms\psx`      |
| PlayStation 2    | `roms\ps2`      |
| PlayStation 3    | `roms\ps3`      |
| Xbox             | `roms\xbox`     |
| Xbox 360         | `roms\xbox360`  |

{% hint style="warning" %}
RetroBat parcourt les sous-dossiers du dossier de la console. Si le dossier du portage contient des fichiers portant une extension de cette console (par exemple des `.zip` ou des `.wad` dans `roms\n64`), ils apparaissent aussi dans la liste des jeux. Masquez-les dans la liste des jeux, ou gardez ces fichiers hors du dossier du portage quand le portage le permet.
{% endhint %}

#### Contenu du fichier .decomp

Le fichier `.decomp` peut rester vide : RetroBat lance alors le premier exécutable (`.exe`) trouvé à côté de lui.

Si le dossier contient plusieurs exécutables, indiquez sur la première ligne le nom de l'exécutable à lancer, **sans l'extension `.exe`** :

```
Starship
```

* Seul le dossier qui contient le fichier `.decomp` est parcouru, pas ses sous-dossiers.
* Les lignes vides et les lignes commençant par `#` sont ignorées.
* Si le nom ne correspond à aucun exécutable du dossier, RetroBat lance le premier exécutable trouvé.

Le portage est lancé depuis le dossier qui contient le fichier `.decomp`.

Si le processus du jeu porte un autre nom que l'exécutable, créez un fichier `.gameexe` portant le même nom que le fichier `.decomp`, dans le même dossier, contenant le nom du processus du jeu (avec ou sans `.exe`). RetroBat attend l'apparition de ce processus pendant environ 6 secondes, puis attend sa fermeture.

### Mise à jour depuis N64RecompLauncher

Quiver Launcher remplace N64RecompLauncher.

* Le dossier `roms\n64recomp` est renommé `roms\recomp` pendant la mise à jour de RetroBat, avec sa liste de jeux et ses médias.
* Les jeux installés avec N64RecompLauncher ne sont pas transférés : réinstallez-les dans Quiver Launcher.
* Vos sauvegardes restent dans `emulators\n64recomplauncher\RecompiledGames\<jeu>`. Copiez-les dans le dossier du même jeu dans `emulators\quiverlauncher\Apps\<jeu>`.
