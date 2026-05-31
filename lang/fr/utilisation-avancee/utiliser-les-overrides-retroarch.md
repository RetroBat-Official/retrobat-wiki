# Utiliser les overrides Retroarch

Si vous ne souhaitez pas utiliser la configuration globale de RetroBat pour les options générales de RetroArch ou si vous souhaitez régler vous-même les Shaders, cela est possible en activant les options de RetroBat permettant de charger automatiquement les fichiers "overrides" préalablement créés dans RetroArch.

### Override pour les options

RetroArch permet de sauvegarder un fichier d'override pour les options générales, cet override peut être sauvegardé pour un jeu, un coeur libretro ou pour un dossier de contenu.

Pour générer un fichier d'override, lancer le menu RetroArch depuis un jeu en appuyant sur SELECT + ![](<../.gitbook/assets/image (2) (1).png>) de votre manette (F1 sur le clavier). Effectuer les réglages souhaités puis aller dans le menu de "Configuration de Substitution":

<div align="left"><figure><img src="https://i.imgur.com/Ao7zf9g.png" alt=""><figcaption></figcaption></figure></div>

A partir de ce menu, sauvegarder le fichier d'override pour le niveau souhaité (jeu, coeur, contenu):

<div align="left"><figure><img src="https://i.imgur.com/YkWoLnW.png" alt=""><figcaption></figcaption></figure></div>

RetroArch va automatiquement sauvegardé un fichier d'override dans le sous-dossier du coeur:

<div align="left"><figure><img src="https://i.imgur.com/k72RIIK.png" alt=""><figcaption></figcaption></figure></div>

Maintenant, activer l'option d'override dans RetroBat dans le [**menu principal de RetroBat > Paramètres des jeux > Options RetroArch > Emulation**](../navigation/main-menu.md#parametres-des-jeux):

<div align="left"><figure><img src="https://i.imgur.com/dr5V9ME.png" alt=""><figcaption></figcaption></figure></div>



### Override pour les shaders

RetroArch permet de sauvegarder un fichier d'override pour les shaders, cet override peut être sauvegardé pour un jeu, un coeur libretro, un dossier de contenu ou globalement.

Pour générer un fichier d'override de shaders, lancer le menu RetroArch depuis un jeu en appuyant sur SELECT + ![](<../.gitbook/assets/image (2) (1).png>) de votre manette (F1 sur le clavier). Puis aller dans le menu **Shaders** pour effectuer les réglages souhaités:

<div align="left"><figure><img src="https://i.imgur.com/zxiggYZ.png" alt=""><figcaption></figcaption></figure></div>

Une fois les réglages terminés, aller dans le menu "**Enregistrer le préréglage**":

<div align="left"><figure><img src="https://i.imgur.com/UZjvbHf.png" alt=""><figcaption></figcaption></figure></div>

Sauvegarder au niveau souhaité (dossier, coeur, jeu, global):

<div align="left"><figure><img src="https://i.imgur.com/C0NjIn7.png" alt=""><figcaption></figcaption></figure></div>

RetroArch va automatiquement sauvegardé un fichier d'override :

<div align="left"><figure><img src="https://i.imgur.com/Y0KTSXc.png" alt=""><figcaption></figcaption></figure></div>

Maintenant, activer l'option d'override de shaders dans RetroBat dans le [**menu principal de RetroBat > Paramètres des jeux > Options RetroArch > Rendu visuel**](../navigation/main-menu.md#parametres-des-jeux):

<div align="left"><figure><img src="https://i.imgur.com/sZ7eHGG.png" alt=""><figcaption></figcaption></figure></div>

### Override du format d'affichage personnalisé dans RetroArch <a href="#override-pour-les-options-2" id="override-pour-les-options-2"></a>

Lorsque vous souhaitez utiliser le format d'affichage "personnalisé" dans **CONFIGURATION AVANCÉE DU SYSTÈME > RAPPORT D'ASPECT**, il est possible d'appliquer la valeur du ration a appliquer dans RetroArch en créant un fichier .txt contenant les informations suivantes :&#x20;

* width (largeur)
* height (hauteur)
* top (haut)
* left (gauche)

Les informations contenues dans le fichier rempliront automatiquement les champs suivants dans RetroArch :

<div align="left"><figure><img src="../.gitbook/assets/image (111).png" alt=""><figcaption></figcaption></figure></div>

Pour ce faire, créez un fichier .txt soit dans le dossier `roms\<system>` du système auquel le rapport doit être appliqué, soit dans le dossier `user\customratio` de votre installation RetroBat :

<div align="left"><figure><img src="../.gitbook/assets/image (112).png" alt=""><figcaption><p>Example for NES</p></figcaption></figure></div>

Le fichier doit être nommé soit :

* `<system>_<romname>_customratio.txt` (pour qu'il s'applique à un jeu spécifique)
* `<system>_customratio.txt` (pour qu'il s'applique a l'ensemble du système)

Enfin, sélectionner la valeur "PERSONNALISÉ" dans le champs **RAPPORT D'ASPECT** de RetroBat :

<div align="left"><figure><img src="../.gitbook/assets/image (113).png" alt=""><figcaption></figcaption></figure></div>
