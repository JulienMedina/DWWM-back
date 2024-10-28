# projet-14-o-last-back
# O'Last - Backend

O'Last est une API RESTful développée avec Node.js et Express, destinée à connecter les joueurs en ligne à travers un système de gestion d’annonces et de profils de jeu. Ce dépôt contient le code back-end de l'application, construit pour fournir une API sécurisée et performante, avec une base de données relationnelle gérée sous PostgreSQL.

## 🚀 Technologies utilisées
![Node.js](https://img.shields.io/badge/-Node.js-339933?logo=node.js&logoColor=white&style=for-the-badge) 
![Express.js](https://img.shields.io/badge/-Express.js-000000?logo=express&logoColor=white&style=for-the-badge)
![PostgreSQL](https://img.shields.io/badge/-PostgreSQL-4169E1?logo=postgresql&logoColor=white&style=for-the-badge)
![Docker](https://img.shields.io/badge/-Docker-2496ED?logo=docker&logoColor=white&style=for-the-badge)
![Sqitch](https://img.shields.io/badge/-Sqitch-E0A030?logo=data&logoColor=white&style=for-the-badge)

## 🌟 Fonctionnalités principales de l'API
- **Gestion des utilisateurs** : CRUD complet pour les utilisateurs et profils, avec vérification par email unique et stockage sécurisé des mots de passe (bcrypt).
- **Gestion des annonces** : Création, lecture, mise à jour et suppression d’annonces de jeu, avec des filtres par critères (jeux, âge, plateforme, etc.).
- **Système de notation** : Les utilisateurs peuvent noter et laisser des avis sur leurs partenaires de jeu pour renforcer la fiabilité de la communauté.
- **Recherche et filtrage avancés** : Filtrage des annonces par âge, type de jeu, et autres critères pour faciliter les recherches.

## 🔐 Sécurité
- **JWT et Cookies** : Authentification sécurisée des utilisateurs via JSON Web Tokens (JWT) et cookies pour le maintien de sessions.
- **Validation des données** : Utilisation de Joi pour garantir que toutes les entrées utilisateur sont valides, sécurisées et conformes aux exigences.
- **CORS** : Paramétrage des en-têtes CORS pour sécuriser les appels API depuis le front-end.

## ⚙️ Architecture 
Une architecture a été mises en place afin de faciliter la gestion et la maintenance du projet :

controllers : Contient la logique métier de l'application
models : gère les requêtes SQL vers la base de données
middlewares : gère les différentes vérifications concernant la sécurité de l'application
routes : Définit les routes et points de terminaison de l'API

## 🗂️ Base de données
La base de données relationnelle est structurée en entités principales, notamment `User`, `Profile`, `Game`, `Post`, et `Rate`. Chaque entité a des relations et des contraintes spécifiques pour garantir l’intégrité et la cohérence des données.

- **Migration** : Sqitch est utilisé pour versionner et gérer les migrations de la base de données, assurant ainsi une transition structurée entre les versions.

## 🛠️ Installation et Lancement
Pour exécuter le projet en local avec Docker :

```bash
# Cloner le dépôt
git clone https://github.com/ton-compte/olast-backend.git

# Lancer les conteneurs avec Docker Compose
docker-compose up

# Accéder à l'application
npm start
