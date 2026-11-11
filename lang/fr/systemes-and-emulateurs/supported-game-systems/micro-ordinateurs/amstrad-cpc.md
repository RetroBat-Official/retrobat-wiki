---
description: Amstrad
---

# Amstrad CPC

<div align="left"><figure><img src="../../../.gitbook/assets/image (518).png" alt=""><figcaption></figcaption></figure></div>

## Présentation

L'**Amstrad CPC** (Colour Personal Computer) est une gamme de micro-ordinateurs 8 bits lancée en 1984 par la société britannique Amstrad, fondée par Alan Sugar. L'idée était simple : vendre un ordinateur complet, prêt à brancher. Le CPC 464 réunit en un seul achat l'unité centrale avec son clavier, un lecteur de cassettes intégré et un moniteur (couleur ou monochrome vert), le tout sur une seule prise électrique.

La machine repose sur un processeur Zilog Z80A à 4 MHz, 64 Ko de mémoire, une palette de 27 couleurs et la puce sonore AY-3-8912. Elle démarre directement sur le Locomotive BASIC : sur un vrai CPC, il faut taper une commande pour lancer un jeu.

La gamme a vite évolué :

* **CPC 464** (1984) : 64 Ko, lecteur de cassettes ;
* **CPC 664** (1985) : un lecteur de disquettes 3 pouces remplace les cassettes ;
* **CPC 6128** (1985) : 128 Ko et lecteur de disquettes, le modèle le plus répandu ;
* **464 Plus** et **6128 Plus** (1990) : port cartouche, palette de 4096 couleurs et sprites matériels, comme la console GX4000 (voir la [page **Amstrad GX4000**](../consoles-de-jeu/gx4000.md)).

Vendu à environ trois millions d'exemplaires, le CPC a connu un très grand succès en France, en Espagne et au Royaume-Uni. Sa ludothèque compte des milliers de titres : Gryzor, Renegade, Rick Dangerous, Sorcery, Crafton & Xunk, L'Aigle d'Or, Head Over Heels, Barbarian, Prince of Persia, La Abadía del Crimen…

{% embed url="https://fr.wikipedia.org/wiki/Amstrad_CPC" %}

## En bref

<table><thead><tr><th width="280.25"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\amstradcpc</code></td></tr><tr><td><strong>Extensions</strong></td><td>.dsk .kcr .sna .tap .cdt .voc .m3u .zip .7z</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: cap32</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro</td></tr><tr><td><strong>RetroAchievements</strong></td><td>cores libretro (cap32)</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>cores libretro</td></tr><tr><td><strong>Pistolets</strong></td><td>cores libretro (cap32)</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="161.5">Émulateur</th><th width="154.25">Pour qui ?</th><th width="232.25">Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>libretro: cap32</strong> (défaut)</td><td>Tout le monde</td><td>Lance les jeux tout seul (disquettes et cassettes), clavier virtuel, touches du clavier déjà placées sur la manette pour près de 400 jeux, jeux multi-disquettes, RetroAchievements, pistolets.</td><td>—</td></tr><tr><td><strong>libretro: crocods</strong></td><td>Ceux qui veulent le plus simple</td><td>Démarre vite, lance les disquettes tout seul.</td><td>Disquettes et snapshots seulement, pas de cassettes, pas de clavier virtuel, pas de RetroAchievements.</td></tr><tr><td><strong>capriceforever</strong></td><td>Utilisateurs avancés</td><td>Émulation très fidèle, nombreuses extensions matérielles (mémoire, synthèses vocales, PlayCity, Multiface II…), deux lecteurs de disquettes.</td><td>Pas de sauvegardes instantanées dans RetroBat, pas de RetroAchievements, un clavier est conseillé.</td></tr></tbody></table>

**En cas de doute, gardez cap32.**

## BIOS

Aucun BIOS n'est nécessaire : les émulateurs contiennent déjà les ROM de l'Amstrad.

### Langue de la machine

Le CPC a existé en version anglaise (clavier QWERTY), française (clavier AZERTY) et espagnole. Par défaut, RetroBat émule un CPC 6128 anglais. Certains jeux français attendent un clavier AZERTY.

<table><thead><tr><th width="152">Émulateur</th><th width="320.5">Option</th><th>Choix</th></tr></thead><tbody><tr><td>cap32</td><td><strong>ÉMULATION > DISPOSITION CLAVIER</strong></td><td>ANGLAIS (défaut), FRANÇAIS, ESPAGNOL</td></tr><tr><td>capriceforever</td><td><strong>ÉMULATION > MODÈLE D'AMSTRAD</strong></td><td>CPC 6128 UK (défaut), CPC 6128 FR, CPC 6128 ES, CPC 464 UK, CPC 464 FR, CPC 464 ES</td></tr><tr><td>crocods</td><td>—</td><td>Anglais seulement</td></tr></tbody></table>

Avec cap32, l'option **ÉMULATION > MODÈLE DE MACHINE ÉMULÉE** permet aussi d'émuler un 464 ou un 664 pour les jeux les plus anciens.

## Quel format de jeu ?

<table><thead><tr><th width="132.25">Format</th><th width="91">cap32</th><th width="100.5">crocods</th><th width="153.25">capriceforever</th><th>Remarques</th></tr></thead><tbody><tr><td><strong>.dsk</strong></td><td>✔</td><td>✔</td><td>✔</td><td>Disquette. Format conseillé : chargement rapide.</td></tr><tr><td>.m3u</td><td>✔</td><td>✘</td><td>✔</td><td>Jeux sur plusieurs disquettes (voir Guides).</td></tr><tr><td>.cdt / .voc</td><td>✔</td><td>✘</td><td>✘</td><td>Cassette. Chargement long, comme sur la vraie machine.</td></tr><tr><td>.tap</td><td>✔</td><td>✘</td><td>✔</td><td>Cassette.</td></tr><tr><td>.sna</td><td>✔</td><td>✔</td><td>✘</td><td>Snapshot : copie de la mémoire d'un jeu déjà chargé.</td></tr><tr><td>.kcr</td><td>✘</td><td>✔</td><td>✘</td><td>Format propre à CrocoDS.</td></tr><tr><td>.zip</td><td>✔</td><td>✘</td><td>✔ (extrait au lancement)</td><td></td></tr><tr><td>.7z</td><td>✔</td><td>✔</td><td>✔ (extrait au lancement)</td><td></td></tr></tbody></table>

## Contrôles

### Configuration automatique

RetroBat configure automatiquement les manettes pour tous les émulateurs (deux manettes au maximum avec Caprice Forever).

Un joystick Amstrad n'a que deux ou trois boutons de tir. Beaucoup de jeux utilisent aussi le clavier : pour choisir « joystick » dans un menu, lancer la partie ou mettre en pause. RetroBat place donc des touches du clavier sur la manette.

| Manette RetroBat                    | cap32                          | crocods         | capriceforever |
| ----------------------------------- | ------------------------------ | --------------- | -------------- |
| Croix directionnelle / stick gauche | Joystick                       | Joystick        | Joystick       |
| EAST                                | Feu 1                          | Feu 1           | Feu 1          |
| SOUTH                               | Feu 2                          | Feu 2           | Feu 2          |
| NORTH                               | Feu 3                          | —               | —              |
| WEST                                | Touche combo (voir ci-dessous) | —               | —              |
| L1                                  | CONTROL                        | —               | —              |
| R1                                  | RETURN (Entrée)                | —               | —              |
| L2                                  | F1                             | —               | —              |
| R2                                  | F2                             | —               | —              |
| START                               | —                              | RETURN (Entrée) | —              |
| SELECT                              | —                              | Espace          | —              |
| L3                                  | Clavier virtuel                |                 |                |

Avec crocods, la deuxième manette envoie les touches curseur et Espace du clavier, pas un deuxième joystick.

### Touche combo et clavier virtuel (cap32)

Maintenez **WEST** et appuyez sur un autre bouton pour envoyer une commande à l'Amstrad :

<table><thead><tr><th width="205.25">Combinaison</th><th>Action</th></tr></thead><tbody><tr><td><strong>L3</strong> ou <strong>WEST + START</strong></td><td>Affiche ou masque le clavier virtuel</td></tr><tr><td>WEST + EAST</td><td>Tape <code>RUN"DISK</code> puis <code>RUN"DISC</code> (lance beaucoup de jeux sur disquette)</td></tr><tr><td>WEST + SOUTH</td><td>Tape <code>CAT</code> (liste le contenu de la disquette)</td></tr><tr><td>WEST + NORTH</td><td>Tape les commandes de lancement d'une cassette</td></tr><tr><td>WEST + HAUT</td><td>Tape <code>1</code> puis <code>Y</code></td></tr><tr><td>WEST + BAS</td><td>Tape <code>2</code> puis <code>N</code></td></tr><tr><td>WEST + DROITE</td><td>Tape <code>3</code> puis <code>J</code></td></tr><tr><td>WEST + GAUCHE</td><td>Tape <code>4</code> puis <code>S</code></td></tr><tr><td>WEST + L1 / R1</td><td>Disquette précédente / suivante (jeux <code>.m3u</code>)</td></tr></tbody></table>

Les combinaisons avec les directions servent à répondre aux menus des jeux (choix 1 à 4, oui / non, joystick…).

Dans le clavier virtuel, déplacez le curseur avec la croix directionnelle et appuyez sur une touche avec **EAST**. La souris fonctionne aussi.

L'option **CONTRÔLES > TOUCHE COMBO** permet de choisir un autre bouton.

### Touches du clavier sur la manette (cap32)

Pour près de 400 jeux, RetroBat place automatiquement sur la manette les touches du clavier dont le jeu a besoin. Le jeu est reconnu par le nom de son fichier (voir [Guides](amstrad-cpc.md#personnaliser-les-touches-dun-jeu-cap32)).

### Clavier

Un clavier branché sur le PC sert de clavier Amstrad avec tous les émulateurs.

* Avec cap32 et crocods, activez **CONTRÔLES > FOCUS CLAVIER** pour que les touches ne déclenchent pas les raccourcis de RetroArch. La touche **Arrêt défil** active ou désactive ce mode en jeu.
* Avec cap32, **F9** affiche le clavier virtuel. Pour les cassettes : **Origine** = lecture, **Fin** = arrêt, **Page précédente** = rembobinage.
* Avec Caprice Forever, l'option **CONTRÔLES > SIMULER JOYSTICK AVEC CLAVIER** transforme les flèches en joystick, **ALT** en feu 1 et **CTRL** en feu 2.

Pour configurer vous-même vos manettes, désactivez **AUTOCONFIGURER LES MANETTES**.

### Raccourcis

**cap32** et **crocods** utilisent les raccourcis RetroArch (voir la [page Raccourcis](../../../navigation/hotkeys.md)).

**Caprice Forever** : **HOTKEY + START** pour quitter.

## Dossiers

<table><thead><tr><th width="344">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Sauvegardes instantanées cap32</td><td><code>saves\amstradcpc\libretro.cap32</code></td></tr><tr><td>Sauvegardes instantanées crocods</td><td><code>saves\amstradcpc\libretro.crocods</code></td></tr><tr><td>Sauvegardes sur disquette (cap32)</td><td><code>saves\amstradcpc</code> (fichier <code>.sav</code> au nom de la disquette, la disquette d'origine n'est pas modifiée)</td></tr><tr><td>Snapshots Caprice Forever</td><td><code>saves\amstradcpc\capriceforever</code></td></tr><tr><td>Captures d'écran Caprice Forever</td><td><code>screenshots\capriceforever</code></td></tr><tr><td>Cheats Caprice Forever</td><td><code>cheats\capriceforever</code></td></tr><tr><td>Profils de manette Caprice Forever</td><td><code>emulators\capriceforever\Profiles</code></td></tr><tr><td>Touches par jeu fournies par RetroBat (cap32)</td><td><code>system\resources\inputmapping\libretro_cap32.json</code></td></tr><tr><td>Touches par jeu personnalisées (cap32)</td><td><code>user\inputmapping\libretro_cap32.json</code></td></tr></tbody></table>

## Guides

### Jeux sur plusieurs disquettes (.m3u)

Créez un fichier texte portant le nom du jeu, avec l'extension `.m3u`, à côté des disquettes. Écrivez un nom de disquette par ligne :

```
Alive (F) - Disk 1A.dsk
Alive (F) - Disk 1B.dsk
```

Lancez ensuite le fichier `.m3u` depuis RetroBat.

* **cap32** : changez de disquette en jeu avec **WEST + L1** (précédente) ou **WEST + R1** (suivante).
* **Caprice Forever** : la première ligne va dans le lecteur A, la deuxième dans le lecteur B.

### Forcer la commande de lancement

cap32 devine la commande à taper pour lancer un jeu. Si le jeu ne démarre pas, vous pouvez imposer la bonne commande.

**cap32** : créez un fichier `.m3u` qui commence par une ligne `#COMMAND:`, suivie du nom de la disquette :

```
#COMMAND:RUN"COMMANDO.BIN
Commando (Europe).dsk
```

**Caprice Forever** : créez à côté du jeu un fichier texte du même nom avec l'extension `.autorun`, par exemple `Commando (Europe).autorun`. Sa première ligne contient la commande :

```
RUN"COMMANDO.BIN
```

Pour connaître le nom du fichier à lancer, affichez le contenu de la disquette avec `CAT` (**WEST + SOUTH** avec cap32).

### Personnaliser les touches d'un jeu (cap32)

RetroBat lit les touches par jeu dans `system\resources\inputmapping\libretro_cap32.json`. Pour modifier ou ajouter un jeu :

1. Copiez ce fichier dans `user\inputmapping`. RetroBat utilise alors votre copie, qui n'est pas écrasée par les mises à jour.
2. Ouvrez la copie avec un éditeur de texte.
3. Dans la liste `Roms` du jeu, ajoutez le nom exact de votre fichier, sans extension. Si le nom n'y figure pas, RetroBat compare le nom simplifié du fichier (minuscules, sans espaces ni texte entre parenthèses ou crochets) avec le champ `Name`.

<div align="left"><figure><img src="../../../.gitbook/assets/image (519).png" alt=""><figcaption></figcaption></figure></div>

### Jouer au pistolet (cap32)

1. Dans les options du jeu, activez **PISTOLETS > ACTIVER LES PISTOLETS**.
2. Choisissez **PISTOLETS > MODE PISTOLET** selon le jeu :

<table><thead><tr><th width="305.25">Mode</th><th>Jeux</th></tr></thead><tbody><tr><td><strong>PHASER</strong> (Amstrad Magnum Phaser)</td><td>Operation Wolf, Bullseye, Missile Ground Zero, Robot Attack, Rookie, Solar Invasion, American Turbo-King, Billy the Kid, Bronx Street Cop, F-16 Fighting Falcon, Jungle Warfare</td></tr><tr><td><strong>GUNSTICK</strong></td><td>Mike Gunner, Bestial Warrior, Cosmic Sheriff, El Equipo A, Guillermo Tell, Outlaws, Solo, Sootland, Space Smugglers, Target Plus, Trigger</td></tr><tr><td><strong>WEST PHASER</strong> (Loriciel West Phaser)</td><td>West Phaser</td></tr><tr><td><strong>TROJAN PHAZER</strong> (Trojan Light Phazer)</td><td>Jeux sur cartouche : voir la page <a href="../consoles-de-jeu/gx4000.md"><strong>Amstrad GX4000</strong></a></td></tr></tbody></table>

L'option **AFFICHER CIBLE** affiche un viseur à l'écran.

## Problèmes connus

<table><thead><tr><th width="340.25">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Le jeu ne démarre pas, l'écran reste sur <code>Ready</code></td><td>La commande automatique n'a pas trouvé le bon fichier. Essayez <strong>WEST + EAST</strong>, tapez la commande au clavier virtuel (<strong>L3</strong> ou <strong>WEST + START</strong>), ou imposez-la (voir <a href="amstrad-cpc.md#forcer-la-commande-de-lancement">Guides</a>).</td></tr><tr><td>Le jeu demande d'appuyer sur une touche ou de choisir clavier / joystick</td><td>Utilisez le clavier virtuel (<strong>L3</strong> ou <strong>WEST + START</strong>) ou les combinaisons <strong>WEST + direction</strong>.</td></tr><tr><td>Les touches tapées ne sont pas les bonnes dans un jeu français</td><td>Choisissez <strong>DISPOSITION CLAVIER</strong> : FRANÇAIS (cap32) ou <strong>MODÈLE D'AMSTRAD</strong> : CPC 6128 FR (Caprice Forever).</td></tr><tr><td>Un jeu très ancien ne fonctionne pas</td><td>Avec cap32, choisissez <strong>MODÈLE DE MACHINE ÉMULÉE</strong> : 464.</td></tr><tr><td>Une cassette met très longtemps à charger</td><td>C'est normal. Utilisez l'avance rapide de RetroArch (voir la <a href="../../../navigation/hotkeys.md">page Raccourcis</a>) ou préférez la version disquette <code>.dsk</code>.</td></tr><tr><td>Les raccourcis RetroArch se déclenchent quand je tape au clavier</td><td>Activez <strong>FOCUS CLAVIER</strong>.</td></tr><tr><td>Le pistolet ne répond pas</td><td>Vérifiez <strong>MODE PISTOLET</strong>. Le mode GUNSTICK ne fonctionne pas avec un moniteur vert : laissez <strong>TYPE DE MONITEUR</strong> sur COULEUR.</td></tr><tr><td>crocods ne lance pas le jeu</td><td>crocods ne lit que les fichiers <code>.dsk</code>, <code>.sna</code> et <code>.kcr</code> : utilisez cap32.</td></tr><tr><td>La manette ne répond pas avec Caprice Forever</td><td>La manette n'est pas reconnue : activez <strong>SIMULER JOYSTICK AVEC CLAVIER</strong> ou utilisez cap32.</td></tr><tr><td>Le clavier virtuel s'ouvre quand j'appuie sur L3</td><td>L3 ouvre toujours le clavier virtuel, même dans les jeux où RetroBat place une touche sur L3, et avec <strong>HOTKEY + L3</strong>. Appuyez de nouveau sur <strong>L3</strong> pour le fermer.</td></tr></tbody></table>
