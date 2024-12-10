# Base de Données : Location de Voitures

Ce projet implémente une base de données MySQL pour la gestion d'une agence de location de voitures. Il contient les structures et données nécessaires pour gérer les voitures, les clients et les contrats de location.

## Structure de la Base de Données

### 1. Table `voiture`
Cette table contient les informations sur les voitures disponibles dans l'agence.

- **Champs** :
  - `matricule` : Identifiant unique de la voiture (clé primaire).
  - `marque` : Marque de la voiture.
  - `modele` : Modèle de la voiture.
  - `Annee` : Année de fabrication.
  - `type_carburant` : Type de carburant (Diesel, Essence, Électrique, Hybride).
  - `image_voiture` : Lien vers une image de la voiture.
  - `etat` : État de la voiture (En Parc, Sous Location).
  - `prix_location` : Prix de location par jour.

### 2. Table `client`
Cette table contient les informations des clients.

- **Champs** :
  - `client_id` : Identifiant unique du client (clé primaire).
  - `nom` : Nom du client.
  - `prenom` : Prénom du client.
  - `email` : Adresse e-mail (unique).
  - `telephone` : Numéro de téléphone.

### 3. Table `contrat`
Cette table gère les contrats de location.

- **Champs** :
  - `contrat_id` : Identifiant unique du contrat (clé primaire).
  - `voiture_id` : Identifiant de la voiture louée (clé étrangère vers `voiture`).
  - `client_id` : Identifiant du client (clé étrangère vers `client`).
  - `date_debut` : Date de début de la location.
  - `date_fin` : Date de fin de la location.
  - `Duree` : Durée de la location en jours.
