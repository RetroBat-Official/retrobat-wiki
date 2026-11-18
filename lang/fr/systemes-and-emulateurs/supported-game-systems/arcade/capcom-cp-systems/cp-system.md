---
description: Capcom
---

# CPS I

<div align="left"><figure><img src="../../../../.gitbook/assets/image (653).png" alt=""><figcaption></figcaption></figure></div>

## Présentation

Le **CP System** (Capcom Play System, ou **CPS-1**) est la première carte d'arcade de Capcom, sortie en 1988. Une trentaine de jeux l'utilisent jusqu'en 1995, dont beaucoup de classiques :

* les jeux de combat **Street Fighter II** (The World Warrior, Champion Edition, Hyper Fighting) ;
* les beat'em up **Final Fight**, **Captain Commando**, **Knights of the Round**, **The King of Dragons** ;
* les jeux d'action et de tir **Strider**, **Ghouls'n Ghosts**, **Forgotten Worlds**, **1941**, **Mercs**, **U.N. Squadron**.

Les derniers jeux (parfois appelés « CPS-1.5 ») ajoutent la puce son QSound : **Cadillacs and Dinosaurs**, **The Punisher**, **Warriors of Fate**, **Saturday Night Slam Masters**.

Dans RetroBat, ces jeux peuvent aussi être rangés dans le système FinalBurn Neo (voir la page [**FinalBurn Neo**](../final-burn-neo.md)).

{% embed url="https://fr.wikipedia.org/wiki/CP_System" %}

## En bref

<table><thead><tr><th width="277.75"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\cps1</code></td></tr><tr><td><strong>Extensions</strong></td><td>.zip .7z</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: fbneo</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro ; FBNeo par raccourcis</td></tr><tr><td><strong>RetroAchievements</strong></td><td>cores libretro (fbneo conseillé)</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>cores libretro</td></tr></tbody></table>

## Quel émulateur choisir ?

| Émulateur                       | Pour qui ?                        | Points forts                                                                                                                                                                 | Limites                                                                                |
| ------------------------------- | --------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| **libretro: fbneo** (défaut)    | Tout le monde                     | La version actuelle de FinalBurn Neo dans RetroArch : très compatible, dispositions pour jeux à 6 boutons, dip switches, meilleurs scores, RetroAchievements, jeu en réseau. | —                                                                                      |
| **libretro: fbalpha2012\_cps1** | PC très modestes, romsets anciens | Core FB Alpha 2012 dédié au CPS-1, très léger.                                                                                                                               | Romset de FB Alpha 0.2.97.28. Ne lit pas le `.7z`.                                     |
| **libretro: fbalpha**           | Romsets anciens                   | FB Alpha 0.2.97.44.                                                                                                                                                          | Romset de sa version, plus mis à jour.                                                 |
| **libretro: fbalpha2012**       | Romsets anciens                   | FB Alpha 0.2.97.29.                                                                                                                                                          | Romset de sa version.                                                                  |
| **fbneo** (autonome)            | Bornes, sticks arcade             | Le FBNeo officiel, boutons réglés jeu par jeu par RetroBat (voir la page [**FinalBurn Neo**](../final-burn-neo.md)).                                                         | Pas de RetroAchievements ni de jeu en réseau. Sauvegardes instantanées par raccourcis. |

**En cas de doute, gardez libretro: fbneo.**

## BIOS

Aucun BIOS n'est nécessaire.

## Quel format de jeu ?

Les jeux sont des romsets `.zip` ou `.7z`, à garder compressés et sous leur nom d'origine (`sf2ce.zip`…). Le romset doit correspondre à la version de l'émulateur :

<table><thead><tr><th width="301.5">Émulateur</th><th>Version du romset</th></tr></thead><tbody><tr><td>libretro: fbneo, fbneo (autonome)</td><td>Dernière version de FBNeo</td></tr><tr><td>libretro: fbalpha2012_cps1</td><td>FB Alpha 0.2.97.28 (<code>.zip</code> seulement)</td></tr><tr><td>libretro: fbalpha</td><td>FB Alpha 0.2.97.44</td></tr><tr><td>libretro: fbalpha2012</td><td>FB Alpha 0.2.97.29</td></tr></tbody></table>

Le core fbalpha2012\_cps1 n'est pas proposé pour un jeu en `.7z`. Pour le détail des romsets (non-merged, split, merged), voir la page [**Le Guide Arcade**](../../../arcade-guide.md).

## Contrôles

RetroBat configure automatiquement les manettes. **SELECT** met une pièce, **START** lance la partie, le stick gauche et la croix déplacent le joueur.

### Core fbneo

L'option **CONTRÔLES > TYPE DE CONTRÔLEUR** choisit la disposition. Pour les jeux de combat à 6 boutons (Street Fighter II) :

<table><thead><tr><th width="160.75">Manette RetroBat</th><th width="225.5">CLASSIQUE (défaut)</th><th>MODERNE</th></tr></thead><tbody><tr><td>OUEST</td><td>Poing faible</td><td>Poing faible</td></tr><tr><td>NORD</td><td>Poing moyen</td><td>Poing moyen</td></tr><tr><td>L1</td><td>Poing fort</td><td>—</td></tr><tr><td>R1</td><td>Pied fort</td><td>Poing fort</td></tr><tr><td>R2</td><td>—</td><td>Pied fort</td></tr><tr><td>SUD</td><td>Pied faible</td><td>Pied faible</td></tr><tr><td>EST</td><td>Pied moyen</td><td>Pied moyen</td></tr></tbody></table>

Les autres jeux utilisent les boutons de face dans l'ordre : SUD = bouton 1, EST = bouton 2, OUEST = bouton 3, NORD = bouton 4.

**PANNEAU 6 BOUTONS** convient à un stick arcade à deux rangées de trois boutons. Les autres choix sont décrits sur la page [**FinalBurn Neo**](../final-burn-neo.md).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (654).png" alt=""><figcaption></figcaption></figure></div>

### Core fbalpha2012\_cps1

Les boutons sont placés comme avec le core fbneo en CLASSIQUE. Ce core n'a pas d'option de disposition.

### FBNeo (autonome)

RetroBat règle les boutons jeu par jeu avec le fichier de mappage `fbneo.yml` : voir la page [**FinalBurn Neo**](../final-burn-neo.md).

### Raccourcis

Les cores libretro utilisent les raccourcis standards de RetroArch (voir la page [**Raccourcis**](../../../../navigation/hotkeys.md)). Pour FBNeo autonome, voir la page [**FinalBurn Neo**](../final-burn-neo.md).

## Dossiers

<table><thead><tr><th width="337.75">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Jeux</td><td><code>roms\cps1</code></td></tr><tr><td>Core fbneo : NVRAM, EEPROM, meilleurs scores</td><td><code>saves\cps1\fbneo</code></td></tr><tr><td>Cores fbalpha2012_cps1, fbalpha, fbalpha2012 : sauvegardes des jeux</td><td><code>saves\cps1</code></td></tr><tr><td>Cores libretro : sauvegardes instantanées</td><td><code>saves\cps1\libretro.&#x3C;core></code></td></tr><tr><td>Fichier des meilleurs scores (<code>hiscore.dat</code>)</td><td><p><code>bios\fbneo</code> (fbneo)</p><p><code>bios\fba</code> (fbalpha), copié dans <code>bios\fbalpha2012</code> (fbalpha2012_cps1) et <code>saves\cps1</code> (fbalpha2012)</p></td></tr><tr><td>FBNeo autonome</td><td>Voir la page <a href="../final-burn-neo.md"><strong>FinalBurn Neo</strong></a></td></tr></tbody></table>

## Guides

### Menu de service et dip switches

Le menu de service de la borne règle la difficulté, le nombre de vies, le jeu gratuit…

* Core fbneo : **START + L1 + R1**, ou une autre combinaison avec **ÉMULATION > ACCÈS AU MENU DIAGNOSTIQUE**.
* **R3** ouvre le menu de service (core fbalpha2012\_cps1).

Les **dip switches** de la carte se règlent dans le menu de RetroArch (**HOTKEY + SUD**), **Options du cœur > Dip switches** (core fbneo). **ÉMULATION > JEU GRATUIT** (core fbneo) règle directement le jeu gratuit quand le jeu le permet.

### Jeux verticaux

Les shoot'em up verticaux (1941, Mercs, Varth) s'affichent dans le bon sens, avec une décoration verticale.

* Core fbneo : **VIDÉO > MODE TATÉ** tourne l'image pour un écran posé à la verticale.
* Core fbalpha2012\_cps1 : **VIDÉO > ROTATION AUTOMATIQUE**, activée par défaut, tourne l'image des jeux verticaux. Désactivée, les directions sont tournées pour un écran posé à la verticale.
* FBNeo autonome : **VIDÉO > INDEX DE L'ÉCRAN VERTICAL** affiche les jeux verticaux sur un autre écran.

### Meilleurs scores

**ÉMULATION > ACTIVER HISCORES**, activé par défaut, garde les meilleurs scores des jeux compatibles. RetroBat fournit le fichier `hiscore.dat` à chaque core (voir [**Dossiers**](cp-system.md#dossiers)).

### RetroAchievements

Le core fbneo est le mieux suivi par RetroAchievements pour l'arcade. En mode hardcore, gardez **ÉMULATION > OVERCLOCKING CPU** à 100 % ou plus. Pour plus de détails, voir la page [**RetroAchievements**](../../../../utilisation-avancee/retroachievements.md).

### Autres options utiles

<table><thead><tr><th width="228.25">Émulateur</th><th width="259">Option</th><th>Effet</th></tr></thead><tbody><tr><td>fbneo, fbalpha2012_cps1</td><td><strong>ÉMULATION > OVERCLOCKING CPU</strong></td><td>Réduit les ralentissements d'origine de certains jeux. Peut créer des bugs.</td></tr><tr><td>fbneo</td><td><strong>VIDÉO > FORCER 60HZ</strong></td><td>Force les jeux à 60 Hz (fréquence d'origine : environ 59,6 Hz).</td></tr><tr><td>fbalpha2012_cps1</td><td><strong>VIDÉO > SAUT D'IMAGE</strong></td><td>Saute des images sur un PC trop lent.</td></tr><tr><td>fbneo</td><td><strong>AUDIO > FILTRE PASSE-BAS</strong></td><td>Adoucit le son.</td></tr><tr><td>fbalpha2012_cps1</td><td><strong>AUDIO > FILTRE AUDIO</strong></td><td>Adoucit le son (de 0 à 95 %).</td></tr></tbody></table>

## Problèmes connus

<table><thead><tr><th width="332.75">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Le jeu ne démarre pas, ou un fichier manque</td><td>Le romset ne correspond pas à la version de l'émulateur (voir <a href="cp-system.md#quel-format-de-jeu"><strong>Quel format de jeu ?</strong></a>).</td></tr><tr><td>Le core fbalpha2012_cps1 n'est pas proposé</td><td>Le jeu est en <code>.7z</code> : ce core ne lit que le <code>.zip</code>.</td></tr><tr><td>Les meilleurs scores ne sont pas gardés</td><td>Le jeu n'est pas dans <code>hiscore.dat</code>, ou <strong>ACTIVER HISCORES</strong> est désactivé. Ils ne sont pas gardés en jeu en réseau.</td></tr><tr><td>RetroAchievements passe en mode normal</td><td><strong>OVERCLOCKING CPU</strong> est sous 100 %, ou des codes de triche sont actifs.</td></tr></tbody></table>
