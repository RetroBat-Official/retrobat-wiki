# Sauvegardes d'état

Les sauvegardes d'état prennent une photo du jeu à n'importe quel moment, pour pouvoir le reprendre plus tard exactement au même endroit.

{% hint style="danger" %}
Les sauvegardes d'état ne sont pas un moyen sûr de garder votre progression. Elles cessent souvent de fonctionner après une mise à jour de l'émulateur. Utilisez toujours d'abord le système de sauvegarde du jeu (carte mémoire, menu de sauvegarde…).
{% endhint %}

## Fonctionnement

* RetroBat gère les sauvegardes d'état des **cores RetroArch** et de plusieurs émulateurs autonomes (voir Émulateurs compatibles). Avec ces émulateurs, vous pouvez lancer un jeu directement depuis une sauvegarde d'état, à partir de la liste des jeux.
* Les sauvegardes d'état sont enregistrées dans `saves\<système>`, dans le dossier de l'émulateur (pour RetroArch : `saves\<système>\libretro.<core>`), avec une capture d'écran du moment de la sauvegarde.
* Un jeu qui a des sauvegardes d'état affiche une icône dans la liste des jeux.
* Les sauvegardes d'état ne sont pas partagées entre émulateurs : une sauvegarde faite avec un émulateur ne peut être chargée que par lui.

### Émulateurs compatibles

Dossiers dans `saves\<système>`. **Sauv. auto** : option SAUV./CHARG. AUTO gérée. **Incrémentales** : option SAUVEGARDES D'ÉTAT INCRÉMENTALES gérée.

| Émulateur                  | Dossier                                | Sauv. auto | Incrémentales |
| -------------------------- | -------------------------------------- | :--------: | :-----------: |
| RetroArch (cores libretro) | `libretro.<core>`                      |      ✔     |       ✔       |
| Amiberry                   | `amiberry`                             |            |               |
| ArcadeDuck                 | `arcadeduck`                           |      ✔     |       ✔       |
| Azahar, Azahar Plus        | `azahar\states` / `azahar-plus\states` |            |       ✔       |
| BigPEmu                    | `bigpemu`                              |            |               |
| BizHawk                    | `bizhawk\sstates\<core>`               |            |               |
| BlastEm                    | `blastem`                              |      ✔     |               |
| DeSmuME                    | `DeSmuME\stateslots`                   |            |               |
| Dolphin                    | `dolphin`                              |            |               |
| DuckStation                | `duckstation`                          |      ✔     |       ✔       |
| Flycast                    | `flycast\sstates`                      |            |               |
| Gopher64                   | `gopher64\states`                      |            |               |
| Jgenesis                   | `jgenesis\states`                      |            |               |
| Keisho                     | `keisho\sstates`                       |            |       ✔       |
| Model3-Vulkan              | `model3-vulkan`                        |            |       ✔       |
| Mupen64 (RMG)              | `mupen64`                              |            |               |
| Odin                       | `odin\sstates`                         |            |       ✔       |
| OpenCDi                    | `opencdi`                              |            |       ✔       |
| openMSX                    | `openmsx`                              |            |               |
| PCSX2                      | `pcsx2`                                |      ✔     |       ✔       |
| PPSSPP                     | `ppsspp`                               |            |               |

{% hint style="info" %}
Azahar, Keisho, Odin et OpenCDi n'enregistrent pas de capture d'écran avec leurs sauvegardes : le gestionnaire affiche l'icône de sauvegarde de RetroBat à la place. Odin ne garde qu'une sauvegarde par jeu (F2 / F4) : RetroBat en fait une nouvelle sauvegarde dans le gestionnaire à chaque fois
{% endhint %}

## Sauvegarder et charger en jeu

Utilisez les raccourcis standards de RetroBat :

| Action                | Manette        | Clavier |
| --------------------- | -------------- | ------- |
| Sauvegarde d'état     | HOTKEY + OUEST | F2      |
| Chargement d'état     | HOTKEY + NORD  | F4      |
| Emplacement précédent | HOTKEY + Bas   | F6      |
| Emplacement suivant   | HOTKEY + Haut  | F7      |

{% hint style="info" %}
Si vous avez personnalisé vos raccourcis, utilisez vos propres combinaisons. Voir la page Raccourcis.
{% endhint %}

## Lancer un jeu depuis une sauvegarde d'état

1. Dans la liste des jeux, placez-vous sur le jeu.
2. Appuyez sur **NORD** (ou **L3**) pour ouvrir le **GESTIONNAIRE DE SAUVEGARDES**. Vous pouvez aussi maintenir **SUD** pour ouvrir les **OPTIONS DU JEU**, puis choisir **SAUVEGARDES D'ÉTAT**.
3. Choisissez une sauvegarde, puis appuyez sur **SUD** (**LANCER**).

<div align="left"><figure><img src="../.gitbook/assets/image (438).png" alt=""><figcaption></figcaption></figure></div>

Le gestionnaire affiche :

<table><thead><tr><th width="249">Élément</th><th>Utilité</th></tr></thead><tbody><tr><td><strong>NOUVELLE PARTIE</strong></td><td>Lance le jeu depuis le début, sans charger de sauvegarde d'état.</td></tr><tr><td><strong>NOUVELLE SAUV. AUTO</strong></td><td>Affiché quand SAUV./CHARG. AUTO est activé et qu'il n'existe pas encore de sauvegarde automatique : lance le jeu et crée une sauvegarde automatique en quittant.</td></tr><tr><td><strong>SAUV. AUTO</strong></td><td>L'état enregistré automatiquement la dernière fois que vous avez quitté le jeu.</td></tr><tr><td>Sauvegardes</td><td>Vos sauvegardes d'état, avec leur date (et leur numéro d'emplacement quand les sauvegardes incrémentales sont désactivées).</td></tr></tbody></table>

Dans le gestionnaire :

* **SUD** : lancer le jeu depuis la sauvegarde sélectionnée.
* **OUEST** : supprimer la sauvegarde sélectionnée.
* **NORD** : copier la sauvegarde sélectionnée vers un emplacement libre.
* **EST** : revenir.

{% hint style="info" %}
- Une sauvegarde faite avec un autre émulateur affiche le nom de cet émulateur. En la lançant, RetroBat utilise automatiquement cet émulateur.
- Si vous avez activé **ACCÉDER AUX OPTIONS DU JEUX AVEC LE BOUTON NORD**, les boutons sont inversés : **NORD** ouvre les options du jeu, et maintenir **SUD** ouvre les sauvegardes d'état.
{% endhint %}

## Options

Les options se trouvent dans **MENU PRINCIPAL > PARAMÈTRES DES JEUX**, groupe **SAUVEGARDES**.

<div align="left"><figure><img src="../.gitbook/assets/image (439).png" alt=""><figcaption></figcaption></figure></div>

### SAUV./CHARG. AUTO

Quand cette option est activée :

* en quittant un jeu, son état est enregistré automatiquement (**SAUV. AUTO**) ;
* en le relançant, le jeu reprend exactement là où vous l'aviez laissé.

Pour recommencer depuis le début, ouvrez le gestionnaire de sauvegardes et choisissez **NOUVELLE PARTIE**.

Cette option peut aussi être réglée pour un seul système : **MENU PRINCIPAL > PARAMÈTRES DES JEUX > CONFIGURATION AVANCÉE PAR SYSTÈME > (système) > SAUV./CHARG. AUTO** (AUTO, OUI ou NON). Elle n'apparaît que si l'émulateur du système la prend en charge (colonne **Sauv. auto** du tableau des émulateurs compatibles).

### SAUVEGARDES D'ÉTAT INCRÉMENTALES

Indique quand une sauvegarde d'état peut en remplacer une plus ancienne (émulateurs cochés dans la colonne **Incrémentales** du tableau des émulateurs compatibles ; les autres utilisent toujours l'emplacement en cours) :

<table><thead><tr><th width="321.5">Choix</th><th>Comportement</th></tr></thead><tbody><tr><td><strong>À CHAQUE SAUVEGARDE</strong> (par défaut)</td><td>Chaque sauvegarde crée une nouvelle sauvegarde d'état : les anciennes ne sont jamais écrasées.</td></tr><tr><td><strong>NOUVEL EMPLACEMENT</strong></td><td>Pendant une partie, sauvegarder écrase l'emplacement en cours, mais chaque nouvelle partie démarre sur un emplacement libre.</td></tr><tr><td><strong>EMPLACEMENT ACTUEL</strong></td><td>Le jeu utilise l'emplacement en cours : une nouvelle sauvegarde peut écraser une ancienne, comme dans l'émulateur seul.</td></tr></tbody></table>

### AFFICHER LE GESTIONNAIRE DE SAUVEGARDES

Ouvre le gestionnaire de sauvegardes quand vous lancez un jeu avec **SUD** :

* **NON** (par défaut) : le jeu démarre directement.
* **TOUJOURS** : le gestionnaire s'ouvre pour chaque jeu qui gère les sauvegardes d'état.
* **SI NON VIDE** : le gestionnaire ne s'ouvre que si le jeu a déjà des sauvegardes d'état.

### Icône des sauvegardes d'état

Pour masquer l'icône des jeux qui ont des sauvegardes d'état, désactivez **AFFICHER LE DRAPEAU SAUV. INSTANTANÉE DANS LES LISTES** dans **MENU PRINCIPAL > PARAMÈTRES D'AFFICHAGE**, groupe **ICÔNES**.

## Bon à savoir

* **RetroAchievements :** en mode hardcore, le chargement des sauvegardes d'état est désactivé.
* **Mises à jour des émulateurs :** après une mise à jour, une ancienne sauvegarde d'état peut ne plus se charger. Gardez une sauvegarde normale du jeu.
* **Émulateurs non gérés par RetroBat :** d'autres émulateurs ont parfois leurs propres sauvegardes d'état, depuis leur menu. Elles n'apparaissent pas dans le gestionnaire de sauvegardes.
