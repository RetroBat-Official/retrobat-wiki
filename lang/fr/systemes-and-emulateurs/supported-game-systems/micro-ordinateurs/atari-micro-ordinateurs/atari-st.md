---
description: Atari
---

# Atari ST

<div align="left">

<figure><picture><source srcset="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/91d85c7849cc550b0cac4e75cb8e0923d3b61b5e/art/logos/atarist-w.svg" media="(prefers-color-scheme: dark)"><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/52ff37c9e265587d006945a2ba695b5a962b3a3d/art/logos/atarist.svg" alt=""></picture><figcaption></figcaption></figure>

</div>

Micro-ordinateur - Durée de vie : 1985 - 1993

{% embed url="https://fr.wikipedia.org/wiki/Atari_ST" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Émulateur</strong></td><td><ul><li>libretro: hatari</li><li>libretro: hatarib</li><li>hatari</li></ul></td><td></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> atarist</td><td></td></tr><tr><td><strong>Extensions</strong></td><td>.st .msa .stx .dim .ipf .m3u .gemdos .zip .7z</td><td></td></tr></tbody></table>

## Fonctionnalités

<table><thead><tr><th width="245">Succès Rétro</th><th width="200">Parties en Réseau</th><th>Auto configuration des contrôles</th></tr></thead><tbody><tr><td>lr-hatari : NON<br>lr-hatarib : NON<br>Hatari : NON</td><td>lr-hatari : NON<br>lr-hatarib : NON<br>Hatari : NON</td><td>lr-hatari : NON<br>lr-hatarib : NON<br>Hatari : NON</td></tr></tbody></table>

## BIOS

<table><thead><tr><th width="149">Fichier BIOS</th><th width="209.03610108303252">Dossier</th><th>md5 hash / remark</th></tr></thead><tbody><tr><td>tos.img</td><td><code>\bios</code></td><td>b2a8570de2e850c5acf81cb80512d9f6</td></tr><tr><td>emutos.img</td><td><code>\bios\hatari\tos</code><br><code>\bios\hatarib</code></td><td></td></tr><tr><td>tos102.img</td><td><code>\bios\hatari\tos</code><br><code>\bios\hatarib</code></td><td></td></tr><tr><td>tos106.img</td><td><code>\bios\hatari\tos</code><br><code>\bios\hatarib</code></td><td></td></tr><tr><td>tos104.img</td><td><code>\bios\hatari\tos</code><br><code>\bios\hatarib</code></td><td></td></tr><tr><td>tos206.img</td><td><code>\bios\hatari\tos</code><br><code>\bios\hatarib</code></td><td></td></tr></tbody></table>

## Contrôles

Utiliser la fonctionnalité [Pad2Key](../../../../controleurs/pad2key.md).

Le mapping par défaut est le suivant:

<table><thead><tr><th width="263">Retrobat</th><th>Atari ST (libretro)</th></tr></thead><tbody><tr><td>START</td><td>Afficher/masquer le clavier virtuel</td></tr><tr><td>SELECT</td><td>Basculer entre le mode joystick et le mode clavier</td></tr><tr><td>D-PAD</td><td></td></tr><tr><td>Stick analogique gauche</td><td>Directions (haut, bas, gauche, droite)</td></tr><tr><td>Stick analogique droit</td><td></td></tr><tr><td><img src="../../../../.gitbook/assets/image (32).png" alt=""></td><td></td></tr><tr><td><img src="../../../../.gitbook/assets/image (19).png" alt=""></td><td>Bouton B de la souris</td></tr><tr><td><img src="../../../../.gitbook/assets/image (6).png" alt=""></td><td>Fire / Bouton A de la souris / appuyer sur le bouton du clavier virtuel</td></tr><tr><td><img src="../../../../.gitbook/assets/image (34).png" alt=""></td><td>Ouvrir l'émulateur</td></tr><tr><td>L1</td><td>Toggle Num Joy</td></tr><tr><td>R1</td><td>Modifier la vitesse de la souris entre 1 et 6</td></tr><tr><td>L2</td><td>Afficher / masquer le statut</td></tr><tr><td>R2</td><td>Activer / désactiver le son</td></tr><tr><td>L3</td><td></td></tr><tr><td>R3</td><td></td></tr></tbody></table>

### Hatari

<table><thead><tr><th width="263">Retrobat</th><th>Hatari</th></tr></thead><tbody><tr><td>SELECT</td><td>Ouvrir le menu de l'émulateur</td></tr><tr><td>D-PAD</td><td>Joystick - D-pad</td></tr><tr><td><img src="../../../../.gitbook/assets/image (19).png" alt=""></td><td>Joystick - FIRE</td></tr><tr><td>F11</td><td>Plein écran</td></tr><tr><td>F12</td><td>Ouvrir le menu de l'émulateur</td></tr><tr><td>ALTGr + Q</td><td>Quitter l'émulateur</td></tr></tbody></table>

## Information spécifique au système

### Lancer une image disque dur "gemdos"

Le coeur libretro Hatari-B permet de charger une image disque dur au format "gemdos", pour cela le fichier de jeu doit être un dossier d'image de disque:

<div align="left">

<figure><img src="https://i.imgur.com/RscLeZw.png" alt=""><figcaption></figcaption></figure>

</div>

Ensuite,créer dans le même dossier un fichier texte vide du même nom que le dossier gemdos, puis sauvegarder le fichier avec l'extension .GEM:

<div align="left">

<figure><img src="https://i.imgur.com/VAu6Ce9.png" alt=""><figcaption></figcaption></figure>

</div>

Il est également possible d'automatiquement lancer un programme se trouvant sur le disque dur qui a été monté.

Pour cela, créer un fichier texte nommé de la même façon que le dossier gemdos, puis à l'intérieur de ce fichier, spécifier les informations suivantes:

<pre><code>#EXTM3U
#AUTO:<a data-footnote-ref href="#user-content-fn-1">&#x3C;nom du programme à lancer></a>
&#x3C;nom du fichier .GEM>
</code></pre>

<div align="left">

<figure><img src="https://i.imgur.com/SvXLkHs.png" alt=""><figcaption></figcaption></figure>

</div>

Enfin: sauvegarder le fichier avec l'extension ".m3u", dans le même dossier que le gemdos:

<div align="left">

<figure><img src="https://i.imgur.com/03PB7np.png" alt=""><figcaption></figcaption></figure>

</div>

Dans l'exemple ci-dessus, RetroBat va automatiquement:

* Lancer l'émulateur lr-hatarib en montant le disque dur "The New Zealand Story" dans l'émulateur
* Lancé le programme RUNME.TOS depuis le disque dur (emplacement `C:\AUTO`)

{% hint style="warning" %}
Les images gemdos nécessitent l'utilisation d'un TOS 2.06 ou de emuTOS pour fonctionner correctement.
{% endhint %}

[^1]: 
