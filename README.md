README – Projet Fil Rouge
Projet Fil Rouge – Cahier de Dettes d’une Boutique

Application Symfony permettant à une boutique de gérer les dettes de ses clients. Elle intègre plusieurs rôles utilisateurs (Admin, Boutiquier, Client) et permet un suivi complet des articles, paiements et dettes contractées.

Technologies utilisées
- Symfony 7.2.x
- PHP 8.2
- Tailwind CSS (via Webpack Encore)
- Twig (pour le rendu serveur)
- Doctrine ORM
- StimulusJS (optionnel pour interactivité)
- PostgreSQL (ou MySQL selon configuration)

Fonctionnalités principales

Gestion des rôles

Admin
- Créer des comptes (Admin ou Boutiquier)
- Activer/désactiver des comptes
- Gérer les articles (stock, création, modification)
- Archiver les dettes soldées

Boutiquier
- Créer et lister des clients (avec ou sans compte utilisateur)
- Enregistrer une dette pour un client (avec articles, paiements partiels)
- Lister les dettes non soldées
- Gérer les demandes de dette (validation/refus)

Client
- Voir ses dettes non soldées
- Faire une demande de dette
- Relancer une demande annulée

Structure du projet

Le projet est organisé par modules métiers :
src/
├── Client/
├── Dette/
├── Paiement/
├── Article/
├── Security/
├── Controller/
└── Form/

Installation du projet

1. Cloner le dépôt
git clone https://github.com/ton-utilisateur/nom-du-projet.git
cd nom-du-projet

2. Installer les dépendances PHP
composer install

3. Installer les dépendances front-end
npm install

4. Configurer Tailwind CSS avec Webpack Encore
npm run dev # Ou npm run watch pour surveiller les changements

5. Configurer la base de données
Créer le fichier .env.local et y définir les identifiants :
DATABASE_URL="postgresql://user:password@localhost:5432/ma_bdd"

Puis exécuter les commandes :
php bin/console doctrine:database:create
php bin/console doctrine:migrations:migrate
php bin/console doctrine:fixtures:load

6. Lancer le serveur local
symfony server:start

Captures d’écran (à ajouter)
- Formulaire de création de client
- Liste des dettes
- Interface Admin

À venir
- Amélioration UX avec Stimulus
- API REST ou GraphQL (phase 2)
- Gestion des notifications (relances, alertes)

Auteur
Projet réalisé par Ton Nom dans le cadre du projet Fil Rouge — Formation Développeur Web.

Licence
Ce projet est open-source et publié sous licence MIT.
