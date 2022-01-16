# Projet 6 - OpenClassrooms
Parcours Data Science

Projet n°6 : "Classifiez automatiquement des biens de consommation"

- Source des données (direct download) : https://s3-eu-west-1.amazonaws.com/static.oc-static.com/prod/courses/files/Parcours_data_scientist/Projet+-+Textimage+DAS+V2/Dataset+projet+pre%CC%81traitement+textes+images.zip

## Introduction du projet
La plateforme de e-commerce "Place de marché" souhaite développer un outil de classification automatique des produits mis en vente par ses vendeurs. Jusqu'à présent les vendeurs renseignaient manuellement la catégorie à laquelle appartient le produit mis en ligne, ce qui en fait une classification peu fiable et peu efficace pour l'utilisateur. En vue d'un passage à l'échelle il devient nécessaire d'automatiser cette tâche.

En se basant sur les données texte (description de l'objet) et des données images (photo de l'objet), un modèle de classification automatique est proposé.

**Conclusions: **
- Données texte: taux de classification de 93% sur les descriptions objets
- Données images: taux de classification de 80% via transfer learning sur le réseau de neurones pré-entraîné *mobilenet v2*

## Travail réalisé
- Données texte (NLP):
  - nettoyage du texte (passage en minuscules, nettoyage pnctuation, suppression des stop words)
  - fonction de racination (stemmer) ou lématisation (lemmer)
  - tokenisation du texte
  - feature extraction
  - réduction de dimensions SVD (décomposition en valeurs singulières)
  - clustering K-Means
- Données images:
  - resizing
  - égalisation de l'histogramme
  - création des descripteurs
  - clustering sur les descripteurs
  - réduction de dimensions ACP
  - réduction de dimensions t-SNE et visualisation 2D des clusters
  - transfer learning sur réseau de neurones convolutionnels pré-entraînés:
    - VGG16
    - mobilenet v2

## Compétences évaluées
- Représenter graphiquement des données à grandes dimensions
- Mettre en œuvre des techniques de réduction de dimension
- Prétraiter des données texte pour obtenir un jeu de données exploitable
- Prétraiter des données image pour obtenir un jeu de données exploitable
