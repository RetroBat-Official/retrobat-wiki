---
description: le patch "en douceur"...
---

# Softpatching

Un **patch** est un fichier qui contient des modifications pour une ROM : traduction, corrections de bugs, améliorations, hacks… Le **softpatching** applique le patch au lancement du jeu, en mémoire : votre ROM d'origine n'est jamais modifiée, et vous pouvez jouer avec ou sans le patch.

{% hint style="info" %}
Le softpatching fonctionne avec les **cores RetroArch** qui chargent le jeu en mémoire (surtout les systèmes à cartouches et les consoles portables). Voir la liste des cores compatibles plus bas.
{% endhint %}

## Formats de patchs

<table><thead><tr><th width="144">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>IPS</strong> (<code>.ips</code>)</td><td>Le format le plus ancien et le plus courant. Simple, mais il ne vérifie pas la ROM : un patch appliqué à la mauvaise version de la ROM peut donner un jeu défectueux.</td></tr><tr><td><strong>UPS</strong> (<code>.ups</code>)</td><td>Vérifie que la ROM est la bonne avant d'appliquer le patch. Souvent utilisé pour la Game Boy Advance.</td></tr><tr><td><strong>BPS</strong> (<code>.bps</code>)</td><td>Le format le plus moderne. Vérifie la ROM et le résultat. À privilégier quand il est disponible.</td></tr><tr><td><strong>xdelta</strong> (<code>.xdelta</code>)</td><td>Format utilisé pour les gros fichiers, par exemple certaines traductions de jeux Nintendo DS. Vérifie la ROM avant d'appliquer le patch.</td></tr></tbody></table>

{% hint style="warning" %}
Un patch est conçu pour **une version précise** d'une ROM (région, révision, avec ou sans en-tête). Le fichier « readme » du patch indique en général quelle ROM utiliser. Avec UPS, BPS et xdelta, le patch n'est pas appliqué si la ROM n'est pas la bonne.
{% endhint %}

## Où placer les patchs

Choisissez où RetroBat cherche les patchs avec l'option **SOFTPATCHING** :

* pour tous les systèmes : **MENU PRINCIPAL > PARAMÈTRES DES JEUX**, groupe **OPTIONS RETROARCH** > **ÉMULATION** > **SOFTPATCHING** ;
* pour un système ou un jeu : **OPTIONS AVANCÉES > ÉMULATION > SOFTPATCHING** dans les options du système ou du jeu.

<div align="left"><figure><img src="../.gitbook/assets/image (455).png" alt=""><figcaption></figcaption></figure></div>

| Choix                             | Où placer le patch                                                              | Nom du patch                                |
| --------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------- |
| **AUTO** (par défaut)             | À côté de la ROM                                                                | Même nom que la ROM : `Jeu.sfc` → `Jeu.ips` |
| **PATCH DANS UN DOSSIER PATCH**   | Dans un dossier `patches` à côté des ROMs : `roms\snes\patches\`                | Même nom que la ROM : `patches\Jeu.ips`     |
| **PATCH DANS UN DOSSIER PAR JEU** | Dans un dossier au nom de la ROM suivi de `-patches` : `roms\snes\Jeu-patches\` | N'importe quel nom                          |
| **DÉSACTIVÉ**                     | Aucun patch n'est appliqué, même si un fichier de patch existe.                 |                                             |

Exemple avec AUTO :

```
roms\snes\
   Jeu.sfc
   Jeu.bps
```

Exemple avec PATCH DANS UN DOSSIER PAR JEU :

```
roms\snes\
   Zelda.sfc
   Zelda-patches\
      Traduction.bps
```

{% hint style="info" %}
* Pour une ROM compressée, nommez le patch comme le .zip : `Jeu.zip` → `Jeu.ips`.
* Quand un patch est appliqué, RetroArch affiche un message au lancement du jeu.
* Avec **PATCH DANS UN DOSSIER PAR JEU**, vous pouvez garder plusieurs versions de patchs pour un même jeu, et passer de l'une à l'autre en renommant le dossier.
{% endhint %}

## Appliquer plusieurs patchs

Plusieurs patchs peuvent s'appliquer l'un après l'autre (par exemple une traduction, puis une correction de cette traduction). Numérotez-les à partir du deuxième :

```
Jeu.ips     ← appliqué en premier
Jeu.ips1    ← appliqué en deuxième
Jeu.ips2    ← appliqué en troisième
```

* Jusqu'à 10 patchs : de `Jeu.ips` à `Jeu.ips9`.
* Utilisez le **même format** pour tous les patchs d'un jeu (`.ips`, `.ips1`… ou `.bps`, `.bps1`… ou `.xdelta`, `.xdelta1`…).
* L'ordre compte : respectez l'ordre indiqué par les auteurs des patchs.
* Avec **PATCH DANS UN DOSSIER PAR JEU**, le premier patch peut avoir n'importe quel nom, et les suivants reprennent ce nom avec le numéro : `Traduction.bps`, `Traduction.bps1`…

## Sauvegardes

Un jeu patché utilise le **même fichier de sauvegarde** que le jeu d'origine, car il porte le même nom. Pour séparer les sauvegardes, faites une copie de la ROM sous un autre nom, et nommez le patch comme cette copie.

## Cores compatibles

L'option **SOFTPATCHING** est disponible pour ces cores RetroArch :

<table><thead><tr><th width="241.5">Système</th><th>Cores</th></tr></thead><tbody><tr><td>Nintendo - NES / Famicom</td><td>FCEUmm, Mesen, Nestopia UE, QuickNES</td></tr><tr><td>Nintendo - SNES / Super Famicom, Satellaview</td><td>bsnes, bsnes HD beta, bsnes-jg, bsnes Mercury Accuracy, bsnes Mercury Balanced, Mednafen SNES, Mesen-S, Snes9x, Snes9x 2002, Snes9x 2005, Snes9x 2005 Plus, Snes9x 2010</td></tr><tr><td>Nintendo - Game Boy / Game Boy Color</td><td>DoubleCherryGB, Gambatte, Gearboy, mGBA, SameBoy, TGB Dual, VBA-M</td></tr><tr><td>Nintendo - Game Boy Advance</td><td>mGBA, mGBA splitscreen, Mednafen GBA, VBA-M, VBA Next</td></tr><tr><td>Nintendo - Nintendo DS</td><td>melonDS, melonDS DS</td></tr><tr><td>Nintendo - Nintendo 64</td><td>Mupen64Plus-Next</td></tr><tr><td>Nintendo - Virtual Boy</td><td>Mednafen VB</td></tr><tr><td>Nintendo - Pokémon mini</td><td>PokeMini</td></tr><tr><td>Sega - Master System / Game Gear</td><td>Gearsystem, Genesis Plus GX, PicoDrive, SMS Plus GX</td></tr><tr><td>Sega - Mega Drive / Genesis</td><td>BlastEm, Genesis Plus GX (Wide, Expanded), PicoDrive</td></tr><tr><td>NEC - PC Engine / TurboGrafx-16</td><td>Mednafen PCE, Mednafen PCE Fast</td></tr><tr><td>Bandai - WonderSwan / Color</td><td>Mednafen WonderSwan</td></tr><tr><td>SNK - Neo Geo Pocket / Color</td><td>Mednafen NGP</td></tr><tr><td>Atari - 2600 / 5200 / 7800</td><td>Stella, Stella 2014 (2600), a5200 (5200), ProSystem (7800)</td></tr><tr><td>Atari - Lynx</td><td>Gearlynx, Handy, Holani, Mednafen Lynx</td></tr><tr><td>Atari - Jaguar</td><td>Virtual Jaguar</td></tr><tr><td>Coleco - ColecoVision</td><td>Gearcoleco, JollyCV</td></tr><tr><td>Vectrex</td><td>vecx</td></tr><tr><td>Watara - Supervision</td><td>Potator</td></tr><tr><td>Magnavox - Odyssey²</td><td>O2EM</td></tr><tr><td>Fairchild - Channel F</td><td>FreeChaF</td></tr></tbody></table>

## Problèmes fréquents

<table><thead><tr><th width="264">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Le patch n'est pas appliqué</td><td>Vérifiez le nom du patch (le même que la ROM, sauf avec PATCH DANS UN DOSSIER PAR JEU), son dossier et l'option SOFTPATCHING. Vérifiez que le core figure dans la liste ci-dessus.</td></tr><tr><td>Le jeu est défectueux ou ne démarre pas</td><td>Le patch n'est pas prévu pour cette version de la ROM. Consultez le readme du patch.</td></tr><tr><td>Seul le premier patch est appliqué</td><td>Vérifiez la numérotation : <code>Jeu.ips</code>, puis <code>Jeu.ips1</code>, <code>Jeu.ips2</code>… avec le même format.</td></tr></tbody></table>
