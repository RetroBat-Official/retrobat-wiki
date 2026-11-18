---
description: Atari
---

# Atari 7800

<div align="left"><figure><img src="../../../../.gitbook/assets/image (664).png" alt=""><figcaption></figcaption></figure></div>

## Présentation

L'**Atari 7800 ProSystem** est présentée en 1984, mais sort vraiment en 1986, après le rachat d'Atari par Jack Tramiel. Sa puce graphique MARIA affiche beaucoup plus de sprites que les consoles précédentes d'Atari. Elle lit aussi presque tous les jeux de l'Atari 2600. Sa manette, la **ProLine**, a deux boutons. La console est arrêtée en 1992.

Sa ludothèque compte une soixantaine de jeux : Asteroids, Ms. Pac-Man, Food Fight, Ballblazer, Choplifter!, Karateka, Commando, Ninja Golf, Midnight Mutants… Les jeux de la 2600 ont leur propre système dans RetroBat (voir la page [**Atari 2600**](atari-2600.md)).

{% embed url="https://fr.wikipedia.org/wiki/Atari_7800" %}

## En bref

<table><thead><tr><th width="286.5"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\atari7800</code></td></tr><tr><td><strong>Extensions</strong></td><td>.a78 .bin .zip .7z</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: prosystem</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (obligatoire pour BizHawk)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>core libretro, BizHawk</td></tr><tr><td><strong>RetroAchievements</strong></td><td>core libretro, BizHawk</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="153">Émulateur</th><th width="146.5">Pour qui ?</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>libretro: prosystem</strong> (défaut)</td><td>Tout le monde</td><td>ProSystem : léger, sans BIOS, base de jeux intégrée, RetroAchievements.</td><td>—</td></tr><tr><td><strong>bizhawk: A78</strong></td><td>Utilisateurs de BizHawk</td><td>A7800Hawk : émulation précise, cartouche High Score (meilleurs scores), RetroAchievements, sauvegardes instantanées dans le menu de RetroBat.</td><td>Demande le BIOS (voir <a href="atari-7800.md#bios"><strong>BIOS</strong></a>).</td></tr></tbody></table>

**En cas de doute, gardez libretro: prosystem.**

## BIOS

ProSystem n'a besoin d'aucun BIOS : il utilise le BIOS de la région du jeu s'il est présent (écran de démarrage Atari). BizHawk demande le BIOS de la région du jeu : il ne lance pas le jeu sans lui.

<table><thead><tr><th width="184.75">Fichier</th><th width="92.75">Dossier</th><th width="262.5">MD5</th><th>Utilisé par</th></tr></thead><tbody><tr><td><code>7800 BIOS (U).rom</code></td><td><code>bios</code></td><td>0763f1ffb006ddbe32e52d497ee848ae</td><td>ProSystem (facultatif), BizHawk (jeux NTSC)</td></tr><tr><td><code>7800 BIOS (E).rom</code></td><td><code>bios</code></td><td>397bb566584be7b9764e7a68974c4263</td><td>ProSystem (facultatif), BizHawk (jeux PAL)</td></tr><tr><td><code>A78_highscore.bin</code></td><td><code>bios</code></td><td>—</td><td>BizHawk : cartouche High Score (facultatif)</td></tr></tbody></table>

La vérification des BIOS de RetroBat les liste comme optionnels, car l'émulateur par défaut n'en a pas besoin. Les fichiers doivent porter exactement ces noms.

> **Ancienne installation** : le fichier `ProSystem.dat` n'est plus utilisé, la base des jeux est intégrée au core. Vous pouvez le supprimer de `bios`.

La cartouche **High Score** d'Atari gardait les meilleurs scores des jeux compatibles (Asteroids, Food Fight…). BizHawk émule cette cartouche si `A78_highscore.bin` est présent.

## Quel format de jeu ?

Les jeux sont des fichiers `.a78`, éventuellement compressés en `.zip` ou `.7z` (un jeu par archive). Le `.a78` a un en-tête qui décrit la cartouche (taille, puce son POKEY, région). Les fichiers `.bin` n'ont pas d'en-tête : l'émulateur doit deviner le type de cartouche. Préférez les `.a78`.

## Contrôles

RetroBat configure automatiquement les manettes. La manette ProLine a deux boutons : les jeux à un seul bouton acceptent les deux. Les interrupteurs de la console sont sur la manette.

<table><thead><tr><th width="208.25">Manette RetroBat</th><th>libretro: prosystem</th><th>bizhawk</th></tr></thead><tbody><tr><td>Croix directionnelle</td><td>Joystick</td><td>Joystick</td></tr><tr><td>SUD</td><td>Bouton 1</td><td>Bouton 1</td></tr><tr><td>EST</td><td>Bouton 2</td><td>Bouton 2</td></tr><tr><td>NORD</td><td>Reset</td><td>Reset</td></tr><tr><td>START</td><td>Pause</td><td>Pause</td></tr><tr><td>SELECT</td><td>Select</td><td>—</td></tr><tr><td>L1</td><td>Difficulté gauche</td><td>—</td></tr><tr><td>R1</td><td>Difficulté droite</td><td>—</td></tr><tr><td>L2</td><td>—</td><td>Select</td></tr></tbody></table>

Avec BizHawk, le bouton SELECT de la manette sert aux raccourcis : l'interrupteur Select de la console est sur L2.

### Raccourcis

ProSystem utilise les raccourcis standards de RetroArch. BizHawk utilise les raccourcis communs de RetroBat. Voir la page [**Raccourcis**](../../../../navigation/hotkeys.md).

## Dossiers

<table><thead><tr><th width="356.5">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Jeux</td><td><code>roms\atari7800</code></td></tr><tr><td>BIOS</td><td><code>bios</code></td></tr><tr><td>ProSystem : sauvegardes instantanées</td><td><code>saves\atari7800\libretro.prosystem</code></td></tr><tr><td>BizHawk : sauvegardes des jeux</td><td><code>saves\atari7800\bizhawk</code></td></tr><tr><td>BizHawk : sauvegardes instantanées</td><td><code>saves\atari7800\bizhawk\sstates\A78</code></td></tr><tr><td>BizHawk : captures d'écran</td><td><code>screenshots\bizhawk\atari7800</code></td></tr></tbody></table>

## Guides

### Jeux à deux sticks

Robotron: 2084 et T:ME Salvo se jouent avec deux joysticks. **CONTRÔLES > DOUBLE STICK** (ProSystem) met le deuxième joystick sur le stick droit du joueur 1.

### RetroAchievements

ProSystem et BizHawk sont compatibles. Pour plus de détails, voir la page [**RetroAchievements**](../../../../utilisation-avancee/retroachievements.md).

### Autres options utiles

<table><thead><tr><th width="143.25">Émulateur</th><th>Option</th><th>Effet</th></tr></thead><tbody><tr><td>ProSystem</td><td><strong>RENDU VISUEL > PROFONDEUR DES COULEURS</strong></td><td><strong>24 BIT</strong> : couleurs plus fidèles.</td></tr><tr><td>ProSystem</td><td><strong>AUDIO > FILTRE AUDIO</strong></td><td>Adoucit le son aigu de certains jeux.</td></tr></tbody></table>

## Problèmes connus

<table><thead><tr><th width="364">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>BizHawk ne lance pas le jeu ou demande un firmware</td><td>Le BIOS de la région du jeu manque dans <code>bios</code> (voir <a href="atari-7800.md#bios"><strong>BIOS</strong></a>), ou il n'a pas exactement le bon nom.</td></tr><tr><td>Le jeu reste en pause ou ne démarre pas</td><td>Appuyez sur START (Pause) ou NORD (Reset).</td></tr><tr><td>Un jeu <code>.bin</code> ne démarre pas</td><td>Utilisez la version <code>.a78</code> du jeu.</td></tr><tr><td>Les jeux au pistolet ne répondent pas</td><td>Le pistolet (Alien Brigade, Barnyard Blaster, Crossbow, Meltdown) n'est configuré par RetroBat avec aucun émulateur.</td></tr></tbody></table>
