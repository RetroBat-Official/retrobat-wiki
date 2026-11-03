# 🎮 Manettes de Jeu

Presque toutes les manettes reconnues par Windows fonctionnent avec RetroBat.

* **Les manettes filaires** sont « plug-and-play » : branchez-les, puis configurez-les dans RetroBat si nécessaire.
* **Les manettes Bluetooth** doivent d'abord être appairées dans les paramètres Bluetooth de Windows.

Quand une nouvelle manette est détectée, RetroBat vous propose de la configurer (voir [Configuration des contrôleurs](../../controller-configuration.md)). La plupart des manettes courantes sont configurées automatiquement.

{% hint style="info" %}
Pour vérifier que Windows détecte bien votre manette et tous ses boutons, testez-la sur [gamepad-tester.com](https://gamepad-tester.com/).
{% endhint %}

## XInput ou DirectInput ?

Windows gère deux types de manettes :

<table><thead><tr><th width="133.25">Type</th><th width="320.75">Manettes</th><th>Dans RetroBat</th></tr></thead><tbody><tr><td><strong>XInput</strong></td><td>Manettes Xbox et manettes en mode « Xbox / X-input »</td><td>✅ Recommandé : reconnues de la même façon par tous les émulateurs</td></tr><tr><td><strong>DirectInput / SDL</strong></td><td>PlayStation, Switch Pro, manettes génériques, 8BitDo en mode Switch ou D-input…</td><td>Fonctionnent, mais certains émulateurs anciens peuvent demander des réglages supplémentaires</td></tr></tbody></table>

{% hint style="warning" %}
Windows ne gère que **4 manettes XInput** en même temps. Au-delà de 4 joueurs, utilisez des manettes dans un autre mode.
{% endhint %}

## Manettes Xbox (et toute manette XInput)

![](<../../../.gitbook/assets/image (337).png>)![](<../../../.gitbook/assets/image (338).png>)

Les manettes Xbox sont les plus compatibles avec RetroBat.

<table><thead><tr><th width="290.25">Modèle</th><th>Connexion</th></tr></thead><tbody><tr><td>Xbox Series X|S, Xbox One S, Xbox Elite Series 2</td><td>USB, Bluetooth ou adaptateur sans fil Xbox</td></tr><tr><td>Xbox One (premier modèle, sans Bluetooth)</td><td>USB ou adaptateur sans fil Xbox</td></tr><tr><td>Xbox 360 filaire</td><td>USB</td></tr><tr><td>Xbox 360 sans fil</td><td>Récepteur sans fil Xbox 360 pour Windows (l'adaptateur Xbox One ne fonctionne pas)</td></tr></tbody></table>

## Manettes 8BitDo

<div align="left"><figure><img src="../../../.gitbook/assets/image (339).png" alt=""><figcaption></figcaption></figure></div>

Les manettes 8BitDo fonctionnent très bien avec RetroBat. La plupart des modèles proposent plusieurs **modes**, qui changent la façon dont Windows voit la manette.

{% hint style="success" %}
**Quel mode pour RetroBat ?**

* **Mode X-input** : recommandé. La manette est vue comme une manette Xbox et fonctionne de la même façon dans tous les émulateurs.
* **Mode Switch** : uniquement si vous avez besoin de la **détection de mouvement** (gyroscope) pour des jeux Wii U ou Switch. Le mode X-input ne gère pas le gyroscope.
{% endhint %}

### Changer de mode

<table><thead><tr><th width="240.25">Modèle</th><th width="186.25">X-input</th><th width="157.25">Switch</th><th width="158.75">D-input</th></tr></thead><tbody><tr><td>Modèles Bluetooth à boutons (SN30 Pro, SN30 Pro+, Lite, M30…) : <strong>éteindre la manette, puis l'allumer avec</strong></td><td><strong>START + X</strong></td><td><strong>START + Y</strong></td><td><strong>START + B</strong></td></tr><tr><td>Modèles avec un interrupteur de mode au dos (Pro 2…) : <strong>placer l'interrupteur sur</strong></td><td><strong>X</strong></td><td><strong>S</strong></td><td><strong>D</strong></td></tr><tr><td>Modèles filaires et connexion USB : <strong>maintenir le bouton en branchant le câble</strong></td><td><strong>X</strong></td><td><strong>START + Y</strong></td><td><strong>B</strong></td></tr><tr><td>Modèles avec dongle USB 2,4 GHz (Ultimate 2.4G, Ultimate 2C…)</td><td>Utiliser le dongle (X-input par défaut)</td><td>—</td><td>—</td></tr></tbody></table>

Pour éteindre une manette, maintenez **START** environ 3 secondes (8 secondes sur certains modèles).

Sur la plupart des modèles, les LED indiquent le mode actif : par exemple sur la Pro 2, LED 2 clignotante = X-input, LED 1 = D-input, LED 3 = macOS, LED qui tournent = Switch ou appairage.

{% hint style="warning" %}
**Après avoir changé le mode d'une manette Bluetooth**, Windows la voit comme un nouvel appareil :

1. Supprimez la manette des paramètres Bluetooth de Windows.
2. Allumez la manette dans le nouveau mode, puis mettez-la en appairage (maintenez le bouton **pair** 3 secondes).
3. Appairez-la à nouveau dans Windows.
4. Si RetroBat vous le demande, configurez à nouveau la manette (une manette dans un autre mode est une manette différente pour RetroBat).
{% endhint %}

{% hint style="info" %}
* Les modes disponibles dépendent du modèle : consultez le manuel de votre manette.
* Mettez votre manette à jour avec **8BitDo Ultimate Software** ou **8BitDo Updater** (Windows), disponibles sur le [site de support 8BitDo](https://support.8bitdo.com/).
{% endhint %}

## Manettes PlayStation

### DualSense (PS5) et DualShock 4 (PS4)

![](<../../../.gitbook/assets/image (340).png>)![](<../../../.gitbook/assets/image (341).png>)

Les DualSense et DualShock 4 fonctionnent en USB et en Bluetooth, et gèrent la détection de mouvement.

Par défaut, RetroBat les utilise en **mode standard**, compatible avec tous les émulateurs. L'option **PS4/PS5 SUPPORT ÉTENDU** (**MENU PRINCIPAL** > **PARAMÈTRES DES JEUX** > **CONTRÔLES** > **CONTRÔLEURS SPÉCIAUX**, ou par système) active les vibrations et le gyroscope dans les émulateurs qui les gèrent (DuckStation, émulateurs Switch…).

{% hint style="warning" %}
Une fois le support étendu utilisé, la manette reste dans ce mode jusqu'à ce qu'elle soit éteinte : les émulateurs qui utilisent DirectInput peuvent alors ne plus la détecter. **Éteignez puis rallumez la manette** si un émulateur ne réagit pas, ou laissez l'option désactivée.
{% endhint %}

### DualShock 3 (PS3)

<div align="left"><figure><img src="../../../.gitbook/assets/image (342).png" alt="" width="188"><figcaption></figcaption></figure></div>

La DualShock 3 n'est pas reconnue nativement par Windows : installez un pilote comme [DsHidMini](https://github.com/nefarius/DsHidMini) et utilisez son mode **XInput** pour une compatibilité optimale.

## Manettes Nintendo

### Manette Nintendo Switch Pro

<div align="left"><figure><img src="../../../.gitbook/assets/image (343).png" alt=""><figcaption></figcaption></figure></div>

La manette Switch Pro fonctionne en USB et en Bluetooth. Elle est idéale pour les émulateurs Wii U et Switch (Cemu, Eden, Citron, Ryujinx…), qui gèrent sa détection de mouvement.

{% hint style="warning" %}
Les noms des boutons Nintendo sont inversés par rapport à Xbox (A à droite, B en bas). RetroBat utilise la **position** des boutons : le bouton Sud (B sur une manette Nintendo) valide toujours.
{% endhint %}

### Joy-Cons

<div align="left"><figure><img src="../../../.gitbook/assets/image (344).png" alt="" width="188"><figcaption></figcaption></figure></div>

Des Joy-Cons connectés ensemble sont vus comme **une seule manette** par RetroBat.

## PC portables

<table><thead><tr><th width="257.75">Appareil</th><th>Contrôles intégrés</th></tr></thead><tbody><tr><td>ASUS ROG Ally, Lenovo Legion Go, MSI Claw…</td><td>Vus comme une manette Xbox (XInput) : ils fonctionnent directement</td></tr><tr><td>Steam Deck (sous Windows)</td><td>Nécessite Steam (Steam Input) ou un pilote pour être vu comme une manette Xbox. Réglages souris et pistolet : <strong>PARAMÈTRES DES MANETTES</strong> > <strong>STEAMDECK MOUSE/GUN SETTINGS</strong></td></tr></tbody></table>

## Problèmes fréquents

<table><thead><tr><th width="236.5">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>La manette apparaît deux fois</td><td>Un outil crée une manette Xbox virtuelle en plus de la vraie (DS4Windows, DsHidMini, Steam Input…). Masquez la vraie manette (par exemple avec HidHide), ou fermez l'outil.</td></tr><tr><td>Steam Input modifie les contrôles</td><td>Fermez Steam, ou désactivez Steam Input pour cette manette, avant de lancer RetroBat.</td></tr><tr><td>Les joueurs ne sont pas dans le bon ordre</td><td>Choisissez la manette de chaque joueur dans <strong>PARAMÈTRES DES MANETTES</strong> (voir <a href="../../controller-configuration.md">Configuration des contrôleurs</a>).</td></tr><tr><td>Une manette ne fonctionne pas dans un seul émulateur</td><td>Réglez <strong>AUTOCONFIGURER LES MANETTES</strong> sur <strong>OFF</strong> pour ce système et configurez les contrôles dans l'émulateur, puis signalez le problème à l'équipe RetroBat.</td></tr></tbody></table>

## Contrôleurs spéciaux

RetroBat configure aussi automatiquement certains contrôleurs spéciaux : manettes de type N64, Mega Drive / Genesis, Saturn… Voir [Contrôleurs spéciaux](controleurs-speciaux.md).
