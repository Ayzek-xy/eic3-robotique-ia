# Devoir N°2 : Robot évitant les obstacles

**Nom complet :** Isaac Denis Lapointe
**Formation :** Robotique & Intelligence Artificielle, EIC 3.0
**Formateur :** Carlos Yfrazin
**Plateforme utilisée :** VEXcode VR (programmation par blocs)
**Terrain utilisé :** Obstacle Course

## Objectif

Programmer le robot virtuel pour qu'il détecte un obstacle devant lui et change de trajectoire automatiquement, sans intervention.

## Fonctionnement du programme

Le robot démarre avec une vitesse de déplacement de 50 % et une vitesse de rotation de 40 %. Il entre ensuite dans une boucle infinie qui lit en permanence le capteur de distance avant. Tant que la distance mesurée reste supérieure ou égale à 150 mm, le robot avance tout droit. Dès qu'elle passe sous ce seuil, il s'arrête, marque une courte pause, puis tourne de 90° vers la droite avant de repartir dans la nouvelle direction. La boucle recommence ensuite, ce qui lui permet d'éviter les obstacles successifs.

![Programme en blocs](captures/blocs.png)
![Robot évitant un obstacle](captures/robot-evite-obstacle.png)

## Ce que j'ai appris et difficultés rencontrées

Ce devoir m'a montré la logique de base d'un robot autonome : percevoir son environnement avec un capteur, comparer la mesure à un seuil, puis choisir une action. Le réglage du seuil de distance a été le point le plus important. Trop petit, le robot s'arrête trop près et touche l'obstacle. Trop grand, il tourne inutilement et perd du temps. J'ai aussi vu que l'angle de rotation compte : un angle trop faible laisse le robot face à l'obstacle et le fait tourner en boucle.

## Contenu du dossier

- `code/evitement_obstacles.py` : le programme en Python
- `captures/` : captures d'écran du programme et du robot en action
