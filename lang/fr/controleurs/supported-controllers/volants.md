---
description: Vroum vroum
---

# 🛞 Volants

La compatibilité des volants est une fonctionnalité très récente dans RetroBat, pour de nombreux émulateurs ou de nombreux modèles, une configuration spécifique est requise pour que le volant soit pleinement fonctionnel.

De nombreux volants sont disponibles sur le marché. [Seuls quelques uns](volants.md#volants-compatible-avec-retrobat) ont été testés et configurés pour fonctionner automatiquement.

## Détection des jeux de course se jouant au volant

<div align="left"><figure><img src="https://i.imgur.com/LaVtSwP.png" alt=""><figcaption><p>Daytona USA est compatible</p></figcaption></figure></div>

La liste des jeux se jouant avec un volant est stockée dans un fichier .xml dans le dossier RetroBat, si vous pensez que certains jeux de cette liste ne devraient pas y figurer, vous pouvez les retirer et gérer votre propre liste.

{% hint style="warning" %}
L'édition de ce fichier est de votre responsabilité.&#x20;

Veillez a en faire une sauvegarde, car il sera écrasé lors des mises à jour de RetroBat.
{% endhint %}

<div align="left"><figure><img src="https://i.imgur.com/2wr4B4z.png" alt=""><figcaption></figcaption></figure></div>

## Configuration des volants

### Activation du volant

Le volant peut être activé pour un système ou pour un jeu.

Pour activer le volant pour un système, depuis la **Vue Jeux**, ouvrez les [Options d'Affichage](../../navigation/view-options.md) et sélectionnez **CONFIGURATION AVANCÉE DU SYSTÈME**.

<div align="left"><figure><img src="https://i.imgur.com/ZY07CeL.png" alt=""><figcaption></figcaption></figure></div>

Naviguez jusqu'à l'option **WHEELS**

<div align="left"><figure><img src="https://i.imgur.com/njj5Mgg.png" alt=""><figcaption></figcaption></figure></div>

Basculez **ENABLE WHEELS** sur **ACTIVÉ**&#x20;

<div align="left"><figure><img src="https://i.imgur.com/Si72acl.png" alt=""><figcaption></figcaption></figure></div>

La même option peut être activé par jeu depuis le menu [Option du Jeu](../../navigation/game-options.md) puis **CONFIGURATION AVANCÉE DU JEU**.<br>

## Volants compatibles avec RetroBat

{% hint style="info" %}
RetroBat ne permet pas de jouer au volant sans pédalier, il est nécessaire d'avoir les deux périphériques connectés lorsque vous activez l'option "wheels".

Le levier de vitesse est optionnel.
{% endhint %}

### Logitech G29

<div align="left"><figure><img src="https://i.imgur.com/KAmr0lK.png" alt="" width="375"><figcaption></figcaption></figure></div>

### Logitech G920

<div align="left"><figure><img src="https://i.imgur.com/tEJuFXl.png" alt="" width="375"><figcaption></figcaption></figure></div>

### Logitech G923

<div align="left"><figure><img src="https://i.imgur.com/TMaOjRK.png" alt="" width="375"><figcaption></figcaption></figure></div>

### Thrustmaster T300RS

<div align="left"><figure><img src="https://i.imgur.com/Aos7B0z.jpeg" alt="" width="375"><figcaption></figcaption></figure></div>

{% hint style="info" %}
Il est très important pour ce volant que le pédalier soit défini comme étant "séparé" dans le panneau de contrôle Thrustmaster.

Assurez-vous également que les pédales ne soient pas inversées (il est possible de régler cela en maintenant les boutons MODE + L3 + R3).
{% endhint %}

## Compatibilité des émulateurs

Les émulateurs suivant ont été configurés pour être compatible avec l'auto-configuration des contrôles au volant :

<table><thead><tr><th width="160">Emulateur</th><th width="229">Retour de Force</th><th>Commentaire</th></tr></thead><tbody><tr><td>Model 2</td><td>OUI</td><td>RetroBat permet une configuration spécifiques par jeu</td></tr><tr><td>Supermodel</td><td>OUI</td><td></td></tr><tr><td>Flycast</td><td>NON (outil externe requis)</td><td>RetroBat propose différentes combinaisons de boutons pour l'embrayage et le frein</td></tr><tr><td>PCSX2</td><td>OUI mais il est nécessaire d'ouvrir le menu et de configurer le retour de force à chaque utilisation</td><td>Il peut être nécessaire de modifier le type de volant depuis les options avancées</td></tr></tbody></table>

## Configurer un volant

Le mapping du volant pour un volant en particulier peut être réalisé depuis les fichiers de configuration situés dans le dossier`system\resources\inputmapping\wheels` de votre installation RetroBat installation:

<div align="left"><figure><img src="https://i.imgur.com/iBP5mGf.png" alt=""><figcaption></figcaption></figure></div>

Ci-dessous, un exemple pour Flycast :

<div align="left"><figure><img src="https://i.imgur.com/5Pq3Bn5.png" alt=""><figcaption></figcaption></figure></div>

Le format est important : chaque volant doit être renseigné dans son propre container, suivi du nom du bouton, lui-même précédé de 2 espaces.

Le volant LogitechG29 peut être utilisé comme exemple.

Pour adapter le fichier a votre volant, configurer votre matériel directement sous Flycast, sauvegarder, ouvrir le fichier de configuration crée dans le dossier `emulators\flycast\mappings` et reporter les valeurs sur le fichier.

{% hint style="info" %}
Si vous paramétrez un volant autre que ceux indiqués dans [la liste des volants compatibles](volants.md#volants-compatibles-avec-retrobat), merci de faire parvenir le fichier à l'équipe RetroBat, pour que celui-ci puissent être intégré lors des mises à jour prochaines.&#x20;
{% endhint %}

Le nom du container pour les volants pouvant potentiellement être pris en charge se trouve [ici](volants.md#volants-supportes).

### Volants supportés

<details>

<summary>Volants supportés et VID/PID correspondant</summary>

VID\_2433\&PID\_F300 : AsetekInvicta\
VID\_2433\&PID\_F301 : AsetekForte\
VID\_2433\&PID\_F303 : AsetekLaPrima\
VID\_2433\&PID\_F306 : AsetekTonyKannan\
VID\_3416\&PID\_0301 : CammusC5\
VID\_3416\&PID\_0302 : CammusC12\
VID\_0EB7\&PID\_0001 : FanatecClubSportWheelBaseV2\
VID\_0EB7\&PID\_0004 : FanatecClubSportWheelBaseV25\
VID\_0EB7\&PID\_0005 : FanatecCSLElitePS4\
VID\_0EB7\&PID\_0006 : FanatecPodiumDD1\
VID\_0EB7\&PID\_0007 : FanatecPodiumDD2\
VID\_0EB7\&PID\_0011 : FanatecCSRElite\
VID\_0EB7\&PID\_0020 : FanatecDD\
VID\_0EB7\&PID\_0E03 : FanatecCSLElite\
VID\_046D\&PID\_C202 : LogitechWingmanFormula\
VID\_046D\&PID\_C20E : LogitechWingmanFormulaGP\
VID\_046D\&PID\_C24F : LogitechG29\
VID\_046D\&PID\_C260 : LogitechG29\
VID\_046D\&PID\_C262 : LogitechG920\
VID\_046D\&PID\_C266 : LogitechG923PS\
VID\_046D\&PID\_C267 : LogitechG923PS\
VID\_046D\&PID\_C26D : LogitechG923X\
VID\_046D\&PID\_C26E : LogitechG923X\
VID\_046D\&PID\_C272 :  LogitechGPro\
VID\_046D\&PID\_C293 : LogitechWingmanFormulaForce\
VID\_046D\&PID\_C294 : LogitechDrivingForce\
VID\_046D\&PID\_C295 : LogitechMomoForce\
VID\_046D\&PID\_C298 : LogitechDrivingForce\
VID\_046D\&PID\_C299 : LogitechG25\
VID\_046D\&PID\_C29A : LogitechDrivingForceGT\
VID\_046D\&PID\_C29B : LogitechG27\
VID\_046D\&PID\_C29C : LogitechSpeedForce\
VID\_046D\&PID\_CA03 : LogitechMomoRacing\
VID\_046D\&PID\_CA04 : LogitechRacingWheel\
VID\_045E\&PID\_001A : MicrosoftSideWinder\
VID\_045E\&PID\_0034 :  MicrosoftSideWinder\
VID\_346E\&PID\_0000 : MozaR16\
VID\_346E\&PID\_0002 : MozaR9\
VID\_346E\&PID\_0004 : MozaR5\
VID\_346E\&PID\_0005 : MozaR3\
VID\_346E\&PID\_0006 : MozaR12\
VID\_0483\&PID\_0522 : SimagicM10\
VID\_16D0\&PID\_0D5A : Simucube1\
VID\_16D0\&PID\_0D5F : Simucube2Ultimate\
VID\_16D0\&PID\_0D60 : Simucube2Pro\
VID\_16D0\&PID\_0D61 : Simucube2Sport\
VID\_1FC9\&PID\_804C : SimXperienceAccuForcePro\
VID\_044F\&PID\_B56A : ThrustmasterF430FF\
VID\_044F\&PID\_B56E : ThrustmasterT500RS\
VID\_044F\&PID\_B605 : ThrustmasterNascarProFF2\
VID\_044F\&PID\_B651 : ThrustmasterFGTRumbleForce\
VID\_044F\&PID\_B653 : ThrustmasterRGT\
VID\_044F\&PID\_B654 : ThrustmasterFGTFF\
VID\_044F\&PID\_B669 : ThrustmasterTX\
VID\_044F\&PID\_B66D : ThrustmasterT300RSPS4\
VID\_044F\&PID\_B66E : ThrustmasterT300RSPS3\
VID\_044F\&PID\_B66F : ThrustmasterT300RSPS3ADV\
VID\_044F\&PID\_B677 : ThrustmasterT150\
VID\_044F\&PID\_B67F : ThrustmasterTMX\
VID\_044F\&PID\_B689 : ThrustmasterTSPC\
VID\_044F\&PID\_B692 : ThrustmasterTSXW\
VID\_044F\&PID\_B696 : ThrustmasterT248\
VID\_0483\&PID\_A355 :  VRSDirectForcePro\
VID\_11FF\&PID\_0511 : PXNV9

</details>
