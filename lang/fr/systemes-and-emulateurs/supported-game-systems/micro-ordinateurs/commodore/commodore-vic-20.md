---
description: Commodore
---

# Commodore VIC-20

<div align="left"><figure><img src="../../../../.gitbook/assets/image (587).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Présentation

Le **VIC-20** sort en 1980 au Japon (sous le nom VIC-1001), puis en 1981 en Europe et aux États-Unis. C'est le premier ordinateur personnel vendu à plus d'un million d'exemplaires. Il ne dispose que de 5 Ko de mémoire et affiche 22 colonnes de texte, mais son prix et sa simplicité en font la première machine de beaucoup de joueurs et de programmeurs.

Les jeux sortent sur cartouche et sur cassette, puis sur disquette. Beaucoup de programmes demandent une **extension mémoire** (3, 8 ou 16 Ko), que l'on branchait sur le port cartouche. On y trouve des adaptations de jeux d'arcade comme Gorf, Omega Race ou Jupiter Lander. Le Commodore 64 le remplace à partir de 1982.

RetroBat émule le VIC-20 avec **VICE**, l'émulateur de référence des ordinateurs Commodore.

{% embed url="https://fr.wikipedia.org/wiki/Commodore_VIC-20" %}

## En bref

<table><thead><tr><th width="260.25"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\c20</code></td></tr><tr><td><strong>Extensions</strong></td><td>.nib .a0 .b0 .crt .d64 .d81 .prg .tap .t64 .m3u .zip .7z</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: vice_xvic</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr><tr><td><strong>Pistolets</strong></td><td>cores libretro (vice_xvic)</td></tr></tbody></table>

## Quel émulateur choisir ?

Le VIC-20 n'a qu'un émulateur dans RetroBat.

<table><thead><tr><th width="164.5">Émulateur</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>libretro: vice_xvic</strong> (défaut)</td><td>Émulation très fidèle, extensions mémoire, lecteurs de disquette et de cassette émulés, clavier virtuel, sauvegardes instantanées, crayon optique.</td><td>Les jeux sur cassette se chargent lentement, comme sur la vraie machine (voir <a href="commodore-vic-20.md#accelerer-le-chargement-des-cassettes">Guides</a>).</td></tr></tbody></table>

## BIOS

Aucun BIOS n'est nécessaire : les ROM du VIC-20 sont intégrées à VICE.

## Quel format de jeu ?

<table><thead><tr><th width="136.5">Format</th><th>Remarques</th></tr></thead><tbody><tr><td><strong>.crt</strong></td><td>Cartouche au format VICE. Démarre immédiatement.</td></tr><tr><td><strong>.a0</strong>, <strong>.b0</strong></td><td>Cartouche en image brute, nommée d'après son adresse en mémoire.</td></tr><tr><td><strong>.prg</strong></td><td>Programme seul, chargé directement en mémoire. Le plus rapide à démarrer.</td></tr><tr><td><strong>.d64</strong>, .d81</td><td>Image de disquette (lecteurs 1541 et 1581).</td></tr><tr><td><strong>.tap</strong></td><td>Image de cassette. Le chargement est long (voir <a href="commodore-vic-20.md#accelerer-le-chargement-des-cassettes">Guides</a>).</td></tr><tr><td>.t64</td><td>Archive de cassette.</td></tr><tr><td>.nib</td><td>Image exacte d'une disquette protégée contre la copie.</td></tr><tr><td>.m3u</td><td>Liste des disquettes ou cassettes d'un même jeu.</td></tr><tr><td>.zip, .7z</td><td>Archive contenant un des formats ci-dessus.</td></tr></tbody></table>

VICE démarre le jeu tout seul : pas besoin de taper la commande de chargement.

## Contrôles

### Configuration automatique

RetroBat configure automatiquement les manettes. Le VIC-20 n'a qu'un port joystick, utilisé par la manette du joueur 1.

<table><thead><tr><th width="266.5">Manette RetroBat</th><th>VIC-20</th></tr></thead><tbody><tr><td>Croix directionnelle</td><td>Joystick</td></tr><tr><td>SUD</td><td>Tir</td></tr><tr><td>NORD</td><td>Barre d'espace</td></tr><tr><td>L2</td><td>RUN/STOP (touche Échap)</td></tr><tr><td>R2</td><td>RETURN (Entrée)</td></tr><tr><td>SELECT</td><td>Clavier virtuel</td></tr></tbody></table>

Beaucoup de jeux demandent d'appuyer sur la barre d'espace, sur RETURN ou sur une touche de fonction pour commencer : utilisez NORD, R2 ou le clavier virtuel.

### Clavier virtuel

**SELECT** affiche ou masque le clavier virtuel. Déplacez-vous avec la croix directionnelle et appuyez sur une touche avec **SUD**. Dans le clavier virtuel, **START** tape RETURN, **NORD** la barre d'espace, **OUEST** verrouille les majuscules (SHIFT LOCK) et **EST** rend le clavier transparent.

### Clavier

Un clavier branché sur le PC sert de clavier VIC-20. Activez **CONTRÔLES > FOCUS CLAVIER** pour que les touches ne déclenchent pas les raccourcis de RetroArch. La touche **Arrêt défil** active ou désactive ce mode en jeu.

### Options de contrôle

| Option                                                 | Effet                                                               |
| ------------------------------------------------------ | ------------------------------------------------------------------- |
| **CONTRÔLES > TYPE DE PORT JOYSTICK**                  | Joystick (par défaut), paddles, souris, crayon optique ou pistolet. |
| **CONTRÔLES > OPTIONS DES BOUTONS DE FAÇADE RETROPAD** | Change le bouton de tir, ou place « haut » (sauter) sur un bouton.  |
| **CONTRÔLES > TYPE DE CONTRÔLEUR JOUEUR 1**            | RETROPAD (par défaut), JOYSTICK ou CLAVIER.                         |

### Pistolets

L'option **PISTOLETS > ACTIVER LES PISTOLETS** branche un crayon optique sur le port joystick. L'option **TYPE DE PORT JOYSTICK** permet de choisir un autre modèle de crayon optique ou de pistolet.

Pour plus de détails, voir la page [**Pistolets**](../../../../controleurs/supported-controllers/lightguns/).

### Raccourcis

vice\_xvic utilise les raccourcis standards de RetroArch (voir la page [**Raccourcis**](../../../../navigation/hotkeys.md)).

## Dossiers

| Contenu                                  | Dossier                        |
| ---------------------------------------- | ------------------------------ |
| Sauvegardes instantanées                 | `saves\c20\libretro.vice_xvic` |
| Disquettes de sauvegarde créées par VICE | `saves\c20`                    |
| Captures d'écran                         | `screenshots`                  |

## Guides

### Extension mémoire

Beaucoup de jeux VIC-20 demandent une extension mémoire. L'option **ÉMULATION > EXTENSION MÉMOIRE** est réglée sur **AUTOMATIQUE** : VICE choisit l'extension d'après la taille du programme.

Vous pouvez aussi indiquer l'extension dans le nom du fichier : `(8k)`, `(16k)`, `[8k]`… Par exemple `Mon jeu (16k).prg`. Ou choisissez une valeur fixe dans l'option (3, 8, 16, 24 ou 35 Ko).

### Accélérer le chargement des cassettes

Un jeu sur cassette met plusieurs minutes à se charger. L'option **ÉMULATION > CHARGEMENT RAPIDE** fait tourner l'émulation à vitesse maximale pendant le chargement, tant qu'aucun son n'est joué. Elle marche aussi avec les disquettes, si **ÉMULATION > ÉMULATION FIDÈLE DU LECTEUR** est activée.

### Choisir le modèle et la région

L'option **ÉMULATION > MODÈLE DE MACHINE ÉMULÉE** choisit la machine émulée : VIC-20 PAL ou NTSC, ou Super VIC (VIC-20 avec 16 Ko de plus).

Les modèles **Auto** choisissent la région d'après le nom du fichier : `NTSC`, `(USA)` ou `(Japan)` lancent le jeu en NTSC, `PAL` ou `(Europe)` en PAL. Sans indication, c'est la région du modèle choisi. Le réglage par défaut est **VIC-20 PAL Auto**.

### Autres options utiles

| Option                                       | Effet                                                 |
| -------------------------------------------- | ----------------------------------------------------- |
| **RENDU VISUEL > PALETTE DE COULEURS**       | Colodore (par défaut), Mike, palette interne de VICE… |
| **RENDU VISUEL > RECADRER (CROP)**           | Masque la bordure autour de l'image.                  |
| **RENDU VISUEL > RATIO D'ASPECT DES PIXELS** | Forme des pixels : automatique, PAL, NTSC ou carrés.  |

## Problèmes connus

| Problème                                                              | Solution                                                                                                                                   |
| --------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| Le jeu ne démarre pas, affiche un écran vide ou une erreur de mémoire | Il demande une autre extension mémoire : ajoutez-la dans le nom du fichier (`(8k)`, `(16k)`…) ou choisissez-la dans **EXTENSION MÉMOIRE**. |
| Le jeu tourne trop vite ou l'image est décalée                        | Il n'est pas lancé dans la bonne région : choisissez un modèle **PAL** ou **NTSC**.                                                        |
| Le jeu reste bloqué sur un écran de chargement                        | C'est normal avec une cassette : activez **CHARGEMENT RAPIDE** ou utilisez une version `.prg` / `.crt`.                                    |
| Le jeu demande d'appuyer sur une touche                               | Utilisez NORD (barre d'espace), R2 (RETURN) ou le clavier virtuel (SELECT).                                                                |
