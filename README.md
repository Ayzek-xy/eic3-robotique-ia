Devoir N°4 : Classificateur d'images simple
Nom complet : Isaac Denis Lapointe
Formation : Robotique & Intelligence Artificielle, EIC 3.0
Formateur : Carlos Yfrazin
Plateforme utilisée : Google Teachable Machine (Image Project)
Lien du modèle : https://teachablemachine.withgoogle.com/models/FhBkEPSXt/
Objectif
Entraîner un modèle d'intelligence artificielle capable de reconnaître en direct deux objets différents grâce à la webcam, sans écrire une seule ligne de code.
Démarche
J'ai créé un Image Project avec deux classes. La première, Me, contient 30 images de mon visage. La seconde, Bottle, contient 54 images d'une bouteille de boisson tenue devant la caméra sous différents angles. J'ai ensuite lancé l'entraînement avec le bouton Train Model, puis activé la webcam dans l'aperçu pour tester le modèle en temps réel.
Résultat
Le modèle distingue correctement les deux classes. Quand la bouteille apparaît devant la caméra, la barre Bottle monte à 100 %. Quand mon visage revient dans l'image, c'est la barre Me qui passe à 100 %.
![Reconnaissance de la bouteille](captures/reconnaissance-bottle.png)
![Reconnaissance de mon visage](captures/reconnaissance-me.png)
Ce qui s'est passé pendant l'entraînement
Teachable Machine ne part pas de zéro. Il s'appuie sur un réseau de neurones déjà entraîné à reconnaître des formes visuelles générales, puis l'ajuste avec mes propres images pour qu'il apprenne à séparer mes deux classes. À chaque passage sur les échantillons, le modèle compare sa prédiction à la bonne étiquette et corrige ses paramètres pour réduire l'erreur. C'est exactement le principe vu en cours : l'IA n'a pas de règles écrites à la main, elle apprend à partir des exemples qu'on lui donne.
Difficultés rencontrées et enseignements
Mes photos ont été prises dans une pièce peu éclairée, ce qui rend les images sombres et moins nettes. Le modèle a quand même bien fonctionné, mais j'ai compris que la qualité des données compte autant que leur quantité. Avec une meilleure lumière et un arrière-plan plus varié, le modèle serait plus fiable. J'ai aussi remarqué que les deux classes n'ont pas le même nombre d'échantillons (30 contre 54), ce qui peut légèrement favoriser la classe la mieux fournie. Un jeu de données équilibré serait préférable pour un usage réel.
Contenu du dossier
`README.md` : cette présentation
`captures/` : captures d'écran du modèle entraîné et du test en direct
`lien-modele.txt` : lien vers le modèle hébergé sur Teachable Machine
