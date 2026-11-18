---
description: Capcom
---

# CPS II

<div align="left"><figure><img src="../../../../.gitbook/assets/image (655).png" alt=""><figcaption></figcaption></figure></div>

## Présentation

Le **CP System II** (**CPS-2**) succède au CPS-1 en 1993. Il est utilisé jusqu'en 2003 par plus de 40 jeux, surtout des jeux de combat et des beat'em up :

* **Super Street Fighter II Turbo**, les **Street Fighter Alpha**, **Darkstalkers** (Vampire), **X-Men: Children of the Atom**, **Marvel vs. Capcom** ;
* **Dungeons & Dragons: Tower of Doom** et **Shadow over Mystara**, **Alien vs. Predator**, **Armored Warriors**, **Battle Circuit** ;
* les shoot'em up verticaux **19XX**, **1944**, **Giga Wing**, **Mars Matrix**, **Progear**.

Les cartouches CPS-2 sont chiffrées, et une pile garde la clé de déchiffrement. Les romsets actuels contiennent des copies déchiffrées ou les clés : rien à faire de votre côté.

Dans RetroBat, ces jeux peuvent aussi être rangés dans le système FinalBurn Neo (voir la page [**FinalBurn Neo**](../final-burn-neo.md)).

{% embed url="https://fr.wikipedia.org/wiki/CP_System_II" %}

## En bref

<table><thead><tr><th width="272.75"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\cps2</code></td></tr><tr><td><strong>Extensions</strong></td><td>.zip .7z</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: fbneo</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro ; FBNeo par raccourcis</td></tr><tr><td><strong>RetroAchievements</strong></td><td>cores libretro (fbneo conseillé)</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>cores libretro</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="181.5">Émulateur</th><th>Pour qui ?</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>libretro: fbneo</strong> (défaut)</td><td>Tout le monde</td><td>La version actuelle de FinalBurn Neo dans RetroArch : très compatible, dispositions pour jeux à 6 boutons, dip switches, meilleurs scores, RetroAchievements, jeu en réseau.</td><td>—</td></tr><tr><td><strong>libretro: fbalpha2012_cps2</strong></td><td>PC très modestes, romsets anciens</td><td>Core FB Alpha 2012 dédié au CPS-2, très léger.</td><td>Romset de FB Alpha 0.2.97.28. Ne lit pas le <code>.7z</code>.</td></tr><tr><td><strong>libretro: fbalpha</strong></td><td>Romsets anciens</td><td>FB Alpha 0.2.97.44.</td><td>Romset de sa version, plus mis à jour.</td></tr><tr><td><strong>libretro: fbalpha2012</strong></td><td>Romsets anciens</td><td>FB Alpha 0.2.97.29.</td><td>Romset de sa version.</td></tr><tr><td><strong>fbneo</strong> (autonome)</td><td>Bornes, sticks arcade</td><td>Le FBNeo officiel, boutons réglés jeu par jeu par RetroBat (voir la page <a href="../final-burn-neo.md"><strong>FinalBurn Neo</strong></a>).</td><td>Pas de RetroAchievements ni de jeu en réseau. Sauvegardes instantanées par raccourcis.</td></tr></tbody></table>

**En cas de doute, gardez libretro: fbneo.**

## BIOS

Aucun BIOS n'est nécessaire.

## Quel format de jeu ?

Les jeux sont des romsets `.zip` ou `.7z`, à garder compressés et sous leur nom d'origine (`ssf2t.zip`…). Le romset doit correspondre à la version de l'émulateur :

<table><thead><tr><th width="294">Émulateur</th><th>Version du romset</th></tr></thead><tbody><tr><td>libretro: fbneo, fbneo (autonome)</td><td>Dernière version de FBNeo</td></tr><tr><td>libretro: fbalpha2012_cps2</td><td>FB Alpha 0.2.97.28 (<code>.zip</code> seulement)</td></tr><tr><td>libretro: fbalpha</td><td>FB Alpha 0.2.97.44</td></tr><tr><td>libretro: fbalpha2012</td><td>FB Alpha 0.2.97.29</td></tr></tbody></table>

Le core fbalpha2012\_cps2 n'est pas proposé pour un jeu en `.7z`. Pour le détail des romsets (non-merged, split, merged), voir la page [**Le Guide Arcade**](../../../arcade-guide.md).

## Contrôles

RetroBat configure automatiquement les manettes. **SELECT** met une pièce, **START** lance la partie, le stick gauche et la croix déplacent le joueur.

### Core fbneo

L'option **CONTRÔLES > TYPE DE CONTRÔLEUR** choisit la disposition. Pour les jeux de combat à 6 boutons (Street Fighter Alpha, Darkstalkers…) :

| Manette RetroBat | CLASSIQUE (défaut) | MODERNE      |
| ---------------- | ------------------ | ------------ |
| OUEST            | Poing faible       | Poing faible |
| NORD             | Poing moyen        | Poing moyen  |
| L1               | Poing fort         | —            |
| R1               | Pied fort          | Poing fort   |
| R2               | —                  | Pied fort    |
| SUD              | Pied faible        | Pied faible  |
| EST              | Pied moyen         | Pied moyen   |

Les autres jeux utilisent les boutons de face dans l'ordre : SUD = bouton 1, EST = bouton 2, OUEST = bouton 3, NORD = bouton 4.

**PANNEAU 6 BOUTONS** convient à un stick arcade à deux rangées de trois boutons. Les autres choix sont décrits sur la page [**FinalBurn Neo**](../final-burn-neo.md).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (656).png" alt=""><figcaption></figcaption></figure></div>

### Core fbalpha2012\_cps2

Les boutons sont placés comme avec le core fbneo en CLASSIQUE. **CONTRÔLES > TYPE DE CONTRÔLEUR** : **manette** (défaut, celle du tableau ci-dessus) ou **arcade** (disposition pour stick arcade).

### FBNeo (autonome)

RetroBat règle les boutons jeu par jeu avec le fichier de mappage `fbneo.yml` : voir la page [**FinalBurn Neo**](../final-burn-neo.md).

### Raccourcis

Les cores libretro utilisent les raccourcis standards de RetroArch (voir la page [**Raccourcis**](../../../../navigation/hotkeys.md)). Pour FBNeo autonome, voir la page [**FinalBurn Neo**](../final-burn-neo.md).

## Dossiers

| Contenu                                                              | Dossier                                                                                                                                                                            |
| -------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Jeux                                                                 | `roms\cps2`                                                                                                                                                                        |
| Core fbneo : NVRAM, EEPROM, meilleurs scores                         | `saves\cps2\fbneo`                                                                                                                                                                 |
| Cores fbalpha2012\_cps2, fbalpha, fbalpha2012 : sauvegardes des jeux | `saves\cps2`                                                                                                                                                                       |
| Cores libretro : sauvegardes instantanées                            | `saves\cps2\libretro.<core>`                                                                                                                                                       |
| Fichier des meilleurs scores (`hiscore.dat`)                         | <p><code>bios\fbneo</code> (fbneo)</p><p><code>bios\fba</code> (fbalpha), copié dans <code>bios\fbalpha2012</code> (fbalpha2012_cps2) et <code>saves\cps2</code> (fbalpha2012)</p> |
| FBNeo autonome                                                       | Voir la page [**FinalBurn Neo**](../final-burn-neo.md)                                                                                                                             |

## Guides

### Menu de service et dip switches

Le menu de service de la borne règle la difficulté, le nombre de vies, le jeu gratuit…

* Core fbneo : **START + L1 + R1**, ou une autre combinaison avec **ÉMULATION > ACCÈS AU MENU DIAGNOSTIQUE**.
* **R3** ouvre le menu de service (core fbalpha2012\_cps2).

Les **dip switches** de la carte se règlent dans le menu de RetroArch (**HOTKEY + SUD**), **Options du cœur > Dip switches** (core fbneo). **ÉMULATION > JEU GRATUIT** (core fbneo) règle directement le jeu gratuit quand le jeu le permet.

### Jeux verticaux

Les shoot'em up verticaux (19XX, 1944, Giga Wing, Mars Matrix) s'affichent dans le bon sens, avec une décoration verticale.

* Core fbneo : **VIDÉO > MODE TATÉ** tourne l'image pour un écran posé à la verticale.
* Core fbalpha2012\_cps2 : **VIDÉO > ROTATION AUTOMATIQUE**, activée par défaut, tourne l'image des jeux verticaux. Désactivée, les directions sont tournées pour un écran posé à la verticale.
* FBNeo autonome : **VIDÉO > INDEX DE L'ÉCRAN VERTICAL** affiche les jeux verticaux sur un autre écran.

### Meilleurs scores

**ÉMULATION > ACTIVER HISCORES**, activé par défaut, garde les meilleurs scores des jeux compatibles. RetroBat fournit le fichier `hiscore.dat` à chaque core (voir [**Dossiers**](cp-system-ii.md#dossiers)).

### RetroAchievements

Le core fbneo est le mieux suivi par RetroAchievements pour l'arcade. En mode hardcore, gardez **ÉMULATION > OVERCLOCKING CPU** à 100 % ou plus. Pour plus de détails, voir la page [**RetroAchievements**](../../../../utilisation-avancee/retroachievements.md).

### Autres options utiles

| Émulateur                | Option                           | Effet                                                                       |
| ------------------------ | -------------------------------- | --------------------------------------------------------------------------- |
| fbneo, fbalpha2012\_cps2 | **ÉMULATION > OVERCLOCKING CPU** | Réduit les ralentissements d'origine de certains jeux. Peut créer des bugs. |
| fbneo                    | **VIDÉO > FORCER 60HZ**          | Force les jeux à 60 Hz (fréquence d'origine : environ 59,6 Hz).             |
| fbalpha2012\_cps2        | **VIDÉO > SAUT D'IMAGE**         | Saute des images sur un PC trop lent.                                       |
| fbneo                    | **AUDIO > FILTRE PASSE-BAS**     | Adoucit le son.                                                             |
| fbalpha2012\_cps2        | **AUDIO > FILTRE AUDIO**         | Adoucit le son (de 0 à 95 %).                                               |

## Problèmes connus

| Problème                                    | Solution                                                                                                                       |
| ------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| Le jeu ne démarre pas, ou un fichier manque | Le romset ne correspond pas à la version de l'émulateur (voir [**Quel format de jeu ?**](cp-system-ii.md#quel-format-de-jeu)). |
| Le core fbalpha2012\_cps2 n'est pas proposé | Le jeu est en `.7z` : ce core ne lit que le `.zip`.                                                                            |
| Les meilleurs scores ne sont pas gardés     | Le jeu n'est pas dans `hiscore.dat`, ou **ACTIVER HISCORES** est désactivé. Ils ne sont pas gardés en jeu en réseau.           |
| RetroAchievements passe en mode normal      | **OVERCLOCKING CPU** est sous 100 %, ou des codes de triche sont actifs.                                                       |
