README — DEVOIR N°3 : Bras robotique à plusieurs degrés de liberté

Étudiant : Isaac Denis LAPOINTE

Cours : Robotique \& Intelligence Artificielle — EIC 3.0

Plateforme utilisée : Tinkercad (https://www.tinkercad.com)

Date : Octobre 2026



1\. Objectif du devoir

L'objectif de ce devoir est de concevoir et de simuler un bras robotique contrôlé par un microcontrôleur Arduino Uno. Le but est de comprendre la notion de degrés de liberté (DDL) et de programmer une séquence de mouvements précis à l'aide de servomoteurs.



2\. Composants utilisés (Simulation Tinkercad)

1x Arduino Uno (Microcontrôleur)



3x Servomoteurs (Modèle standard SG90 ou similaire)



1x Plaque de test (Breadboard)



Fils de connexion (Mâle-Mâle)



Alimentation : Le circuit est alimenté via le port USB de l'Arduino (simulé) ou une source externe pour éviter les chutes de tension.



3\. Analyse des Degrés de Liberté (DDL)

Le bras robotique conçu possède 3 degrés de liberté, répartis comme suit :



Servomoteur 1 (Base) : Permet la rotation du bras sur un plan horizontal (mouvement de gauche à droite). C'est l'articulation principale (épaule).



Servomoteur 2 (Bras) : Permet le mouvement de levage et d'abaissement du bras (mouvement de haut en bas).



Servomoteur 3 (Pince/Effecteur) : Permet l'ouverture et la fermeture de la pince pour saisir ou relâcher un objet.



Note : Ce bras ne possède pas de DDL pour la rotation du poignet, mais il permet déjà une manipulation spatiale simple.



4\. Rôle de chaque servomoteur

Le servomoteur de base sert à positionner le bras au-dessus de la zone de travail.



Le servomoteur de bras sert à descendre ou monter l'effecteur pour atteindre l'objet.



Le servomoteur de pince sert à l'action mécanique de préhension (attraper).



5\. Programme et Séquence de mouvement

Le code Arduino utilise la bibliothèque Servo.h. La séquence programmée effectue les mouvements suivants :



Position de repos (tous les servos à 90°).



Rotation de la base vers la gauche (45°).



Descente du bras (servo 2 à 30°).



Fermeture de la pince (servo 3 à 10°).



Remontée du bras (servo 2 à 90°).



Rotation de la base vers la droite (135°).



Ouverture de la pince pour déposer l'objet.



6\. Difficultés rencontrées

Gestion de l'alimentation : Dans Tinkercad, faire bouger 3 servomoteurs en même temps peut provoquer des "clignotements" ou des arrêts si l'alimentation n'est pas suffisante. J'ai dû ajouter des délais (delay) entre les mouvements pour stabiliser la simulation.



Précision des angles : Il a fallu ajuster les angles manuellement pour que la pince ne traverse pas le sol ou ne bloque pas le bras.



7\. Ce que j'ai appris

J'ai compris qu'un degré de liberté correspond à une articulation indépendante. Plus un robot a de DDL, plus il est flexible, mais plus la programmation devient complexe (coordination des mouvements). J'ai également appris à utiliser la fonction servo.write() pour contrôler la position angulaire précise d'un moteur.

