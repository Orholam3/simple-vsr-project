# Projet VSR - Reconnaissance Visuelle de la Parole 

Système de reconnaissance visuelle pour les mots français : "oui", "non", "un", "deux"
Système peu efficace, mauvaise détection.
Je n'ai testé que très légèrement les méthodes par manque de temps, notamment pour l'augmentation du jeu de données.
Je pense que la qualité des données d'entraînement est médiocre et surtout que les mots choisis ont des phonèmes très proches.
La principale difficulté réside dans la distinction visuelle entre ces mots, particulièrement "deux"/"non" où les mouvements labiaux sont similaires. J'ai utilisé un réseau CNN+LSTM pour capturer les caractéristiques spatiotemporelles des vidéos, mais les résultats restent insatisfaisants avec une précision mauvaise, une très mauvaise sensibilité. 
Les problèmes identifiés sont:

Jeu de données trop limité (seulement 10 vidéos par classe)
Variabilité insuffisante des locuteurs (1 personnes)
Conditions d'éclairage non standardisées, webcam ordinateur faible résolution.
Prétraitement inadéquat des régions labiales

Pour améliorer le modèle, il faudrait:

Enrichir le dataset avec plus de vidéos et de locuteurs
Implémenter des techniques d'augmentation (rotation, zoom, variations de luminosité)
Utiliser un modèle d'attention pour se concentrer sur les régions labiales significatives
Tester avec des mots visuellement plus distincts pour valider l'approche

Ce travail n'a pas pour but d'aboutir mais de m'avoir permis de tester un fonctionnement de VSR. Malgré les résultats peu concluants, j'ai pu me familiariser avec les concepts fondamentaux de la reconnaissance visuelle de la parole et comprendre les défis techniques associés. L'extraction des caractéristiques labiales et la séquence temporelle des mouvements constituent les points critiques à améliorer.
