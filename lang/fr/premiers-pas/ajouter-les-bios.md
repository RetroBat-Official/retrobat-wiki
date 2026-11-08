# Ajouter les BIOS

Certains émulateurs ont besoin de fichiers BIOS pour fonctionner correctement.

## Qu'est-ce qu'un BIOS ?

Le BIOS (parfois appelé firmware) est le programme interne d'une vraie console ou d'un ordinateur : il démarre la machine, gère les cartes mémoire, la langue, le lecteur de disques… Beaucoup d'émulateurs ont besoin d'une copie de ce programme pour lancer les jeux, par exemple pour les PlayStation 1 et 2, la Sega Saturn, la Neo Geo CD ou de nombreux anciens ordinateurs.

D'autres systèmes n'ont besoin d'aucun BIOS : l'émulateur le remplace. La page de chaque système indique si un BIOS est nécessaire.

{% hint style="warning" %}
Les BIOS sont protégés par le droit d'auteur. RetroBat ne les fournit pas, et l'équipe RetroBat ne peut pas les distribuer. Vous devez les extraire de votre propre matériel.
{% endhint %}

## Où placer les BIOS

Pour la plupart des systèmes, les fichiers BIOS doivent être placés dans le dossier `bios` de RetroBat, par exemple `C:\RetroBat\bios\`.

<div align="left"><figure><img src="../.gitbook/assets/image (245).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
* Les noms des fichiers doivent correspondre exactement à ceux attendus par RetroBat (par exemple `scph5501.bin`). Si votre fichier porte un autre nom, renommez-le.
* Certains systèmes ont besoin de leurs BIOS dans un sous-dossier ou un autre emplacement. La [page de chaque système](../systemes-and-emulateurs/supported-game-systems/), dans la section Systèmes compatibles, l'indique et liste les BIOS nécessaires.
* Les BIOS attendus en `.zip` (par exemple `adam.zip`) se copient tels quels, sans les décompresser.
* Windows masque les extensions par défaut : un fichier affiché `scph5501.bin` peut s'appeler `scph5501.bin.bin`. Cochez **Affichage > Extensions de noms de fichiers** dans l'Explorateur pour vérifier.
{% endhint %}

## Vérifier les BIOS

RetroBat peut vérifier vos fichiers BIOS : ouvrez le [MENU PRINCIPAL](../navigation/main-menu.md), allez dans [PARAMÈTRES DES JEUX](../navigation/main-menu.md#parametres-des-jeux), puis sélectionnez **VÉRIFIER LES BIOS MANQUANTS** dans le groupe **PARAMÈTRES BIOS**.

<div align="left"><figure><img src="../.gitbook/assets/image (246).png" alt=""><figcaption></figcaption></figure></div>

Le résultat liste, pour chaque système, les BIOS qui posent problème :

* **MISSING** ![](<../.gitbook/assets/image (436).png>) : le fichier est introuvable.
* **INVALID** ![](<../.gitbook/assets/image (437).png>) : le fichier est présent, mais sa somme MD5 ne correspond à aucune version connue. Il peut quand même fonctionner : testez le système pour vérifier.
* **OPTIONAL** : le fichier n'est pas nécessaire pour lancer les jeux (une autre version acceptée est déjà présente, ou il ne sert qu'à certains jeux ou émulateurs).

L'onglet **Systèmes installés** n'affiche que les systèmes qui ont des jeux, l'onglet **Tous** affiche tous les systèmes.

<div align="left"><figure><img src="../.gitbook/assets/image (257).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Par défaut, RetroBat vérifie aussi les BIOS au lancement d'un jeu. S'il manque un BIOS au système, un avertissement s'affiche, et vous pouvez quand même choisir de lancer le jeu. Seuls les BIOS **MISSING** déclenchent cet avertissement, jamais les BIOS INVALID ou OPTIONAL.
{% endhint %}

## Vérification au lancement d'un jeu

Par défaut, RetroBat vérifie aussi les BIOS au lancement d'un jeu. Si un BIOS du système est **MISSING**, ce message s'affiche :

**ATTENTION : LE SYSTÈME A UN BIOS MANQUANT ET LE JEU PEUT NE PAS FONCTIONNER CORRECTEMENT. VOULEZ-VOUS LE LANCER QUAND MÊME ?**

* **OUI** lance quand même le jeu (utile si vous utilisez un émulateur qui n'a pas besoin de ce BIOS).
* **NON** revient à la liste des jeux.

## Problèmes fréquents

<table><thead><tr><th width="300.25">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Le BIOS est dans le dossier, mais toujours MISSING</td><td>Vérifiez le sous-dossier indiqué sur la page du système et le nom exact du fichier. Vérifiez que l'extension n'est pas doublée (<code>.bin.bin</code>).</td></tr><tr><td>Le BIOS est INVALID</td><td>C'est une autre version que celle attendue. Testez un jeu : s'il démarre, vous pouvez le garder.</td></tr><tr><td>L'avertissement s'affiche, mais le jeu fonctionne</td><td>Vous utilisez un émulateur qui n'a pas besoin de ce BIOS, ou un autre BIOS accepté. Choisissez OUI, ou désactivez la vérification.</td></tr><tr><td>Un BIOS compressé n'est pas trouvé</td><td>Ne le décompressez pas : copiez le .zip tel quel.</td></tr><tr><td>Le jeu ne démarre pas (écran noir, erreur) alors qu'aucun BIOS ne manque</td><td>Le BIOS n'est peut-être pas la bonne version pour l'émulateur. Consultez la page du système.</td></tr></tbody></table>
