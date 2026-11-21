---
description: Worlds of Wonder
---

# Actionmax

## Présentation

L'**Action Max** est une console de Worlds of Wonder, sortie en 1987. Elle ne contient pas de processeur de jeu : les jeux sont des cassettes VHS, lues par un magnétoscope branché à la console. Le joueur tire au pistolet sur la télévision, et un capteur collé sur l'écran détecte les flashs lumineux de la vidéo pour compter les points. Elle disparaît dès 1988.

Seuls 5 jeux sont sortis :

<table><thead><tr><th width="276.5">Jeu</th><th>Fichier</th></tr></thead><tbody><tr><td>.38 Ambush Alley</td><td><code>38ambushalley</code></td></tr><tr><td>Blue Thunder</td><td><code>bluethunder</code></td></tr><tr><td>Hydrosub: 2021</td><td><code>hydrosub2021</code></td></tr><tr><td>Pops 'N Pals: Pops Ghostly</td><td><code>popsghostly</code></td></tr><tr><td>Sonic Fury</td><td><code>sonicfury</code></td></tr></tbody></table>

Dans RetroBat, ces jeux se lancent avec un script **Singe** qui reproduit la console : il lit la vidéo de la cassette, affiche le viseur et compte les tirs réussis.

{% embed url="https://fr.wikipedia.org/wiki/Action_Max" %}

## En bref

<table><thead><tr><th width="270.25"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\actionmax</code></td></tr><tr><td><strong>Extensions</strong></td><td>.actionmax</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>hypseus</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs (joueur 1)</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr><tr><td><strong>Pistolets</strong></td><td>Hypseus, Singe2</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="119.5">Émulateur</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>hypseus</strong> (défaut)</td><td>Lit les jeux de la version Hypseus (zip ou dossier). Plusieurs pistolets, décorations.</td><td>—</td></tr><tr><td><strong>singe2</strong></td><td>L'émulateur de l'auteur de Singe, avec sa propre version des jeux (vidéos en <code>.mkv</code>).</td><td>Fichiers différents de ceux de Hypseus. Demande le mode développeur de Windows. Un seul pistolet.</td></tr></tbody></table>

**En cas de doute, gardez hypseus.**

## BIOS

Aucun BIOS n'est nécessaire.

## Quel format de jeu ?

Chaque jeu se lance à partir d'un **fichier vide** `<jeu>.actionmax` (par exemple `38ambushalley.actionmax`), créé par vous. Ce fichier indique à RetroBat quel jeu lancer ; les vidéos et le script sont à côté.

<table><thead><tr><th width="327.75">Format</th><th width="101.5">hypseus</th><th width="78">singe2</th><th>Remarques</th></tr></thead><tbody><tr><td><strong>Zip</strong> (<code>roms\actionmax\roms\actionmax.zip</code>)</td><td>✔</td><td>✘</td><td>Méthode conseillée pour Hypseus.</td></tr><tr><td>Dossier <code>actionmax.hypseus</code></td><td>✔</td><td>✘</td><td>Ancienne méthode pour Hypseus.</td></tr><tr><td>Dossier <code>ActionMax</code> (version Singe 2)</td><td>✘</td><td>✔</td><td>Seul format pour Singe2.</td></tr></tbody></table>

Les vidéos et le son des cassettes sont à fournir. Les noms des fichiers `.actionmax` doivent être exactement ceux du tableau de **Présentation**, en minuscules.

Le détail de chaque méthode est dans [**Guides**](actionmax.md#guides).

## Contrôles

RetroBat configure automatiquement la manette du joueur 1 pour les deux émulateurs.

L'Action Max se joue au **pistolet** ou à la **souris** : visez, puis tirez. Sur l'écran de choix du mode, tirez sur la moitié gauche pour le mode normal, sur la moitié droite pour le mode à munitions limitées.

<table><thead><tr><th width="114.5">Action</th><th>Hypseus</th><th>Singe2</th></tr></thead><tbody><tr><td>Tirer</td><td>Gâchette du pistolet, clic gauche de la souris, <strong>R1</strong> sur la manette</td><td>Gâchette du pistolet, clic gauche de la souris</td></tr><tr><td>Viser</td><td>Pistolet ou souris</td><td>Pistolet ou souris</td></tr><tr><td>Quitter</td><td><strong>HOTKEY + START</strong>, ÉCHAP</td><td><strong>HOTKEY + START</strong>, ÉCHAP</td></tr></tbody></table>

L'option **AFFICHER CIBLE** affiche ou masque le viseur.

### Pistolets

Pour brancher et régler un pistolet dans RetroBat, voir la page [**Pistolets**](../../../controleurs/supported-controllers/lightguns/).

* **Hypseus** : plusieurs pistolets sont reconnus automatiquement (une souris par pistolet). L'option **PISTOLETS > UN SEUL PISTOLET** n'en garde qu'un. Avec un pistolet Sinden, RetroBat lance le logiciel Sinden et affiche la bordure blanche.
* **Singe2** : un seul pistolet. L'option **PISTOLETS > FORCER L'INDEX** choisit la souris utilisée.

## Dossiers

| Contenu                                     | Dossier                             |
| ------------------------------------------- | ----------------------------------- |
| Fichiers `.actionmax` (méthode zip)         | `roms\actionmax\vldp\actionmax`     |
| Fichiers `.actionmax` (autres méthodes)     | `roms\actionmax`                    |
| Script au format zip                        | `roms\actionmax\roms\actionmax.zip` |
| Vidéos (méthode zip)                        | `roms\actionmax\vldp\actionmax`     |
| Script et vidéos (ancienne méthode Hypseus) | `roms\actionmax\actionmax.hypseus`  |
| Script et vidéos (Singe2)                   | `roms\actionmax\ActionMax`          |
| Touches de Hypseus                          | `emulators\hypseus\hypinput.ini`    |
| Décorations de Hypseus                      | `emulators\hypseus\bezels`          |
| Captures d'écran de Hypseus (F12)           | `emulators\hypseus\screenshots`     |

## Guides

### Installer les jeux au format zip (Hypseus)

1. Récupérez `actionmax.zip` dans le dossier `00-zip-roms\00-Elder-Modernized-zip-rom` du dépôt `hypseus_singe_data` de Hypseus, sur GitHub, et copiez-le dans `roms\actionmax\roms`.
2. Créez le dossier `roms\actionmax\vldp\actionmax`.
3. Copiez-y les fichiers `.txt` des jeux (`38ambushalley.txt`…, dossier `00-singe1\actionmax` du même dépôt) et les vidéos des cassettes. Gardez les noms et les sous-dossiers indiqués dans les fichiers `.txt` : par exemple `video_actionmaxintro.m2v`, `video_menu.m2v` et `38ambushalley\video_38ambushalley.m2v`.
4. Dans ce même dossier, créez un fichier vide par jeu : `38ambushalley.actionmax`, `bluethunder.actionmax`…

```
roms\
└─ actionmax\
   ├─ roms\
   │  └─ actionmax.zip
   └─ vldp\
      └─ actionmax\
         ├─ 38ambushalley.actionmax
         ├─ 38ambushalley.txt
         ├─ video_actionmaxintro.m2v
         ├─ video_menu.m2v
         └─ 38ambushalley\
            ├─ video_38ambushalley.m2v
            └─ video_38ambushalley.ogg
```

<div align="left"><figure><img src="../../../.gitbook/assets/image (699).png" alt=""><figcaption></figcaption></figure></div>

### Installer les jeux au format dossier (ancienne méthode Hypseus)

1. Créez le dossier `roms\actionmax\actionmax.hypseus`.
2. Copiez-y le contenu du dossier `00-singe1\actionmax` du dépôt `hypseus_singe_data` (scripts `.singe`, fichiers `.txt`, sons, images, polices) et les vidéos des cassettes, avec les mêmes sous-dossiers.
3. Dans `roms\actionmax`, créez un fichier vide par jeu : `38ambushalley.actionmax`, `bluethunder.actionmax`…

RetroBat lance alors le script `<jeu>.singe` du dossier `actionmax.hypseus`.

### Installer les jeux pour Singe2

1. Téléchargez la version ActionMax de Singe 2 sur le site de l'émulateur (kangaroopunch.com).
2. Copiez le dossier `ActionMax` dans `roms\actionmax` (le nom `ActionMax.singe` est aussi accepté). Il contient les scripts (`38AmbushAlley.singe`…) et les vidéos (`video_38AmbushAlley.mkv`…).
3. Dans `roms\actionmax`, créez un fichier vide par jeu : `38ambushalley.actionmax`, `bluethunder.actionmax`…
4. Choisissez l'émulateur **singe2** pour le système ou pour le jeu.

Singe2 a besoin que le **mode développeur** de Windows soit activé (Paramètres de Windows) : RetroBat crée un lien vers le dossier `ActionMax` dans `emulators\singe2`.

Les fichiers `.actionmax` de `roms\actionmax` servent aussi à l'ancienne méthode Hypseus : si les dossiers `actionmax.hypseus` et `ActionMax` sont tous les deux présents, chaque jeu peut se lancer avec les deux émulateurs.

## Problèmes connus

<table><thead><tr><th width="359">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>« Unable to find singe file for actionmax »</td><td>Avec l'ancienne méthode, le dossier <code>roms\actionmax\actionmax.hypseus</code> ou le fichier <code>&#x3C;jeu>.singe</code> manque. Avec la méthode zip, le fichier <code>.actionmax</code> doit être dans <code>roms\actionmax\vldp\actionmax</code> et le zip dans <code>roms\actionmax\roms</code>.</td></tr><tr><td>« Framefile (.txt) does not exist »</td><td>Copiez le fichier <code>&#x3C;jeu>.txt</code> à côté du fichier <code>.actionmax</code>, dans <code>roms\actionmax\vldp\actionmax</code>.</td></tr><tr><td>Écran noir ou vidéo absente</td><td>Une vidéo manque ou n'est pas dans le sous-dossier indiqué par le fichier <code>.txt</code>.</td></tr><tr><td>« ActionMax rom folder not found » (Singe2)</td><td>Le dossier <code>roms\actionmax\ActionMax</code> manque.</td></tr><tr><td>Singe2 ne se lance pas, erreur de lien symbolique</td><td>Activez le mode développeur dans les paramètres de Windows.</td></tr><tr><td>Le jeu ne réagit pas aux tirs</td><td>Visez avec la souris ou un pistolet configuré (voir <a href="actionmax.md#pistolets"><strong>Pistolets</strong></a>).</td></tr><tr><td>Le viseur gêne</td><td>Désactivez <strong>AFFICHER CIBLE</strong>.</td></tr></tbody></table>
