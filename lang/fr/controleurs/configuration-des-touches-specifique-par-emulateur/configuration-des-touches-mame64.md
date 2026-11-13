# Configuration des touches MAME

## Présentation

Chaque borne d'arcade avait son propre panneau : un bouton, six boutons, un volant, un trackball… Il n'existe donc pas de réglage de manette valable pour tous les jeux MAME.

RetroBat règle les boutons automatiquement, jeu par jeu, pour **lr-mame**, **mame2003\_plus**, **MAME** et **GroovyMAME**. Cette page explique comment ce réglage est choisi et comment le modifier : disposition pour un stick arcade, correction d'un jeu, panneau IPAC2 ou X-Arcade, profil personnel.

Le tableau des boutons par défaut et les raccourcis sont sur la page [**MAME**](../../systemes-and-emulateurs/supported-game-systems/arcade/mame.md).

## Comment RetroBat choisit les boutons

Au lancement d'un jeu, RetroBat cherche dans cet ordre :

1. **votre configuration** du jeu, dans `user\inputmapping` ;
2. **la configuration du jeu fournie par RetroBat**, dans `system\resources\inputmapping` (plus de 3 000 jeux) ;
3. si le jeu est un clone sans configuration, **celle du jeu parent** ;
4. sinon, **la configuration par défaut** de la disposition choisie.

Les fichiers ne sont pas les mêmes selon l'émulateur :

<table><thead><tr><th width="168.25">Émulateur</th><th width="319">Fichiers fournis par RetroBat</th><th>Vos fichiers</th></tr></thead><tbody><tr><td><strong>MAME, GroovyMAME</strong></td><td>Un fichier <code>&#x3C;jeu>.xml</code> par jeu dans <code>system\resources\inputmapping\mame</code></td><td><code>user\inputmapping\mame\&#x3C;jeu>.xml</code></td></tr><tr><td><strong>lr-mame</strong></td><td><code>system\resources\inputmapping\libretro_mame.yml</code> (boutons) et <code>system\resources\inputmapping\lr-mame\&#x3C;jeu>.cfg</code> (raccourcis du menu MAME)</td><td><code>user\inputmapping\libretro_mame.yml</code></td></tr><tr><td><strong>mame2003_plus</strong></td><td>Le même <code>libretro_mame.yml</code> que lr-mame, et <code>system\resources\inputmapping\libretro_mame2003_plus.yml</code> pour les jeux dont les boutons diffèrent dans cette version de MAME</td><td><code>user\inputmapping\libretro_mame2003_plus.yml</code></td></tr></tbody></table>

Ces fichiers décrivent les boutons avec des noms génériques et contiennent une section par disposition. RetroBat les convertit au lancement selon la manette branchée.

Ne modifiez pas les fichiers du dossier `system` : ils sont remplacés à chaque mise à jour.

## Disposition des boutons

Sur un stick arcade, les boutons sont rangés sur deux lignes. L'option **CONTRÔLES > DISPOSITION DES BOUTONS** indique à RetroBat comment est fait votre panneau, pour qu'il y reproduise la disposition de la borne d'origine.

| Disposition                 | Ligne du haut          | Ligne du bas     |
| --------------------------- | ---------------------- | ---------------- |
| **MANETTE (SNES)** (défaut) | Pour les manettes      |                  |
| **MODERNE 8 BOUTONS**       | OUEST, NORD, R1, L1    | SUD, EST, R2, L2 |
| **8 BOUTONS ALTERNATIF**    | OUEST, NORD, L1, L2    | SUD, EST, R1, R2 |
| **6 BOUTONS**               | OUEST, NORD, L1        | SUD, EST, R1     |
| **CLASSIQUE 8 BOUTONS**     | Traité comme 6 BOUTONS |                  |

<figure><img src="../../.gitbook/assets/image (558).png" alt=""><figcaption></figcaption></figure>

Les configurations par jeu suivent ces règles :

* **jeu à 6 boutons** (Street Fighter II) : boutons 1, 2, 3 sur la ligne du haut, boutons 4, 5, 6 sur la ligne du bas ;
* **jeu à 3 boutons ou moins** : ligne du haut avec MODERNE 8 BOUTONS et 6 BOUTONS, ligne du bas avec 8 BOUTONS ALTERNATIF.

Cette option se règle aussi pour tous les systèmes d'arcade dans **PARAMÈTRES DES JEUX > CONTRÔLES > CONTRÔLEURS SPÉCIAUX** (voir la page [**Sticks Arcade**](../supported-controllers/arcade-sticks.md)).

### Jeux sans configuration dédiée

| Bouton de la borne | MANETTE (SNES)                                     | MODERNE 8 BOUTONS                                  | 6 BOUTONS                                          |
| ------------------ | -------------------------------------------------- | -------------------------------------------------- | -------------------------------------------------- |
| Bouton 1           | OUEST ![](<../../.gitbook/assets/image (559).png>) | OUEST ![](<../../.gitbook/assets/image (560).png>) | OUEST ![](<../../.gitbook/assets/image (561).png>) |
| Bouton 2           | SUD ![](<../../.gitbook/assets/image (562).png>)   | NORD ![](<../../.gitbook/assets/image (569).png>)  | NORD ![](<../../.gitbook/assets/image (570).png>)  |
| Bouton 3           | EST ![](<../../.gitbook/assets/image (565).png>)   | R1                                                 | L1                                                 |
| Bouton 4           | NORD ![](<../../.gitbook/assets/image (568).png>)  | SUD ![](<../../.gitbook/assets/image (563).png>)   | SUD ![](<../../.gitbook/assets/image (564).png>)   |
| Bouton 5           | L1                                                 | EST ![](<../../.gitbook/assets/image (566).png>)   | EST ![](<../../.gitbook/assets/image (567).png>)   |
| Bouton 6           | R1                                                 | R2                                                 | R1                                                 |
| Bouton 7           | L2                                                 | L1                                                 | L2                                                 |
| Bouton 8           | R2                                                 | L2                                                 | R2                                                 |

Les boutons 7 et 8 ne sont réglés que pour MAME, GroovyMAME et mame2003\_plus.

**8 BOUTONS ALTERNATIF** : comme 6 BOUTONS avec lr-mame et mame2003\_plus, comme MANETTE (SNES) avec MAME et GroovyMAME.

## Quelle méthode choisir ?

| Vous voulez…                                                           | MAME, GroovyMAME                                                          | lr-mame                                        |
| ---------------------------------------------------------------------- | ------------------------------------------------------------------------- | ---------------------------------------------- |
| Adapter les boutons à votre stick arcade                               | **DISPOSITION DES BOUTONS**                                               | **DISPOSITION DES BOUTONS**                    |
| Corriger les boutons d'un jeu, en gardant la configuration automatique | Fichier `user\inputmapping\mame\<jeu>.xml`                                | Fichier `user\inputmapping\libretro_mame.yml`  |
| Régler les boutons dans le menu de MAME et les garder                  | **PROFIL DE CONFIGURATION DES MANETTES** : AUCUN                          | **UTILISER SON PROPRE FICHIER CFG**            |
| Utiliser un panneau IPAC2 ou X-Arcade                                  | **PROFIL DE CONFIGURATION DES MANETTES** : IPAC2 ou X-ARCADE              | —                                              |
| Utiliser votre propre fichier de contrôleur                            | **PROFIL DE CONFIGURATION DES MANETTES** : PERSONNALISÉ 1 à 8, ou PAR JEU | —                                              |
| Laisser MAME choisir les boutons du jeu                                | —                                                                         | **ACTIVER LE MAPPING AUTOMATIQUE POUR LE JEU** |
| Tout régler vous-même                                                  | Désactivez **AUTOCONFIGURER LES MANETTES**                                | Désactivez **AUTOCONFIGURER LES MANETTES**     |

Ces options sont dans les options avancées du système, sous-menu **CONTRÔLES**. Pour mame2003\_plus, voir la section qui lui est consacrée plus bas.

<div align="left"><figure><img src="../../.gitbook/assets/image (571).png" alt=""><figcaption></figcaption></figure></div>

## MAME et GroovyMAME

### Profil de configuration des manettes

L'option **CONTRÔLES > PROFIL DE CONFIGURATION DES MANETTES** choisit d'où viennent les boutons :

<table><thead><tr><th width="230.25">Choix</th><th>Effet</th></tr></thead><tbody><tr><td><strong>RETROBAT AUTO</strong> (défaut)</td><td>Configuration automatique de RetroBat, jeu par jeu.</td></tr><tr><td><strong>X-ARCADE</strong>, <strong>IPAC2</strong></td><td>Profils fournis par RetroBat pour ces panneaux : <code>X-Arcade.cfg</code> et <code>ipac2.cfg</code> dans <code>saves\mame\ctrlr</code>.</td></tr><tr><td><strong>PERSONNALISÉ 1</strong> à <strong>8</strong></td><td>Votre fichier <code>custom1.cfg</code> à <code>custom8.cfg</code> dans <code>saves\mame\ctrlr</code>.</td></tr><tr><td><strong>PAR JEU</strong></td><td>Un fichier au nom du jeu dans <code>saves\mame\ctrlr</code>, par exemple <code>wjammers.cfg</code> pour <code>wjammers.zip</code>.</td></tr><tr><td><strong>AUCUN</strong></td><td>RetroBat ne règle rien : MAME utilise ses fichiers <code>.cfg</code>.</td></tr></tbody></table>

### Les fichiers .cfg de MAME

MAME enregistre ses réglages par jeu dans `saves\mame\cfg` : `default.cfg` pour tous les jeux, `<jeu>.cfg` pour un jeu. On y trouve les boutons réglés dans le menu de MAME, mais aussi les interrupteurs de la borne (DIP switches).

MAME lit d'abord le profil de contrôleur, puis `default.cfg`, puis le `.cfg` du jeu : le dernier lu l'emporte. **Un bouton réglé dans un fichier `.cfg` est donc prioritaire sur le profil.**

Avec le profil **RETROBAT AUTO**, RetroBat retire les boutons de `default.cfg` et de `<jeu>.cfg` le temps de la partie, puis les remet. Les DIP switches sont conservés. Les boutons modifiés dans le menu de MAME pendant la partie ne sont pas gardés ; une copie des fichiers de la dernière partie reste dans `saves\mame\cfgbackupmame64`.

Avec les autres profils, RetroBat ne touche pas à ces fichiers.

lr-mame et MAME partagent le dossier `saves\mame\cfg`. L'option **ÉMULATION > DOSSIER CFG SÉPARÉ DE LIBRETRO** donne à MAME son propre dossier, `saves\mame\cfg64`.

### Corriger les boutons d'un jeu (fichier XML)

1. Copiez le fichier du jeu, par exemple `sf2.xml`, de `system\resources\inputmapping\mame` vers `user\inputmapping\mame`.
2. Ouvrez la copie avec un éditeur de texte. Chaque disposition a sa section `<layout type="...">` : `default` (manette), `modern8`, `8alternative`, `6alternative`. Si la section de votre disposition n'existe pas, RetroBat utilise la section `default`.
3. Dans la section voulue, changez le nom du bouton de manette dans la ligne `mapping` :

```xml
<button type="P1_BUTTON1" tag=":IN1" mask="16" defvalue="16" function="P1_BUTTON1">
  <mapping type="standard" name="JOY_west" />
</button>
```

<div align="left"><figure><img src="../../.gitbook/assets/image (572).png" alt=""><figcaption></figcaption></figure></div>

Plusieurs boutons peuvent commander la même action, séparés par `OR` : `JOY_right OR JOY_lsright`.

**Noms acceptés**

| Nom                                                                      | Bouton                                                                              |
| ------------------------------------------------------------------------ | ----------------------------------------------------------------------------------- |
| `JOY_south`, `JOY_east`, `JOY_west`, `JOY_north`                         | Boutons de façade                                                                   |
| `JOY_l1`, `JOY_r1`                                                       | L1 et R1                                                                            |
| `JOY_l2`, `JOY_r2`                                                       | L2 et R2, utilisés comme boutons                                                    |
| `JOY_l2trigger`, `JOY_r2trigger`                                         | L2 et R2, en analogique                                                             |
| `JOY_l3`, `JOY_r3`                                                       | Clics des sticks                                                                    |
| `JOY_start`, `JOY_select`                                                | START et SELECT                                                                     |
| `JOY_up`, `JOY_down`, `JOY_left`, `JOY_right`                            | Croix directionnelle                                                                |
| `JOY_lsup`, `JOY_lsdown`, `JOY_lsleft`, `JOY_lsright`                    | Stick gauche, comme directions                                                      |
| `JOY_rsup`, `JOY_rsdown`, `JOY_rsleft`, `JOY_rsright`                    | Stick droit, comme directions                                                       |
| `JOY_leftstickx`, `JOY_leftsticky`, `JOY_rightstickx`, `JOY_rightsticky` | Axe entier d'un stick (volant, molette, stick analogique)                           |
| `MOUSE_BUTTON1`…, `MOUSE_XAXIS`, `MOUSE_YAXIS`                           | Souris                                                                              |
| `GUN_BUTTON1`…, `GUN_XAXIS`, `GUN_YAXIS`                                 | Pistolet                                                                            |
| `KEYCODE_...`                                                            | Touche du clavier, au format MAME (`KEYCODE_ENTER`, `KEYCODE_P`, `KEYCODE_LSHIFT`…) |

Pour inverser un axe, ajoutez `_reverse` à son nom : `JOY_leftstickx_reverse`.

**Jeu sans fichier** : créez `user\inputmapping\mame\<jeu>.xml` sur le modèle d'un fichier existant. Les attributs `type`, `tag`, `mask` et `defvalue` de chaque bouton doivent être ceux du jeu dans MAME : vous les trouvez dans `saves\mame\cfg\<jeu>.cfg` après avoir réglé une fois ce bouton dans le menu de MAME. Le fichier `README.txt` du dossier `user\inputmapping\mame` décrit le format.

### Créer votre propre profil de contrôleur

1. Lancez `mame.exe` depuis le dossier `emulators\mame`.
2. Ouvrez **General Settings**, puis **Input Assignments**, et réglez les boutons. La partie **User Interface** concerne le menu de MAME, les parties **Player** concernent les jeux.

<div align="left"><figure><img src="../../.gitbook/assets/image (573).png" alt="" width="375"><figcaption></figcaption></figure></div>

3. Enregistrez. MAME crée le fichier `default.cfg` dans `emulators\mame\cfg`.
4. Renommez ce fichier `custom1.cfg` (jusqu'à `custom8.cfg`) et déplacez-le dans `saves\mame\ctrlr`.
5. Dans RetroBat, choisissez **CONTRÔLES > PROFIL DE CONFIGURATION DES MANETTES** : PERSONNALISÉ 1.

<div align="left"><figure><img src="../../.gitbook/assets/image (574).png" alt=""><figcaption></figcaption></figure></div>

Pour un profil propre à un jeu, nommez le fichier comme le romset (`wjammers.cfg` pour `wjammers.zip`), placez-le dans `saves\mame\ctrlr` et choisissez **PAR JEU**.

## lr-mame

### Corriger les boutons d'un jeu (libretro\_mame.yml)

1. Copiez `libretro_mame.yml` de `system\resources\inputmapping` vers `user\inputmapping`. Votre copie remplace alors entièrement le fichier de RetroBat.
2. Cherchez l'entrée du jeu. Il y en a une par disposition : `sf2` (manette), `sf2_modern8`, `sf2_8alternative`, `sf2_6alternative`. Si l'entrée de votre disposition n'existe pas, RetroBat utilise l'entrée `sf2`, qui doit toujours être présente.

```
sf2_modern8:
  analog_dpad_mode: 0
  btn_a: 10
  btn_b: 9
  btn_x: 8
  btn_y: 0
```

3. Chaque ligne donne, pour un bouton de votre manette, le bouton de la borne à déclencher.

<table><thead><tr><th width="225.25">Nom</th><th>Bouton de la manette</th></tr></thead><tbody><tr><td><code>btn_a</code></td><td>EST <img src="../../.gitbook/assets/image (575).png" alt=""></td></tr><tr><td><code>btn_b</code></td><td>SUD <img src="../../.gitbook/assets/image (576).png" alt=""></td></tr><tr><td><code>btn_x</code></td><td>NORD <img src="../../.gitbook/assets/image (577).png" alt=""></td></tr><tr><td><code>btn_y</code></td><td>OUEST <img src="../../.gitbook/assets/image (578).png" alt=""></td></tr><tr><td><code>btn_l</code>, <code>btn_r</code></td><td>L1, R1</td></tr><tr><td><code>btn_l2</code>, <code>btn_r2</code></td><td>L2, R2</td></tr></tbody></table>

<table><thead><tr><th width="154">Valeur</th><th>Bouton de la borne</th></tr></thead><tbody><tr><td><code>0</code></td><td>Bouton 1</td></tr><tr><td><code>8</code></td><td>Bouton 2</td></tr><tr><td><code>1</code></td><td>Bouton 3</td></tr><tr><td><code>9</code></td><td>Bouton 4</td></tr><tr><td><code>10</code></td><td>Bouton 5</td></tr><tr><td><code>11</code></td><td>Bouton 6</td></tr><tr><td><code>14</code></td><td>Bouton 7</td></tr><tr><td><code>15</code></td><td>Bouton 8</td></tr><tr><td><code>-1</code></td><td>Aucun</td></tr></tbody></table>

Dans l'exemple, EST (`btn_a: 10`) déclenche le bouton 5 de la borne.

### Menu de MAME

Le menu de MAME s'ouvre avec **START + SUD**. **SUD** valide et **EST** revient en arrière.

Comme les boutons changent d'un jeu à l'autre, RetroBat écrit à chaque lancement ces raccourcis dans `saves\mame\cfg\<jeu>.cfg`, à partir des fichiers de `system\resources\inputmapping\lr-mame`. Une copie de la session précédente est gardée dans `saves\mame\cfgbackup`.

### Garder vos réglages faits dans le menu de MAME

Activez **CONTRÔLES > UTILISER SON PROPRE FICHIER CFG**. Les boutons réglés dans le menu de MAME sont alors conservés dans `saves\mame\cfg\<jeu>.cfg`. À la première activation, la configuration de la dernière partie est reprise. L'option DISPOSITION DES BOUTONS ne s'applique plus à ce jeu.

### Laisser MAME choisir

Avec **ACTIVER LE MAPPING AUTOMATIQUE POUR LE JEU**, RetroBat n'applique plus ses configurations par jeu : c'est le core qui place les boutons.

## mame2003\_plus

Par défaut, mame2003\_plus reprend les configurations par jeu de lr-mame et suit l'option **DISPOSITION DES BOUTONS**. Les jeux dont les boutons sont différents dans cette ancienne version de MAME ont leur propre configuration, ou à défaut la configuration par défaut.

| Vous voulez…                                                   | Réglage                                                                                                                                           |
| -------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| Utiliser une disposition du core, identique pour tous les jeux | **CONTRÔLES > TYPE DE CONTRÔLEUR JOUEUR 1** : RETROPAD, FIGHTSTICK, 8 BOUTONS ou 6 BOUTONS. RetroBat ne règle alors plus les boutons jeu par jeu. |
| Corriger les boutons d'un jeu                                  | Fichier `user\inputmapping\libretro_mame2003_plus.yml`                                                                                            |
| Régler les boutons dans le menu de MAME                        | **ACTIVER LE REMAPPAGE MAME** (actif par défaut), puis **L3**                                                                                     |

Dans le menu de MAME, les boutons pour valider et annuler dépendent du jeu : **SUD** et **OUEST** avec la configuration par défaut.

**Corriger un jeu** : copiez `libretro_mame2003_plus.yml` de `system\resources\inputmapping` vers `user\inputmapping`, puis ajoutez-y ou modifiez-y l'entrée du jeu. Le format est celui de `libretro_mame.yml`, avec deux différences :

* les boutons 7 et 8 s'écrivent `12` et `13` ;
* une entrée `use: default` désigne un jeu qui utilise la configuration par défaut.

Les jeux absents de ce fichier sont lus dans `libretro_mame.yml`.

## Dossiers

| Contenu                            | Dossier                                                               |
| ---------------------------------- | --------------------------------------------------------------------- |
| Configurations par jeu de RetroBat | `system\resources\inputmapping`                                       |
| Vos configurations par jeu         | `user\inputmapping`                                                   |
| Profils de contrôleur de MAME      | `saves\mame\ctrlr`                                                    |
| Réglages par jeu de MAME (cfg)     | `saves\mame\cfg` (ou `saves\mame\cfg64`)                              |
| Copies de sécurité des cfg         | `saves\mame\cfgbackup` (lr-mame), `saves\mame\cfgbackupmame64` (MAME) |
| Réglages de mame2003\_plus         | `saves\mame\mame2003-plus`                                            |

## Problèmes connus

| Problème                                                         | Solution                                                                                                                             |
| ---------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| Les boutons ne tombent pas au bon endroit sur mon stick arcade   | Réglez **DISPOSITION DES BOUTONS** selon votre panneau.                                                                              |
| Avec mame2003\_plus, **DISPOSITION DES BOUTONS** n'a aucun effet | Laissez **TYPE DE CONTRÔLEUR JOUEUR 1** et **TYPE DE CONTRÔLEUR JOUEUR 2** sur AUTO.                                                 |
| Mes réglages faits dans le menu de MAME sont perdus              | La configuration automatique les remplace. MAME : choisissez le profil AUCUN. lr-mame : activez **UTILISER SON PROPRE FICHIER CFG**. |
| Mon profil de contrôleur personnalisé est ignoré                 | Un fichier `default.cfg` ou `<jeu>.cfg` de `saves\mame\cfg` contient d'autres boutons : supprimez-le ou retirez-en les boutons.      |
| Mon fichier `user\inputmapping\mame\<jeu>.xml` est ignoré        | Le fichier doit porter le nom exact du romset, et le profil doit être **RETROBAT AUTO**.                                             |
| Ma correction dans `libretro_mame.yml` est ignorée               | Modifiez la copie placée dans `user\inputmapping`, et l'entrée de votre disposition (`<jeu>_modern8`…).                              |
