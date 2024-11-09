# Réduction de la latence

## Paramètres de réduction de la latence

Cette fonction peut être utilisée pour réduire la quantité de latence inhérente à chaque jeu et peut également aider à compenser la latence lié aux écrans.
C'est une fonction qui **s'applique uniquement aux systèmes de Retroarch**.

Pour réduire le décalage au minimum, on peut mettre l'émulation en pause, appuyer sur une direction et maintenir la touche enfoncée, et faire avancer l'émulation image par image jusqu'à ce que le personnage bouge.
Le nombre d'images de décalage correspond au nombre d'images avancées - 1.
Attention, **plus le nombre d'images en avance sur l'émulation est élevé, plus le processeur est sollicité**.

De nombreux cœurs ne laissent pas l'émulation audio dans un état propre après le chargement d'état nécessaire à cette fontion, ce qui peut provoquer des bourdonnements. 
L'utilisation du **Mode à deux instances** fait en sorte que le noyau principal n'effectue aucun chargement, ce qui permet d'éviter ce problème.

**Preemptive Frames** est un moyen plus moderne d'obtenir le même résultat que Run-ahead avec moins de puissance de calcul.
Cette option devrait être plus rapide, mais cela dépend du jeu ou du système.

Plus d'informations sont disponibles [dans les docs de libretro](https://docs.libretro.com/guides/runahead/) utilisés comme référence pour cette page wiki.

# Réduire le flou de mouvement

Black Frame Insertion (BFI) permet à l'émulateur d'insérer des images noires entre les images du jeu afin de réduire le flou de mouvement inhérent aux écrans sample-and-hold (LCD, QLED et OLED). 
C'est une fonction qui **s'applique uniquement aux systèmes Retroarch**.

Ce problème n'existait pas sur les écrans cathodiques en raison de leur technologie de balayage par roulement, ce qui explique pourquoi les mouvements semblaient plus fluides.

## Paramètres de synchronisation de l'écran

Le réglage de l'insertion d'images noir dans Retrobat suit la graduation de RetroArch et doit donc être réglé comme suit :
1 - Pour les écrans 120Hz
2 - Pour les écrans à 180 Hz
3 - Pour les écrans à 240 Hz
4 - Pour les écrans à 300 Hz
5 - Pour les écrans 360Hz
6 - Pour les écrans 420Hz
7 - Pour les écrans 480Hz
8 - Pour les écrans 540Hz
9 - Pour les écrans 600Hz
10 - Pour les écrans 660Hz
11 - Pour les écrans 720Hz
12 - Pour les écrans 780Hz
13 - Pour les écrans 840Hz
14 - Pour les écrans 900Hz
15 - Pour les écrans 960Hz

Il est important de noter que **BFI ne peut pas être activé si vous utilisez l'option de compatibilité G-sync/Freesync** (également connue sous le nom de VRR). 
L'option VRR peut être très utile pour les jeux qui fonctionnent à une fréquence autre que 60 Hz (de nombreux jeux d'arcade par exemple) afin de préserver la synchronisation du jeu. 

Pour de tels scénarios, les utilisateurs expérimentés peuvent créer une résolution personalisée dans Windows à l'aide de [Custom Resolution Utility](https://github.com/radamar/Custom-Resolution-Utility-ToastyX) pour définir une fréquence aussi proche que possible de la fréquence mathématiquement correcte qui est un multiple de celle dont le jeu a besoin. 
Par exemple, MK1, 2 et 3 tournent à environ 54,7FPS, vous avez donc besoin d'environ 109,4 Hz pour avoir un bon rendu avec le BFI si vous utilisez un moniteur 120 Hz et le premier réglage dans Retrobat. 
