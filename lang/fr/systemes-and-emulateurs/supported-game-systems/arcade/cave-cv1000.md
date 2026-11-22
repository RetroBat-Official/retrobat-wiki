---
description: Cave
---

# Cave CV1000

<div align="left"><figure><img src="../../../.gitbook/assets/image (704).png" alt="" width="292"><figcaption></figcaption></figure></div>

## Présentation

**CAVE** est un studio japonais fondé en 1994 par d'anciens membres de Toaplan. Il est le spécialiste des shoot'em up « manic » (ou _danmaku_) : des écrans couverts de projectiles, et un vaisseau qui ne meurt que si son tout petit point central est touché.

Ses jeux sont sortis sur trois générations de cartes d'arcade :

* **cartes CAVE à base de 68000** (1994-2001) : **DonPachi**, **DoDonPachi**, **ESP Ra.De.**, **Guwange**, **Dangun Feveron**, **Uo Poko**, mais aussi **Power Instinct 2** ou **Pretty Soldier Sailor Moon** pour d'autres éditeurs ;
* **IGS PGM** (2002-2003) : **DoDonPachi Dai-Ou-Jou**, **Ketsui**, **Espgaluda** ;
* **CV1000** (2004-2012) : **Mushihimesama**, **Espgaluda II**, **Ibara**, **Muchi Muchi Pork!**, **Mushihimesama Futari**, **Deathsmiles**, **DoDonPachi DaiFukkatsu**, **Akai Katana**, **DoDonPachi SaiDaiOuJou**.

Le dossier `roms\cave` accueille les jeux de ces trois générations. Tous les émulateurs ne les lisent pas toutes.

{% embed url="https://fr.wikipedia.org/wiki/Cave_3rd_Generation" %}

## En bref

<table><thead><tr><th width="262.75"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\cave</code></td></tr><tr><td><strong>Extensions</strong></td><td>.zip .7z</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: fbneo</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (<code>pgm.zip</code> pour les jeux sur PGM)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs (boutons réglés jeu par jeu pour les cores mame, mame2003_plus, MAME et FBNeo autonomes)</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro ; MAME, FBNeo et Demul par raccourcis</td></tr><tr><td><strong>RetroAchievements</strong></td><td>cores fbneo, fbalpha, fbalpha2012 (fbneo conseillé)</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>cores libretro</td></tr></tbody></table>

## Quel émulateur choisir ?

| Émulateur                    | Jeux lus                  | Points forts                                                                                                                                                            | Limites                                                                                                                                   |
| ---------------------------- | ------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| **libretro: fbneo** (défaut) | 68000, PGM, CV1000        | La version actuelle de FinalBurn Neo dans RetroArch : très compatible, peu gourmande, dip switches, meilleurs scores, RetroAchievements, jeu en réseau, retour arrière. | —                                                                                                                                         |
| **libretro: fbalpha**        | 68000                     | FB Alpha 0.2.97.44.                                                                                                                                                     | Romset de sa version. Pas de CV1000.                                                                                                      |
| **libretro: fbalpha2012**    | 68000                     | FB Alpha 0.2.97.29, très léger.                                                                                                                                         | Romset de sa version. Pas de CV1000.                                                                                                      |
| **libretro: mame2003\_plus** | 68000                     | Très léger, boutons réglés jeu par jeu comme lr-mame.                                                                                                                   | Romset MAME 0.78. Pas de CV1000.                                                                                                          |
| **libretro: mame2016**       | 68000, PGM, CV1000        | MAME 0.174.                                                                                                                                                             | Romset de sa version. Plus lent que fbneo sur les jeux CV1000. Pas de boutons réglés jeu par jeu.                                         |
| **libretro: mame**           | 68000, PGM, CV1000        | La version actuelle de MAME, boutons réglés jeu par jeu.                                                                                                                | Plus gourmand.                                                                                                                            |
| **fbneo** (autonome)         | 68000, PGM, CV1000        | Le FBNeo officiel, boutons réglés jeu par jeu, écran séparé possible pour les jeux verticaux.                                                                           | Pas de RetroAchievements ni de jeu en réseau. Sauvegardes instantanées par raccourcis.                                                    |
| **mame64**                   | 68000, PGM, CV1000        | Le MAME officiel, avec tous ses réglages. Ralentissements des jeux CV1000 très proches de la borne.                                                                     | Plus gourmand. Sauvegardes instantanées par raccourcis.                                                                                   |
| **demul**                    | CV1000 (liste ci-dessous) | Autre émulation du CV1000.                                                                                                                                              | Ne lit que les jeux CV1000 de sa liste. Même disposition de boutons pour tous les jeux. Sauvegardes instantanées non gérées par RetroBat. |

**En cas de doute, gardez libretro: fbneo.** Il lit toutes les générations et tourne bien sur un PC modeste.

## BIOS

Les jeux CAVE 68000 et CV1000 n'ont besoin d'aucun BIOS.

Les jeux sur IGS PGM (**DoDonPachi Dai-Ou-Jou**, **Ketsui**, **Espgaluda**) ont besoin du BIOS de la carte, `pgm.zip` (cores fbneo, mame, mame2016, FBNeo et MAME autonomes). Placez-le dans `roms\cave`, à côté des jeux.

RetroBat ne vérifie aucun BIOS pour ce système.

## Quel format de jeu ?

Les jeux sont des romsets `.zip` ou `.7z`, à garder compressés et sous leur nom d'origine (`ddonpach.zip`, `mushisam.zip`…). Le romset doit correspondre à la version de l'émulateur :

<table><thead><tr><th width="342.75">Émulateur</th><th>Version du romset</th></tr></thead><tbody><tr><td>libretro: fbneo, fbneo (autonome)</td><td>Dernière version de FBNeo</td></tr><tr><td>libretro: fbalpha</td><td>FB Alpha 0.2.97.44</td></tr><tr><td>libretro: fbalpha2012</td><td>FB Alpha 0.2.97.29</td></tr><tr><td>libretro: mame2003_plus</td><td>MAME 0.78 (et ajouts de mame2003_plus)</td></tr><tr><td>libretro: mame2016</td><td>MAME 0.174</td></tr><tr><td>libretro: mame, mame64</td><td>Dernière version de MAME</td></tr><tr><td>demul</td><td>Jeux CV1000 de la liste ci-dessous</td></tr></tbody></table>

Les clones ont besoin du jeu parent dans le même dossier. Pour le détail des romsets (non-merged, split, merged), voir la page [**Le Guide Arcade**](../../arcade-guide.md).

**Jeux CV1000 lus par Demul** :

| Romset                                                       | Jeu                                            |
| ------------------------------------------------------------ | ---------------------------------------------- |
| `akatana`                                                    | Akai Katana                                    |
| `deathsml`, `dsmbl`                                          | Deathsmiles, Deathsmiles MegaBlack Label       |
| `ddpdfk`, `ddpdfk10`, `dfkbl`                                | DoDonPachi DaiFukkatsu (1.5, 1.0, Black Label) |
| `ddpsdoj`                                                    | DoDonPachi SaiDaiOuJou                         |
| `espgal2`, `espgal2a`                                        | Espgaluda II                                   |
| `futari10`, `futari15`, `futari15a`, `futaribl`, `futariblj` | Mushihimesama Futari (1.0, 1.5, Black Label)   |
| `ibara`, `ibarao`, `ibarablk`, `ibarablka`                   | Ibara, Ibara Kuro Black Label                  |
| `mmmbanc`                                                    | Medal Mahjong Moukari Bancho                   |
| `mmpork`                                                     | Muchi Muchi Pork!                              |
| `mushisam`, `mushisama`, `mushisamb`                         | Mushihimesama                                  |
| `mushitam`, `mushitama`                                      | Puzzle! Mushihimetama                          |
| `pinkswts`, `pinkswtsa`, `pinkswtsb`, `pinkswtsx`            | Pink Sweets: Ibara Sorekara                    |

## Contrôles

RetroBat configure automatiquement les manettes pour tous les émulateurs. **SELECT** met une pièce, **START** lance la partie, le stick gauche et la croix déplacent le vaisseau.

Dans la plupart des jeux, le **bouton 1** tire (maintenu, il donne selon le jeu un tir concentré ou un laser) et le **bouton 2** lance une bombe. Les jeux CAVE utilisent 2 à 4 boutons.

La place des boutons dépend de l'émulateur :

| Manette RetroBat | Cores fbneo, fbalpha, fbalpha2012, mame2016 ; Demul | Core mame, mame2003\_plus ; MAME et FBNeo autonomes |
| ---------------- | --------------------------------------------------- | --------------------------------------------------- |
| SUD              | Bouton 1                                            | Bouton 2                                            |
| EST              | Bouton 2                                            | Bouton 3                                            |
| OUEST            | Bouton 3                                            | Bouton 1                                            |
| NORD             | Bouton 4                                            | Bouton 4                                            |

* **Core mame, mame2003\_plus, MAME** : boutons réglés jeu par jeu. Un jeu sans configuration dédiée utilise la même disposition par défaut. Pour mame2003\_plus, gardez le type de manette du core en automatique.
* **FBNeo autonome** : boutons réglés jeu par jeu à partir du fichier `fbneo.yml`. Un jeu absent du fichier garde les touches réglées dans FBNeo.
* **Demul** : même disposition pour tous les jeux.

### Sticks arcade

Sur un stick arcade, réglez **CONTRÔLES > DISPOSITION DES BOUTONS** selon votre panneau (core mame, mame2003\_plus, MAME et FBNeo autonomes). Avec le core fbneo, choisissez **CONTRÔLES > TYPE DE CONTRÔLEUR > PANNEAU 6 BOUTONS**. Pour plus de détails, voir la page [**Sticks arcade**](../../../controleurs/supported-controllers/arcade-sticks.md).

<div align="left"><figure><img src="../../../.gitbook/assets/image (705).png" alt=""><figcaption></figcaption></figure></div>

### Raccourcis

Les cores libretro utilisent les raccourcis standards de RetroArch (voir la page [**Raccourcis**](../../../navigation/hotkeys.md)).

**MAME (mame64)**

| Raccourci          | Action                 | Clavier        |
| ------------------ | ---------------------- | -------------- |
| **HOTKEY + START** | Quitter                | ÉCHAP          |
| HOTKEY + SUD       | Menu de MAME           | TAB            |
| HOTKEY + OUEST     | Sauvegarde instantanée | F2             |
| HOTKEY + NORD      | Chargement instantané  | F4             |
| HOTKEY + DROITE    | Avance rapide          | ESPACE         |
| HOTKEY + GAUCHE    | Retour en arrière      | RETOUR ARRIÈRE |
| —                  | Pause                  | P              |

**FBNeo (autonome)**

| Raccourci          | Action                              | Clavier |
| ------------------ | ----------------------------------- | ------- |
| **HOTKEY + START** | Quitter                             | —       |
| HOTKEY + OUEST     | Sauvegarde instantanée              | F2      |
| HOTKEY + NORD      | Chargement instantané               | F4      |
| HOTKEY + HAUT      | Emplacement de sauvegarde suivant   | F7      |
| HOTKEY + BAS       | Emplacement de sauvegarde précédent | F6      |
| HOTKEY + DROITE    | Avance rapide (maintenir)           | L       |
| HOTKEY + SUD       | Pause                               | P       |
| HOTKEY + R3        | Capture d'écran                     | F8      |
| —                  | Afficher / masquer le menu de FBNeo | F1      |

**Demul**

| Raccourci          | Action                          | Clavier |
| ------------------ | ------------------------------- | ------- |
| **HOTKEY + START** | Quitter                         |         |
| **HOTKEY + OUEST** | Sauvegarde instantanée de Demul | F2      |
| **HOTKEY + NORD**  | Chargement instantané de Demul  | F4      |

Les sauvegardes instantanées de MAME, FBNeo et Demul restent dans l'émulateur : elles n'apparaissent pas dans le gestionnaire de sauvegardes.

## Dossiers

<table><thead><tr><th width="359">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Jeux, BIOS <code>pgm.zip</code></td><td><code>roms\cave</code></td></tr><tr><td>Core fbneo : NVRAM, EEPROM, meilleurs scores</td><td><code>saves\cave\fbneo</code></td></tr><tr><td>Cores fbalpha, fbalpha2012 : sauvegardes des jeux</td><td><code>saves\cave</code></td></tr><tr><td>Cores libretro : sauvegardes instantanées</td><td><code>saves\cave\libretro.&#x3C;core></code></td></tr><tr><td>Fichier des meilleurs scores (<code>hiscore.dat</code>)</td><td><code>bios\fbneo</code> (fbneo), <code>bios\fba</code> (fbalpha), copié dans <code>saves\cave</code> (fbalpha2012)</td></tr><tr><td>FBNeo autonome : NVRAM, EEPROM, meilleurs scores</td><td><code>saves\fbneo\fbneo</code></td></tr><tr><td>MAME : NVRAM, sauvegardes instantanées</td><td><p><code>saves\mame\nvram</code></p><p><code>saves\mame\states</code></p></td></tr><tr><td>Demul : NVRAM</td><td><code>saves\cave\demul</code></td></tr><tr><td>Demul : configuration</td><td><p><code>emulators\demul\Demul.ini</code></p><p><code>emulators\demul\padDemul.ini</code></p></td></tr><tr><td>Boutons réglés jeu par jeu</td><td><code>system\resources\inputmapping</code> (copie modifiable dans <code>user\inputmapping</code>)</td></tr></tbody></table>

## Guides

### Jeux verticaux

La plupart des jeux CAVE se jouent sur un écran vertical. Ils s'affichent dans le bon sens, avec une décoration verticale.

* Core fbneo : **VIDÉO > MODE TATÉ** tourne l'image pour un écran posé à la verticale.
* FBNeo autonome : **VIDÉO > INDEX DE L'ÉCRAN VERTICAL** affiche les jeux verticaux sur un autre écran.

### Jeux CV1000 : vitesse et ralentissements

Les jeux CV1000 demandent plus de puissance que les autres. Sur un PC modeste, le son saccade et la musique ralentit.

Sur la borne, les jeux ralentissent quand l'écran se remplit de projectiles : ces ralentissements font partie du jeu.

* **Core fbneo** : les jeux CV1000 ont des dip switches propres à leur émulation (**Speed Hacks**, **Thread Blitter**, **Blitter Timing**, **Blitter Delay**, vitesse du processeur). Ils règlent la vitesse de l'émulation et la reproduction des ralentissements. Ouvrez le menu de RetroArch (**HOTKEY + SUD**), puis **Options du cœur > Dip switches**.
* **MAME (mame64)** : le menu de MAME (**HOTKEY + SUD**) donne accès aux réglages du blitter des jeux CV1000.

### Menu de service et dip switches

Le menu de service de la borne règle la difficulté, le nombre de vies, le jeu gratuit…

* **Core fbneo** : **START + L1 + R1**, ou une autre combinaison avec **ÉMULATION > ACCÈS AU MENU DIAGNOSTIQUE**. Les dip switches se règlent dans **Options du cœur > Dip switches**. **ÉMULATION > JEU GRATUIT** règle directement le jeu gratuit quand le jeu le permet.
* **MAME (mame64)** : **R3** ouvre le menu de test, **L3** sert de bouton Service pour s'y déplacer (au clavier : **0** et **9**).
* **Demul** : **R3** (Test) et **L3** (Service) sur la manette du joueur 1 ; au clavier, **0** et **9** quand aucune manette n'est configurée.
* **FBNeo autonome** : dip switches dans le menu de FBNeo (**F1**, puis **Input > Set dipswitches**).

### Meilleurs scores

**ÉMULATION > ACTIVER HISCORES**, activé par défaut, garde les meilleurs scores des jeux compatibles avec les cores fbneo, fbalpha et fbalpha2012. RetroBat fournit le fichier `hiscore.dat` à chaque core (voir [**Dossiers**](cave-cv1000.md#dossiers)).

### RetroAchievements

Le core fbneo est le mieux suivi par RetroAchievements pour l'arcade. En mode hardcore, gardez **ÉMULATION > OVERCLOCKING CPU** à 100 % ou plus. Pour plus de détails, voir la page [**RetroAchievements**](../../../utilisation-avancee/retroachievements.md).

### Autres options utiles

<table><thead><tr><th width="119.5">Émulateur</th><th>Option</th><th>Effet</th></tr></thead><tbody><tr><td>fbneo</td><td><strong>ÉMULATION > OVERCLOCKING CPU</strong></td><td>Réduit les ralentissements d'origine. Change l'expérience de jeu et peut créer des bugs.</td></tr><tr><td>fbneo</td><td><strong>VIDÉO > SAUT D'IMAGE</strong></td><td>Saute des images sur un PC trop lent.</td></tr><tr><td>fbneo</td><td><strong>AUDIO > FILTRE PASSE-BAS</strong></td><td>Adoucit le son.</td></tr><tr><td>demul</td><td><strong>RÉSOLUTION INTERNE</strong></td><td>Augmente la résolution de rendu.</td></tr><tr><td>demul</td><td><strong>RAPPORT D'ASPECT</strong></td><td>4:3, 16:9 ou étiré.</td></tr><tr><td>demul</td><td><strong>ÉMULATION > MODE D'EXÉCUTION CPU</strong></td><td><strong>DYNAREC</strong> (défaut) pour la vitesse, <strong>INTERPRÉTEUR</strong> pour la compatibilité.</td></tr></tbody></table>

## Problèmes connus

| Problème                                                                 | Solution                                                                                                                                                                    |
| ------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Le jeu ne démarre pas, ou un fichier manque                              | Le romset ne correspond pas à la version de l'émulateur (voir [**Quel format de jeu ?**](cave-cv1000.md#quel-format-de-jeu)), ou le jeu parent d'un clone manque.           |
| Un jeu CV1000 ne démarre pas avec fbalpha, fbalpha2012 ou mame2003\_plus | Ces cores ne lisent pas les jeux CV1000 : utilisez le core fbneo.                                                                                                           |
| Un jeu ne démarre pas avec Demul                                         | Demul ne lit que les jeux CV1000 de sa liste (voir [**Quel format de jeu ?**](cave-cv1000.md#quel-format-de-jeu)).                                                          |
| Ketsui, Espgaluda ou DoDonPachi Dai-Ou-Jou ne démarre pas                | Ajoutez `pgm.zip` dans `roms\cave`.                                                                                                                                         |
| Un jeu CV1000 ralentit, le son saccade                                   | Le PC manque de puissance : utilisez le core fbneo, réglez ses dip switches CV1000 (voir [**Guides**](cave-cv1000.md#menu-de-service-et-dip-switches)) ou **SAUT D'IMAGE**. |
| Les boutons ne sont pas à la même place d'un émulateur à l'autre         | Voir le tableau de [**Contrôles**](cave-cv1000.md#controles).                                                                                                               |
| Les meilleurs scores ne sont pas gardés                                  | **ACTIVER HISCORES** est désactivé, ou le jeu n'est pas dans `hiscore.dat`. Ils ne sont pas gardés en jeu en réseau.                                                        |
