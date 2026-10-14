README — DEVOIR N°6 : Robot à décision intelligente

Étudiant : Isaac Denis LAPOINTE

Cours : Robotique \& Intelligence Artificielle — EIC 3.0

Plateforme utilisée : Wokwi (https://wokwi.com)

Microcontrôleur : ESP32

Date : Octobre 2026



1\. Objectif du devoir

L'objectif de ce devoir est de concevoir un système embarqué capable de prendre une décision automatique en fonction d'un seuil mesuré par un capteur. Le système doit déclencher une action (allumer une LED) lorsque la valeur mesurée dépasse un seuil prédéfini.



2\. Composants utilisés (Simulation Wokwi)

1x ESP32 (Microcontrôleur avec Wi-Fi intégré)



1x Capteur DHT22 (Mesure de température et d'humidité)



1x LED rouge (Indicateur d'alerte)



1x Résistance (220Ω pour protéger la LED)



Fils de connexion



3\. Câblage (Pinout)

Composant	Broche ESP32	Description

DHT22 (VCC)	3V3	Alimentation

DHT22 (DATA)	GPIO 4	Lecture des données

DHT22 (GND)	GND	Masse

LED (Anode)	GPIO 2	Signal de sortie

LED (Cathode)	GND (via résistance)	Masse

4\. Logique du programme

Le code utilise la bibliothèque DHT.h pour lire la température. Le seuil d'alerte est fixé à 30.0 °C.



Initialisation : Le moniteur série et le capteur DHT sont démarrés. La LED est configurée en sortie.



Lecture : Le programme lit la température toutes les 2 secondes.



Prise de décision :



Si la température > 30.0 °C : La LED s'allume (HIGH) et le message "ALERTE : Température trop élevée !" s'affiche.



Sinon : La LED reste éteinte (LOW) et le message "Température normale" s'affiche.



Sécurité : Si le capteur renvoie une valeur invalide (isnan), un message d'erreur est affiché.



5\. Résultats de la simulation

Capture 1 (Température normale) : Lorsque la température est de -3.4 °C (ou 22.1 °C), la LED est éteinte et le moniteur série affiche "Température normale".



Capture 2 (Alerte) : Lorsque la température est réglée à 58.9 °C, la LED s'allume en rouge et le moniteur série affiche "ALERTE : Température trop élevée !".



6\. Difficultés rencontrées

Choix du capteur : J'ai initialement hésité entre un capteur de distance et un capteur de température. J'ai choisi le DHT22 car il permet de simuler facilement des variations avec le curseur dans Wokwi.



Gestion du seuil : Il a fallu s'assurer que la condition if (temperature > seuil) fonctionne correctement avec des nombres décimaux (float).



Bibliothèque : Comprendre comment inclure la bibliothèque DHT dans Wokwi a demandé quelques essais.



7\. Ce que j'ai appris

J'ai appris à utiliser un capteur numérique (DHT22) avec un ESP32 et à implémenter une logique conditionnelle simple pour déclencher une action physique (allumer une LED). C'est la base de l'automatisation et de l'Internet des Objets (IoT) : un système qui perçoit son environnement et réagit en conséquence.

