# Succès Rétro

RetroAchievements ajoute des succès (trophées) aux jeux rétro, comme sur les consoles modernes. Pour l'utiliser, créez un compte gratuit sur le site [RetroAchievements](https://retroachievements.org).

## Émulateurs compatibles

* **RetroArch :** la plupart des cores libretro.
* **Émulateurs autonomes :** BizHawk, Dolphin, DuckStation, Flycast, Gopher64, PCSX2, PPSSPP et Snes9x.

Vous ne vous connectez qu'une fois, dans RetroBat : RetroBat transmet automatiquement votre compte à tous ces émulateurs.

## Activer RetroAchievements

1. Ouvrez le [**MENU PRINCIPAL**](../navigation/main-menu.md) > **PARAMÈTRES DES JEUX** > **PARAMÈTRES RETROACHIEVEMENTS**.
2. Activez **RETROACHIEVEMENTS**.
3. Saisissez votre **NOM D'UTILISATEUR** et votre **MOT DE PASSE** du site RetroAchievements.

<div align="left"><figure><img src="../.gitbook/assets/image (441).png" alt=""><figcaption></figcaption></figure></div>

4. Revenez en arrière : RetroBat se connecte à votre compte, puis indexe vos jeux. Un message s'affiche quand c'est terminé.

{% hint style="info" %}
Si le message **IMPOSSIBLE D'ACTIVER RETROACHIEVEMENTS** s'affiche, vérifiez votre nom d'utilisateur et votre mot de passe, ainsi que votre connexion Internet.
{% endhint %}

## Options

| Option                                                    | Effet                                                                                                                                                                                   |
| --------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **MODE DIFFICILE**                                        | Désactive les sauvegardes d'état, le retour arrière et la triche. Les succès débloqués dans ce mode rapportent plus de points.                                                          |
| **CLASSEMENTS**                                           | Participe aux classements de scores et de temps des jeux. Nécessite le mode difficile.                                                                                                  |
| **MODE VERBEUX**                                          | Affiche votre progression dans le jeu au lancement, et plus de notifications.                                                                                                           |
| **RICH PRESENCE**                                         | Affiche sur votre profil RetroAchievements ce que vous faites dans le jeu.                                                                                                              |
| **MODE ENCORE**                                           | Les succès déjà débloqués peuvent être débloqués à nouveau.                                                                                                                             |
| **CAPTURE D'ÉCRAN AUTOMATIQUE**                           | Prend une capture d'écran quand vous débloquez un succès.                                                                                                                               |
| **INDICATEURS DE CHALLENGE**                              | Affiche des icônes en bas à droite de l'écran quand un succès peut être débloqué.                                                                                                       |
| **SUCCÈS NON OFFICIELS**                                  | Active aussi les succès qui ne sont pas encore officiels.                                                                                                                               |
| **SON DE DÉBLOCAGE**                                      | Son joué quand vous débloquez un succès (RetroArch uniquement). Les sons sont les fichiers `.ogg` du dossier `sounds\retroachievements` de RetroBat : vous pouvez y ajouter les vôtres. |
| **AFFICHER LES RETROACHIEVEMENTS DANS LE MENU PRINCIPAL** | Affiche l'entrée RETROACHIEVEMENTS dans le menu principal (activé par défaut).                                                                                                          |

{% hint style="warning" %}
En **MODE DIFFICILE**, impossible de charger une sauvegarde d'état. Utilisez le système de sauvegarde du jeu.
{% endhint %}

## Index des jeux

L'indexation vérifie lesquels de vos jeux ont des succès. Ces jeux affichent alors une icône de **trophée** dans la liste des jeux.

* **INDEXER LES NOUVEAUX JEUX AU DÉMARRAGE** (activé par défaut) : les nouveaux jeux sont vérifiés à chaque démarrage de RetroBat.
* **INDEXER LES JEUX** : vérifie vos jeux maintenant (utile après l'ajout de nombreux jeux).

<div align="left"><figure><img src="../.gitbook/assets/image (442).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Pour masquer l'icône de trophée, désactivez **AFFICHER L'ICÔNE RETROACHIEVEMENTS** dans **MENU PRINCIPAL > PARAMÈTRES D'AFFICHAGE**, groupe **ICÔNES**.
{% endhint %}

## Succès d'un jeu

1. Dans la liste des jeux, placez-vous sur le jeu et maintenez **SUD** pour ouvrir les **OPTIONS DU JEU**.

<div align="left"><figure><img src="../.gitbook/assets/image (443).png" alt=""><figcaption></figcaption></figure></div>

2. Choisissez **VOIR LES SUCCÈS DU JEU**.

<div align="left"><figure><img src="../.gitbook/assets/image (444).png" alt=""><figcaption></figcaption></figure></div>

## Votre profil

Ouvrez le [**MENU PRINCIPAL**](../navigation/main-menu.md) > **RETROACHIEVEMENTS** pour voir vos points, votre rang et la progression de vos derniers jeux. Vous pouvez lancer un jeu directement depuis cette liste.

<div align="left"><figure><img src="../.gitbook/assets/image (445).png" alt=""><figcaption></figcaption></figure></div>

## Problèmes fréquents

<table><thead><tr><th width="275.25">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Aucun succès dans un jeu</td><td>Vérifiez que le jeu affiche l'icône de trophée et que l'émulateur choisi est compatible. Seules les versions de jeux connues par RetroAchievements fonctionnent : les jeux traduits, patchés ou modifiés ne sont en général pas reconnus.</td></tr><tr><td>L'icône de trophée n'apparaît pas</td><td>Lancez <strong>INDEXER LES JEUX</strong>, puis vérifiez la version du jeu sur le site RetroAchievements.</td></tr><tr><td>Les sauvegardes d'état ne se chargent pas</td><td>Le mode difficile est activé. Désactivez-le, ou utilisez le système de sauvegarde du jeu.</td></tr><tr><td>IMPOSSIBLE D'ACTIVER RETROACHIEVEMENTS</td><td>Nom d'utilisateur ou mot de passe incorrect, ou pas de connexion Internet.</td></tr></tbody></table>
