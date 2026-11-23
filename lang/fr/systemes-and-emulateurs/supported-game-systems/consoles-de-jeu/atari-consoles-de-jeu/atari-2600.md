---
description: Atari
---

# Atari 2600

<div align="left"><figure><img src="../../../../.gitbook/assets/image (13).png" alt="" width="425"><figcaption></figcaption></figure></div>

## Présentation

L'**Atari 2600**, d'abord appelée **Atari VCS** (Video Computer System), sort en 1977. Ce n'est pas la première console à cartouches, mais c'est elle qui rend le jeu vidéo populaire dans les foyers : elle se vend à plus de 30 millions d'exemplaires et reste en production jusqu'en 1992.

Sa ludothèque compte plus de 500 jeux : Adventure, Pitfall!, River Raid, Space Invaders, Pac-Man, Combat, Yars' Revenge, Kaboom!, Missile Command… La console a un joystick à un bouton, des paddles (manettes rotatives) et des interrupteurs en façade : **Reset** (lance la partie), **Select** (choix du mode de jeu), **Difficulté** gauche et droite (A ou B) et **Couleur / Noir et blanc**.

{% embed url="https://fr.wikipedia.org/wiki/Atari_2600" %}

## En bref

<table><thead><tr><th width="262.75"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\atari2600</code></td></tr><tr><td><strong>Extensions</strong></td><td>.a26 .bin .rom .gz .zip .7z</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: stella</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro, BizHawk ; Stella par raccourcis</td></tr><tr><td><strong>RetroAchievements</strong></td><td>cores libretro, BizHawk</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>cores libretro stella et stella2014</td></tr><tr><td><strong>Pistolets</strong></td><td>core stella</td></tr></tbody></table>

## Quel émulateur choisir ?

| Émulateur                     | Pour qui ?              | Points forts                                                                                               | Limites                                                            |
| ----------------------------- | ----------------------- | ---------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------ |
| **libretro: stella** (défaut) | Tout le monde           | Stella récent : excellente compatibilité, paddles, pistolet, filtres TV, RetroAchievements, jeu en réseau. | —                                                                  |
| **libretro: stella2014**      | PC modestes             | Ancienne version de Stella, très légère. RetroAchievements, jeu en réseau.                                 | Moins compatible. Pas de filtres TV.                               |
| **stella** (autonome)         | Utilisateurs de Stella  | Stella dans sa version d'origine : filtres TV, lignes de balayage, tir automatique, débogueur.             | Pas de RetroAchievements. Sauvegardes instantanées par raccourcis. |
| **bizhawk: Atari2600Hawk**    | Utilisateurs de BizHawk | Émulation propre à BizHawk, RetroAchievements, sauvegardes instantanées dans le menu de RetroBat.          | Moins compatible que Stella.                                       |

**En cas de doute, gardez libretro: stella.**

## BIOS

Aucun BIOS n'est nécessaire : l'Atari 2600 n'en a pas.

## Quel format de jeu ?

Les jeux sont des images de cartouche `.a26` (ou `.bin`, `.rom`), éventuellement compressées en `.zip` ou `.7z` (un jeu par archive). Les émulateurs reconnaissent le type de cartouche (taille, système de banques) et le contrôleur du jeu (joystick, paddles…) d'après leur base de jeux.

## Contrôles

RetroBat configure automatiquement les manettes. Le joystick a un seul bouton. Les interrupteurs de la console sont sur la manette.

<table><thead><tr><th width="176.5">Manette RetroBat</th><th>cores libretro (stella, stella2014)</th><th>stella</th><th>bizhawk</th></tr></thead><tbody><tr><td>Croix directionnelle</td><td>Joystick</td><td>Joystick</td><td>Joystick</td></tr><tr><td>SUD</td><td>Tir</td><td>Tir</td><td>Tir</td></tr><tr><td>EST</td><td>—</td><td>Select</td><td>Select</td></tr><tr><td>OUEST</td><td>Tir des paddles (stella2014)</td><td>Bouton du Booster Grip</td><td>—</td></tr><tr><td>NORD</td><td>—</td><td>2e bouton du Booster Grip</td><td>—</td></tr><tr><td>START</td><td>Reset (lance la partie)</td><td>Reset (lance la partie)</td><td>Reset (lance la partie)</td></tr><tr><td>SELECT</td><td>Select</td><td>—</td><td>—</td></tr><tr><td>L1</td><td>Difficulté gauche A</td><td>Difficulté gauche (bascule)</td><td>—</td></tr><tr><td>R1</td><td>Difficulté droite A</td><td>Difficulté droite (bascule)</td><td>—</td></tr><tr><td>L2</td><td>Difficulté gauche B</td><td>—</td><td>—</td></tr><tr><td>R2</td><td>Difficulté droite B</td><td>—</td><td>—</td></tr><tr><td>L3</td><td>Couleur</td><td>Couleur / Noir et blanc (bascule)</td><td>—</td></tr><tr><td>R3</td><td>Noir et blanc</td><td>—</td><td>—</td></tr></tbody></table>

Avec Stella et BizHawk, le bouton SELECT de la manette sert aux raccourcis : l'interrupteur Select de la console est sur EST.

Les paddles et les manettes de course sont reconnus automatiquement par les deux versions de Stella : jouez au stick gauche ou à la souris. Avec Stella autonome, **CONTRÔLES > UTILISER LA SOURIS COMME CONTRÔLEUR** règle l'usage de la souris.

### Raccourcis

Les cores libretro utilisent les raccourcis standards de RetroArch. BizHawk utilise les raccourcis communs de RetroBat. Stella autonome utilise aussi les raccourcis communs : HOTKEY + SUD ouvre le menu des options, HOTKEY + OUEST / NORD sauvegarde / charge, HOTKEY + haut / bas change d'emplacement, HOTKEY + R3 fait une capture d'écran et HOTKEY + L3 passe en plein écran. Voir la page [**Raccourcis**](../../../../navigation/hotkeys.md).

### Pistolets

Le core stella gère le pistolet de l'Atari (XG-1) pour les quelques jeux qui l'utilisent (Sentinel, Shooting Arcade…). Activez **PISTOLETS > ACTIVER LES PISTOLETS** (lien à ajouter vers la page [**Pistolets**](../../../../controleurs/supported-controllers/lightguns/)). **PISTOLETS > AFFICHER CIBLE** affiche le viseur.

## Dossiers

<table><thead><tr><th width="340.25">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Jeux</td><td><code>roms\atari2600</code></td></tr><tr><td>Cores libretro : sauvegardes instantanées</td><td><code>saves\atari2600\libretro.&#x3C;core></code></td></tr><tr><td>Stella : sauvegardes instantanées</td><td><code>emulators\stella\state</code></td></tr><tr><td>Stella : configuration</td><td><code>emulators\stella\stella.sqlite3</code></td></tr><tr><td>Stella : captures d'écran</td><td><code>screenshots\stella</code></td></tr><tr><td>BizHawk : sauvegardes instantanées</td><td><code>saves\atari2600\bizhawk\sstates\Atari2600Hawk</code></td></tr><tr><td>BizHawk : captures d'écran</td><td><code>screenshots\bizhawk\atari2600</code></td></tr></tbody></table>

## Guides

### Lancer une partie

Sur la vraie console, la partie démarre avec l'interrupteur **Reset** : appuyez sur START. L'interrupteur **Select** choisit le mode de jeu (nombre de joueurs, variante) avant de lancer la partie. La plupart des jeux ont plusieurs dizaines de modes : la notice du jeu les décrit.

### Difficulté

Les interrupteurs de difficulté (A = difficile, B = facile) changent le jeu : taille de la raquette, vitesse des ennemis… Dans quelques jeux, l'interrupteur gauche (joueur 1) est indispensable.

* Cores libretro : L1 / L2 (gauche A / B), R1 / R2 (droite A / B).
* Stella : L1 et R1 basculent entre A et B.
* BizHawk : **ÉMULATION > DIFFICULTÉ** (**DÉBUTANT** ou **ADVANCED**), pour les deux interrupteurs.

### RetroAchievements

Les cores stella et stella2014 et BizHawk sont compatibles. Pour plus de détails, voir la page [**RetroAchievements**](../../../../utilisation-avancee/retroachievements.md).

### Autres options utiles

<table><thead><tr><th width="144.5">Émulateur</th><th width="367.25">Option</th><th>Effet</th></tr></thead><tbody><tr><td>core stella</td><td><strong>ÉMULATION > FORMAT VIDÉO ÉMULÉ</strong></td><td>Force NTSC, PAL, SECAM… (automatique par défaut).</td></tr><tr><td>core stella</td><td><strong>RENDU VISUEL > EFFETS TV</strong></td><td>Rendu composite, S-Vidéo, RGB…</td></tr><tr><td>core stella</td><td><strong>RENDU VISUEL > MODE PHOSPHORE</strong></td><td>Mélange les images pour supprimer le scintillement de certains jeux.</td></tr><tr><td>core stella</td><td><strong>VIDÉO > ROGNER LES BORDURES</strong></td><td>Cache les bordures noires.</td></tr><tr><td>core stella2014</td><td><strong>RENDU VISUEL > MÉLANGE INTER-IMAGE</strong></td><td>Réduit le scintillement.</td></tr><tr><td>stella</td><td><strong>RENDU VISUEL > FILTRE VIDÉO</strong>, <strong>INTENSITÉ DES LIGNES DE BALAYAGE</strong></td><td>Filtres TV et lignes de balayage.</td></tr><tr><td>stella</td><td><strong>CONTRÔLES > TIR AUTOMATIQUE</strong></td><td>Tir automatique, de 5 à 30 coups par seconde.</td></tr><tr><td>stella</td><td><strong>ÉMULATION > SAUVEGARDER EN QUITTANT</strong></td><td>Sauvegarde la partie en quittant et la recharge au lancement suivant.</td></tr></tbody></table>

## Problèmes connus

<table><thead><tr><th width="337.75">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Le jeu reste sur l'écran titre</td><td>Appuyez sur START (Reset).</td></tr><tr><td>Le jeu scintille</td><td><strong>MODE PHOSPHORE</strong> (core stella) ou <strong>MÉLANGE INTER-IMAGE</strong> (core stella2014). Certains jeux affichent leurs objets une image sur deux, comme sur la vraie console.</td></tr><tr><td>Un jeu à paddles est injouable à la croix</td><td>Utilisez le stick gauche ou la souris.</td></tr><tr><td>Le jeu est trop difficile ou trop facile</td><td>Changez les interrupteurs de difficulté (voir <a href="atari-2600.md#difficulte"><strong>Difficulté</strong></a>).</td></tr></tbody></table>







<div align="left"><figure><img src="https://i.imgur.com/OP8tnMg.png" alt=""><figcaption></figcaption></figure></div>

## Information spécifique du système

Aucune information spécifique.
