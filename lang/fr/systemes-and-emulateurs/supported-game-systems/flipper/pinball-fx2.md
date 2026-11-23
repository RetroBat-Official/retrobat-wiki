---
description: Zen Studios
---

# Pinball FX2

<div align="left"><figure><img src="../../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure></div>

## Présentation

**Pinball FX2** est la plateforme de flipper de **Zen Studios** sortie en 2010 sur Xbox 360, puis en 2013 sur PC. Retiré de la vente sur Steam en 2017, remplacé par Pinball FX3, il reste téléchargeable par ses propriétaires.

{% embed url="https://fr.wikipedia.org/wiki/Pinball_FX" %}

## En bref

<table><thead><tr><th width="267.75"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\pinballfx2</code></td></tr><tr><td><strong>Extensions</strong></td><td>.pxp .table</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>pinballfx (version steam)</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Par le jeu (RetroBat ne la modifie pas)</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr></tbody></table>

## Quel émulateur choisir ?

L'émulateur `pinballfx` a deux versions (core) :

<table><thead><tr><th width="178.25">Version</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>steam</strong> (par défaut)</td><td>Le jeu installé avec Steam est lancé par Steam, directement sur la table choisie.</td><td>Steam doit être installé, avec le jeu.</td></tr><tr><td><strong>nonsteam</strong></td><td>Lance directement l'exécutable du jeu, sans passer par Steam.</td><td>Le jeu doit se trouver dans <code>emulators\pinballfx2</code>.</td></tr></tbody></table>

Pour **nonsteam**, RetroBat cherche `Pinball FX2.exe` dans le dossier `emulators\pinballfx2`. Si le jeu n'y est pas, un message indique le dossier attendu.

## BIOS

Aucun BIOS nécessaire.

## Mode cabinet

Pour lancer une table depuis RetroBat, il faut :

* [x] le jeu Pinball FX2 ;
* [x] au moins une table achetée ;
* [x] le **mode cabinet** activé avec un code d'activation personnel, demandé à Zen Studios.

{% hint style="info" %}
Demande du code : [formulaire de Zen Studios](https://zenstudios.com/home/pinball-cabinet-support-request/). Plus d'informations sur le [mode cabinet](https://www.pinballfx.com/?page_id=7754#end-anchor).
{% endhint %}

## Ajouter des tables

Une fois le mode cabinet activé, chaque table est un fichier placé dans `roms\pinballfx2` :

* soit le fichier `.pxp` de la table, copié depuis le dossier `data_steam` du jeu ;
* soit un fichier vide `.table` qui porte exactement le nom de la table (par exemple `Citadel.table`).

<div align="left"><figure><img src="../../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure></div>

Les fichiers `.pxp` de toutes les tables se trouvent dans le dossier `data_steam` du jeu (dans Steam : clic droit sur le jeu, **Gérer > Parcourir les fichiers locaux**).

{% hint style="warning" %}
Le dossier `data_steam` contient toutes les tables : seules celles que vous possédez se lancent.
{% endhint %}

<details>

<summary>Noms des tables</summary>

* `Alien_Isolation`
* `Alien_vs_Predator`
* `Aliens`
* `AmericanDad`
* `Archer`
* `Atlantis`
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
* `Football`
* `Football_Arsenal`
* `Football_Barcelona`
* `Football_Juventus`
* `Football_Liverpool`
* `Football_Milan`
* `Football_RealMadrid`
* `Football_Roma`
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
* `PlantsVsZombies`
* `Portal`
* `Rome`
* `Shaman`
* `SouthPark1`
* `SouthPark2`
* `SplosionMan`
* `STARWARS_Boba_Fett`
* `STARWARS_CloneWars`
* `STARWARS_Darth_Vader`
* `STARWARS_Droids`
* `STARWARS_Episode_4`
* `STARWARS_Episode_5`
* `STARWARS_Episode_6`
* `STARWARS_Episode_7`
* `STARWARS_Han_Solo`
* `STARWARS_Light_VS_Dark`
* `STARWARS_MFO`
* `STARWARS_Rebels`
* `STARWARS_SFA`
* `Tesla`
* `TheWalkingDead`
* `V12`
* `Western`

</details>

## Contrôles

Le jeu gère la manette lui-même (manette XInput conseillée) : RetroBat ne change pas sa configuration. Les commandes se modifient dans les options du jeu.

<table><thead><tr><th width="324">Action</th><th>Manette</th></tr></thead><tbody><tr><td>Flipper gauche</td><td>L1 ou L2</td></tr><tr><td>Flipper droit</td><td>R1 ou R2</td></tr><tr><td>Lancer la bille</td><td>Stick droit vers le bas (tirer puis relâcher)</td></tr><tr><td>Lancement automatique de la bille</td><td>SUD</td></tr><tr><td>Vue du fronton</td><td>Stick droit vers le haut</td></tr><tr><td>Bousculer la table</td><td>Stick gauche</td></tr><tr><td>Extras visuels</td><td>EST</td></tr><tr><td>Pouvoir de magicien</td><td>OUEST</td></tr><tr><td>Changer de vue</td><td>NORD</td></tr><tr><td>Menu</td><td>START ou SELECT</td></tr></tbody></table>

## Raccourcis

<table><thead><tr><th width="261.5">Action</th><th>Manette</th></tr></thead><tbody><tr><td>Quitter le jeu</td><td>HOTKEY + START</td></tr></tbody></table>

Le Game Control Center n'est pas disponible pour ces systèmes.

## Options utiles

Dans les options avancées du système ou du jeu :

* **VIDÉO > RÉSOLUTION DE L'ÉCRAN** : résolution de Windows pendant la partie.
* **ÉMULATION > FERMER LE LAUNCHER EN QUITTANT** : ferme Steam en quittant le jeu (version steam).

## Dossiers

<table><thead><tr><th width="295.25">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Tables</td><td><code>roms\pinballfx2</code></td></tr><tr><td>Jeu (version nonsteam)</td><td><code>emulators\pinballfx2</code></td></tr><tr><td>Sauvegardes, scores, réglages</td><td>Gérés par le jeu (et par Steam)</td></tr></tbody></table>

## Problèmes connus

* **Le jeu s'ouvre sur son menu, sans la table** : mode cabinet non activé (voir plus haut), ou table non possédée.
* **« Game not found: copy it in '…' »** (version nonsteam) : le jeu n'est pas dans le dossier indiqué, ou son exécutable porte un autre nom.
* **« Steam is not installed. »** (version steam) : Steam est introuvable.

