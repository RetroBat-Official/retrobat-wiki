---
description: Sega
---

# Sega Model 1

<div align="left"><figure><img src="../../../../.gitbook/assets/model1.png" alt="" width="525"><figcaption></figcaption></figure></div>

## Présentation

Le **Sega Model 1** est la première carte d'arcade 3D de Sega, sortie en 1992. Conçue par l'équipe AM2 de Yu Suzuki, elle affiche des polygones pleins, sans texture, grâce à un processeur NEC V60 et à un coprocesseur dédié aux calculs de géométrie.

Seuls six jeux sont sortis sur Model 1, mais ils ont marqué l'histoire : **Virtua Racing** (1992), qui a popularisé la 3D en arcade, et **Virtua Fighter** (1993), le premier jeu de combat en 3D. Suivent Star Wars Arcade, Wing War, Virtua Formula (une version de Virtua Racing en cabine géante) et NetMerc, un jeu en réalité virtuelle avec casque. La carte est remplacée dès 1994 par le Model 2.

RetroBat propose quatre émulateurs : **Keisho** (anciennement sm2-emu, un émulateur dédié aux Model 1, 2 et 3), **Supermodel**, et **MAME** en version autonome ou en core libretro.

{% embed url="https://fr.wikipedia.org/wiki/Model_1" %}

## En bref

<table><thead><tr><th width="247.75"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\model1</code></td></tr><tr><td><strong>Extensions</strong></td><td>.zip .7z .decomp</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>Keisho</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (<code>model1io.zip</code> / <code>model1io2.zip</code> selon le romset, voir BIOS)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro, Keisho ; Supermodel et MAME par raccourcis</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>cores libretro (mame)</td></tr><tr><td><strong>Volants</strong></td><td>Keisho, Supermodel</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="169.5">Émulateur</th><th width="305.25">Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>Keisho</strong> (défaut)</td><td>Émulateur dédié aux Model 1, 2 et 3, rapide, résolution augmentée, filtre CRT, retour de force et vibrations, sauvegardes instantanées.</td><td>NetMerc encore préliminaire (presque sans son).</td></tr><tr><td><strong>supermodel</strong></td><td>Lance aussi Virtua Fighter et NetMerc, que MAME n'émule pas encore correctement. Mode écran large.</td><td>Pas de Virtua Formula. Sauvegardes instantanées au clavier uniquement.</td></tr><tr><td><strong>libretro: mame</strong> / <strong>mame64</strong></td><td>Tous les jeux, y compris Virtua Formula.</td><td>Virtua Fighter et NetMerc ne fonctionnent pas. Plus lent.</td></tr></tbody></table>

| Jeu              | Set                                                | Keisho          | Supermodel    | MAME |
| ---------------- | -------------------------------------------------- | --------------- | ------------- | ---- |
| Virtua Racing    | `vr`                                               | ✅               | ✅             | ✅    |
| Virtua Formula   | `vformula`                                         | ✅               | ❌             | ✅    |
| Virtua Fighter   | `vf`                                               | ✅               | ✅             | ❌    |
| Star Wars Arcade | `swa`, `swaj`                                      | ✅               | ✅             | ✅    |
| Wing War         | `wingwar` (+ `wingwaru`, `wingwarj`, `wingwar360`) | ✅               | ✅ (`wingwar`) | ✅    |
| NetMerc          | `netmerc`                                          | ⚠️ préliminaire | ✅             | ❌    |

## BIOS

Le Model 1 n'a pas de BIOS. Les jeux utilisent en revanche la ROM de leur carte d'entrées-sorties, rangée dans une archive à part :

<table><thead><tr><th width="155.75">Fichier</th><th>Jeux</th><th>Utilité</th></tr></thead><tbody><tr><td><code>model1io.zip</code></td><td>Virtua Racing, Virtua Formula, Virtua Fighter, Star Wars Arcade</td><td>MAME (romsets split ou merged), Keisho</td></tr><tr><td><code>model1io2.zip</code></td><td>Wing War, NetMerc</td><td>MAME (romsets split ou merged)</td></tr></tbody></table>

Placez ces archives dans `roms\model1`, à côté des jeux. Avec un romset MAME [**non-merged**](../../../arcade-guide.md#types-de-romsets), elles sont déjà incluses dans chaque jeu. RetroBat les contrôle comme BIOS optionnels.

## Quel format de jeu ?

Les jeux sont des archives `.zip` (ou `.7z`) au format MAME, à garder sans les décompresser et sans les renommer.

* Les clones (`vformula`, `swaj`, `wingwaru`…) ont besoin de leur jeu parent (`vr`, `swa`, `wingwar`) dans le même dossier, sauf avec un romset non-merged.
* Keisho reconnaît les jeux par leur contenu : une archive merged qui contient plusieurs versions lance celle qui porte le nom de l'archive. Il cherche le jeu parent et les archives `model1io` à côté du jeu.

L'extension `.decomp` correspond aux portages PC, voir la page [**Recompilations**](../../autres/recomp.md).

## Contrôles

### Configuration automatique

RetroBat configure automatiquement les manettes pour tous les émulateurs. L'option **AUTOCONFIGURER LES MANETTES** de Keisho et de Supermodel permet de garder sa propre configuration.

<table><thead><tr><th width="289">Borne</th><th>Manette</th></tr></thead><tbody><tr><td>Joystick, volant</td><td>Stick gauche (et croix directionnelle pour le joystick)</td></tr><tr><td>Accélérateur, frein</td><td>R2, L2</td></tr><tr><td>Rapport supérieur / inférieur</td><td>R1 / L1</td></tr><tr><td>Boutons de vue (VR1 à VR4)</td><td>Boutons de face (SUD, EST, OUEST, NORD)</td></tr><tr><td>Start, Coin</td><td>START, SELECT</td></tr><tr><td>Service, Test</td><td>L3, R3</td></tr></tbody></table>

**Par jeu :**

* **Virtua Fighter** : Punch = OUEST, Kick = NORD, Guard = SUD.
* **Star Wars Arcade** : laser = OUEST (ou L2), torpille = EST (ou R2) ; le stick gauche dirige le vaisseau. Le joueur 2 est le canonnier.
* **Wing War** : le stick gauche est le manche ; tirer le stick droit vers soi ou appuyer sur L2 ralentit ; la croix directionnelle change de vue. Avec Supermodel, R1 et L1 font monter et descendre la manette des gaz.
* **Virtua Racing**, **Virtua Formula** : boutons de vue sur les quatre boutons de face, rapports sur L1 / R1. Avec Supermodel, l'option **CONTRÔLES > UTILISER R1/L1 POUR LES JEUX DE COURSE** met l'accélérateur et le frein sur R1 / L1, et les rapports sur la croix directionnelle.

**DISPOSITION DES BOUTONS** (Keisho, Supermodel) adapte les boutons aux sticks arcade (modern8, 8alternative, 6alternative). Pour plus de détails sur les dispositions arcade, voir la page [**Le Guide Arcade**](../../../arcade-guide.md).

Les boutons de chaque jeu sont réglés dans les fichiers `keisho.yml` et `supermodel.yml` (`system\resources\inputmapping`), que vous pouvez copier dans `user\inputmapping` pour les modifier. Pour plus de détails sur `keisho.yml`, voir la page [**Configuration des touches Keisho**](../../../../controleurs/configuration-des-touches-specifique-par-emulateur/configuration-des-touches-keisho.md).

### Volants

Keisho et Supermodel gèrent les volants, avec l'option **VOLANTS DE COURSE > ACTIVER LES VOLANTS**, pour Virtua Racing et Virtua Formula.

* Keisho : **ACTIVER LE RETOUR DE FORCE** et **FORCE DU RETOUR DE FORCE** pour le retour de force de la carte de pilotage. La direction et les pédales sont détectées par Keisho ; les boutons sont réglés par type de volant dans `keisho_wheels.yml` (copie modifiable dans `user\inputmapping`), et un volant absent du fichier garde les boutons réglés dans le menu de Keisho.
* Supermodel : **ACTIVER LE RETOUR DE FORCE**.

Pour plus de détails sur les volants, voir la page [**Volants**](../../../../controleurs/supported-controllers/volants.md).

### Raccourcis

**Keisho**

| Raccourci           | Action                                  | Clavier        |
| ------------------- | --------------------------------------- | -------------- |
| **HOTKEY + START**  | Quitter                                 | ÉCHAP          |
| **HOTKEY + SUD**    | Menu de Keisho                          | F1             |
| **HOTKEY + OUEST**  | Sauvegarde instantanée                  | F2             |
| **HOTKEY + NORD**   | Chargement de la sauvegarde instantanée | F4             |
| **HOTKEY + GAUCHE** | Retour arrière (option **REMBOBINAGE**) | RETOUR ARRIÈRE |
| **HOTKEY + DROITE** | Avance rapide                           | L              |
| **L3** / **R3**     | Service / Test                          | 9 / 0          |
| —                   | Capture d'écran                         | F8             |
| —                   | Pause                                   | P              |
| —                   | Plein écran                             | F              |

Dans Virtua Racing et Virtua Formula, F1 à F5 servent aux rapports au clavier : le menu passe sur F10, la sauvegarde sur F6 et le chargement sur F7. Les raccourcis de la manette suivent automatiquement. Les touches du clavier sont personnalisables, voir la page [**Raccourcis**](../../../../navigation/hotkeys.md).

**Supermodel**

<table><thead><tr><th width="185.75">Raccourci</th><th width="293.5">Action</th><th>Clavier</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quitter</td><td>ÉCHAP</td></tr><tr><td><strong>L3</strong> / <strong>R3</strong></td><td>Service / Test (option <strong>ACTIVER LE MENU SERVICE</strong>)</td><td>9 / 0</td></tr><tr><td>—</td><td>Sauvegarde instantanée / changer d'emplacement / chargement</td><td>F5 / F6 / F7</td></tr><tr><td>—</td><td>Pause</td><td>ALT + P</td></tr><tr><td>—</td><td>Réinitialiser</td><td>ALT + R</td></tr><tr><td>—</td><td>Capture d'écran</td><td>ALT + S</td></tr><tr><td>—</td><td>Plein écran</td><td>ALT + ENTRÉE</td></tr><tr><td>—</td><td>Effacer la NVRAM</td><td>ALT + N</td></tr></tbody></table>

**MAME et core libretro mame** : voir la page [**MAME**](../mame.md).

## Dossiers

<table><thead><tr><th width="304">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Archives des cartes d'entrées-sorties</td><td><code>roms\model1</code></td></tr><tr><td>Keisho : NVRAM (réglages et records des bornes)</td><td><code>saves\model1\keisho</code></td></tr><tr><td>Keisho : sauvegardes instantanées (gérées par RetroBat)</td><td><code>saves\model1\keisho\sstates</code></td></tr><tr><td>Keisho : sauvegardes instantanées (dossier de l'émulateur)</td><td><code>saves\model1\keisho\states</code></td></tr><tr><td>Keisho : captures d'écran</td><td><code>screenshots\keisho</code></td></tr><tr><td>Keisho : configuration</td><td><code>emulators\keisho\keisho.ini</code></td></tr><tr><td>Keisho : boutons du volant</td><td><code>system\resources\inputmapping\wheels\keisho_wheels.yml</code> (copie modifiable dans <code>user\inputmapping</code>)</td></tr><tr><td>Supermodel : configuration</td><td><code>emulators\supermodel\Config\Supermodel.ini</code></td></tr><tr><td>Supermodel : NVRAM</td><td><code>emulators\supermodel\NVRAM</code></td></tr><tr><td>Supermodel : sauvegardes instantanées</td><td><code>emulators\supermodel\Saves</code></td></tr><tr><td>Correspondance des boutons par jeu</td><td><code>system\resources\inputmapping\keisho.yml</code>, <code>supermodel.yml</code> (copie modifiable dans <code>user\inputmapping</code>)</td></tr></tbody></table>

Pour les dossiers de MAME, voir la page [**MAME**](../mame.md).

## Guides

### Autres options utiles

**Keisho**

<table><thead><tr><th width="335.25">Option</th><th>Effet</th></tr></thead><tbody><tr><td><strong>RÉSOLUTION INTERNE</strong></td><td>Augmente la résolution de rendu (Vulkan et OpenGL).</td></tr><tr><td><strong>RAPPORT D'ASPECT</strong></td><td>4/3 par défaut, comme le moniteur d'arcade (la décoration ne s'affiche qu'en 4/3). 16/9 élargit la vue 3D.</td></tr><tr><td><strong>RENDU VISUEL > FILTRE CRT</strong></td><td>Aspect d'un écran cathodique : lignes de balayage, masque, halo.</td></tr><tr><td><strong>RENDU VISUEL > TRANSPARENCE</strong></td><td><strong>MÉLANGÉE</strong> : transparences lissées au lieu du damier de la borne (Vulkan et OpenGL).</td></tr><tr><td><strong>RENDU VISUEL > AJUSTER LA LUMINOSITÉ</strong></td><td>Niveau du noir de l'image (50 % par défaut, calé sur une capture de borne).</td></tr><tr><td><strong>ÉMULATION > REMBOBINAGE</strong></td><td>Active le retour arrière (<strong>HOTKEY + GAUCHE</strong>).</td></tr><tr><td><strong>CONTRÔLES > ACTIVER LES VIBRATIONS</strong></td><td>Vibrations de la manette dans les jeux de course.</td></tr></tbody></table>

**Supermodel**

<table><thead><tr><th width="375.25">Option</th><th>Effet</th></tr></thead><tbody><tr><td><strong>VIDÉO > HACK ÉCRAN LARGE</strong></td><td>Affiche les jeux en 16/9.</td></tr><tr><td><strong>ÉMULATION > GÉOMÉTRISEUR HAUT NIVEAU</strong></td><td>Activé par défaut (rapide). Désactivé, Supermodel exécute les vrais programmes de géométrie, plus précis mais plus lent.</td></tr><tr><td><strong>RENDU VISUEL > SURÉCHANTILLONNAGE</strong></td><td>Lisse l'image (SSAA), au prix des performances.</td></tr></tbody></table>

## Problèmes connus

<table><thead><tr><th width="355.25">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Virtua Fighter ou NetMerc ne démarrent pas avec MAME</td><td>MAME ne les émule pas encore : utilisez Keisho ou Supermodel (NetMerc : Supermodel).</td></tr><tr><td>Virtua Formula ne démarre pas avec Supermodel</td><td>Supermodel ne gère pas ce jeu : utilisez Keisho ou MAME.</td></tr><tr><td>Un jeu ne démarre pas avec MAME (fichier manquant)</td><td>Ajoutez <code>model1io.zip</code> ou <code>model1io2.zip</code> dans <code>roms\model1</code>, et le jeu parent pour un clone.</td></tr><tr><td>Le joueur 2 de Star Wars Arcade ne fait rien</td><td>C'est le canonnier : il faut une deuxième manette.</td></tr><tr><td>Les boutons ne correspondent pas à la borne</td><td>Choisissez une <strong>DISPOSITION DES BOUTONS</strong>, ou modifiez <code>keisho.yml</code> / <code>supermodel.yml</code> dans <code>user\inputmapping</code>.</td></tr></tbody></table>
