---
description: Sega
---

# Saturn

<div align="left"><figure><img src="../../../../.gitbook/assets/image (465).png" alt=""><figcaption></figcaption></figure></div>

## Présentation

La **Sega Saturn** est une console de salon 32 bits sortie par Sega en novembre 1994 au Japon, puis en 1995 en Amérique du Nord (lancement surprise annoncé lors du premier E3) et en Europe. Elle succède à la Mega Drive et au Mega-CD et affronte directement la PlayStation de Sony, puis la Nintendo 64.

À l'intérieur, la Saturn est réputée pour sa complexité : deux processeurs Hitachi SH-2 qui travaillent en parallèle, deux puces vidéo (le VDP1 dessine les sprites et les polygones, le VDP2 gère les décors qui défilent), un processeur sonore Yamaha piloté par un Motorola 68000 et un processeur dédié au lecteur CD. Cette architecture en fait une reine de la 2D mais la rend difficile à programmer en 3D, et c'est encore aujourd'hui l'une des consoles les plus difficiles à émuler.

La Saturn possède un port cartouche, utilisé pour les cartes de sauvegarde et pour les cartouches d'extension mémoire (1 Mo et 4 Mo) nécessaires à certaines adaptations de jeux d'arcade japonais comme _X-Men vs. Street Fighter_ ou _Metal Slug_.

La console s'est vendue à environ 9 millions d'exemplaires et a été arrêtée en 1998 en occident et en 2000 au Japon. Sa ludothèque compte de nombreux classiques : _Panzer Dragoon Saga_, _NiGHTS into Dreams_, _Virtua Fighter 2_, _Guardian Heroes_, _Radiant Silvergun_, _Burning Rangers_, _Sega Rally Championship_, _Saturn Bomberman_ et beaucoup de jeux de combat et de shoot'em up, dont une grande partie n'est sortie qu'au Japon.

{% embed url="https://fr.wikipedia.org/wiki/Saturn_(console_de_jeux_vid%C3%A9o)" %}

## En bref

<table><thead><tr><th width="270.25"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\saturn</code></td></tr><tr><td><strong>Extensions</strong></td><td>.zip .cue .toc .m3u .ccd .chd .iso .cso .mds .squashfs .decomp</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: kronos</td></tr><tr><td><strong>BIOS</strong></td><td><code>sega_101.bin</code>, <code>mpr-17933.bin</code> ou <code>saturn_bios.bin</code> (au moins un)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro, BizHawk</td></tr><tr><td><strong>RetroAchievements</strong></td><td>cores libretro (sauf yabasanshiro), BizHawk</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>core libretro (mednafen_saturn)</td></tr><tr><td><strong>Pistolets</strong></td><td>cores libretro (kronos, mednafen_saturn, ymir), Mednafen, Kronos, BizHawk</td></tr><tr><td><strong>BIOS optionnels</strong></td><td><code>mpr-18811-mx.ic1</code> (KOF 95), <code>mpr-19367-mx.ic1</code> (Ultraman), <code>mpeg_card.bin</code> (Video CD)</td></tr></tbody></table>

## Quel émulateur choisir ?

RetroBat propose 10 émulateurs pour la Saturn. Si vous hésitez, gardez l'émulateur par défaut (**lr-kronos**) : il fait tourner la plupart des jeux, permet d'augmenter la résolution et gère les RetroAchievements et le jeu en réseau.

<table><thead><tr><th width="230.75">Émulateur</th><th width="288">Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>libretro: kronos</strong> (défaut)</td><td>Bonne compatibilité, résolution interne jusqu'à 8x, RetroAchievements, jeu en réseau</td><td>Quelques défauts graphiques sur de rares jeux</td></tr><tr><td>libretro: mednafen_saturn</td><td>Émulation la plus fidèle (Beetle Saturn), RetroAchievements, jeu en réseau, nombreux types de manettes (3D Pad, Arcade Racer, pistolets)</td><td>Demande un processeur puissant, résolution d'origine uniquement, BIOS de la région du jeu</td></tr><tr><td>libretro: ymir</td><td>Émulateur récent, précis et rapide, RetroAchievements</td><td>Résolution d'origine uniquement</td></tr><tr><td>libretro: yabasanshiro</td><td>Léger, haute résolution</td><td>Compatibilité plus faible</td></tr><tr><td>ymir</td><td>Version standalone de Ymir : très bonne compatibilité, retour arrière, gestionnaire de mémoire (F1)</td><td>2 joueurs maximum</td></tr><tr><td>mednafen</td><td>Même moteur que Beetle Saturn, jusqu'à 12 joueurs</td><td>Pas de support du .chd</td></tr><tr><td>yabasanshiro</td><td>Version standalone de YabaSanshiro, rendu Vulkan</td><td>Compatibilité plus faible</td></tr><tr><td>kronos</td><td>Version standalone de Kronos, haute résolution, pistolets</td><td></td></tr><tr><td>bizhawk: saturnus</td><td>Basé sur Mednafen, outils de jeu assisté (TAS)</td><td>Pas de support du .chd</td></tr><tr><td>ssf</td><td>Émulateur japonais très compatible, fonctionne sans BIOS</td><td>Interface en partie en japonais</td></tr></tbody></table>

## BIOS

### Fichiers BIOS

Copiez les fichiers BIOS dans le dossier `bios` de RetroBat.

<table><thead><tr><th width="172">Fichier BIOS</th><th width="333">MD5</th><th>Utilisé par</th></tr></thead><tbody><tr><td>sega_101.bin</td><td>85ec9ca47d8f6807718151cbcca8b964</td><td>BIOS japonais – Mednafen, BizHawk (jeux japonais), lr-kronos, lr-ymir, Ymir</td></tr><tr><td>mpr-17933.bin</td><td>3240872c70984b6cbfda1586cab68dbe</td><td>BIOS US/EU – Mednafen, BizHawk (jeux américains et européens), lr-kronos, lr-ymir, Ymir</td></tr><tr><td>saturn_bios.bin</td><td>af5828fdff51384f99b3c4926be27762</td><td>lr-kronos, lr-yabasanshiro, lr-ymir, Kronos, YabaSanshiro, Ymir</td></tr><tr><td>mpr-18811-mx.ic1</td><td>255113ba943c92a54facd25a10fd780c</td><td>Cartouche ROM de <em>The King of Fighters '95</em> (optionnel)</td></tr><tr><td>mpr-19367-mx.ic1</td><td>1cd19988d1d72a3e7caa0b73234c96b4</td><td>Cartouche ROM de <em>Ultraman: Hikari no Kyojin Densetsu</em> (optionnel)</td></tr><tr><td>mpeg_card.bin</td><td></td><td>Carte Video CD pour lr-mednafen_saturn (optionnel)</td></tr></tbody></table>

{% hint style="info" %}
RetroBat vérifie qu'au moins un des trois BIOS **sega\_101.bin**, **mpr-17933.bin** ou **saturn\_bios.bin** est présent. Les autres fichiers sont indiqués comme OPTIONAL.
{% endhint %}

### Quel BIOS me faut-il ?

* **Pour faire simple** : copiez **sega\_101.bin** et **mpr-17933.bin** dans le dossier bios. Tous les émulateurs fonctionneront, quelle que soit la région de vos jeux.
* **lr-kronos** (défaut) et **lr-ymir** acceptent n'importe lequel des trois BIOS. **Ymir** choisit automatiquement le BIOS correspondant à la région du jeu parmi les fichiers présents dans le dossier bios.
* **lr-mednafen\_saturn, Mednafen et BizHawk** utilisent le BIOS de la région du jeu : sega\_101.bin pour les jeux japonais, mpr-17933.bin pour les jeux américains et européens.
* **lr-yabasanshiro, Kronos et YabaSanshiro** utilisent saturn\_bios.bin. Kronos et YabaSanshiro se rabattent sur sega\_101.bin ou mpr-17933.bin s'il est absent.
* **SSF** utilise par défaut son BIOS intégré (HLE) et n'a besoin d'aucun fichier.
* Les émulateurs standalone Ymir, Kronos, YabaSanshiro et SSF disposent de l'option **FORCER LE FIRMWARE** (sous-menu ÉMULATION) pour choisir le fichier à utiliser. Kronos, YabaSanshiro et SSF proposent aussi le choix **HLE** (BIOS intégré, moins compatible).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (466).png" alt=""><figcaption></figcaption></figure></div>

### Changer la langue de la console

Beaucoup de jeux Saturn utilisent la langue réglée dans la console, surtout les jeux européens multilingues.

<table><thead><tr><th width="389">Émulateur</th><th>Option (sous-menu ÉMULATION)</th></tr></thead><tbody><tr><td>lr-kronos, lr-mednafen_saturn, lr-yabasanshiro</td><td>LANGUE</td></tr><tr><td>Kronos</td><td>LANGUE DE LA CONSOLE (par défaut : la langue de RetroBat)</td></tr><tr><td>Mednafen</td><td>LANGUE DE LA CONSOLE</td></tr><tr><td>BizHawk</td><td>LANGUE DU BIOS</td></tr></tbody></table>

<div align="left"><figure><img src="../../../../.gitbook/assets/image (468).png" alt=""><figcaption></figcaption></figure></div>

Pour **Ymir** et **YabaSanshiro**, il n'y a pas d'option : activez **LANCER LE BIOS** (sous-menu ÉMULATION), lancez n'importe quel jeu, puis choisissez la langue dans les paramètres de la console. Le réglage est conservé dans la mémoire interne de l'émulateur. Désactivez ensuite LANCER LE BIOS.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (467).png" alt=""><figcaption></figcaption></figure></div>

## Quel format pour les jeux ?

### Formats conseillés

* Le **.chd** est conseillé : un seul fichier compressé par disque. Il fonctionne avec tous les émulateurs sauf **Mednafen** et **BizHawk** (utilisez le .cue avec eux). Si un jeu en .chd ne démarre pas avec SSF, utilisez la version .cue.
* Les formats **.cue/.bin**, **.ccd/.img/.sub**, **.mds/.mdf** et **.iso** sont aussi pris en charge.
* Les archives **.zip / .7z / .squashfs** sont décompressées à chaque lancement, ce qui est plus lent. Préférez le .chd.

### Jeux multi-disques

Utilisez un fichier .m3u pour regrouper les disques d'un jeu. Exemple pour _Panzer Dragoon Saga_ : créez le fichier `Panzer Dragoon Saga.m3u` dans le dossier `roms\saturn` avec ce contenu :

```
Panzer Dragoon Saga (Disc 1).chd
Panzer Dragoon Saga (Disc 2).chd
Panzer Dragoon Saga (Disc 3).chd
Panzer Dragoon Saga (Disc 4).chd
```

RetroBat masque automatiquement de la liste des jeux les disques référencés dans le .m3u.

Pour changer de disque :

* **cores libretro** : utilisez les raccourcis de changement de disque (HOTKEY + L1 pour éjecter/insérer, HOTKEY + L2/R2 pour choisir le disque précédent/suivant).
* **Mednafen** : HOTKEY + R2 sélectionne le disque suivant, HOTKEY + L1 l'éjecte/l'insère.
* **Ymir, Kronos, YabaSanshiro** : choisissez le disque de démarrage avec l'option **NUMÉRO DE DISQUE** (sous-menu ÉMULATION), **SSF** : option **INDEX DISQUE**.

## Contrôles

### Configuration automatique des manettes

RetroBat configure automatiquement vos manettes pour tous les émulateurs Saturn.

<table><thead><tr><th width="231.25">Émulateur</th><th width="187">Configuration auto</th><th>Joueurs</th></tr></thead><tbody><tr><td>cores libretro</td><td>Oui</td><td>Jusqu'à 8 (multitap)</td></tr><tr><td>Ymir</td><td>Oui</td><td>2</td></tr><tr><td>Mednafen</td><td>Oui</td><td>Jusqu'à 12 (multitap)</td></tr><tr><td>Kronos, YabaSanshiro</td><td>Oui</td><td>Jusqu'à 12 (option ADAPTATEUR MULTIJOUEURS)</td></tr><tr><td>BizHawk</td><td>Oui</td><td>Jusqu'à 12</td></tr><tr><td>SSF</td><td>Oui</td><td>Jusqu'à 12</td></tr></tbody></table>

Pour jouer à plus de 2, activez le multitap : **ADAPTATEUR MULTIJOUEURS** (Kronos, YabaSanshiro, Mednafen, lr-kronos, lr-yabasanshiro) ou **MULTITAP PORT 1 / PORT 2** (lr-mednafen\_saturn).

### Disposition par défaut

La manette Saturn possède 6 boutons de façade (A B C / X Y Z) et deux boutons de tranche (L R). Par défaut, RetroBat les place ainsi :

<table><thead><tr><th width="305.25">Manette Saturn</th><th>Votre manette</th></tr></thead><tbody><tr><td>A</td><td>SUD</td></tr><tr><td>B</td><td>EST</td></tr><tr><td>C</td><td>R1</td></tr><tr><td>X</td><td>OUEST</td></tr><tr><td>Y</td><td>NORD</td></tr><tr><td>Z</td><td>L1</td></tr><tr><td>L</td><td>L2</td></tr><tr><td>R</td><td>R2</td></tr><tr><td>START</td><td>START</td></tr><tr><td>Croix</td><td>Croix</td></tr></tbody></table>

<div align="left"><figure><img src="../../../../.gitbook/assets/image (471).png" alt="" width="225"><figcaption></figcaption></figure></div>

### Autres dispositions

L'option **DISPOSITION DES BOUTONS** (sous-menu CONTRÔLES) déplace les 6 boutons de façade, ce qui est pratique pour les jeux de combat :

<table><thead><tr><th>Option</th><th width="95.5">A</th><th width="76.75">B</th><th width="73">C</th><th width="96.75">X</th><th width="99.25">Y</th><th>Z</th></tr></thead><tbody><tr><td>L/R pour Z/C (défaut)</td><td>SUD</td><td>EST</td><td>R1</td><td>OUEST</td><td>NORD</td><td>L1</td></tr><tr><td>L/R pour Y/Z</td><td>OUEST</td><td>SUD</td><td>EST</td><td>NORD</td><td>L1</td><td>R1</td></tr><tr><td>L/R pour X/Z</td><td>OUEST</td><td>SUD</td><td>EST</td><td>L1</td><td>NORD</td><td>R1</td></tr></tbody></table>

L'option **INVERSER GÂCHETTES ET ÉPAULES** utilise LB/RB pour les boutons L et R de la Saturn à la place des gâchettes.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (469).png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../../../../.gitbook/assets/image (470).png" alt="" width="225"><figcaption></figcaption></figure></div>

| Option                 | Schéma de contrôle                                                                                                                                        |
| ---------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| L/R pour Y/Z           | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/saturn_lr_yz.png?raw=true" alt="" data-size="original">                 |
| L/R pour Y/Z (inversé) | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/saturn_lr_yz_invert_triggers.png?raw=true" alt="" data-size="original"> |
| L/R pour X/Z           | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/saturn_lr_xz.png?raw=true" alt="" data-size="original">                 |
| L/R pour X/Z (inversé) | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/saturn_lr_xz_invert_triggers.png?raw=true" alt="" data-size="original"> |

### Utiliser une manette de type Saturn

RetroBat reconnaît la **8BitDo M30** (modes XInput, Switch, DInput et 2.4G) et la configure comme une manette Saturn d'origine. En modes XInput, Switch et DInput, activez **UTILISER UNE MANETTE DE TYPE SATURN** (sous-menu CONTRÔLES). La version 2.4G est configurée automatiquement.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (472).png" alt=""><figcaption></figcaption></figure></div>

Le mapping est enregistré dans le fichier `system\resources\inputmapping\saturnControllers.json` : vous pouvez y ajouter d'autres manettes.

### 3D Pad, Arcade Racer et souris

L'option **TYPE DE CONTRÔLEUR** (sous-menu CONTRÔLES) émule d'autres manettes Saturn :

| Émulateur           | Types disponibles                                                                              |
| ------------------- | ---------------------------------------------------------------------------------------------- |
| lr-mednafen\_saturn | Manette, 3D Pad, Arcade Racer, Mission Stick, souris, Stunner, Twin-Stick, Virtua Gun, clavier |
| lr-ymir             | Manette Saturn, souris, Virtua Gun, 3D Pad, Arcade Racer, Mission Stick                        |
| lr-kronos           | Manette, 3D Pad, volant, souris                                                                |
| lr-yabasanshiro     | Manette Saturn, 3D Pad                                                                         |
| Ymir                | Manette standard, 3D Pad, Shuttle Mouse, Virtua Gun (souris)                                   |

Le 3D Pad est conseillé pour _NiGHTS into Dreams_ et les jeux analogiques. Les volants ne sont pas configurés automatiquement : choisissez **Arcade Racer** et utilisez le stick analogique, ou configurez votre volant dans le menu de RetroArch.

### Pistolets

| Émulateur           | Activation                                                                                       |
| ------------------- | ------------------------------------------------------------------------------------------------ |
| lr-mednafen\_saturn | ACTIVER LES PISTOLETS (sous-menu PISTOLETS) : Virtua Gun, option de cible, Sinden pris en charge |
| lr-ymir             | ACTIVER LES PISTOLETS + TYPE DE PISTOLET (Stunner/Virtua Gun ou souris)                          |
| lr-kronos           | ACTIVER LES PISTOLETS (le pistolet est émulé comme une souris)                                   |
| Kronos              | ACTIVER LES PISTOLETS + PORT DU PISTOLET (port 2 par défaut)                                     |
| Mednafen            | ACTIVER LES PISTOLETS                                                                            |
| BizHawk             | ACTIVER LES PISTOLETS                                                                            |
| Ymir                | TYPE DE CONTRÔLEUR = VIRTUA GUN (MOUSE)                                                          |

### Raccourcis

**Cores libretro** : raccourcis standards de RetroBat (menu, sauvegardes d'état, retour arrière, avance rapide, capture d'écran, changement de disque…).

**Émulateurs standalone** :

<table><thead><tr><th>Raccourci</th><th width="116.75">Ymir</th><th width="106.75">Mednafen</th><th width="96.75">BizHawk</th><th width="86.75">Kronos</th><th width="121.75">YabaSanshiro</th><th>SSF</th></tr></thead><tbody><tr><td>HOTKEY + START</td><td>Quitter</td><td>Quitter</td><td>Quitter</td><td>Quitter</td><td>Quitter</td><td>Quitter</td></tr><tr><td>HOTKEY + SUD</td><td>Paramètres de Ymir</td><td>Pause</td><td>Pause</td><td></td><td></td><td></td></tr><tr><td>HOTKEY + OUEST</td><td>Sauvegarder l'état</td><td>Sauvegarder l'état</td><td>Sauvegarder l'état</td><td></td><td>Sauvegarder (slot 1)</td><td></td></tr><tr><td>HOTKEY + NORD</td><td>Charger l'état</td><td>Charger l'état</td><td>Charger l'état</td><td></td><td>Charger (slot 1)</td><td></td></tr><tr><td>HOTKEY + HAUT / BAS</td><td></td><td>Changer de slot</td><td>Changer de slot</td><td></td><td></td><td></td></tr><tr><td>HOTKEY + GAUCHE</td><td>Retour arrière (TAMPON DE RETOUR ARRIÈRE)</td><td>Retour arrière</td><td>Retour arrière</td><td></td><td></td><td></td></tr><tr><td>HOTKEY + DROITE</td><td>Avance rapide</td><td>Avance rapide</td><td>Avance rapide</td><td></td><td></td><td></td></tr><tr><td>HOTKEY + R3</td><td>Capture d'écran</td><td>Capture d'écran</td><td>Capture d'écran</td><td>Capture d'écran</td><td>Capture d'écran</td><td></td></tr><tr><td>HOTKEY + L3</td><td>Plein écran</td><td>Plein écran</td><td>Plein écran</td><td>Plein écran</td><td>Plein écran</td><td></td></tr><tr><td>HOTKEY + L1</td><td></td><td>Éjecter le disque</td><td></td><td></td><td></td><td></td></tr><tr><td>HOTKEY + R2</td><td></td><td>Disque suivant</td><td></td><td></td><td></td><td></td></tr></tbody></table>

{% hint style="info" %}
Avec Ymir, le retour arrière ne fonctionne que si **TAMPON DE RETOUR ARRIÈRE** est activé (sous-menu ÉMULATION).
{% endhint %}

## Dossiers

### Sauvegardes (mémoire interne)

Chaque émulateur utilise ses propres fichiers de sauvegarde : une partie sauvegardée avec un émulateur n'est pas disponible dans un autre, sauf entre lr-kronos et lr-mednafen\_saturn (option **PARTAGER LES SAUVEGARDES AVEC MEDNAFEN** de lr-kronos, activée par défaut).

<table><thead><tr><th width="155.25">Émulateur</th><th>Dossier des sauvegardes</th></tr></thead><tbody><tr><td>cores libretro</td><td><code>saves\saturn</code></td></tr><tr><td>Ymir</td><td><code>saves\saturn\ymir\state</code> (un fichier par jeu avec RAM DE SAUVEGARDE PAR JEU, activée par défaut), <code>saves\saturn\ymir\backup</code> (exports du gestionnaire de mémoire)</td></tr><tr><td>Mednafen</td><td><code>saves\saturn</code></td></tr><tr><td>Kronos</td><td><code>saves\saturn\kronos\bkram.bin</code></td></tr><tr><td>YabaSanshiro</td><td><code>saves\saturn\yabasanshiro\bkram.bin</code></td></tr><tr><td>BizHawk</td><td><code>saves\saturn\bizhawk</code></td></tr><tr><td>SSF</td><td>dossier de l'émulateur (<code>emulators\ssf</code>)</td></tr></tbody></table>

### Sauvegardes d'état et captures d'écran

<table><thead><tr><th width="165.75">Émulateur</th><th>Sauvegardes d'état</th><th>Captures d'écran</th></tr></thead><tbody><tr><td>cores libretro</td><td><code>saves\saturn\libretro.&#x3C;core></code></td><td><code>screenshots</code></td></tr><tr><td>Ymir</td><td><code>saves\saturn\ymir\savestates</code></td><td><code>screenshots\ymir</code></td></tr><tr><td>Mednafen</td><td><code>saves\saturn\mednafen\sstates</code></td><td><code>screenshots\mednafen</code></td></tr><tr><td>Kronos</td><td><code>saves\saturn\kronos\sstates</code></td><td><code>screenshots\kronos</code></td></tr><tr><td>YabaSanshiro</td><td><code>saves\saturn\yabasanshiro\sstates</code></td><td></td></tr><tr><td>BizHawk</td><td><code>saves\saturn\bizhawk\sstates</code></td><td><code>screenshots\bizhawk\saturn</code></td></tr></tbody></table>

### Autres dossiers utiles

* `bios\cdb` : ROM du lecteur CD pour l'option **CD BLOCK BAS NIVEAU** de Ymir (et lr-ymir).
* `emulators\ssf\Setting` : fichiers de réglages personnels de SSF (option **UTILISER MON PROPRE FICHIER DE RÉGLAGES**).

## Guides

### Améliorer les graphismes

* **Résolution plus élevée** : option **RÉSOLUTION INTERNE** avec lr-kronos (jusqu'à 8x), Kronos, YabaSanshiro et lr-yabasanshiro. Beetle Saturn et Ymir affichent uniquement en résolution d'origine.
* **MESH AMÉLIORÉ** : remplace la fausse transparence « en grille » de la Saturn par une vraie transparence (lr-kronos, lr-mednafen\_saturn, Ymir, Kronos).
* **DÉSENTRELACEMENT** : supprime le scintillement des jeux en haute résolution (Ymir, lr-ymir ; lr-mednafen\_saturn : DEINTERLACE MODE).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (473).png" alt=""><figcaption></figcaption></figure></div>

### Cartouches d'extension

Certains jeux ont besoin d'une cartouche dans le port de la console :

* **Cartouches RAM (1 Mo / 4 Mo)** : nécessaires à de nombreux jeux japonais SNK et Capcom (_X-Men vs. Street Fighter_, _Marvel Super Heroes_, _Metal Slug_, _The King of Fighters '96_…). lr-kronos, Kronos, lr-mednafen\_saturn, Ymir et lr-ymir insèrent automatiquement la bonne cartouche pour les jeux connus. Sinon, choisissez-la avec l'option de cartouche (sous-menu ÉMULATION) : **CARTOUCHE ADDITIONNELLE**, **CARTOUCHE**, **TYPE DE CARTOUCHE** ou **CARTE D'EXTENSION** selon l'émulateur.
* **Cartouches ROM** : _The King of Fighters '95_ et _Ultraman: Hikari no Kyojin Densetsu_ ont besoin de leur propre cartouche. Copiez **mpr-18811-mx.ic1** et **mpr-19367-mx.ic1** dans le dossier bios : elles sont chargées automatiquement.
* **Cartouches de sauvegarde** : augmentent la mémoire de sauvegarde.

### Utiliser le menu du BIOS de la console

Activez **LANCER LE BIOS** (sous-menu ÉMULATION de Ymir, Kronos et YabaSanshiro) pour démarrer le BIOS de la console à la place du jeu : vous pouvez alors gérer les sauvegardes de la mémoire interne, régler l'horloge et la langue ou lire des CD audio.

Avec Ymir, le gestionnaire de mémoire est aussi accessible depuis les paramètres de Ymir (HOTKEY + SUD ou F1).

### Réglages de SSF

Par défaut, RetroBat écrit sa propre configuration de SSF et supprime à chaque lancement les réglages par jeu du dossier `emulators\ssf\Setting\Saturn`. Pour utiliser vos propres réglages, activez **UTILISER MON PROPRE FICHIER DE RÉGLAGES** : RetroBat ne modifie alors plus rien dans la configuration de SSF (manettes comprises).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (474).png" alt=""><figcaption></figcaption></figure></div>

## Problèmes connus

<table><thead><tr><th width="326.5">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Écran noir ou erreur au lancement</td><td>Vérifiez les BIOS (VÉRIFIER LES BIOS MANQUANTS). Avec lr-mednafen_saturn, Mednafen et BizHawk, ajoutez le BIOS de la région du jeu.</td></tr><tr><td>Le jeu demande une cartouche d'extension ou se bloque sur l'écran titre</td><td>Choisissez une cartouche RAM 4 Mo dans l'option de cartouche, ou utilisez lr-kronos / Ymir qui l'insèrent automatiquement.</td></tr><tr><td><em>KOF '95</em> ou <em>Ultraman</em> ne démarrent pas</td><td>Copiez mpr-18811-mx.ic1 / mpr-19367-mx.ic1 dans le dossier bios.</td></tr><tr><td>Le jeu n'est pas dans la bonne langue</td><td>Voir « Changer la langue de la console ».</td></tr><tr><td>Un jeu en .chd ne démarre pas avec Mednafen ou BizHawk</td><td>Ces émulateurs ne lisent pas le .chd : utilisez la version .cue ou un autre émulateur.</td></tr><tr><td>Ralentissements avec lr-mednafen_saturn</td><td>Beetle Saturn demande un processeur puissant : utilisez lr-kronos ou Ymir.</td></tr><tr><td>Les boutons de la 8BitDo M30 sont mélangés</td><td>Activez UTILISER UNE MANETTE DE TYPE SATURN.</td></tr><tr><td>Mes sauvegardes ont disparu après un changement d'émulateur</td><td>Chaque émulateur a ses propres sauvegardes (voir Dossiers).</td></tr></tbody></table>
