---
description: >-
  Portages PC natifs de jeux console : recompilations, décompilations et autres
  portages communautaires
---

# Recompilations

<div align="left"><figure><img src="../../../.gitbook/assets/image (202).png" alt="" width="375"><figcaption></figcaption></figure></div>

## Présentation

Cette page concerne les portages PC natifs de jeux console, comme les recompilations et les décompilations. Aucun émulateur n'intervient : RetroBat lance directement l'exécutable du portage et attend sa fermeture.

RetroBat ne fournit pas ces portages. Installez-les avec Quiver Launcher ou téléchargez-les depuis la page de leur projet, puis fournissez les données du jeu original selon ce que demande chaque portage.

## En bref

<table><thead><tr><th width="264"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\recomp</code></td></tr><tr><td><strong>Extensions</strong></td><td>.lnk .game .m3u .bat .decomp</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>quiverlauncher</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (données du jeu original à fournir selon le portage)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Non, à régler dans chaque portage</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr></tbody></table>

## Contrôles

* RetroBat ne configure pas automatiquement les manettes pour ces portages. Réglez les contrôles dans chaque portage.
* **HOTKEY + START** ferme le jeu et revient à RetroBat. Dans Quiver Launcher, il ferme le launcher.

## Quiver Launcher

{% embed url="https://github.com/tgeorgiadis/quiver-launcher" %}

Quiver Launcher télécharge, installe et met à jour les portages de la communauté depuis les releases GitHub et GitLab.

* **Ouverture :** sélectionnez Quiver Launcher dans le menu de RetroBat (téléchargé à la première utilisation), ou activez **DEMARRER LE LAUNCHER** dans les [options avancées d'un jeu](../../../navigation/game-options.md).

<div align="left"><figure><img src="../../../.gitbook/assets/image (203).png" alt=""><figcaption><p>Démarrer QuiverLauncher depuis le menu RetroBat...</p></figcaption></figure></div>

<div align="left"><figure><img src="../../../.gitbook/assets/image (204).png" alt=""><figcaption><p>... ou activer DEMARRER LE LAUNCHER depuis les options avancées du système ou du jeu.</p></figcaption></figure></div>

* **Ajout des jeux :**
  1. Installez les jeux dans Quiver Launcher et fournissez leurs données.
  2. Ajoutez-les à RetroBat automatiquement en activant **MENU PRINCIPAL > PARAMÈTRES DES JEUX > SCAN RECOMPILATION (QUIVERLAUNCHER)**, ou manuellement en déplaçant un raccourci du bureau dans `roms\recomp`.
  3. Mettez à jour la liste des jeux ou redémarrez RetroBat.
* Si le dossier d'un jeu contient plusieurs exécutables, choisissez-en un d'abord dans Quiver Launcher, sinon le scan automatique l'ignore.
* **Au lancement d'un jeu :** il démarre directement, suit le réglage plein écran / fenêtré de RetroBat, et range sa configuration et ses sauvegardes dans `emulators\quiverlauncher\Apps\<jeu>`. Pour Perfect Dark, l'option **RÉGION** choisit l'exécutable Europe, USA ou Japon.

## Portages installés hors de Quiver Launcher

Un portage installé ailleurs sur votre ordinateur peut aussi être ajouté dans `roms\recomp` :

* **Raccourci (`.lnk`) :** un raccourci qui ne pointe pas vers un jeu Quiver est lancé tel quel, avec sa cible, ses arguments et son dossier de travail.
* **Fichier `.game` :** un fichier texte avec le chemin de l'exécutable sur la première ligne. Les lignes suivantes sont passées en arguments.
* **Fichier `.m3u` :** un fichier texte avec le chemin de l'exécutable sur sa première ligne.
* **Fichier `.bat` :** le fichier batch est exécuté directement.

Dans les fichiers `.game` et `.m3u`, un chemin commençant par `.\` est relatif au dossier du fichier.

Si le processus du jeu ne porte pas le même nom que l'exécutable, créez un fichier `.gameexe` portant le même nom, qui contient le nom du processus.

## Portages decomp (.decomp)

Un fichier `.decomp` placé dans le dossier d'une console fait apparaître le portage dans la liste des jeux de cette console. Il est toujours lancé comme un portage decomp, quel que soit l'émulateur choisi. Par exemple, un portage de Star Fox 64 peut se trouver dans `roms\n64`.

Systèmes qui acceptent les fichiers `.decomp` : MAME, CPS-III, Model 1, Model 2, Model 3, Naomi, Naomi 2, Saturn, Super Nintendo, Nintendo 64, GameCube, Wii, Wii U, Switch, Game Boy Advance, Nintendo DS, Nintendo 3DS, PlayStation, PlayStation 2, PlayStation 3, PlayStation 4, PSP, PS Vita, Xbox et Xbox 360, ainsi que `roms\recomp`.

{% hint style="warning" %}
RetroBat parcourt les sous-dossiers : les fichiers au format de la console (par exemple `.zip` ou `.wad`) présents dans le dossier d'un portage apparaissent aussi dans la liste des jeux.
{% endhint %}

* **Contenu du fichier :** il peut être vide ; RetroBat lance alors le premier `.exe` situé à côté. Pour choisir un exécutable précis, écrivez son nom sur la première ligne, sans `.exe`. Seul le dossier du fichier est parcouru, et un nom introuvable revient au premier exécutable.
* **Nom de processus différent :** créez un fichier `.gameexe` portant le même nom, qui contient le nom du processus. RetroBat l'attend environ 6 secondes, puis attend sa fermeture.

## Mise à jour depuis N64RecompLauncher

Quiver Launcher remplace N64RecompLauncher. Copiez `roms\n64recomp` vers `roms\recomp`, puis réinstallez vos jeux dans Quiver Launcher : ils ne sont pas transférés.

Pour garder vos sauvegardes, copiez-les de `emulators\n64recomplauncher\RecompiledGames\<jeu>` vers `emulators\quiverlauncher\Apps\<jeu>`.
