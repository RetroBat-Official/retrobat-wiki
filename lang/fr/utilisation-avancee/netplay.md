# Parties en Réseau

## Qu'est-ce que le jeu en réseau ?

Le jeu en réseau (netplay) permet de jouer à plusieurs à travers un réseau, comme si vos amis étaient à côté de vous sur la même console. Chaque joueur lance le jeu sur son propre PC, et les actions des joueurs sont envoyées par le réseau.

{% hint style="warning" %}
Le jeu en réseau n'émule pas les fonctions en ligne des consoles d'origine, et il n'y a aucun serveur dédié. Les jeux ou modes qui nécessitaient un service en ligne (Phantasy Star Online sur Dreamcast, par exemple) ne fonctionnent pas en netplay.
{% endhint %}

Le jeu en réseau fonctionne avec les **cores RetroArch** qui le prennent en charge.

## Activer le jeu en réseau

1. Ouvrez le [**MENU PRINCIPAL**](../navigation/main-menu.md) > **PARAMÈTRES DES JEUX** > **PARAMÈTRES DE JEU EN RÉSEAU**.
2. Activez **ACTIVER LE JEU EN RÉSEAU**.
3. Saisissez un **SURNOM** : c'est le nom que voient les autres joueurs.

<div align="left"><figure><img src="../.gitbook/assets/image (446).png" alt=""><figcaption></figcaption></figure></div>

4. Revenez en arrière : RetroBat indexe vos jeux (voir plus bas).

## Options

<table><thead><tr><th width="286.5">Option</th><th>Effet</th></tr></thead><tbody><tr><td><strong>PORT</strong></td><td>Port réseau utilisé quand vous hébergez une partie (55435 par défaut).</td></tr><tr><td><strong>UTILISER UN SERVEUR RELAIS</strong></td><td>Passe par un serveur relais au lieu d'une connexion directe. Utile quand les joueurs ne peuvent pas se connecter directement (ports fermés, certaines box Internet). Choisissez le serveur le plus proche, ou <strong>CUSTOM</strong> pour saisir votre propre serveur dans <strong>SERVEUR RELAI PERSONNALISÉ</strong>.</td></tr><tr><td><strong>CRÉER AUTOMATIQUEMENT UN LOBBY</strong></td><td>Quand cette option est activée (par défaut), chaque jeu compatible lancé normalement crée aussi une partie en réseau que d'autres joueurs peuvent rejoindre.</td></tr><tr><td><strong>AFFICHER UNIQUEMENT LES JEUX AVEC SERVEUR RELAIS</strong></td><td>Ne liste que les parties hébergées via un serveur relais, plus faciles à rejoindre (activé par défaut).</td></tr><tr><td><strong>AFFICHER LES JEUX NON DISPONIBLES</strong></td><td>Liste aussi les parties de jeux absents de votre PC (activé par défaut).</td></tr></tbody></table>

{% hint style="info" %}
Pour lancer vos jeux seul, sans créer de partie en réseau, désactivez **CRÉER AUTOMATIQUEMENT UN LOBBY**. Vous pouvez toujours héberger une partie depuis les options du jeu (voir plus bas).
{% endhint %}

## Index des jeux

L'indexation calcule une empreinte (CRC) de vos jeux, pour que RetroBat puisse vérifier que vous avez le même jeu que les autres joueurs.

* **INDEXER LES NOUVEAUX JEUX AU DÉMARRAGE** (activé par défaut) : les nouveaux jeux sont indexés à chaque démarrage de RetroBat.
* **INDEXER LES JEUX** : indexe vos jeux maintenant (utile après l'ajout de nombreux jeux).

## Héberger une partie

1. Dans la [liste des jeux](../navigation/system-view-and-game-view.md#vue-jeux), placez-vous sur le jeu et maintenez **SUD** pour ouvrir les **OPTIONS DU JEU**.
2. Choisissez **DÉMARRER UNE PARTIE EN RÉSEAU**.
3. Réglez les options si besoin :
   * **ANNONCER PUBLIQUEMENT LA PARTIE** : affiche votre partie dans la liste publique, pour tous les joueurs RetroArch et RetroBat. Laissez-la désactivée pour ne jouer qu'avec des amis qui connaissent votre partie.
   * **MOT DE PASSE JOUEUR** : mot de passe demandé aux joueurs qui rejoignent la partie.
   * **MOT DE PASSE SPECTATEUR** : mot de passe demandé aux spectateurs.
4. Choisissez **HÉBERGER UNE PARTIE EN RÉSEAU** : le jeu démarre et attend les autres joueurs.

<div align="left"><figure><img src="../.gitbook/assets/image (447).png" alt=""><figcaption></figcaption></figure></div>

## Rejoindre une partie

1. Dans la [vue des systèmes](../navigation/system-view-and-game-view.md#vue-systemes), appuyez sur **NORD** (**PARTIES EN RÉSEAU**) pour ouvrir la liste des parties.
2. La liste affiche les **JEUX EN RÉSEAU** (sur votre réseau local), les **JEUX DISPONIBLES** (jeux que vous avez) et les **JEUX NON DISPONIBLES** (jeux que vous n'avez pas).
3. Choisissez une partie, puis :
   * **REJOINDRE LE JEU** pour jouer ;
   * **REGARDER LE JEU** pour suivre la partie en spectateur.

<div align="left"><figure><img src="../.gitbook/assets/image (448).png" alt=""><figcaption></figcaption></figure></div>

Chaque partie affiche un statut :

<table><thead><tr><th width="279">Statut</th><th>Signification</th></tr></thead><tbody><tr><td><strong>ROM IDENTIQUE</strong></td><td>Vous avez exactement le même jeu que l'hôte : vous pouvez rejoindre la partie.</td></tr><tr><td><strong>ROM DIFFÉRENTE</strong></td><td>Vous avez le jeu, mais pas la même version : la partie ne fonctionnera pas correctement.</td></tr><tr><td><strong>VERSION DE ROM INCONNUE</strong></td><td>La version du jeu n'a pas pu être vérifiée.</td></tr><tr><td><strong>CŒUR NON DISPONIBLE</strong></td><td>Le core utilisé par l'hôte n'est pas disponible sur votre PC.</td></tr></tbody></table>

Appuyez sur **RAFRAÎCHIR** pour mettre la liste à jour.

## Bon à savoir

### Héberger

Pour héberger une partie, les autres joueurs doivent pouvoir se connecter à votre PC :

* votre box Internet doit prendre en charge l'**UPnP**, qui ouvre le port automatiquement ;
* sinon, ouvrez le port (55435 par défaut, ou votre **PORT**) dans les réglages de votre box ;
* ou utilisez un serveur relais (**UTILISER UN SERVEUR RELAIS**), qui évite d'ouvrir un port.

### Limites

* **Connexion :** une connexion stable avec un ping faible est indispensable. La qualité de la partie dépend du joueur le plus lent.
* **Même version :** tous les joueurs doivent avoir le **même jeu** (même ROM, vérifiez le statut ROM IDENTIQUE) et la **même version du core**, donc idéalement la même version de RetroBat.
* **Core compatible :** seuls les cores RetroArch qui gèrent le jeu en réseau peuvent être utilisés.
* **Même architecture :** certains cores n'autorisent pas le jeu en réseau entre architectures différentes. Un message s'affiche au démarrage du core.
