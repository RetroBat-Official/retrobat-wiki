---
description: Avant de démarrer...
---

# Prérequis

Avant d'installer RetroBat, assurez-vous que votre PC remplit les conditions ci-dessous. Sans cela, RetroBat risque de ne pas fonctionner correctement.

<table><thead><tr><th width="161.5"></th><th></th></tr></thead><tbody><tr><td><strong>Système d'exploitation :</strong></td><td>Windows 10 ou Windows 11 (64 bits).<br>Windows 8.1 (64 bits) peut fonctionner, mais plusieurs émulateurs récents ne le supportent plus.</td></tr><tr><td><strong>Processeur :</strong></td><td>Processeur 64 bits avec support SSE2 (minimum).<br>Nous recommandons un processeur double cœur à 3 GHz, datant de 2008 ou plus récent. Certains émulateurs récents exigent des jeux d'instructions plus récents (ex. : SSE4.1).</td></tr><tr><td><strong>Carte graphique :</strong></td><td>Carte graphique supportant Direct3D 11.1, OpenGL 4.4 ou Vulkan.<br>Installez les derniers pilotes depuis le site du fabricant (NVIDIA, AMD ou Intel), et pas seulement ceux fournis par Windows Update.</td></tr><tr><td><strong>Dépendances :</strong></td><td>Les Visual C++ Redistributables et DirectX sont installés automatiquement par l'installeur de RetroBat.<br>Si un émulateur ne démarre pas, vous pouvez les réinstaller manuellement :</td></tr><tr><td></td><td><a href="https://www.techpowerup.com/download/visual-c-redistributable-runtime-package-all-in-one/">Visual C++ Redistributable Runtimes All-in-One</a> : installe en une fois toutes les versions nécessaires (2010, 2015-2022, 32 et 64 bits).</td></tr><tr><td></td><td><a href="https://www.microsoft.com/download/details.aspx?id=35">DirectX End-User Runtime</a> : nécessaire même sous Windows 10/11, qui n'incluent pas les anciens composants DirectX 9 utilisés par certains émulateurs.</td></tr><tr><td><strong>Manettes :</strong></td><td>Les manettes XInput (compatibles Xbox) sont recommandées pour une compatibilité optimale.<br>La plupart des autres manettes (PlayStation, Switch Pro…) fonctionnent aussi, mais peuvent demander une configuration supplémentaire dans certains émulateurs.<br>Vous pouvez tester votre manette sur <a href="https://gamepad-tester.com/">gamepad-tester.com</a>.</td></tr></tbody></table>

{% hint style="warning" %}
**Où installer RetroBat**

Installez RetroBat dans un chemin court, sans espaces ni caractères spéciaux, par exemple `C:\RetroBat` ou `D:\RetroBat`.

À éviter :

* `C:\Program Files` ou `C:\Program Files (x86)` (Windows y limite l'écriture, les réglages et sauvegardes risquent de ne pas être enregistrés)
* Les dossiers synchronisés avec OneDrive (Bureau, Documents, Images sont souvent synchronisés par défaut)
{% endhint %}
