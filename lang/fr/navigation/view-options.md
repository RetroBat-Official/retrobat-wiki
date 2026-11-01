---
description: Configurer la Vue Jeux et appliquer des réglages propres à un système
---

# Options d'Affichage

Le menu **OPTIONS D'AFFICHAGE** s'ouvre en appuyant sur **SELECT** dans la [Vue Jeux](system-view-and-game-view.md#vue-jeux).

<div align="left"><figure><img src="../.gitbook/assets/image (283).png" alt=""><figcaption></figcaption></figure></div>

Ses réglages s'appliquent uniquement au **système** (ou à la collection) que vous parcourez.

## Navigation

<table><thead><tr><th width="207.75">Paramètre</th><th>Description</th></tr></thead><tbody><tr><td><strong>FILTRER LES JEUX PAR TEXTE</strong></td><td>N'afficher que les jeux dont le nom contient le texte saisi</td></tr><tr><td><strong>AUTRES FILTRES</strong></td><td>Filtrer la liste par favoris, genre, nombre de joueurs, jeux déjà joués, région, langue, jeux avec des succès, médias manquants, jeux pour enfants, jeux au pistolet…</td></tr><tr><td><strong>SÉLECTIONNER UN JEU AU HASARD</strong></td><td>Aller à un jeu au hasard dans la liste</td></tr><tr><td><strong>ALLER À LA LETTRE</strong></td><td>Aller directement aux jeux commençant par une lettre</td></tr><tr><td><strong>TRIER PAR</strong></td><td>Trier la liste par nom, note, nombre de parties, dernière partie, nombre de joueurs, date de sortie, genre, développeur, éditeur, temps de jeu… (croissant ou décroissant)</td></tr></tbody></table>

{% hint style="info" %}
Les filtres restent actifs tant que vous ne les réinitialisez pas. Si des jeux semblent manquer dans un système, vérifiez qu'aucun filtre n'est actif.
{% endhint %}

### Dans une collection

Quand vous parcourez une collection, un groupe supplémentaire s'affiche :

* Dans une **collection dynamique** : **ÉDITER LES FILTRES DE LA COLLECTION** permet de modifier ses critères.
* Dans une **collection éditable** : **SUPPRIMER LA COLLECTION**.
* Dans les autres systèmes : **NOUVELLE COLLECTION DYNAMIQUE** crée une collection à partir des filtres appliqués.

Voir [Collections](game-collections.md).

## Options d'affichage

<table><thead><tr><th width="215.25">Paramètre</th><th>Description</th></tr></thead><tbody><tr><td><strong>TYPE DE VUE</strong></td><td>Affichage de la liste de jeux pour ce système (liste, détaillée, grille…). <strong>AUTOMATIQUE</strong> utilise le type défini dans la configuration du thème. Affiché uniquement si le thème propose plusieurs types de vue.</td></tr><tr><td><strong>PERSONNALISER LA VUE</strong></td><td>Personnaliser l'affichage de ce système, voir ci-dessous</td></tr></tbody></table>

### Personnaliser la vue

<table><thead><tr><th width="175.25">Section</th><th>Paramètres</th></tr></thead><tbody><tr><td>Style des listes de jeux</td><td>Type de vue, taille de la grille par défaut</td></tr><tr><td>Options du thème</td><td>Options proposées par le thème pour les listes de jeux (disposition, couleurs…)</td></tr><tr><td>Options des listes de jeux</td><td>Favoris en haut, fichiers cachés, dossiers, dossier parent <code>..</code>, icônes (drapeau de région, sauvegarde, manuel, RetroAchievements, pistolet, volant…), noms des roms au lieu des noms de jeux, <strong>EXTENSIONS DE FICHIERS</strong> (masquer certains types de fichiers pour ce système)</td></tr><tr><td>Outils</td><td><strong>RÉINITIALISER LES PERSONNALISATIONS</strong> : revenir aux réglages généraux</td></tr></tbody></table>

{% hint style="info" %}
Ces réglages remplacent, pour ce système uniquement, ceux définis dans **MENU PRINCIPAL** > **PARAMÈTRES D'AFFICHAGE**.
{% endhint %}

## Options

<table><thead><tr><th width="210.25">Paramètre</th><th>Description</th></tr></thead><tbody><tr><td><strong>VOIR LE PROFIL MANETTE À CLAVIER</strong></td><td>Afficher la correspondance manette / clavier utilisée pour ce système ou ce jeu (affiché uniquement s'il existe un profil <a href="../controleurs/pad2key.md">PadToKey</a>)</td></tr><tr><td><strong>CONFIGURATION AVANCÉE DU SYSTÈME</strong></td><td>Choix de l'émulateur et réglages d'émulation pour ce système, voir ci-dessous</td></tr></tbody></table>

### Configuration avancée du système

<div align="left"><figure><img src="../.gitbook/assets/image (284).png" alt=""><figcaption></figcaption></figure></div>

1. **ÉMULATEUR** : choisir l'émulateur et le core utilisés pour ce système. **AUTO** utilise l'émulateur par défaut choisi par RetroBat. Voir [Démarrer un jeu](../premiers-pas/running-a-game.md).
2. **Réglages généraux** : les réglages communs à la plupart des émulateurs (filtres vidéo, décorations, format d'affichage, mode vidéo, autoconfiguration des manettes…).
3. **Réglages de l'émulateur** : les réglages propres à l'émulateur ou au core choisi, que RetroBat écrit dans la configuration de l'émulateur au lancement du jeu.

{% hint style="info" %}
* Les réglages disponibles dépendent de l'émulateur choisi : changez d'abord l'émulateur, le menu affiche alors les réglages correspondants.
* **AUTO** signifie que le réglage défini dans **MENU PRINCIPAL** > **PARAMÈTRES DES JEUX** est utilisé.
* Pour modifier un réglage pour un seul jeu, utilisez les [Options du jeu](game-options.md) > **CONFIGURATION AVANCÉE DU JEU** : les réglages du jeu priment sur ceux du système, qui priment sur les réglages généraux.
{% endhint %}

{% hint style="warning" %}
Le groupe **OPTIONS D'AFFICHAGE** n'est affiché qu'en mode d'interface **Complet**. **CONFIGURATION AVANCÉE DU SYSTÈME** n'est affiché que pour les systèmes qui ont des réglages ou plusieurs émulateurs.
{% endhint %}
