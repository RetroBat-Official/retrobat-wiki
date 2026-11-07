# Décorations (bezels)

La plupart des écrans TV et moniteurs étaient au format 4:3 jusqu'à la fin des années 90. Sur un écran 16:9, les jeux de cette époque s'affichent avec des bandes noires de chaque côté. RetroBat peut remplir cet espace avec des **décorations** (bezels).

<div align="left"><figure><img src="../.gitbook/assets/image (390).png" alt=""><figcaption></figcaption></figure></div>

RetroBat propose :

* des **packs de décorations**, fournis avec RetroBat, avec un bezel par système ;
* **The Bezel Project**, un bezel par jeu pour de nombreux systèmes, à télécharger ;
* les **Mega Bezels**, des packs de shaders pour RetroArch qui dessinent le bezel avec des effets (reflets, lueur…) ;
* les **tatouages**, une image des contrôles affichée par-dessus le bezel.

{% hint style="info" %}
Les décorations sont faites pour les écrans larges (16:10, 16:9 et plus). Sur un écran 4:3 ou 5:4, aucune décoration n'est affichée.
{% endhint %}

## Choisir les décorations

L'option **DÉCORATIONS** se règle :

* pour tous les jeux : **MENU PRINCIPAL > PARAMÈTRES DES JEUX > DÉCORATIONS** ;

<div align="left"><figure><img src="../.gitbook/assets/image (391).png" alt=""><figcaption></figcaption></figure></div>

* pour un système : [Options d'affichage](../navigation/view-options.md) > **CONFIGURATION AVANCÉE DU SYSTÈME > DÉCORATIONS** ;

<div align="left"><figure><img src="../.gitbook/assets/image (392).png" alt=""><figcaption></figcaption></figure></div>

* pour un jeu : [Options du jeu](../navigation/game-options.md) > **CONFIGURATION AVANCÉE DU JEU > DÉCORATIONS**.

<div align="left"><figure><img src="../.gitbook/assets/image (393).png" alt=""><figcaption></figcaption></figure></div>

<table><thead><tr><th width="336.5">Choix</th><th>Résultat</th></tr></thead><tbody><tr><td><strong>AUTO</strong> (par défaut)</td><td>Le bezel du jeu, s'il y en a un (scrapé ou téléchargé avec The Bezel Project), sinon le bezel du système de <strong>DEFAULT UNGLAZED</strong></td></tr><tr><td><strong>AUCUN</strong></td><td>Pas de décoration</td></tr><tr><td><strong>DEFAULT UNGLAZED</strong></td><td>Bezel du système (style par défaut de RetroBat)</td></tr><tr><td><strong>DEFAULT CURVE</strong>, <strong>DEFAULT CURVE NIGHT</strong>, <strong>DEFAULT NOCURVE</strong>, <strong>DEFAULT NOCURVE NIGHT</strong></td><td>Bezel du système, avec un écran bombé ou plat, éclairage de jour ou de nuit</td></tr><tr><td><strong>AMBIANCE BROADCAST</strong>, <strong>AMBIANCE GAMEROOM</strong>, <strong>AMBIANCE MONITOR 1084S</strong>, <strong>AMBIANCE NIGHT</strong>, <strong>AMBIANCE VINTAGE TV</strong></td><td>Le jeu dans une pièce ou dans un vieux téléviseur / moniteur</td></tr><tr><td><strong>ARCADE 1980S</strong>, <strong>ARCADE 1980S VERTICAL</strong>, <strong>ARCADE VERTICAL DEFAULT</strong></td><td>Style borne d'arcade (jeux horizontaux ou verticaux)</td></tr><tr><td><strong>ANIMATED</strong></td><td>Bezels animés pour RetroArch : les boutons de la manette dessinée s'allument quand vous appuyez dessus (Dreamcast, Game Boy Advance, Mega Drive, NES, PlayStation, Saturn, Super Nintendo)</td></tr><tr><td><strong>THEBEZELPROJECT</strong></td><td>Bezels du Bezel Project (une fois téléchargés, voir plus bas)</td></tr></tbody></table>

Un aperçu de chaque pack est affiché dans la liste.

<div align="left"><figure><img src="../.gitbook/assets/image (394).png" alt=""><figcaption></figcaption></figure></div>

* **Jeux d'arcade verticaux** (MAME, FBNeo) : avec les packs par défaut, RetroBat utilise automatiquement un bezel vertical.
* **Émulateurs standalone** : selon l'émulateur, le bezel est affiché avec ReShade ou avec une fenêtre derrière l'émulateur. L'option **MENU PRINCIPAL > PARAMÈTRES DES JEUX > RESHADE** règle l'utilisation de ReShade : **DÉSACTIVÉ** (le bezel est alors affiché avec une fenêtre), **UTILISER LE MIEN** (RetroBat n'installe, ne modifie ni ne supprime jamais les fichiers ReShade dans les dossiers des émulateurs).
* L'option DÉCORATIONS n'apparaît que pour les émulateurs capables d'afficher des bezels.

## Bezels par jeu

### The Bezel Project

The Bezel Project fournit un bezel pour chaque jeu de nombreux systèmes.

1. Ouvrez **MENU PRINCIPAL > MISES À JOUR & TÉLÉCHARGEMENTS > LE BEZEL PROJECT**.

<div align="left"><figure><img src="../.gitbook/assets/image (395).png" alt=""><figcaption></figcaption></figure></div>

2. Sélectionnez le système et confirmez l'installation.

<div align="left"><figure><img src="../.gitbook/assets/image (396).png" alt=""><figcaption></figcaption></figure></div>

3. Attendez la fin du téléchargement.

<div align="left"><figure><img src="../.gitbook/assets/image (398).png" alt=""><figcaption></figcaption></figure></div>

Les bezels sont enregistrés dans `decorations\thebezelproject\games\<système>`. Ils sont utilisés avec **AUTO** ou **THEBEZELPROJECT**. Pour FBNeo, le pack MAME est utilisé si le pack FBNeo n'est pas installé.

Un bezel est utilisé pour un jeu quand son nom correspond au nom du fichier du jeu, sans tenir compte des majuscules, de la ponctuation et du texte entre parenthèses ou entre crochets : `Super Mario World (USA).png` est utilisé pour `Super Mario World (Europe).sfc`.

<div align="left"><figure><img src="../.gitbook/assets/image (399).png" alt=""><figcaption></figcaption></figure></div>

### Bezels scrapés

ScreenScraper fournit des bezels 16:9 pour certains jeux. Activez **MENU PRINCIPAL > SCRAPEUR > DÉCORATION (16:9)** avant de scraper. Le bezel est enregistré avec les autres médias du jeu et il est utilisé avec **AUTO**.

<div align="left"><figure><img src="../.gitbook/assets/image (400).png" alt=""><figcaption></figcaption></figure></div>

Vous pouvez aussi choisir une image pour un jeu dans **ÉDITER LES MÉTADONNÉES DE CE JEU > Décoration (16:9)**.

## Comment RetroBat trouve le bezel

Pour le pack choisi (`<pack>`), RetroBat utilise la première image trouvée :

1. `decorations\<pack>\games\<système>\<jeu>.png`, puis `system\decorations\<pack>\games\<système>\<jeu>.png`
2. `decorations\<pack>\games\<jeu>.png`, puis `system\decorations\<pack>\games\<jeu>.png`
3. Mêmes dossiers, avec un nom qui correspond (voir The Bezel Project plus haut)
4. `decorations\<pack>\systems\<système>.png`, puis `system\decorations\<pack>\systems\<système>.png`
5. `decorations\<pack>\default.png`, puis `system\decorations\<pack>\default.png`
6. `decorations\default_unglazed\systems\<système>.png`, puis `system\decorations\default_unglazed\systems\<système>.png`

`system\decorations` contient les packs fournis avec RetroBat et il est écrasé par les mises à jour. `decorations` (à la racine de RetroBat) est pour vos propres bezels et pour The Bezel Project : il n'est jamais écrasé et il est lu en priorité.

## Créer vos propres bezels

### Un bezel pour un jeu ou un système

Copiez votre image (PNG, 1920×1080 pour un écran 16:9, transparente là où le jeu s'affiche) dans :

* `decorations\<pack>\games\<système>\<jeu>.png` pour un jeu (le nom du fichier du jeu, sans l'extension) ;
* `decorations\<pack>\systems\<système>.png` pour un système.

Par exemple, `decorations\default_unglazed\games\snes\Super Mario World.png`.

### Votre propre pack

Tout dossier placé dans `decorations` apparaît comme un pack dans la liste DÉCORATIONS (en majuscules, `_` remplacé par des espaces). Par exemple, `decorations\mes_bezels` apparaît sous le nom **MES BEZELS** :

```
decorations\mes_bezels\default.png                   → bezel pour tous les systèmes
decorations\mes_bezels\systems\snes.png              → bezel pour la Super Nintendo
decorations\mes_bezels\games\snes\Super Metroid.png  → bezel pour un jeu
```

### Le fichier .info

Par défaut, RetroBat place le jeu dans la zone transparente de l'image. Pour régler la position vous-même, ajoutez un fichier `.info` du même nom à côté de l'image (ex. `snes.info` à côté de `snes.png`) :

```json
{
 "width":1920,
 "height":1080,
 "top":24,
 "left":273,
 "bottom":24,
 "right":273,
 "opacity":1.0,
 "messagex":0.22,
 "messagey":0.12
}
```

* `width`, `height` : taille de l'image.
* `top`, `left`, `bottom`, `right` : marges, en pixels, entre les bords de l'image et le jeu.
* `opacity` : opacité du bezel (RetroArch).
* `messagex`, `messagey` : position des messages de RetroArch.

## Mega Bezels

Les Mega Bezels sont des packs de shaders RetroArch qui dessinent eux-mêmes le bezel et les effets d'écran (reflets, courbure, lueur…). Ils ne fonctionnent qu'avec les cores RetroArch.

<div align="left"><figure><img src="../.gitbook/assets/image (401).png" alt=""><figcaption></figcaption></figure></div>

1. Téléchargez un pack depuis **MENU PRINCIPAL > MISES À JOUR & TÉLÉCHARGEMENTS > TÉLÉCHARGEMENT DE CONTENU**. Les packs sont enregistrés dans `emulators\retroarch\shaders`.

<div align="left"><figure><img src="../.gitbook/assets/image (402).png" alt=""><figcaption></figcaption></figure></div>

2. Sélectionnez-le dans **SHADERS** (dans **PARAMÈTRES DES JEUX**, ou dans la configuration avancée d'un système ou d'un jeu).

<div align="left"><figure><img src="../.gitbook/assets/image (404).png" alt=""><figcaption></figcaption></figure></div>

Avec un pack Mega Bezel, RetroBat règle automatiquement **DÉCORATIONS** sur **AUCUN**, le **RAPPORT D'ASPECT** en plein écran et le pilote vidéo **Vulkan**, sauf si vous avez modifié ces options vous-même. Si vous changez de pilote vidéo, n'utilisez pas **OPENGL** : les Mega Bezels ne fonctionnent pas avec (OPENGL CORE ou DirectX 10, 11, 12 peuvent fonctionner).

Pour les personnaliser, voir [Adapter et personnaliser les Mega Bezels](../tutoriels/adapter-et-personnaliser-les-mega-bezels.md).

## Tatouages

Un tatouage est une image des contrôles, affichée par-dessus le bezel.

<div align="left"><figure><img src="../.gitbook/assets/image (403).png" alt=""><figcaption></figcaption></figure></div>

Options dans **MENU PRINCIPAL > PARAMÈTRES DES JEUX > TATOUAGE** (ou dans la configuration avancée d'un système ou d'un jeu) :

<table><thead><tr><th width="310.25">Option</th><th>Description</th></tr></thead><tbody><tr><td><strong>AFFICHER LE TATOUAGE</strong></td><td>Affiche le tatouage</td></tr><tr><td><strong>COIN DU TATOUAGE</strong></td><td>Coin de l'écran : <strong>EN HAUT À GAUCHE</strong> (par défaut), <strong>EN HAUT À DROITE</strong>, <strong>EN BAS À DROITE</strong>, <strong>EN BAS À GAUCHE</strong></td></tr><tr><td><strong>REDIMENSIONNER LE TATOUAGE</strong></td><td>Garde la taille d'origine du tatouage (réduite seulement s'il est plus grand que l'écran). Par défaut, le tatouage est redimensionné à une largeur fixe</td></tr></tbody></table>

* Un tatouage ne s'affiche qu'avec un bezel : pas de bezel, pas de tatouage.
* Le tatouage fourni par RetroBat suit la manette et la disposition des boutons utilisées (ex. 3 ou 6 boutons sur Mega Drive).
* **Vos propres tatouages** : placez-les dans `user\tattoos\games\<système>\<jeu>.png` (un jeu) ou `user\tattoos\default\<système>.png` (un système). Ils sont utilisés en priorité et ne sont pas écrasés par les mises à jour.
* Quand **AUTOCONFIGURER LES MANETTES** est sur **NON**, seuls vos propres tatouages sont affichés (ceux de RetroBat ne correspondraient pas à votre configuration).
