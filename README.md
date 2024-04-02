# Prédiction des Chiffres du Loto

Ce projet vise à développer un modèle d'apprentissage profond capable de prédire les numéros du loto à partir d'un historique de tirages. Nous utilisons une architecture LSTM (Long Short-Term Memory) pour traiter la séquence des tirages passés et prédire le tirage suivant.

## Dépendances

- Python 3.11
- Pandas
- NumPy
- TensorFlow

## Installation

Assurez-vous d'avoir Python installé sur votre machine. Installez ensuite les dépendances requises en exécutant la commande suivante dans votre terminal :

```bash
pip install pandas numpy tensorflow
```

## Données

Le jeu de données doit être un fichier CSV nommé `loto.csv` avec les colonnes suivantes : `date_de_tirage`, `boule_1`, `boule_2`, `boule_3`, `boule_4`, `boule_5`, `numero_chance`. Chaque ligne représente un tirage avec la date et les numéros tirés.

## Usage

Après avoir installé les dépendances et préparé le jeu de données, vous pouvez exécuter le script principal. Le script effectuera les étapes suivantes :

1. Chargement et préparation des données.
2. Transformation des données en séquences pour l'entraînement du modèle LSTM.
3. Construction et entraînement du modèle LSTM.
4. Prédiction des numéros du prochain tirage.


## Structure du Code

- Le script commence par charger le jeu de données à partir du fichier CSV.
- Les données sont nettoyées et préparées pour l'entraînement. Cela inclut la conversion des types de données et la gestion des valeurs manquantes.
- Nous construisons ensuite les séquences à partir des tirages précédents. Chaque séquence consiste en un ensemble de tirages consécutifs utilisés pour prédire le tirage suivant.
- Le modèle LSTM est défini avec une couche d'entrée correspondant au nombre de caractéristiques (nombres tirés) et une couche de sortie prédit les numéros du tirage suivant.
- Le modèle est entraîné sur les données préparées.
- Enfin, le script prédit les numéros du prochain tirage en utilisant le dernier tirage disponible.
