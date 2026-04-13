# Configuration des Contrôleurs

RetroBat configure automatiquement les contrôleurs en utilisant une base de données fournies par la librairie SDL, cela signifie que, dans la plupart des cas, si vous possédez une manette d'un constructeur connu (XBox, Sony, Nintendo Switch Pro, 8BitDo...), il ne devrait y avoir aucune intervention de la part de l'utilisateur, la manette étant configurée automatiquement.

Dans certains cas cependant, la configuration automatique ne fonctionne pas ou effectue une assignation incorrecte de certaines touches, RetroBat propose des options supplémentaires pour configurer correctement votre manette :

* Désactiver l'[autoconfiguration RetroBat](controller-configuration.md#activer-une-configuration-specifique-par-jeu) complètement et procéder à votre propre configuration pour chaque système (ou pour un jeu spécifique)
* [Écraser la configuration RetroBat](controller-configuration.md#utiliser-les-fichiers-de-remplacement-retrobat) avec des fichiers de substitution.

{% hint style="warning" %}
La configuration des contrôleurs se fait au niveau de l'émulateur. Cela signifie que si vous configurez votre contrôleur manuellement (par exemple dans RetroArch) et que vous lancez plus tard un jeu depuis un autre système mais utilisant le même émulateur, et que vous activez l'autoconfiguration, cela écrasera votre configuration manuelle.
{% endhint %}

## Configuration des contrôleurs

RetroBat détecte et configure automatiquement la grande majorité des contrôleurs de marques disponibles sur le marché, toutefois, si le contrôleur n'est pas reconnu, il suffira de presser une touche et/ou un bouton et le menu suivant apparaîtra :

<figure><img src="https://i.imgur.com/eNTHkgt.png" alt=""><figcaption></figcaption></figure>

Presser et maintenir appuyé un bouton pour passer à l'écran **CONFIGURATION**

<div align="left"><figure><img src="https://i.imgur.com/yGkfqEt.png" alt=""><figcaption></figcaption></figure></div>

Configurer les boutons en fonction de la position indiquée sur l'écran pour finaliser la configuration.&#x20;

{% hint style="info" %}
Si la manette de jeu contient moins de bouton que ceux disponibles dans Retrobat, rester appuyer sur un bouton pour ignorer la ligne en cours et passer à la ligne suivante.

Il est toutefois nécessaire d'assigner les boutons A, B, D-PAD, START, SELECT et HOTKEY pour pouvoir utiliser Retrobat correctement.
{% endhint %}

Les correspondances de boutons "standard" pour les manettes XBOX, PlayStation et Nintendo sont listées dans la table ci-dessous:

<table><thead><tr><th width="184">Retrobat</th><th>Microsoft XBOX</th><th>PlayStation</th><th>Nintendo</th></tr></thead><tbody><tr><td><img src="../.gitbook/assets/image (20) (1).png" alt="A"></td><td>A</td><td><img src="../.gitbook/assets/image (13) (1).png" alt=""></td><td>B</td></tr><tr><td><img src="../.gitbook/assets/image (7) (1).png" alt=""></td><td>B</td><td><img src="../.gitbook/assets/image (23) (1).png" alt=""></td><td>A</td></tr><tr><td><img src="../.gitbook/assets/image (35).png" alt=""></td><td>Y</td><td><img src="../.gitbook/assets/image (21) (1).png" alt=""></td><td>X</td></tr><tr><td><img src="../.gitbook/assets/image (33).png" alt="" data-size="line"></td><td>X</td><td><img src="../.gitbook/assets/image (6) (1).png" alt=""></td><td>Y</td></tr><tr><td>START</td><td><img src="../.gitbook/assets/image (25) (1).png" alt=""></td><td>START / OPTIONS</td><td>+</td></tr><tr><td>SELECT</td><td><img src="../.gitbook/assets/image (24) (1).png" alt=""></td><td>SELECT / SHARE</td><td>-</td></tr><tr><td>D-PAD HAUT</td><td>D-PAD HAUT</td><td>D-PAD HAUT</td><td>D-PAD HAUT</td></tr><tr><td>D-PAD BAS</td><td>D-PAD BAS</td><td>D-PAD BAS</td><td>D-PAD BAS</td></tr><tr><td>D-PAD GAUCHE</td><td>D-PAD GAUCHE</td><td>D-PAD GAUCHE</td><td>D-PAD GAUCHE</td></tr><tr><td>D-PAD DROITE</td><td>D-PAD DROITE</td><td>D-PAD DROITE</td><td>D-PAD DROITE</td></tr><tr><td>L1</td><td>L1</td><td>L1</td><td>L</td></tr><tr><td>R1</td><td>R1</td><td>R1</td><td>R</td></tr><tr><td>Stick gauche haut</td><td>Stick gauche haut</td><td>Stick gauche haut</td><td>Stick gauche haut</td></tr><tr><td>Stick gauche gauche</td><td>Stick gauche gauche</td><td>Stick gauche gauche</td><td>Stick gauche gauche</td></tr><tr><td>Stick droit haut</td><td>Stick droit haut</td><td>Stick droit haut</td><td>Stick droit haut</td></tr><tr><td>Stick droit gauche</td><td>Stick droit gauche</td><td>Stick droit gauche</td><td>Stick droit gauche</td></tr><tr><td>L2</td><td>L2</td><td>L2</td><td>ZL</td></tr><tr><td>R2</td><td>R3</td><td>R2</td><td>ZR</td></tr><tr><td>L3</td><td>L3 (stick)</td><td>L3 (stick)</td><td>L3 (stick)</td></tr><tr><td>R3</td><td>R3 (stick)</td><td>R3 (stick)</td><td>R3 (stick)</td></tr></tbody></table>

## Désactiver une configuration spécifique par jeu

Si, pour une raison ou une autre, la configuration des manettes par défaut ne fonctionne pas pour vous, ou que vous souhaitez modifier la configuration manuellement, il y a la possibilité de désactiver la configuration automatique des contrôleur afin de gérer la configuration directement par l’émulateur / le cœur lui-mème.

La configuration automatique des manettes peut être désactivées pour tous les systèmes, par système ou uniquement pour un jeu.

### **Désactivation pour tous les systèmes**

Ouvrir le [MENU PRINCIPAL](../navigation/main-menu.md#parametres-des-jeux) et aller dans les **PARAMETRES DES JEUX.**

<div align="left"><figure><img src="https://i.imgur.com/EZGqHO6.png" alt=""><figcaption></figcaption></figure></div>

Désactiver **AUTOCONFIGURER LES MANETTES.**

<div align="left"><figure><img src="https://i.imgur.com/ExUlbH4.png" alt=""><figcaption></figcaption></figure></div>

### **Désactivation pour un système**

Ouvrir le menu [**OPTIONS D'AFFICHAGE**](../navigation/view-options.md#configuration-avancees-du-systeme) et aller dans **CONFIGURATION AVANCÉE DU SYSTÈME.**

<div align="left"><figure><img src="https://i.imgur.com/yluNDLe.png" alt=""><figcaption></figcaption></figure></div>

Puis régler l'option **AUTOCONFIGURER LES MANETTES**  sur **NON.**

<div align="left"><figure><img src="https://i.imgur.com/I45PNhI.png" alt=""><figcaption></figcaption></figure></div>

### **Désactivation pour un jeu**

Ouvrir le menu [**OPTIONS DU JEU**](../navigation/game-options.md#configuration-avancee-du-jeu) et sélectionner **CONFIGURATION AVANCEE DU JEU.**

<div align="left"><figure><img src="https://i.imgur.com/nedAp7Z.png" alt=""><figcaption></figcaption></figure></div>

Puis régler l'option **AUTOCONFIGURER LES MANETTES**  sur **NON.**

<div align="left"><figure><img src="https://i.imgur.com/Z96x4mm.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="warning" %}
Lorsque l'option AUTOCONFIGURER LES MANETTES est réglée sur NON, il est nécessaire de configurer les contrôleurs directement dans l'émulateur.

Pour accéder aux menus des émulateurs, naviguer dans la **Vue Système** et sélectionner le système "RETROBAT". (Il est également possible de lancer chaque émulateur depuis le dossier `\emulators` dans le répertoire d'installation de RetroBat)

Pour RetroArch, il est possible de créer une configuration spécifique à chaque jeu en pressant F1 (hotkey + ![A](<../.gitbook/assets/image (20) (1).png>)) en cours de jeu et en naviguant dans le menu RetroArch pour accéder à la configuration du contrôleur.
{% endhint %}

## Utiliser les fichiers de remplacement RetroBat

Pour certains émulateurs, RetroBat à inclus un process pour se substituer à la configuration automatique et standardisée. Selon l'émulateur, vous pouvez procéder de la façon suivante :&#x20;

* En sélectionnant des configurations prédéfinis (depuis le menu RetroBat),
* En utilisant les fichiers de remplacement yml / json (dans le dossier inputmapping de RetroBat)
* En activant la détection de types de contrôleurs spécifiques (des manettes reprenant la disposition N64 ou Genesis, des adaptateurs pour les manettes d'origines...)

Ci-après la liste des émulateurs qui permettent ces remplacement de fichiers, ou qui permettent différents type de disposition :

<table><thead><tr><th width="250.75">Émulateur</th><th width="165" align="center">Différentes dispositions ?</th><th width="164.5" align="center">Fichier de substitution ?</th><th width="197.75" align="center">Contrôleurs spéciaux ?</th></tr></thead><tbody><tr><td><a href="https://wiki.retrobat.org/francais/controleurs/configuration-des-touches-specifique-par-emulateur/configuration-des-touches-retroarch">RETROARCH</a></td><td align="center">X</td><td align="center">X</td><td align="center">X</td></tr><tr><td><a href="https://wiki.retrobat.org/francais/controleurs/configuration-des-touches-specifique-par-emulateur/configuration-des-touches-mame64">MAME</a></td><td align="center">X</td><td align="center">X</td><td align="center"></td></tr><tr><td>FBNEO (standalone)</td><td align="center">X</td><td align="center">X</td><td align="center"></td></tr><tr><td>FLYCAST</td><td align="center">X</td><td align="center">X</td><td align="center"></td></tr><tr><td><a href="configuration-des-touches-specifique-par-emulateur/configuration-des-touches-dolphin.md">DOLPHIN</a></td><td align="center">X</td><td align="center">X</td><td align="center">X</td></tr><tr><td>ARES</td><td align="center">X</td><td align="center"></td><td align="center">X</td></tr><tr><td>BIZHAWK</td><td align="center">X</td><td align="center"></td><td align="center">X</td></tr><tr><td>JGENESIS</td><td align="center">X</td><td align="center"></td><td align="center">X</td></tr><tr><td>KEGA-FUSION</td><td align="center">X</td><td align="center"></td><td align="center">X</td></tr><tr><td>MEDNAFEN</td><td align="center">X</td><td align="center"></td><td align="center">X</td></tr><tr><td>MUPEN64 (RMG)</td><td align="center">X</td><td align="center"></td><td align="center">X</td></tr><tr><td>SIMPLE64</td><td align="center">X</td><td align="center"></td><td align="center">X</td></tr><tr><td>2SHIP, SOH, GHOSTSHIP</td><td align="center">X</td><td align="center"></td><td align="center">X</td></tr><tr><td>PLAY!</td><td align="center"></td><td align="center">X</td><td align="center"></td></tr><tr><td>KRONOS</td><td align="center">X</td><td align="center"></td><td align="center">X</td></tr><tr><td>YABASANSHIRO</td><td align="center">X</td><td align="center"></td><td align="center">X</td></tr><tr><td>YMIR</td><td align="center">X</td><td align="center"></td><td align="center">X</td></tr><tr><td>SSF</td><td align="center">X</td><td align="center"></td><td align="center">X</td></tr><tr><td><a href="../systemes-and-emulateurs/supported-game-systems/arcade/sega/sega-model-3.md#controles">SUPERMODEL</a></td><td align="center"></td><td align="center">X</td><td align="center"></td></tr><tr><td><a href="configuration-des-touches-specifique-par-emulateur/configuration-des-touches-model2.md">MODEL2</a></td><td align="center"></td><td align="center">X</td><td align="center"></td></tr><tr><td><a href="configuration-des-touches-specifique-par-emulateur/configuration-des-touches-teknoparrot.md">TEKNOPARROT</a></td><td align="center"></td><td align="center">X</td><td align="center"></td></tr></tbody></table>

{% hint style="info" %}
Cliquez sur le lien présent sur le nom de l'émulateur pour accéder à la page spécifiquement lié a celui-ci.

Pour voir les différentes dispositions existantes pour un émulateur / un système, visitez la [page système](/broken/pages/fJXiuEVjCa5cxzU2P86Z).
{% endhint %}

### Principe de substitution des fichiers

Les fichiers de substitution fournis se trouvent dans le dossier `\system\resources\inputmapping` de votre installation RetroBat. Ces fichiers peuvent être modifiés lors des mises à jour RetroBat, il est donc recommandé de copier ceux que vous souhaitez modifier dans le dossier `\user\inputmapping` .

Ces fichiers sont des fichiers YAML (.yml), qui contiennent plusieurs conteneur (habituellement par jeu ou par cœur pour RetroArch, accompagné d'un conteneur "default") que RetroBat va inspecter afin de chercher le mappage des touches a appliquer.

#### Exemple 1 : Flycast standalone

Le fichier "`flycast_arcade.yml`" contient le mappage pour de nombreux jeux d'arcade qui peuvent être lancés à l'aide de l'émulateur Flycast (Atomiswave, Naomi et Naomi2), ci-après un exemple du contenu du fichier :

<div align="left"><figure><img src="../.gitbook/assets/image (79).png" alt=""><figcaption></figcaption></figure></div>

Chaque conteneur contient le mappage pour un jeu, car le nommage des jeux d'arcade étant fixe, cela permettra d'appliquer automatiquement ce mappage pour le jeu prévu.

Par exemple, la ligne `l2: btn_trigger_left` signifie que la valeur "btn\_trigger\_left" dans le fichier de configuration de l'émulateur Flycast sera attribué à la gâchette gauche de la manette, que RetroBat convertira L2 en la touche que vous avez défini comme L2 sur votre contrôleur (axe ou bouton) :

<div align="left"><figure><img src="../.gitbook/assets/image (80).png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../.gitbook/assets/image (81).png" alt=""><figcaption></figcaption></figure></div>

#### Exemple 2 : RetroArch (cœur Flycast)

Le fichier "`libretro_flycast_naomi.yml`" contient le mappage pour les jeux Naomi qui peuvent être lancés avec le cœur Libretro-Flycast, ci-après un exemple du contenu du fichier :

<div align="left"><figure><img src="../.gitbook/assets/image (82).png" alt=""><figcaption></figcaption></figure></div>

Chaque conteneur contient les informations de position des touches qui seront utilisés pour reparamétrer les boutons "RetroPad par défaut pour le cœur flycast. Le nommage des jeux d'arcade étant fixe, cela permettra d'appliquer automatiquement ce mappage pour le jeu prévu.

Par exemple, la ligne `btn_b: 4` signifie que le bouton SUD sur le contrôleur sera configuré sur le bouton avec l'identifiant 4 pour le cœur Libretro-Flycast (l'ID 4 correspond à la commande de la boite de vitesse) :

<div align="left"><figure><img src="../.gitbook/assets/image (83).png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../.gitbook/assets/image (84).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Pour RetroArch, ces fichiers ne changeront pas le mappage entre le contrôleur physique et le retropad générique RetroArch. Cela créera un fichier de remap par cœur. Les fichiers de remaps se trouvent dans le dossier `\emulators\retroarch\config\remaps\<core name>` .
{% endhint %}

## Résolution de soucis liés aux contrôleurs

En cas de problème avec vos contrôleurs, procédez de la façon suivante :&#x20;

1. Essayez de refaire une configuration de la manette
2. Vérifiez la configuration crée par RetroBat (sauvegardez le fichier pour plus tard)
3. Configurez le contrôleur directement depuis l'émulateur (sauvegardez le fichier pour plus tard)
4. Contactez le staff RetroBat et partagez les fichiers crées aux étapes 2 et 3
