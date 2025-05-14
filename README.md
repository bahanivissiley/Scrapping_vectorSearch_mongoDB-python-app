# 🎬 Movie Database with Image Embeddings and Flask  

Ce projet est une application web qui permet de gérer une base de données de films, d'analyser les images d'affiches à l'aide de modèles d'apprentissage profond et de proposer des films similaires en fonction de l'image fournie.  

## 🚀 Fonctionnalités  
- **Gestion des films** :  
  - Ajouter, modifier et supprimer des films.  
  - Afficher les détails d'un film (titre, synopsis, date de sortie, durée, langue originale, budget, revenus, genres).  
- **Recherche intelligente** :  
  - Rechercher un film par son affiche en utilisant la similarité cosinus des embeddings générés par un modèle **ResNet18**.  
- **Recommandations de films** :  
  - Trouver les films les plus similaires à une affiche téléchargée.  
- **API REST** :  
  - Récupérer les informations des films sous forme de JSON.  
  - Rechercher des films similaires via une API dédiée.  
- **Gestion des images** :  
  - Stocker les affiches de films dans **MongoDB** via **GridFS**.  
  - Générer des embeddings à partir des affiches en utilisant **PyTorch**.  

## 💻 Technologies utilisées  
- **Python** avec **Flask** pour le développement web.  
- **MongoDB** pour le stockage des données.  
- **GridFS** pour la gestion des fichiers volumineux (affiches).  
- **PyTorch** pour le traitement d'image et la génération d'embeddings.  
- **ResNet18** pour extraire des caractéristiques visuelles des affiches.  
- **HTML**, **CSS**, **JavaScript** pour l'interface utilisateur.  

## 📂 Structure du projet  
- `app.py` : Point d'entrée de l'application Flask.  
- `templates/` : Fichiers HTML pour l'interface web.  
- `static/` : Fichiers CSS et ressources statiques.  
- `movie_database/` : Base de données MongoDB pour stocker les informations des films.  
- `uploads/` : Répertoire pour les affiches de films.  

## 🌟 Fonctionnement  
1. **Ajout d'un film** :  
   - Télécharger l'affiche et saisir les informations du film.  
   - Génération d'un embedding pour l'affiche à l'aide de **ResNet18**.  
   - Enregistrement dans MongoDB avec l'image et l'embedding.  
2. **Recherche par image** :  
   - Télécharger une affiche pour rechercher des films similaires.  
   - Calcul de la similarité cosinus avec les embeddings stockés.  
   - Affichage des résultats triés par similarité.  
3. **Mise à jour/Suppression** :  
   - Modifier les informations ou remplacer l'affiche d'un film.  
   - Supprimer un film de la base de données.  

## 🛠️ Installation  
1. Cloner le dépôt :  
   ```bash
   git clone https://github.com/username/movie-database.git  
   cd movie-database
   pip install -r requirements.txt  
    mongod --dbpath /path/to/db
   python app.py  
    http://localhost:5000  

