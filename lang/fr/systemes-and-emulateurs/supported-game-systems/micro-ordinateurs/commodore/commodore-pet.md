---
description: Commodore
---

# Commodore PET

<div align="left"><figure><img src="../../../../.gitbook/assets/image (584).png" alt="" width="240"><figcaption></figcaption></figure></div>

## Présentation

Le **Commodore PET** (Personal Electronic Transactor) sort en 1977. Avec l'Apple II et le TRS-80, il fait partie des tout premiers ordinateurs personnels vendus prêts à l'emploi. Tout est dans le même boîtier : écran monochrome, clavier et, sur le premier modèle, lecteur de cassette.

Il a surtout servi dans les écoles et les entreprises. Plusieurs séries se succèdent : 2001, 3000, 4000, puis 8000 avec un affichage de 80 colonnes. Ses jeux sont simples, souvent dessinés avec les caractères graphiques PETSCII et joués au clavier : le PET n'a pas de port joystick.

RetroBat émule le PET avec **VICE**, l'émulateur de référence des ordinateurs Commodore.

{% embed url="https://fr.wikipedia.org/wiki/Commodore_PET" %}

## En bref

<table><thead><tr><th width="266.5"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\pet</code></td></tr><tr><td><strong>Extensions</strong></td><td>.crt .d64 .d80 .d81 .d82 .prg .tap .t64 .m3u .zip .7z</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: vice_xpet</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique (touches du clavier sur la manette)</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr></tbody></table>

## Quel émulateur choisir ?

Le PET n'a qu'un émulateur dans RetroBat.

| Émulateur                         | Points forts                                                                                                               | Limites                        |
| --------------------------------- | -------------------------------------------------------------------------------------------------------------------------- | ------------------------------ |
| **libretro: vice\_xpet** (défaut) | Émule tous les modèles de PET, les lecteurs de disquette et de cassette, avec clavier virtuel et sauvegardes instantanées. | Les jeux se jouent au clavier. |

## BIOS

Aucun BIOS n'est nécessaire : les ROM des différents PET sont intégrées à VICE.

## Quel format de jeu ?

<table><thead><tr><th width="227.75">Format</th><th>Remarques</th></tr></thead><tbody><tr><td><strong>.prg</strong></td><td>Programme seul, chargé directement en mémoire. Le format le plus courant pour les jeux PET.</td></tr><tr><td><strong>.d64</strong>, .d80, .d81, .d82</td><td>Image de disquette (lecteurs 2040 / 4040, 8050, 1581, 8250).</td></tr><tr><td>.tap, .t64</td><td>Cassette. Le chargement d'une <code>.tap</code> est long.</td></tr><tr><td>.crt</td><td>Cartouche.</td></tr><tr><td>.m3u</td><td>Liste des disquettes d'un même programme.</td></tr><tr><td>.zip, .7z</td><td>Archive contenant un des formats ci-dessus.</td></tr></tbody></table>

VICE démarre le programme tout seul : pas besoin de taper la commande de chargement.

## Contrôles

### Configuration automatique

Le PET n'a pas de port joystick : les jeux se jouent au clavier. Quelques touches du clavier sont placées sur la manette :

<table><thead><tr><th width="180.25">Manette RetroBat</th><th>PET</th></tr></thead><tbody><tr><td>NORD</td><td>Barre d'espace</td></tr><tr><td>L2</td><td>RUN/STOP (touche Échap)</td></tr><tr><td>R2</td><td>RETURN (Entrée)</td></tr><tr><td>SELECT</td><td>Clavier virtuel</td></tr></tbody></table>

### Clavier virtuel

**SELECT** affiche ou masque le clavier virtuel. Déplacez-vous avec la croix directionnelle et appuyez sur une touche avec **SUD**. Dans le clavier virtuel, **START** tape RETURN, **NORD** la barre d'espace, **OUEST** verrouille les majuscules (SHIFT LOCK) et **EST** rend le clavier transparent.

### Clavier

Un clavier branché sur le PC sert de clavier PET : c'est la façon la plus simple de jouer. Activez **CONTRÔLES > FOCUS CLAVIER** pour que les touches ne déclenchent pas les raccourcis de RetroArch. La touche **Arrêt défil** active ou désactive ce mode en jeu.

Pour placer d'autres touches sur la manette, créez un profil PadToKey (voir la page [**PadToKey**](../../../../controleurs/pad2key.md)).

### Raccourcis

vice\_xpet utilise les raccourcis standards de RetroArch (voir la page [**Raccourcis**](../../../../navigation/hotkeys.md)).

## Dossiers

| Contenu                                  | Dossier                        |
| ---------------------------------------- | ------------------------------ |
| Sauvegardes instantanées                 | `saves\pet\libretro.vice_xpet` |
| Disquettes de sauvegarde créées par VICE | `saves\pet`                    |
| Captures d'écran                         | `screenshots`                  |

## Guides

### Choisir le modèle

L'option **ÉMULATION > MODÈLE DE MACHINE ÉMULÉE** choisit le PET émulé. Le modèle par défaut est le **PET 8032** (80 colonnes, 32 Ko).

Beaucoup de jeux ont été écrits pour les modèles à 40 colonnes : s'ils s'affichent mal ou ne démarrent pas, choisissez **PET 4032**, ou **PET 2001** pour les plus anciens.

### Autres options utiles

<table><thead><tr><th width="355.25">Option</th><th>Effet</th></tr></thead><tbody><tr><td><strong>RENDU VISUEL > PALETTE DE COULEURS</strong></td><td>Couleur du moniteur : interne (par défaut), vert, ambre ou blanc.</td></tr><tr><td><strong>RENDU VISUEL > RECADRER (CROP)</strong></td><td>Masque la bordure autour de l'image.</td></tr><tr><td><strong>ÉMULATION > CHARGEMENT RAPIDE</strong></td><td>Fait tourner l'émulation à vitesse maximale pendant le chargement d'une disquette ou d'une cassette.</td></tr></tbody></table>

## Problèmes connus

<table><thead><tr><th width="256.5">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Le jeu s'affiche mal ou ne démarre pas</td><td>Il est écrit pour un autre modèle : choisissez <strong>PET 4032</strong> ou <strong>PET 2001</strong>.</td></tr><tr><td>La manette ne déplace rien dans le jeu</td><td>Le PET n'a pas de joystick : jouez au clavier, avec le clavier virtuel (SELECT) ou avec un profil <a href="../../../../controleurs/pad2key.md">PadToKey</a>.</td></tr></tbody></table>
