# IA de Traduction

## Paramétrage du service IA de traduction

La fonctionnalité de traduction permet de traduire les écrans de jeux depuis une langue étangère vers une langue comprise par l'utilisateur. (par exemple: du Japonais vers le Français).

La configuration du service est disponible dans la section [**PARAMETRES DES JEUX** du MENU PRINCIPAL](../navigation/main-menu.md#parametres-des-jeux), sous le nom **IA DE TRADUCTION**.

<div align="left">

<figure><img src="https://i.imgur.com/knusTqh.png" alt=""><figcaption></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://i.imgur.com/AKf6Q8j.png" alt=""><figcaption></figcaption></figure>

</div>

<table><thead><tr><th width="290">Paramètre</th><th>Description</th></tr></thead><tbody><tr><td><strong>Activer le service IA</strong></td><td>Activer / désactiver le service</td></tr><tr><td><strong>Langue cible</strong></td><td>Choisir la langue de destination de la traduction</td></tr><tr><td><strong>URL du service IA</strong></td><td>Entrer l'URL et la clé API du service (voir plus bas)</td></tr><tr><td><strong>Pause sur l'écran de traduction</strong></td><td>Activer le fait de mettre le jeu en pause lors de l'affichage de la traduction</td></tr></tbody></table>

### URL du service de traduction

Le service de traduction est fourni par [ztranslate.net](https://ztranslate.net/).

Il est nécessaire de créer un compte sur le site.

<div align="left">

<figure><img src="https://i.imgur.com/rLddOm8.png" alt=""><figcaption><p>Register</p></figcaption></figure>

</div>

Une fois enregistré, aller dans **Settings** pour récupérer la clé API du compte.

<div align="left">

<figure><img src="https://i.imgur.com/7Oe139R.png" alt=""><figcaption><p>Retrieve API key at the bottom</p></figcaption></figure>

</div>

Dans Retrobat, renseigner ensuite le lien URL ainsi que la clé API dans le menu **IA DE TRADUCTION** se trouvant dans les [PARAMÈTRES DES JEUX du MENU PRINCIPAL](../navigation/main-menu.md#parametres-des-jeux).

Utiliser le format suivant:

```
http://ztranslate.net/service?api_key=XXXYYYZZZ
```

(Remplacer XXXYYYZZZ avec la clé API du compte)

<div align="left">

<figure><img src="https://i.imgur.com/OiGEpQD.png" alt=""><figcaption></figcaption></figure>

</div>

Confirmer.

## Afficher la traduction dans le jeu

Il est possible de faire appel au service de traduction en jeu en pressant simultanément les touches `HOTKEY` + `R1` du contrôleur.
