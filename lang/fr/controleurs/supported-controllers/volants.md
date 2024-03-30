---
description: Vroum vroum
---

# 🛞 Volants

La compatibilité des volants est une fonctionnalité très récente dans RetroBat, pour de nombreux émulateurs ou de nombreux modèles, une configuration spécifique est requise pour que le volant soit pleinement fonctionnel.

De nombreux volants sont disponibles sur le marché. [Seuls quelques uns](volants.md#volants-compatible-avec-retrobat) ont été testés et configurés pour fonctionner automatiquement.

## Détection des jeux de course se jouant au volant

<div align="left">

<figure><img src="https://i.imgur.com/LaVtSwP.png" alt=""><figcaption><p>Daytona USA est compatible</p></figcaption></figure>

</div>

La liste des jeux se jouant avec un volant est stockée dans un fichier .xml dans le dossier RetroBat, si vous pensez que certains jeux de cette liste ne devraient pas y figurer, vous pouvez les retirer et gérer votre propre liste.

{% hint style="warning" %}
L'édition de ce fichier est de votre responsabilité.&#x20;

Veillez a en faire une sauvegarde, car il sera écrasé lors des mises à jour de RetroBat.
{% endhint %}

<div align="left">

<figure><img src="https://i.imgur.com/2wr4B4z.png" alt=""><figcaption></figcaption></figure>

</div>

## Configuration des volants

### Activation du volant

Le volant peut être activé pour un système ou pour un jeu.

Pour activer le volant pour un système, depuis la **Vue Jeux**, ouvrez les [Options d'Affichage](../../navigation/view-options.md) et sélectionnez **CONFIGURATION AVANCÉE DU SYSTÈME**.

<div align="left">

<figure><img src="https://i.imgur.com/ZY07CeL.png" alt=""><figcaption></figcaption></figure>

</div>

Naviguez jusqu'à l'option **WHEELS**

<div align="left">

<figure><img src="https://i.imgur.com/njj5Mgg.png" alt=""><figcaption></figcaption></figure>

</div>

Basculez **ENABLE WHEELS** sur **ACTIVÉ**&#x20;

<div align="left">

<figure><img src="https://i.imgur.com/Si72acl.png" alt=""><figcaption></figcaption></figure>

</div>

La même option peut être activé par jeu depuis le menu [Option du Jeu](../../navigation/game-options.md) puis **CONFIGURATION AVANCÉE DU JEU**.\


## Volants compatibles avec RetroBat

{% hint style="info" %}
RetroBat ne permet pas de jouer au volant sans pédalier, il est nécessaire d'avoir les deux périphériques connectés lorsque vous activez l'option "wheels".

Le levier de vitesse est optionnel.
{% endhint %}

### Logitech G29

<div align="left">

<figure><img src="https://i.imgur.com/KAmr0lK.png" alt="" width="375"><figcaption></figcaption></figure>

</div>

### Logitech G920

<div align="left">

<figure><img src="https://i.imgur.com/tEJuFXl.png" alt="" width="375"><figcaption></figcaption></figure>

</div>

### Logitech G923

<div align="left">

<figure><img src="https://i.imgur.com/TMaOjRK.png" alt="" width="375"><figcaption></figcaption></figure>

</div>

### Thrustmaster T300RS

<div align="left">

<figure><img src="https://i.imgur.com/Aos7B0z.jpeg" alt="" width="375"><figcaption></figcaption></figure>

</div>

{% hint style="info" %}
Il est très important pour ce volant que le pédalier soit défini comme étant "séparé" dans le panneau de contrôle Thrustmaster.

Assurez-vous également que les pédales ne soient pas inversées (il est possible de régler cela en maintenant les boutons MODE + L3 + R3).
{% endhint %}

## Compatibilité des émulateurs

Les émulateurs suivant ont été configurés pour être compatible avec l'auto-configuration des contrôles au volant :

<table><thead><tr><th width="160">Emulateur</th><th width="229">Retour de Force</th><th>Commentaire</th></tr></thead><tbody><tr><td>Model 2</td><td>OUI</td><td>RetroBat permet une configuration spécifiques par jeu</td></tr><tr><td>Supermodel</td><td>OUI</td><td></td></tr><tr><td>Flycast</td><td>NON (outil externe requis)</td><td>RetroBat propose différentes combinaisons de boutons pour l'embrayage et le frein</td></tr><tr><td>PCSX2</td><td>OUI mais il est nécessaire d'ouvrir le menu et de configurer le retour de force à chaque utilisation</td><td>Il peut être nécessaire de modifier le type de volant depuis les options avancées</td></tr></tbody></table>

