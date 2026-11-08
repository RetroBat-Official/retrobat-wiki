# IA de Traduction

Le service de traduction par IA traduit le texte d'un jeu en direct. Quand vous appuyez sur le raccourci, RetroArch prend une capture du jeu, l'envoie à un service en ligne qui lit et traduit le texte, puis affiche la traduction par-dessus le jeu.

{% hint style="info" %}
* Le service ne fonctionne qu'avec les **cores RetroArch**.
* Une **connexion Internet** est nécessaire.
* La traduction est automatique : elle peut être approximative, et certains textes (polices stylisées, petits textes) peuvent être mal lus.
{% endhint %}

## Activer la traduction

1. Ouvrez le [**MENU PRINCIPAL**](../navigation/main-menu.md) > **PARAMÈTRES DES JEUX**, groupe **OPTIONS RETROARCH** > **TRADUCTION ASSISTÉE PAR IA**.
2. Activez **ACTIVER LE SERVICE DE TRADUCTION PAR IA**.
3. Choisissez votre **LANGUE CIBLE** : la langue dans laquelle le texte est traduit. La langue du jeu est détectée automatiquement.

<div align="left"><figure><img src="../.gitbook/assets/image (449).png" alt=""><figcaption></figcaption></figure></div>

<table><thead><tr><th width="289">Option</th><th>Effet</th></tr></thead><tbody><tr><td><strong>ACTIVER LE SERVICE DE TRADUCTION PAR IA</strong></td><td>Active la traduction dans les jeux RetroArch.</td></tr><tr><td><strong>LANGUE CIBLE</strong></td><td>Langue de la traduction.</td></tr><tr><td><strong>URL DU SERVICE DE TRADUCTION IA</strong></td><td>Adresse du service de traduction. Laissez-la vide pour utiliser le service par défaut (voir plus bas).</td></tr><tr><td><strong>PAUSE SUR L'ÉCRAN TRADUIT</strong></td><td>Met le jeu en pause pendant l'affichage de la traduction.</td></tr></tbody></table>

## Traduire en jeu

| Action                                                        | Manette               |
| ------------------------------------------------------------- | --------------------- |
| Traduire l'écran                                              | HOTKEY + R1           |
| Masquer la traduction (et reprendre le jeu s'il est en pause) | HOTKEY + R1 à nouveau |

<div align="left"><figure><img src="../.gitbook/assets/image (450).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Si vous avez personnalisé vos raccourcis, utilisez votre propre combinaison. Voir la page Raccourcis.
{% endhint %}

## Service de traduction

Par défaut, RetroBat utilise le service **ZTranslate** avec une clé partagée : il fonctionne sans aucun compte. Cette clé étant partagée par de nombreux joueurs, le service peut parfois être lent ou indisponible.

Pour utiliser votre propre clé :

1. Créez un compte gratuit sur [ztranslate.net](https://ztranslate.net), puis récupérez votre clé API dans votre profil.

<div align="left"><figure><img src="../.gitbook/assets/image (451).png" alt=""><figcaption></figcaption></figure></div>

2. Dans **URL DU SERVICE DE TRADUCTION IA**, saisissez : `http://ztranslate.net/service?api_key=VOTRE_CLÉ` (remplacez `VOTRE_CLÉ` par votre clé).

<div align="left"><figure><img src="../.gitbook/assets/image (452).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="warning" %}
Écrivez l'adresse avec `http://`, et non `https://`. RetroBat ajoute lui-même à la fin de l'adresse les réglages de langue et d'affichage : ne les ajoutez pas.
{% endhint %}

## Problèmes fréquents

| Problème                                      | Solution                                                                                                       |
| --------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| Rien ne se passe en appuyant sur HOTKEY + R1  | Vérifiez que le service est activé et que le jeu utilise un core RetroArch. Vérifiez votre connexion Internet. |
| La traduction est longue ou n'apparaît jamais | Le service partagé est peut-être surchargé : réessayez plus tard, ou utilisez votre propre clé.                |
| La traduction est fausse ou incomplète        | Le texte n'a pas pu être bien lu (police stylisée, petit texte). Essayez sur un écran au texte plus lisible.   |
