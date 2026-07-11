QuickChange  - Projet 3 : Intégration de la Base de Données
 Présentation du Projet

Cette étape est dédiée à la Persistance d'État. L'objectif était de connecter notre API backend à une base de données relationnelle permanente pour stocker chaque conversion et concevoir un coffre-fort numérique fiable.
🛠️ Technologies Utilisées

    MySQL / phpMyAdmin : Stockage relationnel des données de conversion.

    mysql2 : Pilote natif Node.js pour exécuter les requêtes SQL.

 Sécurité & Intégrité des Données

    Contre les Injections SQL : Utilisation stricte de requêtes paramétrées (?) pour séparer la logique SQL des entrées utilisateurs.

    Validation Server-Side : Les montants négatifs ou invalides sont bloqués avec un statut HTTP 400 Bad Request.

 Structure de la Base de Données

Le schéma complet est disponible dans le fichier conversions.sql :

    id : Clé primaire unique (Auto-incrémentée).

    amount, result : Types numériques précis (DECIMAL(10,2)).

    created_at : Horodatage automatique de l'action.

 Processus pour Lancer le Projet

    Importez le fichier conversions.sql dans votre instance phpMyAdmin locale pour configurer la base de données decodelabs_db.

    Ouvrez votre terminal dans le dossier racine et installez les modules nécessaires :
    Bash

    npm install

    Démarrez le serveur connecté à MySQL :
    Bash

    npm start

    Ouvrez le fichier index.html dans votre navigateur pour tester l'enregistrement persistant.
