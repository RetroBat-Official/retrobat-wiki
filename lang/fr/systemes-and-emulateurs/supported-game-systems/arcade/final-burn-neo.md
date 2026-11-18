# Final Burn Neo

<div align="left"><figure><img src="../../../.gitbook/assets/image (660).png" alt=""><figcaption></figcaption></figure></div>

## Présentation

**FinalBurn Neo** (FBNeo) est un émulateur d'arcade. Son histoire commence en 2000 avec **Final Burn**, créé par Dave pour les bornes CPS-1 et CPS-2 de Capcom. Le projet devient **FinalBurn Alpha** (FB Alpha), puis l'équipe le reprend en 2019 sous le nom de FinalBurn Neo.

FBNeo vise la jouabilité plus que la documentation complète des machines : il est léger, rapide et réputé pour ses jeux de combat et ses shoot'em up. Il émule des milliers de jeux, notamment :

* Capcom CPS-1, CPS-2 et CPS-3 ;
* SNK Neo Geo ;
* Cave, IGS PGM, Toaplan ;
* Konami, Sega System 16 / 18, Taito, Data East, Irem…

Chaque jeu est un fichier appelé [**romset**](../../arcade-guide.md#comprendre-les-romsets) (`sf2.zip` pour Street Fighter II), dont le contenu doit correspondre à la version de l'émulateur (voir [**Quel format de jeu ?**](final-burn-neo.md#quel-format-de-jeu)).

Dans RetroBat, le système FinalBurn Neo réunit tous les jeux du romset FBNeo. Les CPS-1, CPS-2, CPS-3, Neo Geo et Cave ont aussi leur propre système.

{% embed url="https://github.com/finalburnneo/FBNeo" %}

## En bref

<table><thead><tr><th width="291.5"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\fbneo</code></td></tr><tr><td><strong>Extensions</strong></td><td>.zip .7z</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: fbneo</td></tr><tr><td><strong>BIOS</strong></td><td>Selon les jeux (voir BIOS)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique (cores libretro ; FBNeo pour les jeux du fichier de mappage)</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro ; FBNeo par raccourcis</td></tr><tr><td><strong>RetroAchievements</strong></td><td>cores libretro (fbneo conseillé)</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>cores libretro</td></tr><tr><td><strong>Pistolets</strong></td><td>core fbneo (jusqu'à 4)</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="192.75">Émulateur</th><th>Pour qui ?</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>libretro: fbneo</strong> (défaut)</td><td>Tout le monde</td><td>La version actuelle de FBNeo dans RetroArch : shaders, décorations, sauvegardes instantanées, RetroAchievements, jeu en réseau, pistolets, dip switches dans les options du core.</td><td>—</td></tr><tr><td><strong>fbneo</strong> (autonome)</td><td>Bornes, sticks arcade</td><td>Le FBNeo officiel. Boutons réglés jeu par jeu par RetroBat (fichier de mappage), avec des dispositions pour sticks arcade, et un écran séparé possible pour les jeux verticaux.</td><td>Pas de RetroAchievements ni de jeu en réseau. Sauvegardes instantanées par raccourcis seulement.</td></tr><tr><td><strong>libretro: fbalpha</strong></td><td>Romsets anciens</td><td>FB Alpha 0.2.97.44.</td><td>Romset de sa propre version, plus mis à jour.</td></tr><tr><td><strong>libretro: fbalpha2012, fbalpha2012_neogeo</strong></td><td>PC très modestes, romsets anciens</td><td>FB Alpha 0.2.97.29, plus léger.</td><td>Romset de sa propre version. Le BIOS Neo Geo de fbalpha2012_neogeo se place à côté des jeux (voir BIOS).</td></tr></tbody></table>

**En cas de doute, gardez libretro: fbneo.**

## BIOS

Seuls certains jeux ont besoin d'un BIOS : c'est un romset partagé entre plusieurs jeux d'un même matériel. Il doit venir de la même version de FBNeo que vos jeux.

<table><thead><tr><th width="392.75">Fichier</th><th>Matériel</th></tr></thead><tbody><tr><td><code>neogeo.zip</code></td><td>SNK Neo Geo</td></tr><tr><td><code>pgm.zip</code></td><td>IGS PolyGame Master</td></tr><tr><td><code>skns.zip</code></td><td>Kaneko Super Nova System</td></tr><tr><td><code>decocass.zip</code></td><td>Data East Cassette System</td></tr><tr><td><code>isgsm.zip</code></td><td>ISG Selection Master Type 2006</td></tr><tr><td><code>atarisy1.zip</code></td><td>Atari System 1</td></tr><tr><td><code>bubsys.zip</code></td><td>Konami Bubble System</td></tr><tr><td><code>cchip.zip</code></td><td>Taito C-Chip (ROM interne)</td></tr><tr><td><code>midssio.zip</code></td><td>Midway SSIO (ROM interne de la carte son)</td></tr><tr><td><code>namcoc69.zip</code>, <code>namcoc70.zip</code>, <code>namcoc75.zip</code></td><td>Namco C69 / C70 / C75</td></tr><tr><td><code>nmk004.zip</code></td><td>NMK004 (ROM interne)</td></tr><tr><td><code>ym2608.zip</code></td><td>Yamaha YM2608 (ROM interne)</td></tr></tbody></table>

Placez ces fichiers dans `bios`, `bios\fbneo` ou à côté des jeux, dans `roms\fbneo`. La vérification des BIOS de RetroBat les liste tous comme optionnels, dans `bios`.

Avec **libretro: fbalpha2012\_neogeo**, `neogeo.zip` doit se trouver à côté des jeux, dans `roms\fbneo` : ce core ne lit pas le dossier `bios`.

**BIOS Neo Geo** : avec le core fbneo, l'option **ÉMULATION > BIOS** choisit le BIOS des jeux Neo Geo. Par défaut, RetroBat utilise le **BIOS UNIVERSE**, sauf en mode hardcore des RetroAchievements (voir [**Guides**](final-burn-neo.md#retroachievements)). Le BIOS Universe doit être présent dans `neogeo.zip` : c'est le cas avec le `neogeo.zip` de FBNeo.

## Quel format de jeu ?

Les jeux sont des romsets `.zip` ou `.7z`, à garder compressés et sous leur nom d'origine (`mslug.zip`, `sfiii3n.zip`…).

| Émulateur                                  | Version du romset                                          |
| ------------------------------------------ | ---------------------------------------------------------- |
| libretro: fbneo, fbneo (autonome)          | Dernière version de FBNeo (fichiers `.dat` du dépôt FBNeo) |
| libretro: fbalpha                          | FB Alpha 0.2.97.44                                         |
| libretro: fbalpha2012, fbalpha2012\_neogeo | FB Alpha 0.2.97.29                                         |

Un romset d'une autre version, ou d'une version de MAME, peut ne pas se lancer ou mal fonctionner. Pour le détail des types de romsets (non-merged, split, merged) et des samples, voir la page [**Le Guide Arcade**](../../arcade-guide.md).

## Contrôles

### Core fbneo (libretro)

RetroBat configure automatiquement les manettes, jusqu'à 4 joueurs. **SELECT** met une pièce, **START** lance la partie, le stick gauche et la croix déplacent le joueur.

L'option **CONTRÔLES > TYPE DE CONTRÔLEUR** choisit la disposition des boutons :

<table><thead><tr><th width="159.5">Manette RetroBat</th><th width="222.75">CLASSIQUE (défaut)</th><th>MODERNE</th></tr></thead><tbody><tr><td>SUD</td><td>Bouton 1</td><td>Bouton 1</td></tr><tr><td>EST</td><td>Bouton 2</td><td>Bouton 2</td></tr><tr><td>OUEST</td><td>Bouton 3</td><td>Bouton 3</td></tr><tr><td>NORD</td><td>Bouton 4</td><td>Bouton 4</td></tr><tr><td>R1</td><td>Bouton 5</td><td>Bouton 6</td></tr><tr><td>L1</td><td>Bouton 6</td><td>—</td></tr><tr><td>R2</td><td>—</td><td>Bouton 5</td></tr></tbody></table>

Jeux de combat à 6 boutons (Street Fighter…) :

<table><thead><tr><th width="180.75">Manette RetroBat</th><th width="210.5">CLASSIQUE (défaut)</th><th>MODERNE</th></tr></thead><tbody><tr><td>OUEST</td><td>Poing faible</td><td>Poing faible</td></tr><tr><td>NORD</td><td>Poing moyen</td><td>Poing moyen</td></tr><tr><td>L1</td><td>Poing fort</td><td>—</td></tr><tr><td>R1</td><td>Pied fort</td><td>Poing fort</td></tr><tr><td>R2</td><td>—</td><td>Pied fort</td></tr><tr><td>SUD</td><td>Pied faible</td><td>Pied faible</td></tr><tr><td>EST</td><td>Pied moyen</td><td>Pied moyen</td></tr></tbody></table>

Jeux Neo Geo :

<table><thead><tr><th width="195.75">Manette RetroBat</th><th width="219.75">CLASSIQUE (défaut)</th><th>MODERNE</th></tr></thead><tbody><tr><td>SUD</td><td>A</td><td>B</td></tr><tr><td>EST</td><td>B</td><td>D</td></tr><tr><td>OUEST</td><td>C</td><td>A</td></tr><tr><td>NORD</td><td>D</td><td>C</td></tr></tbody></table>

Les autres choix de **TYPE DE CONTRÔLEUR** adaptent la manette à un matériel :

* **4 BOUTONS - NEOGEO MINI**, **6 BOUTONS - VARIANTE NEOGEO** et les trois **8 BOUTONS - MVS** : manettes et sticks Neo Geo ;
* **PANNEAU 6 BOUTONS** : panneau arcade à 6 boutons ;
* **SOURIS**, **POINTEUR**, **ÉCRAN TACTILE** : jeux à trackball ou à pointeur ;
* **LIGHTGUN**, **PISTOLET ARCADE ANALOGIQUE** : pistolets (voir [**Guides**](final-burn-neo.md#pistolets)).

**CONTRÔLES > VITESSE ANALOGIQUE** ralentit les commandes analogiques (volants, trackballs) des jeux qui réagissent trop vite.

<div align="left"><figure><img src="../../../.gitbook/assets/image (661).png" alt=""><figcaption></figcaption></figure></div>

### FBNeo (autonome)

RetroBat configure les manettes jeu par jeu, à partir du fichier de mappage `fbneo.yml` (près de 3 000 jeux). Le fichier se trouve dans `system\resources\inputmapping`. Pour le modifier, copiez-le dans `user\inputmapping` : c'est cette copie qui est utilisée.

Un clone sans entrée propre utilise celle de son jeu parent. Un jeu absent du fichier n'est pas configuré par RetroBat : il garde les touches réglées dans FBNeo (**F5**, ou menu **Input > Map game inputs**).

L'option **CONTRÔLES > DISPOSITION DES BOUTONS** choisit la disposition. Elle est utile surtout avec un stick arcade :

* **MANETTE (SNES)** (défaut) ;
* **MODERNE 8 BOUTONS** ;
* **CLASSIQUE 8 BOUTONS** ;
* **8 BOUTONS ALTERNATIF** ;
* **6 BOUTONS**.

Avec la disposition par défaut, un jeu de combat à 6 boutons se joue comme avec le core en CLASSIQUE : OUEST / NORD / L1 pour les poings, SUD / EST / R1 pour les pieds. Le bouton Service de la borne est sur **R3**.

Avec des manettes XInput (manettes Xbox et compatibles), FBNeo utilise XInput. Dès qu'une manette n'est pas XInput, il passe en DirectInput pour toutes les manettes. **PILOTES > MANETTES** permet de forcer DirectInput. En DirectInput, si les manettes ne commandent pas les bons joueurs, activez **CONTRÔLES > INDEX DE MANETTE ALTERNATIF**.

Sans manette, FBNeo garde sa configuration clavier par défaut.

### Raccourcis

Les cores libretro utilisent les raccourcis standards de RetroArch (voir la page [**Raccourcis**](../../../navigation/hotkeys.md)).

**FBNeo (autonome)**

<table><thead><tr><th width="199.5">Raccourci</th><th>Action</th><th>Clavier</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quitter</td><td>—</td></tr><tr><td>HOTKEY + OUEST</td><td>Sauvegarde instantanée</td><td>F2</td></tr><tr><td>HOTKEY + NORD</td><td>Chargement instantané</td><td>F4</td></tr><tr><td>HOTKEY + HAUT</td><td>Emplacement de sauvegarde suivant</td><td>F7</td></tr><tr><td>HOTKEY + BAS</td><td>Emplacement de sauvegarde précédent</td><td>F6</td></tr><tr><td>HOTKEY + DROITE</td><td>Avance rapide (maintenir)</td><td>L</td></tr><tr><td>HOTKEY + GAUCHE</td><td>Retour en arrière (à activer dans le menu de FBNeo : <strong>Input > Rewind Settings</strong>)</td><td>RETOUR ARRIÈRE</td></tr><tr><td>HOTKEY + EST</td><td>Pause</td><td>P</td></tr><tr><td>HOTKEY + R3</td><td>Capture d'écran</td><td>F8</td></tr><tr><td>—</td><td>Afficher / masquer le menu de FBNeo</td><td>F1</td></tr><tr><td>—</td><td>Plein écran / fenêtre</td><td>F</td></tr><tr><td>—</td><td>Avance rapide (activer / désactiver)</td><td>ESPACE</td></tr><tr><td>—</td><td>Quitter le plein écran</td><td>ÉCHAP</td></tr></tbody></table>

Les touches se changent dans le fichier `kb_hotkeys.yml` (voir la page [**Raccourcis**](../../../navigation/hotkeys.md)).

## Dossiers

<table><thead><tr><th width="371.5">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Jeux</td><td><code>roms\fbneo</code></td></tr><tr><td>BIOS</td><td><code>bios</code>, <code>bios\fbneo</code> ou <code>roms\fbneo</code></td></tr><tr><td>Samples (core fbneo, FBNeo)</td><td><code>bios\fbneo\samples</code></td></tr><tr><td>Fichier des meilleurs scores (<code>hiscore.dat</code>)</td><td><code>bios\fbneo</code> (copié dans <code>saves\fbneo\fbneo</code> pour FBNeo autonome)</td></tr><tr><td>Codes de triche (core fbneo, FBNeo)</td><td><code>bios\fbneo\cheats</code></td></tr><tr><td>NVRAM, EEPROM, meilleurs scores, cartes mémoire Neo Geo</td><td><code>saves\fbneo\fbneo</code></td></tr><tr><td>Core fbneo : sauvegardes instantanées</td><td><code>saves\fbneo\libretro.fbneo</code></td></tr><tr><td>Core fbneo : patchs IPS</td><td><code>bios\fbneo\ips\&#x3C;jeu></code></td></tr><tr><td>FBNeo : sauvegardes instantanées</td><td><code>emulators\fbneo\savestates</code></td></tr><tr><td>FBNeo : patchs IPS</td><td><code>emulators\fbneo\support\ips\&#x3C;jeu></code></td></tr><tr><td>FBNeo : configuration</td><td><code>emulators\fbneo\config\fbneo64.ini</code>, touches par jeu dans <code>emulators\fbneo\config\games</code></td></tr><tr><td>Mappage par jeu (FBNeo)</td><td><code>system\resources\inputmapping\fbneo.yml</code> (copie modifiable dans <code>user\inputmapping</code>)</td></tr><tr><td>Samples (fbalpha2012)</td><td><code>bios\fba\samples</code></td></tr></tbody></table>

## Guides

### Menu de diagnostic et dip switches

Beaucoup de bornes ont un menu de test, souvent appelé menu de service. On y règle la difficulté, le nombre de vies, le jeu gratuit…

Avec le core fbneo, la combinaison **START + L1 + R1** ouvre ce menu en jeu. **ÉMULATION > ACCÈS AU MENU DIAGNOSTIQUE** permet de choisir une autre combinaison (ou **AUCUN**). Le menu n'existe pas sur toutes les bornes.

<div align="left"><figure><img src="../../../.gitbook/assets/image (663).png" alt=""><figcaption></figcaption></figure></div>

Les **dip switches** sont les interrupteurs de la carte de la borne. Avec le core fbneo :

1. Ouvrez le menu de RetroArch (**HOTKEY + SUD**).
2. Allez dans **Options du cœur > Dip switches**.
3. Changez les réglages du jeu.

Chaque jeu a ses propres dip switches. **ÉMULATION > JEU GRATUIT** règle directement celui du jeu gratuit quand le jeu en a un.

<div align="left"><figure><img src="../../../.gitbook/assets/image (662).png" alt=""><figcaption></figcaption></figure></div>

Avec FBNeo autonome, les dip switches se règlent dans le menu de FBNeo : **F1** pour l'afficher, puis **Input > Set dipswitches** (ou **Ctrl + F5**).

### Meilleurs scores

**ÉMULATION > ACTIVER HISCORES**, activé par défaut, garde les meilleurs scores des jeux d'une partie à l'autre, comme les bornes équipées d'une sauvegarde. Le fichier `hiscore.dat` est fourni par RetroBat dans `bios\fbneo`.

Les scores sont rangés dans `saves\fbneo\fbneo`, le même dossier pour le core fbneo et FBNeo autonome. Ils ne sont pas gardés en jeu en réseau.

### RetroAchievements

FBNeo est le core le mieux suivi par RetroAchievements pour l'arcade. En mode hardcore, RetroArch refuse :

* le BIOS Universe des jeux Neo Geo ;
* les romsets patchés ;
* une fréquence de processeur réduite ;
* les codes de triche.

RetroBat règle tout seul le BIOS et les romsets patchés en hardcore. Laissez **ÉMULATION > BIOS** sur son réglage par défaut et **ÉMULATION > OVERCLOCKING CPU** à 100 % ou plus.

Pour plus de détails, voir la page [**RetroAchievements**](../../../utilisation-avancee/retroachievements.md).

### Jeux verticaux

Les shoot'em up verticaux (Cave, Toaplan…) s'affichent tournés dans le bon sens, avec une décoration verticale par défaut.

* Avec le core fbneo, **VIDÉO > MODE TATÉ** tourne l'image pour un écran posé à la verticale.
* Avec FBNeo autonome, **VIDÉO > INDEX DE L'ÉCRAN VERTICAL** affiche les jeux verticaux sur un autre écran.

### Pistolets

Le core fbneo gère jusqu'à 4 pistolets dans les jeux qui en utilisent (Operation Wolf, Lethal Enforcers…). Pour le réglage des pistolets, voir la page [**Pistolets**](../../../controleurs/supported-controllers/lightguns/).

### Patchs IPS

Les patchs IPS modifient un jeu : traduction, correction, version hack. Ce sont des fichiers `.dat` rangés dans un dossier au nom du jeu.

* **Core fbneo** : placez les patchs dans `bios\fbneo\ips\<jeu>`, puis choisissez-les dans les options du core de RetroArch (menu de RetroArch, **Options du cœur**). Ils sont désactivés en mode hardcore des RetroAchievements.
* **FBNeo (autonome)** : placez les patchs dans `emulators\fbneo\support\ips\<jeu>`, puis activez **ÉMULATION > ACTIVER LES PATCHS IPS**. Sans autre réglage, les patchs cochés dans FBNeo sont appliqués. **ÉMULATION > FICHIER DU PATCH IPS** choisit un seul patch, qui doit se trouver dans ce dossier.

### Autres options utiles

**Core fbneo**

<table><thead><tr><th width="340.25">Option</th><th>Effet</th></tr></thead><tbody><tr><td><strong>ÉMULATION > OVERCLOCKING CPU</strong></td><td>Accélère le processeur émulé, pour réduire les ralentissements d'origine de certains jeux. Sous 100 %, le mode hardcore des RetroAchievements est refusé.</td></tr><tr><td><strong>VIDÉO > SAUT D'IMAGE</strong></td><td>Saute des images sur un PC trop lent.</td></tr><tr><td><strong>VIDÉO > FORCER 60HZ</strong></td><td>Force les jeux à 60 Hz (fréquence d'origine parfois différente, par exemple 59,18 Hz sur Neo Geo).</td></tr><tr><td><strong>VIDÉO > RÉSOLUTION VECTORIELLE</strong></td><td>Résolution de rendu des jeux vectoriels (Asteroids…).</td></tr><tr><td><strong>AUDIO > TAUX D'ÉCHANTILLONNAGE</strong></td><td>44 100 Hz (par défaut avec RetroBat) ou 48 000 Hz.</td></tr><tr><td><strong>AUDIO > FILTRE PASSE-BAS</strong></td><td>Adoucit le son.</td></tr></tbody></table>

**FBNeo (autonome)**

<table><thead><tr><th width="345.25">Option</th><th>Effet</th></tr></thead><tbody><tr><td><strong>PILOTES > VIDÉO</strong></td><td><strong>DIRECTX9</strong> (par défaut), <strong>DIRECTX9 (ALT)</strong>, <strong>DIRECT3D 11</strong>… Les décorations par ReShade ne fonctionnent qu'avec DirectX 9 et Direct3D 11.</td></tr><tr><td><strong>RENDU VISUEL > SCANLINES</strong></td><td>Lignes de balayage, de <strong>LÉGER</strong> à <strong>TRÈS INTENSE</strong>.</td></tr><tr><td><strong>RÉDUCTION DE LA LATENCE > ACTIVER L'EXÉCUTION EN AVANCE</strong></td><td>Réduit le délai entre l'appui sur un bouton et sa réaction à l'écran.</td></tr><tr><td><strong>VIDÉO > FORCER 60HZ</strong></td><td>Force les jeux à 60 Hz.</td></tr><tr><td><strong>MISE À L'ÉCHELLE (NOMBRE ENTIER)</strong></td><td>Agrandit l'image d'un nombre entier de fois, pour des pixels nets.</td></tr><tr><td><strong>PILOTES > AUDIO</strong></td><td><strong>DIRECT SOUND</strong> (par défaut), <strong>XAUDIO 2</strong> ou <strong>WASAPI</strong>.</td></tr></tbody></table>

## Problèmes connus

| Problème                                                         | Solution                                                                                                                                                                                  |
| ---------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Le jeu ne démarre pas, ou un fichier manque                      | Le romset ne correspond pas à la version de l'émulateur, ou un BIOS manque (voir [**BIOS**](final-burn-neo.md#bios) et [**Quel format de jeu ?**](final-burn-neo.md#quel-format-de-jeu)). |
| Écran noir avec du son sur un jeu Neo Geo                        | Le BIOS choisi manque dans `neogeo.zip` : utilisez le `neogeo.zip` de la même version de FBNeo, ou réglez **ÉMULATION > BIOS** sur **BIOS UNIVERSE**.                                     |
| Un jeu Konami ou autre échoue à son test de démarrage            | La NVRAM / EEPROM enregistrée est abîmée : supprimez les fichiers du jeu dans `saves\fbneo\fbneo`.                                                                                        |
| RetroAchievements passe en mode normal sur un jeu Neo Geo        | Le BIOS est réglé sur **BIOS UNIVERSE** : remettez **ÉMULATION > BIOS** sur son réglage par défaut.                                                                                       |
| Effets de transparence étranges                                  | Des fichiers `.bld` dans le dossier blend (`bios\fbneo\blend` pour le core) : retirez-les.                                                                                                |
| FBNeo autonome : les boutons d'un jeu ne sont pas configurés     | Le jeu n'est pas dans `fbneo.yml` : réglez les touches dans FBNeo (**F5**), ou ajoutez le jeu dans une copie du fichier placée dans `user\inputmapping`.                                  |
| FBNeo autonome : les manettes ne commandent pas les bons joueurs | Activez **CONTRÔLES > INDEX DE MANETTE ALTERNATIF**, ou débranchez les manettes qui ne servent pas.                                                                                       |
| Un fichier `.bin` ou `.chd` ne se lance pas                      | FBNeo ne lit que les romsets `.zip` / `.7z` dans ce système. Les CD Neo Geo vont dans le système Neo Geo CD.                                                                              |
