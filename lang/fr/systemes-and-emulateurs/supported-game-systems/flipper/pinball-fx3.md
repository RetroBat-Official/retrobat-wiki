---
description: Zen Studios
---

# Pinball FX3

<div align="left"><figure><img src="../../../.gitbook/assets/image (5).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Présentation

**Pinball FX3** est la plateforme de flipper de **Zen Studios** sortie en 2017. Sur Steam, elle s'appelle **Pinball FX Classic** depuis mars 2026. Elle reprend les tables achetées dans Pinball FX2. Son successeur est Pinball FX.

{% embed url="https://fr.wikipedia.org/wiki/Pinball_FX" %}

## En bref

<table><thead><tr><th width="280.25"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\pinballfx3</code></td></tr><tr><td><strong>Extensions</strong></td><td>.pxp .table</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>pinballfx (version steam)</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Par le jeu (RetroBat ne la modifie pas)</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr></tbody></table>

## Quel émulateur choisir ?

L'émulateur `pinballfx` a deux versions (core) :

<table><thead><tr><th width="168.25">Version</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>steam</strong> (par défaut)</td><td>Le jeu installé avec Steam est lancé par Steam, directement sur la table choisie.</td><td>Steam doit être installé, avec le jeu.</td></tr><tr><td><strong>nonsteam</strong></td><td>Lance directement l'exécutable du jeu, sans passer par Steam.</td><td>Le jeu doit se trouver dans <code>emulators\pinballfx3</code>.</td></tr></tbody></table>

Pour **nonsteam**, RetroBat cherche `Pinball FX Classic.exe` ou `Pinball FX3.exe` dans le dossier `emulators\pinballfx3`. Si le jeu n'y est pas, un message indique le dossier attendu.

## BIOS

Aucun BIOS nécessaire.

## Mode cabinet

Pour lancer une table depuis RetroBat, il faut :

* [x] le jeu Pinball FX3 ;
* [x] au moins une table achetée ;
* [x] le **mode cabinet** activé avec un code d'activation personnel, demandé à Zen Studios.

{% hint style="info" %}
Demande du code : [formulaire de Zen Studios](https://zenstudios.com/home/pinball-cabinet-support-request/). Plus d'informations sur le [mode cabinet](https://www.pinballfx.com/?page_id=7754#end-anchor).
{% endhint %}

## Ajouter des tables

Une fois le mode cabinet activé, chaque table est un fichier placé dans `roms\pinballfx3` :

* soit le fichier `.pxp` de la table, copié depuis le dossier `data\steam` du jeu ;
* soit un fichier vide `.table` qui porte exactement le nom de la table (par exemple `Western.table`).

<div align="left"><figure><img src="../../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure></div>

Pour ouvrir le dossier du jeu :

* Dans Steam, ouvrez la **Bibliothèque**.

<div align="left"><figure><img src="../../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure></div>

* Faites un clic droit sur le jeu, puis **Gérer > Parcourir les fichiers locaux**.

<div align="left"><figure><img src="../../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure></div>

* Ouvrez le dossier `data\steam` : il contient les fichiers `.pxp` de toutes les tables.

{% hint style="warning" %}
Le dossier `data\steam` contient toutes les tables : seules celles que vous possédez se lancent.
{% endhint %}

<details>

<summary>Noms des tables</summary>

* `Alien_Isolation`
* `Alien_vs_Predator`
* `Aliens`
* `AmericanDad`
* `Amusement_Park`
* `Archer`
* `Atlantis`
* `BALLY_Attack_from_Mars`
* `BALLY_BlackRose`
* `BALLY_Champion_Pub`
* `BALLY_Cirqus_Voltaire`
* `BALLY_Creature_from_the_Black_Lagoon`
* `BALLY_Dr_Dude`
* `BALLY_Party_Zone`
* `BALLY_Safe_Cracker`
* `BALLY_TheatreOfMagic`
* `BETHESDA_Doom`
* `BETHESDA_Fallout`
* `BETHESDA_Skyrim`
* `BioLab`
* `BobsBurgers`
* `CastleStorm`
* `Citadel`
* `EarthDefense`
* `Eldorado`
* `Excalibur`
* `FamilyGuy`
* `Hercules`
* `Looter`
* `Mars`
* `MARVEL_Age_of_Ultron`
* `MARVEL_Ant-Man`
* `MARVEL_Avengers`
* `MARVEL_Blade`
* `MARVEL_CaptainAmerica`
* `MARVEL_CivilWar`
* `MARVEL_Deadpool`
* `MARVEL_DrStrange`
* `MARVEL_FantasticFour`
* `MARVEL_FearItSelf`
* `MARVEL_GhostRider`
* `MARVEL_Guardians`
* `MARVEL_InfinityGauntlet`
* `MARVEL_IronMan`
* `MARVEL_MoonKnight`
* `MARVEL_MsMarvel`
* `MARVEL_SpiderMan`
* `MARVEL_Thor`
* `MARVEL_Venom`
* `MARVEL_Wolverine`
* `MARVEL_WOP_TheNextGeneration`
* `MARVEL_WWH`
* `MARVEL_XMen`
* `Paranormal`
* `Pasha`
* `Portal`
* `RedCup1`
* `RedCup2`
* `RedCup3`
* `Rome`
* `Shaman`
* `SpaceBear1`
* `SpaceBear2`
* `STARWARS_AVCO2`
* `STARWARS_Boba_Fett`
* `STARWARS_CloneWars`
* `STARWARS_Darth_Vader`
* `STARWARS_Droids`
* `STARWARS_Episode7`
* `STARWARS_Episode_4`
* `STARWARS_Episode_5`
* `STARWARS_Episode_6`
* `STARWARS_Han_Solo`
* `STARWARS_LAPB`
* `STARWARS_Light_VS_Dark`
* `STARWARS_Rebels`
* `STARWARS_SFA`
* `Tesla`
* `TheWalkingDead`
* `UNIVERSAL_BTTF`
* `UNIVERSAL_ET`
* `UNIVERSAL_Jaws`
* `UNIVERSAL_Jurassic_Park`
* `UNIVERSAL_Jurassic_Theme_Park`
* `UNIVERSAL_Jurassic_World`
* `V12`
* `Western`
* `WMS_Funhouse`
* `WMS_Getaway`
* `WMS_Hurricane`
* `WMS_Indiana_Jones`
* `WMS_Junkyard`
* `WMS_Medieval_Madness`
* `WMS_Monster_Bash`
* `WMS_No_Good_Gofers`
* `WMS_Roadshow`
* `WMS_Space_Station`
* `WMS_Tales_of_the_Arabian_Nights`
* `WMS_White_Water`

</details>

## Contrôles

Le jeu gère la manette lui-même (manette XInput conseillée) : RetroBat ne change pas sa configuration. Les commandes se modifient dans les options du jeu.

| Action                            | Manette                                       |
| --------------------------------- | --------------------------------------------- |
| Flipper gauche                    | L1 ou L2                                      |
| Flipper droit                     | R1 ou R2                                      |
| Lancer la bille                   | Stick droit vers le bas (tirer puis relâcher) |
| Lancement automatique de la bille | SUD                                           |
| Vue du fronton                    | Stick droit vers le haut                      |
| Bousculer la table                | Stick gauche                                  |
| Extras visuels                    | EST                                           |
| Pouvoir de magicien               | OUEST                                         |
| Changer de vue                    | NORD                                          |
| Menu                              | START ou SELECT                               |

## Raccourcis

<table><thead><tr><th width="204">Action</th><th>Manette</th></tr></thead><tbody><tr><td>Quitter le jeu</td><td>HOTKEY + START</td></tr></tbody></table>

Le Game Control Center n'est pas disponible pour ces systèmes.

## Options utiles

Dans les options avancées du système ou du jeu :

* **OPTIONS DU JEU > NOMBRE DE JOUEURS** : de 1 à 4, chacun son tour.
* **OPTIONS DU JEU > MODE CLASSIQUE** : partie classique, sans améliorations de table.
* **OPTIONS DU JEU > MODE HORS LIGNE** : lance le jeu hors ligne.
* **VIDÉO > RÉSOLUTION DE L'ÉCRAN** : résolution de Windows pendant la partie.
* **ÉMULATION > FERMER LE LAUNCHER EN QUITTANT** : ferme Steam en quittant le jeu (version steam).

## Dossiers

<table><thead><tr><th width="289">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Tables</td><td><code>roms\pinballfx3</code></td></tr><tr><td>Jeu (version nonsteam)</td><td><code>emulators\pinballfx3</code></td></tr><tr><td>Sauvegardes, scores, réglages</td><td>Gérés par le jeu (et par Steam)</td></tr></tbody></table>

## Problèmes connus

* **Le jeu s'ouvre sur son menu, sans la table** : mode cabinet non activé (voir plus haut), ou table non possédée.
* **« Game not found: copy it in '…' »** (version nonsteam) : le jeu n'est pas dans le dossier indiqué, ou son exécutable porte un autre nom.
* **« Steam is not installed. »** (version steam) : Steam est introuvable.
