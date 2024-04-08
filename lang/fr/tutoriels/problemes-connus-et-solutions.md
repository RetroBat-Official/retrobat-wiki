# Problèmes connus et solutions

Cette section est mise à jour fréquemment, elle contient des solutions / fix temporaires pour les problèmes particuliers en attendant une mise à jour de version RetroBat.

{% hint style="danger" %}
Attention, les solutions ci-dessous ne sont compatibles uniquement avec la dernière version de RetroBat.
{% endhint %}

## Fichier es\_input "propre"

Si vous rencontrez des problèmes de configuration de vos manettes ou que ces dernières fonctionnent bizaremment, vous pouvez copier le fichier ci-dessous dans le dossier `retrobat\emulationstation\.emulationstation` afin de réinitialiser la configuration de vos manettes.

Il faudra à nouveau configurer vos manettes une à une mais cela peut corriger certains problèmes.

{% file src="../.gitbook/assets/es_input.cfg" %}

## PSP: écran noir au démarrage des jeux avec lr-ppsspp

Le core libretro ppsspp n'est pas compatible avec la fonctionnalité de rembobinage, désactiver la fonction pour que les jeux fonctionnent correctement.

<div align="left">

<figure><img src="https://i.imgur.com/1r60ZlG.png" alt=""><figcaption></figcaption></figure>

</div>

## Autres problèmes connus

Pour résoudre tous les problèmes ci-dessou, téléchargez le fichier emulationstation.zip disponible en fin de page et le dézippez-le dans le dossier emulationstation\ de votre dossier RetroBat.

* Erreur de "path" en quittant OpenBOR
* Mauvais index des contrôleurs dans MAME64
* Features Chihiro manquantes
* Contrôle XBOX inactif dans Ryujinx ou Cemu
* Options Future Pinball ne fonctionnent pas
* Ares - contrôles et shaders ne fonctionnent pas avec la version 137
* Citra - controllers not working with autoconfiguration

{% file src="../.gitbook/assets/EmulationStation (2).zip" %}
