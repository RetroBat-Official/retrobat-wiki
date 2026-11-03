# Le Guide Arcade

<div align="left"><figure><img src="../.gitbook/assets/image (330).png" alt=""><figcaption></figcaption></figure></div>

Les jeux d'arcade sont plus complexes à émuler que les jeux de consoles : chaque borne est différente, et les fichiers des jeux (ROMs) doivent correspondre à l'émulateur utilisé. Ce guide explique l'essentiel : quel système et quel émulateur choisir, ce qu'est un romset, et comment vérifier vos romsets.

## Quel système utiliser ?

Les émulateurs arcade se répartissent en deux familles :

* **Les émulateurs multi-machines** (MAME, FinalBurn Neo…) : ils font tourner des milliers de bornes d'arcade.
* **Les émulateurs dédiés** (Supermodel, Flycast, Demul…) : ils font tourner une famille de cartes arcade (Model 3, Naomi…), généralement avec de meilleures performances.

Dans RetroBat, chaque famille de jeux arcade a son propre dossier dans `roms`. Placez vos jeux dans le dossier qui correspond à l'émulateur et au romset que vous avez.

## Émulateurs multi-machines

<table><thead><tr><th width="122.75">Système</th><th width="127.25">Dossier</th><th>Émulateurs / cores</th><th>Version du romset</th></tr></thead><tbody><tr><td>MAME</td><td><code>roms\mame</code></td><td>MAME (autonome), lr-mame</td><td>MAME 0.289 (version actuelle)</td></tr><tr><td></td><td></td><td>GroovyMAME</td><td>Identique à MAME</td></tr><tr><td></td><td></td><td>lr-mame2016</td><td>MAME 0.174</td></tr><tr><td></td><td></td><td>lr-mame2014</td><td>MAME 0.159</td></tr><tr><td></td><td></td><td>lr-mame2010</td><td>MAME 0.139</td></tr><tr><td></td><td></td><td>lr-mame2003_plus</td><td>MAME 0.78-plus (dernière version)</td></tr><tr><td></td><td></td><td>lr-mame2003, lr-mame2003_midway</td><td>MAME 0.78</td></tr><tr><td></td><td></td><td>lr-mame2000</td><td>MAME 0.37b5</td></tr><tr><td>FinalBurn Neo</td><td><code>roms\fbneo</code></td><td>FBNeo (autonome), lr-fbneo</td><td>Dernière version FBNeo</td></tr><tr><td></td><td></td><td>lr-fbalpha</td><td>FB Alpha 0.2.97.44</td></tr><tr><td></td><td></td><td>lr-fbalpha2012</td><td>FB Alpha 0.2.97.29</td></tr><tr><td>MAME Homebrew</td><td><code>roms\hbmame</code></td><td>HBMAME, lr-mame</td><td>HBMAME</td></tr></tbody></table>

{% hint style="info" %}
* **MAME** est le plus complet : utilisez-le par défaut.
* **FinalBurn Neo** est souvent plus léger et très bon pour les jeux de combat, beat'em up et shoot'em up (CPS, Neo Geo, Cave…).
* Le système **Arcade** permet de mélanger dans un même dossier des jeux pour différents émulateurs : choisissez l'émulateur jeu par jeu avec la [CONFIGURATION AVANCÉE DU JEU](../navigation/configuration-des-systemes-et-des-jeux.md#pour-un-jeu).
{% endhint %}

### Systèmes par famille de cartes

Ces systèmes utilisent les mêmes émulateurs multi-machines, mais regroupent les jeux d'une famille de cartes dans leur propre dossier :

<table><thead><tr><th width="135.75">Système</th><th width="181">Dossier</th><th>Émulateurs / cores</th></tr></thead><tbody><tr><td>CPS-1</td><td><code>roms\cps1</code></td><td>lr-fbneo, lr-fbalpha2012_cps1, lr-fbalpha, lr-fbalpha2012</td></tr><tr><td>CPS-2</td><td><code>roms\cps2</code></td><td>lr-fbneo, lr-fbalpha2012_cps2, lr-fbalpha, lr-fbalpha2012</td></tr><tr><td>CPS-3</td><td><code>roms\cps3</code></td><td>lr-fbneo, lr-fbalpha2012_cps3, lr-fbalpha, lr-fbalpha2012</td></tr><tr><td>CAVE</td><td><code>roms\cave</code></td><td>lr-fbneo, lr-fbalpha, lr-fbalpha2012, lr-mame2003_plus, lr-mame2016, lr-mame, MAME, Demul</td></tr><tr><td>Neo Geo</td><td><code>roms\neogeo</code></td><td>lr-fbneo, lr-geolith (fichiers <code>.neo</code>), lr-fbalpha, lr-fbalpha2012_neogeo, Raine, MAME</td></tr><tr><td>Neo Geo CD</td><td><code>roms\neogeocd</code></td><td>lr-neocd, lr-fbneo, Raine</td></tr><tr><td>Hyper Neo Geo 64</td><td><code>roms\neogeo64</code></td><td>lr-mame, lr-mame2016, MAME</td></tr><tr><td>ST-V</td><td><code>roms\segastv</code></td><td>lr-kronos, lr-mame (toutes versions), Mednafen, MAME</td></tr></tbody></table>

## Émulateurs dédiés

<table><thead><tr><th width="210.75">Borne(s)</th><th width="180.5">Dossier</th><th>Émulateurs</th></tr></thead><tbody><tr><td>Laserdisc (jeux FMV)</td><td><code>roms\daphne</code></td><td>Hypseus, Daphne, Singe 2</td></tr><tr><td>Singe</td><td><code>roms\singe</code></td><td>Hypseus, Singe 2</td></tr><tr><td>ActionMax</td><td><code>roms\actionmax</code></td><td>Hypseus, Singe 2</td></tr><tr><td>DICE</td><td><code>roms\dice</code></td><td>lr-dice</td></tr><tr><td>Sega Model 2</td><td><code>roms\model2</code></td><td>Model 2 Emulator (multi CPU / single CPU), SM2-emu, lr-sm2, lr-mame, MAME</td></tr><tr><td>Sega Model 3</td><td><code>roms\model3</code></td><td>Supermodel, lr-supermodel, Model3-Vulkan</td></tr><tr><td>Atomiswave</td><td><code>roms\atomiswave</code></td><td>Flycast, lr-flycast, Demul</td></tr><tr><td>Sega Naomi</td><td><code>roms\naomi</code></td><td>Flycast, lr-flycast, Demul</td></tr><tr><td>Sega Naomi 2</td><td><code>roms\naomi2</code></td><td>Flycast, lr-flycast, Demul</td></tr><tr><td>Sega Hikaru</td><td><code>roms\hikaru</code></td><td>Odin, Demul</td></tr><tr><td>Gaelco PowerVR</td><td><code>roms\gaelco</code></td><td>Demul, lr-mame, lr-mame2016, lr-mame2014</td></tr><tr><td>Triforce</td><td><code>roms\triforce</code></td><td>Dolphin, lr-dolphin, Dolphin-Triforce, TeknoParrot</td></tr><tr><td>Sega Chihiro</td><td><code>roms\chihiro</code></td><td>xemu-chihiro, Cxbx-Reloaded, TeknoParrot</td></tr><tr><td>Sega Lindbergh</td><td><code>roms\lindbergh</code></td><td>Linuxloader, TeknoParrot</td></tr><tr><td>PSX Arcade (ZN-1/ZN-2…)</td><td><code>roms\psxarcade</code></td><td>ArcadeDuck, PSXMame, Zinc, lr-mame, MAME</td></tr><tr><td>Namco 246/256</td><td><code>roms\namco2x6</code></td><td>PCSX2x6, Play!, TeknoParrot</td></tr><tr><td>Namco 357/369</td><td><code>roms\namco3xx</code></td><td>TeknoParrot</td></tr><tr><td>Arcade sur PC</td><td><code>roms\teknoparrot</code></td><td>TeknoParrot</td></tr></tbody></table>

{% hint style="info" %}
Chaque système a sa propre page dans [Systèmes compatibles](supported-game-systems/), avec les formats de fichiers et les BIOS nécessaires.
{% endhint %}

## Comprendre les romsets

### Vocabulaire

* **ROM, romset** : un jeu d'arcade est généralement un fichier `.zip` qui contient plusieurs fichiers ROM (les puces de la carte d'origine). C'est pourquoi on appelle souvent un jeu d'arcade un **romset**.
* **Version du romset** : chaque version d'émulateur attend des ROMs de **la même version**. Par exemple, lr-mame2000 a besoin de ROMs MAME 0.37b5 : des ROMs MAME 0.139 (pour lr-mame2010) ne fonctionneront pas correctement avec lui, et inversement. **La version de votre romset doit correspondre à l'émulateur ou au core utilisé.**
* **Parent / clone** : un jeu existe souvent en plusieurs versions (régions, révisions, bootlegs). L'une d'elles est le **parent** (par exemple `sf2.zip`), les autres sont des **clones** (`sf2ua.zip`, `sf2j.zip`…). Les clones ne contiennent que les fichiers qui diffèrent du parent.
* **BIOS** : certaines cartes partagent un BIOS, lui aussi stocké sous forme de romset (`neogeo.zip`, `naomi.zip`, `pgm.zip`…). Il doit se trouver dans le même dossier que les jeux (ou dans `bios`, selon l'émulateur).

### Types de romsets

<table><thead><tr><th width="172">Type</th><th>Contenu</th><th>Dans RetroBat</th></tr></thead><tbody><tr><td><strong>Non-merged</strong></td><td>Chaque zip contient tout ce dont le jeu a besoin, y compris les fichiers de son parent. Seuls les BIOS sont à part.</td><td>✅ <strong>Recommandé</strong> : chaque jeu fonctionne seul</td></tr><tr><td><strong>Full non-merged</strong></td><td>Comme non-merged, mais chaque zip contient aussi le BIOS.</td><td>✅ Fonctionne, mais prend plus de place</td></tr><tr><td><strong>Split</strong></td><td>Les clones ne contiennent que leurs propres fichiers : le <strong>zip du parent est obligatoire</strong> dans le même dossier (par exemple <code>sf2ua.zip</code> a besoin de <code>sf2.zip</code>).</td><td>⚠️ Fonctionne si vous gardez les parents</td></tr><tr><td><strong>Merged</strong></td><td>Tous les clones sont dans le zip du parent.</td><td>❌ Non pris en charge : seul le jeu parent apparaît dans RetroBat</td></tr></tbody></table>

{% hint style="warning" %}
* Utilisez des romsets **non-merged** autant que possible.
* **Ne renommez pas** les fichiers zip : les émulateurs et les scrapeurs reconnaissent les jeux grâce au nom du fichier.
* **Ne décompressez pas** les jeux d'arcade.
{% endhint %}

### Vérifier et reconstruire vos romsets

Si un jeu ne démarre pas, la cause la plus fréquente est un romset qui ne correspond pas à la version de l'émulateur. Des outils comme [clrmamepro](https://mamedev.emulab.it/clrmamepro/) vérifient vos romsets à partir d'un **fichier DAT** (la liste officielle des fichiers d'une version d'émulateur) et peuvent les reconstruire au bon format.

1. **Récupérez le fichier DAT** de votre version d'émulateur :
   * MAME : sur [Progetto Snaps](https://www.progettosnaps.net/dats/MAME/), ou générez-le avec MAME : `mame.exe -listxml > mame.xml` (depuis le dossier `emulators\mame`) ;
   * FinalBurn Neo : dans le [dépôt FBNeo](https://github.com/libretro/FBNeo/tree/master/dats) ;
   * anciens cores libretro (mame2003, mame2010, fbalpha2012…) : dans le dépôt de chaque core, ou dans le [guide arcade de libretro](https://docs.libretro.com/guides/arcade-getting-started/).
2. Dans clrmamepro, cliquez sur **Add DatFile**, puis chargez-le.
3. **Settings** : ajoutez votre dossier de ROMs (par exemple `roms\mame`).
4. **Scanner** : vérifiez vos romsets. Les fichiers manquants ou incorrects sont listés.
5. **Rebuilder** : reconstruisez vos romsets au format **non-merged** dans un nouveau dossier, puis copiez-les dans le dossier de RetroBat.

{% hint style="info" %}
Le [guide arcade de libretro](https://docs.libretro.com/guides/arcade-getting-started/) (en anglais) explique les romsets et clrmamepro plus en détail.
{% endhint %}

## Fichiers complémentaires

### Samples

Certains jeux ont besoin de **samples** (sons enregistrés) pour jouer leurs sons. Placez les fichiers zip de samples (par exemple `galaga.zip`) dans le dossier de votre émulateur :

<table><thead><tr><th width="281.5">Émulateur / core</th><th>Dossier</th></tr></thead><tbody><tr><td>MAME (autonome), lr-mame</td><td><code>bios\mame\samples</code></td></tr><tr><td>lr-mame2016</td><td><code>bios\mame2016\samples</code></td></tr><tr><td>lr-mame2014</td><td><code>bios\mame2014\samples</code></td></tr><tr><td>lr-mame2010</td><td><code>bios\mame2010\samples</code></td></tr><tr><td>lr-mame2003_plus</td><td><code>bios\mame2003-plus\samples</code></td></tr><tr><td>lr-mame2003</td><td><code>bios\mame2003\samples</code></td></tr><tr><td>HBMAME</td><td><code>bios\hbmame\samples</code></td></tr><tr><td>FBNeo, lr-fbneo</td><td><code>bios\fbneo\samples</code></td></tr><tr><td>lr-fbalpha2012</td><td><code>bios\fba\samples</code></td></tr></tbody></table>

### Fichiers CHD

Certains jeux d'arcade ont aussi besoin d'un fichier **CHD** (image du disque dur, du CD ou du laserdisc de la borne d'origine).

Placez le fichier CHD dans un dossier qui porte exactement le nom du zip du jeu, à côté du zip. Par exemple, pour `kinst.zip` : `roms\mame\kinst\kinst.chd`.

<div align="left"><figure><img src="../.gitbook/assets/image (331).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
La version du CHD doit aussi correspondre à la version de l'émulateur, comme pour les romsets.
{% endhint %}

## Contrôles arcade

RetroBat utilise les mêmes contrôles arcade pour la plupart des émulateurs arcade :

<table><thead><tr><th width="321.5">Fonction</th><th width="228.25">Manette</th><th>Clavier</th></tr></thead><tbody><tr><td>Insérer une pièce (joueur 1 / joueur 2)</td><td>SELECT</td><td><code>5</code> / <code>6</code></td></tr><tr><td>Start (joueur 1 / joueur 2)</td><td>START</td><td><code>1</code> / <code>2</code></td></tr><tr><td>Test (menu opérateur)</td><td>R3</td><td><code>9</code></td></tr><tr><td>Service (crédit gratuit)</td><td>L3</td><td><code>0</code></td></tr><tr><td>Quitter le jeu</td><td>HOTKEY + START</td><td><code>Échap</code></td></tr></tbody></table>

{% hint style="warning" %}
* Dans **MAME** (autonome), Test et Service sont tous les deux sur **L3 + R3** appuyés en même temps. Au clavier, `0` ouvre le menu de test et `9` ajoute un crédit service.
* Dans certains émulateurs (Model3-Vulkan, Linuxloader…), Test et Service à la manette doivent être activés dans la [CONFIGURATION AVANCÉE DU SYSTÈME](../navigation/configuration-des-systemes-et-des-jeux.md#pour-un-systeme), pour éviter d'ouvrir le menu opérateur par erreur.
{% endhint %}

### Dispositions pour sticks arcade

Pour MAME, lr-mame et FBNeo, RetroBat peut placer les boutons comme sur la borne d'origine, selon votre contrôleur. Choisissez la disposition dans **CONFIGURATION AVANCÉE DU SYSTÈME** > **CONTRÔLES** > **CONTROLLER LAYOUT** :

<table><thead><tr><th width="245.25">Disposition</th><th>Pour</th></tr></thead><tbody><tr><td><strong>CONTROLLER (SNES)</strong></td><td>Une manette (par défaut)</td></tr><tr><td><strong>MODERN 8 BUTTONS</strong></td><td>Stick arcade 8 boutons : X, Y, RB, LB en haut / A, B, RT, LT en bas</td></tr><tr><td><strong>8 BUTTONS ALTERNATIVE</strong></td><td>Stick arcade 8 boutons : X, Y, LB, LT en haut / A, B, RB, RT en bas</td></tr><tr><td><strong>6 BUTTONS</strong></td><td>Stick arcade 6 boutons : X, Y, LB en haut / A, B, RB en bas</td></tr><tr><td><strong>CLASSIC 8 BUTTONS</strong></td><td>Identique à <strong>6 BUTTONS</strong></td></tr></tbody></table>

Voir aussi [Sticks Arcade](../controleurs/supported-controllers/arcade-sticks.md).

### Personnaliser les contrôles arcade

Pour de nombreux émulateurs arcade, RetroBat configure les contrôles **jeu par jeu**, à partir de fichiers de mapping fournis dans `system\resources\inputmapping` :

<table><thead><tr><th width="280.25">Émulateur</th><th>Fichier de mapping</th></tr></thead><tbody><tr><td>MAME (autonome)</td><td><code>mame\&#x3C;jeu>.xml</code> (un fichier par jeu)</td></tr><tr><td>lr-mame et autres cores libretro</td><td><code>libretro_&#x3C;core>.yml</code> (par exemple <code>libretro_mame.yml</code>), <code>libretro_&#x3C;core>_&#x3C;système>.yml</code> (par exemple <code>libretro_flycast_naomi.yml</code>)</td></tr><tr><td>FBNeo (autonome)</td><td><code>fbneo.yml</code></td></tr><tr><td>Flycast (Naomi, Atomiswave)</td><td><code>flycast_Arcade.yml</code></td></tr><tr><td>Supermodel / Model3-Vulkan</td><td><code>supermodel.yml</code> / <code>model3vulkan.yml</code></td></tr><tr><td>SM2-emu</td><td><code>sm2emu.yml</code></td></tr><tr><td>Odin</td><td><code>odin.yml</code></td></tr><tr><td>ArcadeDuck</td><td><code>arcadeduck.yml</code></td></tr><tr><td>Play! (Namco 246/256)</td><td><code>play_Arcade.yml</code></td></tr><tr><td>TeknoParrot</td><td><code>teknoparrot.yml</code></td></tr></tbody></table>

Pour modifier le mapping d'un jeu, **copiez le fichier dans `user\inputmapping`** (avec le même nom et le même sous-dossier, par exemple `user\inputmapping\mame\sf2.xml`) et modifiez la copie : RetroBat utilise votre fichier en priorité. Les fichiers de `system\resources\inputmapping` sont remplacés à chaque mise à jour.

{% hint style="info" %}
* Pour MAME, si aucun fichier n'existe pour un clone, c'est le fichier de son jeu parent qui est utilisé.
* Les mappings des volants sont dans des fichiers séparés (`*_wheels.yml`, dossier `wheels`) : voir [Volants](../controleurs/supported-controllers/volants.md).
{% endhint %}

Guides détaillés : [Configuration des touches par émulateur](../controleurs/configuration-des-touches-specifique-par-emulateur/)

### Liens et références

{% hint style="info" %}
**Crédits**

Une partie de cette page s'appuie sur la documentation libretro : [https://docs.libretro.com/guides/arcade-getting-started/](https://docs.libretro.com/guides/arcade-getting-started/)
{% endhint %}
