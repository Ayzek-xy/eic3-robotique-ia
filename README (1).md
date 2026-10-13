# Devoir N°1 : Robot suiveur de ligne

**Nom complet :** Isaac Denis Lapointe
**Formation :** Robotique & Intelligence Artificielle, EIC 3.0
**Formateur :** Carlos Yfrazin
**Plateforme utilisée :** VEXcode VR (programmation par blocs)
**Terrain utilisé :** Art Canvas

## Objectif

Programmer le robot virtuel pour qu'il détecte une ligne au sol grâce à son capteur et corrige sa direction automatiquement pour la suivre.

## Fonctionnement du programme

Le robot démarre avec une vitesse de déplacement de 20 % et une vitesse de rotation de 15 %, puis abaisse le stylo pour laisser une trace de son trajet. Il entre ensuite dans une boucle infinie qui lit la luminosité du capteur Down Eye. Lorsque la valeur est inférieure à 50 %, le robot considère qu'il est sur la ligne et avance de 10 mm. Dans le cas contraire, il tourne de 10° vers la droite, puis, si la ligne n'est toujours pas détectée, il revient de 20° vers la gauche. Ce balayage des deux côtés lui permet de retrouver la ligne et de la suivre par petits pas.

![Programme en blocs](captures/blocs.png)
![Robot suivant la ligne](captures/robot-sur-la-ligne.png)

## Ce que j'ai appris et difficultés rencontrées

Ce devoir m'a montré qu'un robot peut se corriger lui-même avec une logique très simple : lire un capteur, comparer à un seuil, puis agir. Le plus délicat a été de choisir le seuil de luminosité et la taille des rotations. Des angles trop grands font osciller le robot, et des angles trop petits lui font perdre la ligne dans les courbes. J'ai ajusté ces valeurs par essais successifs.

## Contenu du dossier

- `code/suiveur_de_ligne.py` : le programme en Python
- `captures/` : captures d'écran du programme et du robot en action
