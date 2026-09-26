# Shifumi — PCB HTMAA

Ce projet consiste à réaliser un jeu électronique de Shifumi (Pierre–Feuille–Ciseaux) sur un PCB conçu avec KiCad.

Le système possède un bouton START permettant de lancer une partie et un bouton END permettant de terminer la partie. Trois boutons supplémentaires permettent au joueur de sélectionner son choix : Pierre, Feuille ou Ciseaux.

Le fonctionnement du système repose sur un ESP32-S3 associé à plusieurs circuits logiques, notamment des 74HC164, 74HC00 et 74HC86. L'ESP32 permet de contrôler le fonctionnement général du jeu et de générer un nombre pseudo-aléatoire compris entre 1 et 3. Le 74HC164 participe au traitement de cette génération pseudo-aléatoire.

Une fois la partie lancée, l'écran OLED SSD1306 intégré à la boîte Creakit affiche un décompte. À la fin du décompte, le système récupère le nombre généré et affiche sur l'écran le symbole correspondant : Pierre pour 1, Feuille pour 2 et Ciseaux pour 3.

L'alimentation du circuit est assurée par un TPS63031DSK, qui permet de fournir une tension régulée de 3,3 V nécessaire au fonctionnement des différents composants du circuit. Des condensateurs sont également utilisés pour assurer le découplage et la stabilité de l'alimentation.

Le PCB regroupe ainsi la partie alimentation, les circuits logiques, l'ESP32-S3, les boutons de commande et l'interface avec l'écran OLED.

# Schéma électronique
images/Capture d'écran 2026-09-26 104114.png
# PCB
images/Capture d'écran 2026-09-26 104007.png
# Vue 3D
images/ProjetKicad.png

# Composants principaux

L'ESP32-S3 assure le contrôle du système. Les 74HC164 sont utilisés dans la partie logique du système et la génération pseudo-aléatoire, tandis que les 74HC00 et 74HC86 permettent de réaliser différentes fonctions logiques NAND et XOR. L'écran OLED SSD1306 permet d'afficher le décompte et le résultat de la partie. Enfin, le TPS63031DSK assure la conversion et la régulation de l'alimentation à 3,3 V.


