---
description: Zen Studios
---

# Pinball FX Midnight

<div align="left"><figure><img src="../../../.gitbook/assets/image (10).png" alt="" width="375"><figcaption></figcaption></figure></div>

## Présentation

**Pinball FX Midnight**, appelé **Pinball M** jusqu'en mars 2026, est la plateforme de flipper de **Zen Studios** consacrée aux tables d'horreur, sortie fin 2023. Comme Pinball FX, le jeu est gratuit et les tables s'achètent séparément ; Wrath of the Elder Gods est gratuite.

RetroBat lance directement une table, dans le mode de jeu choisi.

{% embed url="https://fr.wikipedia.org/wiki/Pinball_FX" %}

## En bref

<table><thead><tr><th width="277.75"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\pinballm</code></td></tr><tr><td><strong>Extensions</strong></td><td>.table</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>pinballfx (version steam)</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Par le jeu (RetroBat ne la modifie pas)</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr></tbody></table>

## Quel émulateur choisir ?

L'émulateur `pinballfx` a deux versions (core) :

<table><thead><tr><th width="169.5">Version</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>steam</strong> (par défaut)</td><td>Le jeu installé avec Steam est lancé par Steam, directement sur la table choisie.</td><td>Steam doit être installé, avec le jeu.</td></tr><tr><td><strong>nonsteam</strong></td><td>Lance directement l'exécutable du jeu, sans passer par Steam.</td><td>Le jeu doit se trouver dans <code>emulators\pinballm</code>.</td></tr></tbody></table>

Pour **nonsteam**, RetroBat cherche `Pinball FX Midnight.exe`, `Pinball M.exe` ou `PinballM.exe` dans le dossier `emulators\pinballm`. Si le jeu n'y est pas, un message indique le dossier attendu.

## BIOS

Aucun BIOS nécessaire.

## Ajouter des tables

Chaque table est un petit fichier texte `.table` qui contient le **numéro de la table** :

1. Dans `roms\pinballm`, créez un fichier texte, par exemple `The Thing.txt`.
2. Écrivez le numéro de la table sur la première ligne (175 pour The Thing).
3. Enregistrez, puis remplacez l'extension `.txt` par `.table`.

<div align="left"><figure><img src="../../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure></div>

Voir l'exemple de la page [Pinball FX](pinball-fx.md).

{% hint style="warning" %}
Seules les tables que vous possédez se lancent depuis RetroBat (en plus de la table gratuite).
{% endhint %}

<details>

<summary>Numéros des tables</summary>

| N°  | Table                                    |
| --- | ---------------------------------------- |
| 90  | Fallout™ Pinball                         |
| 91  | The Elder Scrolls V: Skyrim™ Pinball     |
| 92  | DOOM™ Pinball                            |
| 147 | Wrath of the Elder Gods (Director's Cut) |
| 171 | Chucky's Killer Pinball                  |
| 174 | Dead by Daylight™ Pinball                |
| 175 | The Thing Pinball                        |
| 176 | Duke Nukem's Big Shot Pinball            |
| 180 | Texas Chainsaw Massacre Pinball          |
| 183 | System Shock Pinball                     |
| 191 | Camp Bloodbrook                          |

</details>

## Contrôles

Le jeu gère la manette lui-même (manette XInput conseillée) : RetroBat ne change pas sa configuration. Les commandes se modifient dans les options du jeu.

<table><thead><tr><th width="297.75">Action</th><th>Manette</th></tr></thead><tbody><tr><td>Flipper gauche</td><td>L1 ou L2</td></tr><tr><td>Flipper droit</td><td>R1 ou R2</td></tr><tr><td>Lancer la bille</td><td>Stick droit vers le bas (tirer puis relâcher)</td></tr><tr><td>Lancement automatique de la bille</td><td>SUD</td></tr><tr><td>Vue du fronton</td><td>Stick droit vers le haut</td></tr><tr><td>Bousculer la table</td><td>Stick gauche</td></tr><tr><td>Extras visuels</td><td>EST</td></tr><tr><td>Pouvoir de magicien</td><td>OUEST</td></tr><tr><td>Changer de vue</td><td>NORD</td></tr><tr><td>Menu</td><td>START ou SELECT</td></tr></tbody></table>

## Raccourcis

<table><thead><tr><th width="211.5">Action</th><th>Manette</th></tr></thead><tbody><tr><td>Quitter le jeu</td><td>HOTKEY + START</td></tr></tbody></table>

Le Game Control Center n'est pas disponible pour ces systèmes.

## Options utiles

Dans les options avancées du système ou du jeu :

* **OPTIONS DU JEU > MODE DE JEU** : mode lancé avec la table. Sans réglage, le jeu garde le mode choisi dans son menu.

<table><thead><tr><th width="299">Choix</th><th>Mode de jeu</th></tr></thead><tbody><tr><td>Classique</td><td>Partie classique (<code>Classic</code>)</td></tr><tr><td>Pro</td><td>Mode Pro (<code>Pro</code>)</td></tr><tr><td>Entraînement</td><td>Entraînement (<code>Practice</code>)</td></tr><tr><td>Chacun son tour 2 / 3 / 4 joueurs</td><td>Partie à plusieurs, chacun son tour (<code>Hotseat_2</code> à <code>Hotseat_4</code>)</td></tr><tr><td>Défi 1 bille</td><td>Une seule bille (<code>Challenge_BallLimited</code>)</td></tr><tr><td>Défi 5 minutes</td><td>Partie limitée à 5 minutes (<code>Challenge_TimeLimited</code>)</td></tr><tr><td>Défi de distance</td><td>Défi de distance (<code>Challenge_DistanceLimited</code>)</td></tr><tr><td>Défi des flips</td><td>Nombre de coups de flipper limité (<code>Challenge_FlipLimited</code>)</td></tr></tbody></table>

* **VIDÉO > RÉSOLUTION DE L'ÉCRAN** : résolution de Windows pendant la partie.
* **ÉMULATION > FERMER LE LAUNCHER EN QUITTANT** : ferme Steam en quittant le jeu (version steam).

Un mode qui n'existe pas pour la table est ignoré : la table démarre avec ses réglages par défaut.

## Dossiers

<table><thead><tr><th width="274">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Tables</td><td><code>roms\pinballm</code></td></tr><tr><td>Jeu (version nonsteam)</td><td><code>emulators\pinballm</code></td></tr><tr><td>Sauvegardes, scores, réglages</td><td>Gérés par le jeu (et par Steam)</td></tr></tbody></table>

## Problèmes connus

* **Le jeu s'ouvre sans lancer la table** : vous ne possédez pas la table, ou son numéro est faux.
* **« '….table' must contain the table number on its first line. »** : le fichier `.table` est vide ou ne contient pas un numéro.
* **« Game not found: copy it in '…' »** (version nonsteam) : le jeu n'est pas dans le dossier indiqué, ou son exécutable porte un autre nom.
* **« Steam is not installed. »** (version steam) : Steam est introuvable.
