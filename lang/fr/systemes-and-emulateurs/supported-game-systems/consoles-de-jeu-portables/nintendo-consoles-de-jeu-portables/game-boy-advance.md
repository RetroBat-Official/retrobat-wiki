---
description: Nintendo
---

# Game Boy Advance

<div align="left"><figure><img src="../../../../.gitbook/assets/image (797).png" alt=""><figcaption></figcaption></figure></div>

## Présentation

La **Game Boy Advance** est la console portable 32 bits de Nintendo, sortie au Japon en mars 2001, puis en Amérique du Nord et en Europe en juin 2001. Plus large que le Game Boy, elle ajoute les gâchettes L et R et un écran couleur plus grand. Elle a été déclinée en **Game Boy Advance SP** (2003, écran éclairé, batterie rechargeable) et en **Game Boy Micro** (2005), pour plus de 80 millions d'exemplaires en tout.

Sa ludothèque mêle créations originales et portages Super Nintendo : Pokémon Rubis, Saphir, Émeraude, Rouge Feu et Vert Feuille, The Legend of Zelda: The Minish Cap, Metroid Fusion et Zero Mission, Advance Wars, Fire Emblem, Golden Sun, Castlevania: Aria of Sorrow, Mario Kart: Super Circuit… Le câble Game Link relie jusqu'à quatre consoles : ces parties ont leur propre système dans RetroBat, [**Game Boy Advance 2 Players**](game-boy-advance-2-players.md).

La console lit aussi les jeux Game Boy et Game Boy Color : ils se rangent dans `roms\gb` et `roms\gbc`.

{% embed url="https://fr.wikipedia.org/wiki/Game_Boy_Advance" %}

## En bref

<table><thead><tr><th width="267.75"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\gba</code></td></tr><tr><td><strong>Extensions</strong></td><td>.gba .zip .7z .decomp</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: mgba</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun avec l'émulateur par défaut (<code>gba_bios.bin</code> nécessaire pour ares, jgenesis et Mesen)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, sauf NO$GBA</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro, BizHawk, jgenesis ; Mesen, Mednafen et ares par raccourcis ; mGBA et NO$GBA par leur menu</td></tr><tr><td><strong>RetroAchievements</strong></td><td>cores libretro, BizHawk</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>cores libretro</td></tr></tbody></table>

## Quel émulateur choisir ?

| Émulateur                   | Pour qui ?               | Points forts                                                                                                                   | Limites                                                                                        |
| --------------------------- | ------------------------ | ------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------- |
| **libretro: mgba** (défaut) | Tout le monde            | Très précis et rapide, aucun fichier à ajouter, capteur solaire, vibrations Game Boy Player, RetroAchievements, jeu en réseau. | —                                                                                              |
| **libretro: mednafen\_gba** | Curieux                  | Version de VBA-M adaptée par Mednafen, capteur solaire.                                                                        | Peu d'options.                                                                                 |
| **libretro: gpsp**          | Petites configurations   | Très léger (recompilateur dynamique), vibrations des cartouches.                                                               | Moins précis.                                                                                  |
| **mgba** (autonome)         | Utilisateurs de mGBA     | mGBA pour Windows : shaders, résolution interne.                                                                               | Pas de RetroAchievements. Sauvegardes instantanées par le menu de mGBA.                        |
| **jgenesis**                | Curieux                  | Émulateur multi-systèmes récent et précis.                                                                                     | `gba_bios.bin` obligatoire. Pas de RetroAchievements.                                          |
| **mesen**                   | Utilisateurs de Mesen    | Mesen 2 : émulation précise et outils de débogage.                                                                             | `gba_bios.bin` obligatoire. Pas de RetroAchievements. Sauvegardes instantanées par raccourcis. |
| **nosgba**                  | Curieux                  | NO$GBA, aussi émulateur Nintendo DS.                                                                                           | Manettes à configurer dans NO$GBA. Pas de RetroAchievements.                                   |
| **mednafen**                | Utilisateurs de Mednafen | Même émulation que le core mednafen\_gba.                                                                                      | Pas de RetroAchievements. Sauvegardes instantanées par raccourcis.                             |
| **ares**                    | Puristes                 | Émulation très précise.                                                                                                        | `gba_bios.bin` obligatoire. Pas de RetroAchievements. Sauvegardes instantanées par raccourcis. |
| **bizhawk: mGBA**           | Utilisateurs de BizHawk  | RetroAchievements, sauvegardes instantanées dans le menu de RetroBat.                                                          | —                                                                                              |

**En cas de doute, gardez libretro: mgba.**

## BIOS

L'émulateur par défaut (mgba) et la plupart des autres n'ont pas besoin du BIOS : ils en émulent les fonctions. Le BIOS d'origine affiche le logo Game Boy au démarrage et améliore la compatibilité de quelques jeux.

ares, jgenesis et Mesen ne démarrent pas les jeux sans lui.

<table><thead><tr><th width="144">Fichier</th><th width="218.75">Description</th><th width="74">Dossier</th><th>md5</th></tr></thead><tbody><tr><td><code>gba_bios.bin</code></td><td>BIOS de la Game Boy Advance</td><td><code>bios</code></td><td>a860e8c0b6d573d191e4ec7db1b1e4f6</td></tr></tbody></table>

Ce fichier est optionnel (sauf pour ares, jgenesis et Mesen) et contrôlé par RetroBat. Avec gpsp, choisissez **ÉMULATION > BIOS > EXTERNE** pour l'utiliser ; avec Mednafen, **ÉMULATION > UTILISER LE BIOS EXTERNE**. **ÉMULATION > SAUTER LE BIOS** (mgba, mGBA, jgenesis, BizHawk) ou **PASSER L'ANIMATION** (Mesen) évite l'écran de démarrage.

## Quel format de jeu ?

<table><thead><tr><th width="189">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.gba</strong></td><td>Image d'une cartouche Game Boy Advance.</td></tr><tr><td><strong>.zip</strong>, <strong>.7z</strong></td><td>Un jeu compressé (un jeu par archive).</td></tr></tbody></table>

## Contrôles

RetroBat configure automatiquement les manettes pour tous les émulateurs sauf NO$GBA. Les boutons gardent la place qu'ils ont sur la manette Super Nintendo :

<table><thead><tr><th width="244">Manette RetroBat</th><th>Game Boy Advance</th></tr></thead><tbody><tr><td>Croix directionnelle</td><td>Croix directionnelle</td></tr><tr><td>SUD</td><td>B</td></tr><tr><td>EST</td><td>A</td></tr><tr><td>L1</td><td>L</td></tr><tr><td>R1</td><td>R</td></tr><tr><td>SELECT</td><td>SELECT</td></tr><tr><td>START</td><td>START</td></tr></tbody></table>

Certains émulateurs ajoutent des boutons turbo ou les touches du capteur solaire (Boktai) :

| Émulateur                                                                                | Schéma                                                                              |
| ---------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| core mgba, Mesen                                                                         | <img src="../../../../.gitbook/assets/image (802).png" alt="" data-size="original"> |
| core mednafen\_gba                                                                       | <img src="../../../../.gitbook/assets/image (801).png" alt="" data-size="original"> |
| core gpsp                                                                                | <img src="../../../../.gitbook/assets/image (800).png" alt="" data-size="original"> |
| Mednafen                                                                                 | <img src="../../../../.gitbook/assets/image (799).png" alt="" data-size="original"> |
| mGBA, ares, jgenesis, BizHawk (avec **CONTRÔLES > ACTIVER TURBO** : schéma du core mgba) | <img src="../../../../.gitbook/assets/image (798).png" alt="" data-size="original"> |

Pour retrouver les lettres de votre manette (A en bas, B à droite), activez **CONTRÔLES > INVERSER LES BOUTONS A/B/X/Y** (tous les émulateurs sauf NO$GBA).

### Raccourcis

Les cores libretro utilisent les raccourcis standards de RetroArch (voir la page [**Raccourcis**](../../../../navigation/hotkeys.md)).

Mesen, Mednafen, ares, jgenesis et BizHawk utilisent les raccourcis de RetroBat :

| Action                          | Manette             | Clavier          |
| ------------------------------- | ------------------- | ---------------- |
| Quitter                         | HOTKEY + START      | `Échap`          |
| Pause                           | HOTKEY + SUD        | `P`              |
| Sauvegarde instantanée          | HOTKEY + OUEST      | `F2`             |
| Chargement                      | HOTKEY + NORD       | `F4`             |
| Emplacement précédent / suivant | HOTKEY + Bas / Haut | `F6` / `F7`      |
| Rembobiner (si activé)          | HOTKEY + Gauche     | `Retour arrière` |
| Avance rapide (maintenir)       | HOTKEY + Droite     | `L`              |
| Capture d'écran                 | HOTKEY + R3         | `F8`             |
| Plein écran                     | HOTKEY + L3         | `F`              |

jgenesis n'a pas de raccourci pour la capture d'écran. Avec mGBA et NO$GBA, seul HOTKEY + START (quitter) est configuré : les sauvegardes instantanées se font depuis leur menu.

## Dossiers

<table><thead><tr><th width="360.25">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Cores libretro, mGBA, Mesen, Mednafen, NO$GBA : sauvegardes des jeux</td><td><code>saves\gba</code></td></tr><tr><td>Cores libretro : sauvegardes instantanées</td><td><p><code>saves\gba\libretro.&#x3C;core></code></p><p>(ex. <code>saves\gba\libretro.mgba</code>)</p></td></tr><tr><td>mGBA : sauvegardes instantanées</td><td><code>saves\gba\mgba\sstates</code></td></tr><tr><td>Mesen : sauvegardes instantanées</td><td><code>saves\gba\mesen\SaveStates</code></td></tr><tr><td>Mednafen : sauvegardes instantanées</td><td><code>saves\gba\mednafen\sstates</code></td></tr><tr><td>NO$GBA : sauvegardes instantanées</td><td><code>saves\gba\nosgba\sstates</code></td></tr><tr><td>ares : sauvegardes des jeux et instantanées</td><td><code>saves\gba\ares</code></td></tr><tr><td>jgenesis : sauvegardes des jeux</td><td><code>saves\gba\jgenesis</code></td></tr><tr><td>BizHawk : sauvegardes des jeux</td><td><code>saves\gba\bizhawk</code></td></tr><tr><td>BIOS</td><td><code>bios</code> (copié par RetroBat dans <code>emulators\mesen\Firmware</code> pour Mesen)</td></tr><tr><td>Codes de triche</td><td><p><code>cheats\mgba</code> (mGBA)</p><p><code>cheats\mednafen</code> (Mednafen)</p><p><code>cheats\jgenesis</code> (jgenesis)</p><p><code>cheats\bizhawk\gba</code> (BizHawk)</p></td></tr><tr><td>Captures d'écran</td><td><p><code>screenshots\mgba</code></p><p><code>screenshots\mesen</code></p><p><code>screenshots\mednafen</code></p><p><code>screenshots\ares</code></p><p><code>screenshots\bizhawk\gba</code></p></td></tr></tbody></table>

## Guides

### Couleurs de l'écran

L'écran de la première Game Boy Advance n'était pas éclairé : les jeux utilisent des couleurs très vives, criardes sur un écran moderne.

<table><thead><tr><th width="134.5">Émulateur</th><th>Option</th><th>Effet</th></tr></thead><tbody><tr><td>core mgba</td><td><strong>RENDU VISUEL > CORRECTION DES COULEURS</strong></td><td><strong>GBA</strong> : couleurs de l'écran d'origine.</td></tr><tr><td>core gpsp</td><td><strong>RENDU VISUEL > CORRECTION DES COULEURS</strong></td><td>Active ou non la correction.</td></tr><tr><td>jgenesis</td><td><strong>RENDU VISUEL > CORRECTION DES COULEURS</strong></td><td>Couleurs de l'écran d'origine (activé par défaut).</td></tr><tr><td>NO$GBA</td><td><strong>RENDU VISUEL > MODE COULEUR</strong></td><td><strong>RÉTROÉCLAIRAGE</strong> (Game Boy Advance SP, défaut), <strong>SANS RÉTROÉCLAIRAGE</strong>, <strong>FLOU</strong> ou <strong>VIF</strong> (Nintendo DS / DS Lite).</td></tr></tbody></table>

Certains jeux font clignoter des objets pour simuler la transparence : **RENDU VISUEL > MÉLANGE INTER-IMAGE** (cores mgba et gpsp, mGBA) ou **FUSION D'IMAGES** (jgenesis, activé par défaut) reproduit l'écran d'origine.

### Capteur solaire et vibrations

Quelques cartouches embarquent un capteur ou un moteur :

<table><thead><tr><th width="240.75">Cartouche</th><th>Jeux</th><th>Émulateur</th></tr></thead><tbody><tr><td>Capteur solaire</td><td>Boktai 1 à 3</td><td>core mednafen_gba (touches indiquées sur son schéma, voir <strong>Contrôles</strong>), core mgba</td></tr><tr><td>Vibrations</td><td>Drill Dozer, WarioWare: Twisted!</td><td>core gpsp (détection automatique)</td></tr><tr><td>Vibrations Game Boy Player</td><td>Jeux compatibles Game Boy Player (Pokémon Pinball: Ruby &#x26; Sapphire…)</td><td>core mgba : <strong>CONTRÔLES > ACTIVER LES VIBRATIONS</strong> (peut causer des ralentissements)</td></tr></tbody></table>

### Jouer à plusieurs

Les parties par câble Game Link (Mario Kart: Super Circuit, échanges Pokémon, The Legend of Zelda: Four Swords…) se jouent dans le système **Game Boy Advance 2 Players** (`roms\gba2players`) : voir [sa page](game-boy-advance-2-players.md).

### Autres options utiles

<table><thead><tr><th width="127">Émulateur</th><th>Option</th><th>Effet</th></tr></thead><tbody><tr><td>core gpsp</td><td><strong>ÉMULATION > RECOMPILATEUR DYNAMIQUE</strong></td><td>Activé par défaut : beaucoup plus rapide.</td></tr><tr><td>core gpsp</td><td><strong>RENDU VISUEL > DÉSACTIVER LA LIMITE DE SPRITES</strong></td><td>Supprime les clignotements quand beaucoup d'objets sont à l'écran.</td></tr><tr><td>core mgba</td><td><strong>AUDIO > FILTRE AUDIO</strong></td><td>Adoucit le son métallique de certains jeux.</td></tr><tr><td>mGBA</td><td><strong>RÉSOLUTION INTERNE</strong></td><td>Taille de l'image avant les shaders (4X par défaut).</td></tr><tr><td>mGBA</td><td><strong>SHADERS</strong></td><td>Filtres d'image de mGBA (écran AGB-001, AGS-001, LCD…).</td></tr><tr><td>mGBA</td><td><strong>PILOTES > VIDÉO</strong></td><td><strong>OPENGL</strong> (défaut) ou <strong>LOGICIEL</strong>. OpenGL est requis pour les shaders et la résolution interne.</td></tr><tr><td>jgenesis</td><td><strong>AUDIO > INTERPOLATION AUDIO</strong></td><td>Qualité du son.</td></tr></tbody></table>

## Problèmes connus

<table><thead><tr><th width="356.5">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>ares, jgenesis ou Mesen ne démarre pas le jeu</td><td>Ajoutez <code>gba_bios.bin</code> dans <code>bios</code>.</td></tr><tr><td>La manette ne répond pas avec NO$GBA</td><td>RetroBat ne configure pas NO$GBA : réglez les touches dans ses options, ou utilisez un autre émulateur.</td></tr><tr><td>Les couleurs sont trop vives</td><td>Voir <a href="game-boy-advance.md#couleurs-de-lecran"><strong>Couleurs de l'écran</strong></a>.</td></tr><tr><td>Un jeu <code>.gb</code> ou <code>.gbc</code> n'apparaît pas</td><td>Les jeux Game Boy et Game Boy Color se rangent dans <code>roms\gb</code> et <code>roms\gbc</code>.</td></tr><tr><td>Le jeu à plusieurs ne fonctionne pas</td><td>Rangez le jeu dans <code>roms\gba2players</code>.</td></tr></tbody></table>
