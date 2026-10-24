# Zelda Classic

<div align="left"><figure><img src="../../../.gitbook/assets/image (214).png" alt=""><figcaption></figcaption></figure></div>

Moteur de jeu - Sortie : 1999

{% embed url="https://zquestclassic.com" %}

Zelda Classic (aujourd'hui appelé ZQuest Classic) est un moteur de jeu qui reproduit le premier _The Legend of Zelda_. Des milliers d'aventures créées par des fans, appelées **quêtes**, ont été réalisées avec. RetroBat permet de jouer à ces quêtes.

RetroBat ne fournit aucune quête. On en trouve sur les sites de la communauté (par exemple [PureZC](https://www.purezc.net)).

## Informations

| **Émulateurs**       | <ul><li>zquestclassic (par défaut)</li><li>Libretro : zc255</li></ul> |
| -------------------- | --------------------------------------------------------------------- |
| **Dossier des jeux** | :open\_file\_folder: roms \ :open\_file\_folder: zeldaclassic         |
| **Extensions**       | .qst .zip .7z                                                         |

| Émulateur     | Quêtes compatibles                | Sauvegardes instantanées | Remarques                                     |
| ------------- | --------------------------------- | ------------------------ | --------------------------------------------- |
| zquestclassic | Toutes les versions, jusqu'à 2.55 | Non                      | Lecteur officiel de ZQuest Classic (zplayer). |
| zc255         | 2.55 et antérieures               | Oui                      | Core libretro (RetroArch).                    |

Si l'émulateur n'est pas encore installé, RetroBat propose de le télécharger au lancement du premier jeu.

## Bios

Aucun BIOS n'est nécessaire. Les données du moteur, la soundfont et les effets sonores sont inclus dans les deux émulateurs.

## Ajouter des quêtes

* Placez le fichier `.qst` directement dans `roms\zeldaclassic`, ou gardez-le compressé dans une archive `.zip` ou `.7z`.
* Une seule quête par archive : RetroBat lance le premier fichier `.qst` trouvé dans l'archive.
* **Musique améliorée** : certaines quêtes sont fournies avec des fichiers de musique. Gardez-les à côté du fichier `.qst`, ou dans un dossier portant le nom de la quête suivi de `_music` (pour `Adventure.qst` : `Adventure.qst_music`). Dans une archive, gardez la même organisation : RetroBat extrait toute l'archive avant de lancer la quête.

```
roms\zeldaclassic\
   Adventure.qst
   Adventure.qst_music\
   Autre Quete.zip
```

## Contrôles

RetroBat configure automatiquement la manette du **joueur 1**. Zelda Classic est un moteur à un seul joueur.

| Manette RetroBat                 | zquestclassic      | zc255 (libretro)                                  |
| -------------------------------- | ------------------ | ------------------------------------------------- |
| Croix directionnelle             | Déplacement        | Déplacement                                       |
| Stick analogique gauche          | Déplacement        | Déplacement (voir options)                        |
| Bouton du bas (Xbox A / PS ✕)    | A                  | A                                                 |
| Bouton de droite (Xbox B / PS ◯) | B                  | B                                                 |
| Bouton de gauche (Xbox X / PS ▢) | EX1                | EX1                                               |
| Bouton du haut (Xbox Y / PS △)   | EX2                | EX2                                               |
| START                            | Start (sous-écran) | Start (sous-écran)                                |
| SELECT                           | Carte              | Carte                                             |
| L1                               | L                  | L                                                 |
| R1                               | R                  | R                                                 |
| L2                               | EX3                | -                                                 |
| R2                               | EX4                | Recharge (seulement si les triches sont activées) |
| Guide / Home                     | Menu du moteur     | -                                                 |

A, B et les boutons EX sont utilisés par la quête elle-même : leur action dépend de la quête (épée, objet, objets supplémentaires…).

L'option **SWAP A/B AND X/Y** inverse les boutons de façade, par exemple pour retrouver une disposition de type Nintendo.

### Raccourcis

| Raccourci         | zquestclassic                 | zc255 (libretro)                                                         |
| ----------------- | ----------------------------- | ------------------------------------------------------------------------ |
| HOTKEY + START    | Quitter et revenir à RetroBat | Quitter et revenir à RetroBat                                            |
| Autres raccourcis | -                             | Raccourcis RetroArch habituels (sauvegardes instantanées, rewind, menu…) |

Avec l'émulateur **zquestclassic**, le clavier garde les touches du moteur : flèches = déplacement, `Z` = A, `X` = B, `Entrée` = Start, `Espace` = Carte, `Q` / `W` = L / R, `A` `S` `D` `C` = EX1 à EX4, `Échap` = menu du moteur.

## Sauvegardes

Chaque quête a sa propre sauvegarde, créée par la quête elle-même (points de sauvegarde, écran de continue…).

| Émulateur     | Emplacement                         | Nom du fichier de sauvegarde               |
| ------------- | ----------------------------------- | ------------------------------------------ |
| zquestclassic | `saves\zeldaclassic\zquestclassic\` | nom du fichier du jeu (`Adventure.sav`)    |
| zc255         | `saves\zeldaclassic\`               | contenu de la quête (`zc255-<nombre>.sav`) |

{% hint style="warning" %}
Les deux émulateurs ne partagent pas leurs sauvegardes. Utilisez toujours le même émulateur pour une quête.

Avec **zquestclassic**, renommer le fichier du jeu démarre une nouvelle sauvegarde. Avec **zc255**, le renommage ne pose pas de problème, mais une nouvelle version de la quête démarre une nouvelle sauvegarde.
{% endhint %}

## Options

Les options de triche du core (invincibilité, traverser les murs, recharges avec R2) ne sont pas gérées par RetroBat. Elles se règlent dans le menu de RetroArch, dans **Options du cœur**.

### Informations spécifiques au système

* **zquestclassic** est l'émulateur conseillé : c'est le lecteur officiel et il lit toutes les versions de quêtes.
* **zc255** permet d'avoir les sauvegardes instantanées et les fonctions de RetroArch (shaders, rewind…). Quelques quêtes ne permettent pas les sauvegardes instantanées.
