---
description: Nintendo
---

# Family Computer Disk System

<div align="left"><figure><img src="../../../../.gitbook/assets/image (652).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Présentation

Le **Famicom Disk System** est un lecteur de disquettes qui se branche sous la Famicom, sorti au Japon en février 1986. Ses disquettes (Disk Cards) contiennent plus de données que les cartouches de l'époque, permettent de sauvegarder la partie et pouvaient être réécrites avec un nouveau jeu dans des bornes en magasin. Il ajoute aussi une voie sonore.

Sa ludothèque compte la version originale de The Legend of Zelda, Metroid, Kid Icarus, Super Mario Bros. 2 (la suite japonaise), Doki Doki Panic, Akumajō Dracula (Castlevania)… Beaucoup de ces jeux sont ensuite sortis en cartouche en Occident : ces versions se rangent dans `roms\nes`.

{% embed url="https://fr.wikipedia.org/wiki/Famicom_Disk_System" %}

## En bref

<table><thead><tr><th width="292.75"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\fds</code></td></tr><tr><td><strong>Extensions</strong></td><td>.nes .fds .zip .7z</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: fceumm</td></tr><tr><td><strong>BIOS</strong></td><td><code>disksys.rom</code> obligatoire</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro ; Mesen et ares par raccourcis</td></tr><tr><td><strong>RetroAchievements</strong></td><td>cores libretro</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>cores libretro</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="140.25">Émulateur</th><th width="168.75">Pour qui ?</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>libretro: fceumm</strong> (défaut)</td><td>Tout le monde</td><td>Très compatible, RetroAchievements, jeu en réseau.</td><td>Changement de face manuel (voir <a href="family-computer-disk-system.md#changer-de-face"><strong>Changer de face</strong></a>).</td></tr><tr><td><strong>libretro: nestopia</strong></td><td>Tout le monde</td><td>Très précis, RetroAchievements, jeu en réseau.</td><td>Changement de face manuel.</td></tr><tr><td><strong>libretro: mesen</strong></td><td>Puristes</td><td>Très précis, changement de face automatique, avance rapide pendant les chargements, RetroAchievements, jeu en réseau.</td><td>—</td></tr><tr><td><strong>mesen</strong></td><td>Utilisateurs de Mesen</td><td>Mesen 2 : changement de face automatique, avance rapide pendant les chargements.</td><td>Pas de RetroAchievements. Sauvegardes instantanées par raccourcis.</td></tr><tr><td><strong>ares</strong></td><td>Puristes</td><td>Émulation très précise.</td><td>Pas de RetroAchievements. Sauvegardes instantanées par raccourcis.</td></tr></tbody></table>

**En cas de doute, gardez libretro: fceumm**, ou choisissez libretro: mesen pour ne pas changer de face à la main.

## BIOS

<table><thead><tr><th width="127.75">Fichier</th><th width="210">Description</th><th width="80">Dossier</th><th>md5</th></tr></thead><tbody><tr><td><code>disksys.rom</code></td><td>BIOS du Famicom Disk System</td><td><code>bios</code></td><td>ca30b50f880eb660a320674ed365ef7a</td></tr></tbody></table>

Ce fichier est obligatoire (tous les émulateurs) et contrôlé par RetroBat. Pour Mesen, RetroBat le copie dans `emulators\mesen\Firmware`.

## Quel format de jeu ?

<table><thead><tr><th width="177.75">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.fds</strong></td><td>Image d'une disquette (toutes ses faces).</td></tr><tr><td><strong>.nes</strong></td><td>Jeu en cartouche, accepté aussi.</td></tr><tr><td><strong>.zip</strong>, <strong>.7z</strong></td><td>Un jeu compressé (un jeu par archive).</td></tr></tbody></table>

## Contrôles

Les contrôles sont ceux de la NES : voir la page [**NES**](nintendo-entertainment-system-family-computer.md#controles), section **Contrôles** (disposition, boutons tournés, disposition Xbox, turbo).

Avec les cores fceumm et nestopia, L1 et R1 servent au lecteur de disquettes : voir [**Changer de face**](family-computer-disk-system.md#changer-de-face).

Raccourcis : voir la page [**NES**](nintendo-entertainment-system-family-computer.md#raccourcis), section **Raccourcis** (Mesen, ares ; raccourcis de RetroArch pour les cores libretro).

## Dossiers

<table><thead><tr><th width="362.75">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Cores libretro, Mesen : sauvegardes des jeux</td><td><code>saves\fds</code></td></tr><tr><td>Cores libretro : sauvegardes instantanées</td><td><p><code>saves\fds\libretro.&#x3C;core></code> </p><p>(ex. <code>saves\fds\libretro.fceumm</code>)</p></td></tr><tr><td>Mesen : sauvegardes instantanées</td><td><code>saves\fds\mesen\SaveStates</code></td></tr><tr><td>ares : sauvegardes des jeux et instantanées</td><td><code>saves\fds\ares</code></td></tr><tr><td>BIOS</td><td><code>bios</code></td></tr><tr><td>Captures d'écran</td><td><code>screenshots\mesen</code>, <code>screenshots\ares</code></td></tr></tbody></table>

## Guides

### Changer de face

Beaucoup de jeux demandent de retourner la disquette (« PLEASE SET DISK CARD SIDE B ») :

<table><thead><tr><th width="234">Émulateur</th><th>Comment faire</th></tr></thead><tbody><tr><td>core fceumm</td><td>R1 éjecte la disquette, L1 change de face, R1 l'insère de nouveau.</td></tr><tr><td>core nestopia</td><td>L1 change de face. Pour un jeu sur deux disquettes, R1 passe à l'autre disquette.</td></tr><tr><td>core mesen, Mesen</td><td>Automatique : <strong>ÉMULATION > INSÉRER LE DISQUE AUTOMATIQUEMENT</strong> (activé par défaut) change de face quand le jeu le demande.</td></tr></tbody></table>

### Chargements plus rapides

Les chargements de disquette sont lents, comme sur la vraie console. Avec Mesen (core ou autonome), **ÉMULATION > AVANCE RAPIDE PENDANT LE CHARGEMENT** accélère l'émulation pendant chaque chargement.

## Problèmes connus

| Problème                                           | Solution                                                                                      |
| -------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| Le jeu ne démarre pas, ou Mesen demande un fichier | Ajoutez `disksys.rom` dans `bios` (voir [**BIOS**](family-computer-disk-system.md#bios)).     |
| Le jeu reste sur « SET DISK CARD SIDE B »          | Changez de face (voir [**Changer de face**](family-computer-disk-system.md#changer-de-face)). |
