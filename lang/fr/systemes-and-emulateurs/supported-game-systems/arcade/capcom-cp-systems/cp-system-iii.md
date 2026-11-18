---
description: Capcom
---

# CPS III

<div align="left"><figure><img src="../../../../.gitbook/assets/image (658).png" alt=""><figcaption></figcaption></figure></div>

## Présentation

Le **CP System III** (**CPS-3**) est la dernière carte d'arcade de Capcom, sortie en 1996. Les jeux étaient livrés sur CD-ROM, avec une cartouche de sécurité. Seuls six jeux l'utilisent, tous en 2D :

* **Street Fighter III** : New Generation, 2nd Impact et 3rd Strike ;
* **JoJo's Venture** et **JoJo's Bizarre Adventure: Heritage for the Future** ;
* **Red Earth** (Warzard au Japon).

Les romsets actuels contiennent le jeu complet (BIOS compris) dans un seul fichier `.zip` : il n'y a pas de CD ni de fichier `.chd` à fournir.

Dans RetroBat, ces jeux peuvent aussi être rangés dans le système FinalBurn Neo (voir la page [**FinalBurn Neo**](../final-burn-neo.md)).

{% embed url="https://fr.wikipedia.org/wiki/CP_System_III" %}

## En bref

<table><thead><tr><th width="265.25"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\cps3</code></td></tr><tr><td><strong>Extensions</strong></td><td>.zip .7z .decomp</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: fbneo</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro ; FBNeo par raccourcis</td></tr><tr><td><strong>RetroAchievements</strong></td><td>cores libretro (fbneo conseillé)</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>cores libretro</td></tr></tbody></table>

## Quel émulateur choisir ?

| Émulateur                       | Pour qui ?                        | Points forts                                                                                                                                                                 | Limites                                                                                |
| ------------------------------- | --------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| **libretro: fbneo** (défaut)    | Tout le monde                     | La version actuelle de FinalBurn Neo dans RetroArch : très compatible, dispositions pour jeux à 6 boutons, dip switches, meilleurs scores, RetroAchievements, jeu en réseau. | —                                                                                      |
| **libretro: fbalpha2012\_cps3** | PC très modestes, romsets anciens | Core FB Alpha 2012 dédié au CPS-3, très léger.                                                                                                                               | Romset de FB Alpha 0.2.97.29. Ne lit pas le `.7z`.                                     |
| **libretro: fbalpha**           | Romsets anciens                   | FB Alpha 0.2.97.44.                                                                                                                                                          | Romset de sa version, plus mis à jour.                                                 |
| **libretro: fbalpha2012**       | Romsets anciens                   | FB Alpha 0.2.97.29.                                                                                                                                                          | Romset de sa version.                                                                  |
| **fbneo** (autonome)            | Bornes, sticks arcade             | Le FBNeo officiel, boutons réglés jeu par jeu par RetroBat (voir la page [**FinalBurn Neo**](../final-burn-neo.md)).                                                         | Pas de RetroAchievements ni de jeu en réseau. Sauvegardes instantanées par raccourcis. |

**En cas de doute, gardez libretro: fbneo.**

## BIOS

Aucun BIOS n'est nécessaire. Le BIOS de la carte CPS-3 est inclus dans le romset de chaque jeu.

## Quel format de jeu ?

Les jeux sont des romsets `.zip` ou `.7z`, à garder compressés et sous leur nom d'origine (`sfiii3.zip`…). Le romset doit correspondre à la version de l'émulateur :

<table><thead><tr><th width="295.25">Émulateur</th><th>Version du romset</th></tr></thead><tbody><tr><td>libretro: fbneo, fbneo (autonome)</td><td>Dernière version de FBNeo</td></tr><tr><td>libretro: fbalpha2012_cps3</td><td>FB Alpha 0.2.97.29 (<code>.zip</code> seulement)</td></tr><tr><td>libretro: fbalpha</td><td>FB Alpha 0.2.97.44</td></tr><tr><td>libretro: fbalpha2012</td><td>FB Alpha 0.2.97.29</td></tr></tbody></table>

Le core fbalpha2012\_cps3 n'est pas proposé pour un jeu en `.7z`. Pour le détail des romsets (non-merged, split, merged), voir la page [**Le Guide Arcade**](../../../arcade-guide.md).

L'extension `.decomp` correspond aux portages PC, voir la page [**Recompilations**](../../autres/recomp.md).

## Contrôles

RetroBat configure automatiquement les manettes. **SELECT** met une pièce, **START** lance la partie, le stick gauche et la croix déplacent le joueur.

### Core fbneo

L'option **CONTRÔLES > TYPE DE CONTRÔLEUR** choisit la disposition. Pour les jeux de combat à 6 boutons (Street Fighter III, JoJo, Red Earth) :

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

<div align="left"><figure><img src="../../../../.gitbook/assets/image (659).png" alt=""><figcaption></figcaption></figure></div>

### Core fbalpha2012\_cps3

Les boutons sont placés comme avec le core fbneo en CLASSIQUE. **CONTRÔLES > TYPE DE CONTRÔLES JOUEUR 1 / 2** : **manette** (défaut, celle du tableau ci-dessus) ou **arcade** (disposition pour stick arcade).

* **BOUTONS LATÉRAUX JOUEUR 1 / 2** : **L1/R1** (défaut) ou **R1/R2** pour le poing et le pied forts.

### FBNeo (autonome)

RetroBat règle les boutons jeu par jeu avec le fichier de mappage `fbneo.yml` : voir la page [**FinalBurn Neo**](../final-burn-neo.md).

### Raccourcis

Les cores libretro utilisent les raccourcis standards de RetroArch (voir la page [**Raccourcis**](../../../../navigation/hotkeys.md)). Pour FBNeo autonome, voir la page [**FinalBurn Neo**](../final-burn-neo.md).

## Dossiers

| Contenu                                                              | Dossier                                                                                                                                          |
| -------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| Jeux                                                                 | `roms\cps3`                                                                                                                                      |
| Core fbneo : NVRAM, EEPROM, meilleurs scores                         | `saves\cps3\fbneo`                                                                                                                               |
| Cores fbalpha2012\_cps3, fbalpha, fbalpha2012 : sauvegardes des jeux | `saves\cps3`                                                                                                                                     |
| Cores libretro : sauvegardes instantanées                            | `saves\cps3\libretro.<core>`                                                                                                                     |
| Fichier des meilleurs scores (`hiscore.dat`)                         | <p><code>bios\fbneo</code> (fbneo)</p><p><code>bios\fba</code> (fbalpha), copié dans <code>saves\cps3</code> (fbalpha2012_cps3, fbalpha2012)</p> |
| FBNeo autonome                                                       | Voir la page [**FinalBurn Neo**](../final-burn-neo.md)                                                                                           |

## Guides

### Menu de service et dip switches

Le menu de service de la borne règle la difficulté, le nombre de vies, le jeu gratuit…

* Core fbneo : **START + L1 + R1**, ou une autre combinaison avec **ÉMULATION > ACCÈS AU MENU DIAGNOSTIQUE**.
* Avec le core fbalpha2012\_cps3, choisissez une combinaison dans **ÉMULATION > ACCÈS AU MENU DIAGNOSTIQUE** (aucune par défaut).

Les **dip switches** de la carte se règlent dans le menu de RetroArch (**HOTKEY + SUD**), **Options du cœur > Dip switches** (core fbneo). La région des jeux CPS-3 (Japon, Asie, Europe, USA…) se change de la même façon : certains jeux changent de nom ou de contenu selon la région.

### Meilleurs scores

**ÉMULATION > ACTIVER HISCORES**, activé par défaut, garde les meilleurs scores des jeux compatibles. RetroBat fournit le fichier `hiscore.dat` à chaque core (voir [**Dossiers**](cp-system-iii.md#dossiers)).

### RetroAchievements

Le core fbneo est le mieux suivi par RetroAchievements pour l'arcade. En mode hardcore, gardez **ÉMULATION > OVERCLOCKING CPU** à 100 % ou plus. Pour plus de détails, voir la page [**RetroAchievements**](../../../../utilisation-avancee/retroachievements.md).

### Autres options utiles

| Émulateur                | Option                             | Effet                                                                       |
| ------------------------ | ---------------------------------- | --------------------------------------------------------------------------- |
| fbneo, fbalpha2012\_cps3 | **ÉMULATION > OVERCLOCKING CPU**   | Réduit les ralentissements d'origine de certains jeux. Peut créer des bugs. |
| fbneo                    | **VIDÉO > FORCER 60HZ**            | Force les jeux à 60 Hz (fréquence d'origine : environ 59,6 Hz).             |
| fbalpha2012\_cps3        | **VIDÉO > SAUT D'IMAGE**           | Saute des images sur un PC trop lent.                                       |
| fbneo                    | **AUDIO > FILTRE PASSE-BAS**       | Adoucit le son.                                                             |
| fbalpha2012\_cps3        | **AUDIO > TAUX D'ÉCHANTILLONNAGE** | 44 100 Hz par défaut.                                                       |

## Problèmes connus

| Problème                                    | Solution                                                                                                                        |
| ------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| Le jeu ne démarre pas, ou un fichier manque | Le romset ne correspond pas à la version de l'émulateur (voir [**Quel format de jeu ?**](cp-system-iii.md#quel-format-de-jeu)). |
| Le core fbalpha2012\_cps3 n'est pas proposé | Le jeu est en `.7z` : ce core ne lit que le `.zip`.                                                                             |
| Les meilleurs scores ne sont pas gardés     | Le jeu n'est pas dans `hiscore.dat`, ou **ACTIVER HISCORES** est désactivé. Ils ne sont pas gardés en jeu en réseau.            |
| RetroAchievements passe en mode normal      | **OVERCLOCKING CPU** est sous 100 %, ou des codes de triche sont actifs.                                                        |
