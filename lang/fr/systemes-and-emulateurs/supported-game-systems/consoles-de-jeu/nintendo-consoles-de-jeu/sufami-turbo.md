---
description: Bandai
---

# SuFami Turbo

<div align="left"><figure><img src="../../../../.gitbook/assets/image (754).png" alt="" width="441"><figcaption></figcaption></figure></div>

## Présentation

Le **Sufami Turbo** est un adaptateur de Bandai sorti au Japon en juin 1996. Branché dans le port cartouche de la Super Famicom, il accueille deux mini-cartouches, vendues moins cher que les jeux classiques. Une seule suffit pour jouer ; avec deux cartouches compatibles, certains jeux échangent des données ou débloquent des bonus (SD Gundam Generation, SD Ultra Battle).

Treize jeux sont sortis, tous au Japon : la série SD Gundam Generation, Poi Poi Ninja World, Crayon Shin-chan: Nagagutsu Dobon!!, Gegege no Kitarou, Sailor Moon Stars: Fuwa Fuwa Panic 2…

Les jeux se jouent comme des jeux Super Nintendo : les contrôles, les raccourcis et les options des émulateurs sont décrits sur la page [**Super Nintendo**](super-nintendo-entertainment-system-super-famicom.md).

{% embed url="https://fr.wikipedia.org/wiki/Super_Nintendo" %}

## En bref

<table><thead><tr><th width="286.5"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\sufami</code></td></tr><tr><td><strong>Extensions</strong></td><td>.st .fig .bs .smc .sfc .zip .7z</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: snes9x</td></tr><tr><td><strong>BIOS</strong></td><td><code>STBIOS.bin</code> obligatoire</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro ; ares par raccourcis</td></tr><tr><td><strong>RetroAchievements</strong></td><td>cores libretro</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>cores libretro</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="167.75">Émulateur</th><th width="136">Pour qui ?</th><th width="185.75">Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>libretro: snes9x</strong> (défaut)</td><td>Tout le monde</td><td>Rapide et très compatible.</td><td>Une seule cartouche à la fois.</td></tr><tr><td><strong>libretro: bsnes-jg</strong></td><td>Puristes</td><td>Émulation très précise de bsnes.</td><td>Une seule cartouche à la fois.</td></tr><tr><td><strong>ares</strong></td><td>Puristes</td><td>Émulation très précise.</td><td>Une seule cartouche à la fois. Pas de RetroAchievements. Sauvegardes instantanées par raccourcis.</td></tr></tbody></table>

**En cas de doute, gardez libretro: snes9x.**

## BIOS

Les jeux se lancent à travers l'adaptateur Sufami Turbo : son contenu est nécessaire pour tous les émulateurs.

<table><thead><tr><th width="135.25">Fichier</th><th width="208.5">Description</th><th width="79.5">Dossier</th><th>md5</th></tr></thead><tbody><tr><td><code>STBIOS.bin</code></td><td>Adaptateur Sufami Turbo (Japon)</td><td><code>bios</code></td><td>d3a44ba7d42a74d3ac58cb9c14c6a5ca</td></tr></tbody></table>

Ce fichier est obligatoire et contrôlé par RetroBat.

## Quel format de jeu ?

<table><thead><tr><th width="182.75">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.st</strong></td><td>Image d'une mini-cartouche Sufami Turbo.</td></tr><tr><td><strong>.zip</strong>, <strong>.7z</strong></td><td>Un jeu compressé (un jeu par archive).</td></tr></tbody></table>

## Contrôles

RetroBat configure automatiquement les manettes. Les boutons, l'option **INVERSER LES BOUTONS A/B/X/Y** et les raccourcis sont les mêmes que sur la page [**Super Nintendo**](super-nintendo-entertainment-system-super-famicom.md#controles).

## Dossiers

| Contenu                                     | Dossier                                                             |
| ------------------------------------------- | ------------------------------------------------------------------- |
| Cores libretro : sauvegardes des jeux       | `saves\sufami`                                                      |
| Cores libretro : sauvegardes instantanées   | `saves\sufami\libretro.<core>` (ex. `saves\sufami\libretro.snes9x`) |
| ares : sauvegardes des jeux et instantanées | `saves\sufami\ares`                                                 |
| Captures d'écran                            | `screenshots\ares`                                                  |

## Problèmes connus

| Problème                                      | Solution                                                 |
| --------------------------------------------- | -------------------------------------------------------- |
| Le jeu ne démarre pas                         | Vérifiez que `STBIOS.bin` est dans `bios`.               |
| Les bonus à deux cartouches ne s'activent pas | RetroBat ne charge qu'une cartouche à la fois.           |
| Un jeu `.bs` ne démarre pas                   | Les jeux Satellaview se rangent dans `roms\satellaview`. |
