# REminiscence

<div align="left" data-full-width="true"><figure><img src="../../../.gitbook/assets/image (810).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Présentation

**Flashback** (Delphine Software, 1992) est un jeu d'action et d'aventure en 2D, aux animations en rotoscopie, dans un monde de science-fiction.

RetroBat le lance avec le core libretro **REminiscence**, une réécriture du moteur du jeu.

Les fichiers du jeu ne sont pas fournis : utilisez ceux de votre propre exemplaire, **version PC (DOS ou CD)**, ou les fichiers des versions [GOG](https://www.gog.com/game/flashback) / [Steam](https://store.steampowered.com/app/961620/Flashback/).

{% embed url="https://docs.libretro.com/library/reminiscence/" %}

## En bref

<table><thead><tr><th width="300.25"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\reminiscence</code></td></tr><tr><td><strong>Extensions</strong></td><td>.rem</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: reminiscence</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (fichiers du jeu à fournir)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr><tr><td><strong>Pistolets</strong></td><td>—</td></tr><tr><td><strong>Volants</strong></td><td>—</td></tr><tr><td><strong>BIOS optionnels</strong></td><td>—</td></tr></tbody></table>

{% hint style="warning" %}
Le core ne lance que la version PC (DOS) du jeu : les fichiers Amiga ou Macintosh ne sont pas reconnus.
{% endhint %}

## Quel format de jeu ?

Un fichier `.rem` vide lance le jeu dont les fichiers sont dans son dossier ou ses sous-dossiers.

## Contrôles

<table><thead><tr><th width="247.75">Manette RetroBat</th><th>Action</th></tr></thead><tbody><tr><td>Croix, stick gauche</td><td>Se déplacer</td></tr><tr><td>SUD</td><td>Sortir / ranger l'arme</td></tr><tr><td>EST</td><td>Utiliser l'objet</td></tr><tr><td>NORD</td><td>Action</td></tr><tr><td>OUEST</td><td>Inventaire / passer</td></tr></tbody></table>

### Raccourcis

Raccourcis de RetroArch. Voir la page [**Raccourcis**](../../../navigation/hotkeys.md).

## Dossiers

<table><thead><tr><th width="164">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Jeu</td><td><code>roms\reminiscence\Flashback</code></td></tr></tbody></table>

## Guides

### Organisation des fichiers

Dans `roms\reminiscence`, créez un dossier `Flashback`. Copiez-y les fichiers du jeu ; pour les versions GOG et Steam, ce sont ceux du dossier `Flashback_Data\StreamingAssets\data` :

<div align="left"><figure><img src="../../../.gitbook/assets/image (813).png" alt=""><figcaption></figcaption></figure></div>

Certaines voix et musiques peuvent manquer. Les musiques Amiga de Raphaël Gesqua peuvent être ajoutées dans le dossier `Flashback` :

<div align="left"><figure><img src="../../../.gitbook/assets/image (812).png" alt=""><figcaption></figcaption></figure></div>

Enfin, créez un fichier texte vide dans `roms\reminiscence`, nommé `Flashback`, avec l'extension `.rem` :

<div align="left"><figure><img src="../../../.gitbook/assets/image (811).png" alt=""><figcaption></figcaption></figure></div>

## Problèmes connus

<table><thead><tr><th width="267.75">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Le jeu ne se lance pas</td><td>Les fichiers ne sont pas ceux de la version PC (DOS), ou ne sont pas dans le dossier du fichier <code>.rem</code> ou un de ses sous-dossiers.</td></tr></tbody></table>
