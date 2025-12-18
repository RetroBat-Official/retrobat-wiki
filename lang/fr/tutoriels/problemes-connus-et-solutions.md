# Problèmes connus et solutionsChange opengl2.1

Cette section est mise à jour fréquemment, elle contient des solutions / fix temporaires pour les problèmes particuliers en attendant une mise à jour de version RetroBat.

{% hint style="danger" %}
Attention, les solutions ci-dessous ne sont compatibles uniquement avec la dernière version de RetroBat.
{% endhint %}

## Fichier es\_input "propre"

Si vous rencontrez des problèmes de configuration de vos manettes ou que ces dernières fonctionnent bizaremment, vous pouvez copier le fichier ci-dessous dans le dossier `retrobat\emulationstation\.emulationstation` afin de réinitialiser la configuration de vos manettes.

Il faudra à nouveau configurer vos manettes une à une mais cela peut corriger certains problèmes.

{% file src="../.gitbook/assets/es_input.cfg" %}

## Problèmes graphiques dans l'interface RetroBat

Si vous disposez d'une ancienne carte graphique non compatible avec les dernières version de OpenGL, il est possible que l'interface RetroBat soit corrompue ou que celle-ci ne démarre pas.

Pour résoudre ce problème, il est possible de forcer RetroBat à utiliser un affichage compatible avec la version OpenGL 2.1.

Ouvrir le fichier **retrobat.ini** situé à la racine de votre installation RetroBat et mettre la valeur suivante à 1:

<div align="left"><figure><img src="https://i.imgur.com/fqv5SM1.png" alt=""><figcaption></figcaption></figure></div>

Sauvegarder le fichier et démarrer RetroBat.

Ce paramétrage est également accessible dans **BatGUI**:

<div align="left"><figure><img src="https://i.imgur.com/5aJ94sX.png" alt=""><figcaption></figcaption></figure></div>
