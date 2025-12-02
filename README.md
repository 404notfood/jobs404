# Jobs404

[![Laravel](https://img.shields.io/badge/Laravel-12.0-FF2D20?style=for-the-badge&logo=laravel&logoColor=white)](https://laravel.com)
[![Vue.js](https://img.shields.io/badge/Vue.js-3.5-4FC08D?style=for-the-badge&logo=vue.js&logoColor=white)](https://vuejs.org)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.2+-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org)
[![PHP](https://img.shields.io/badge/PHP-8.2+-777BB4?style=for-the-badge&logo=php&logoColor=white)](https://php.net)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-4.1-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://tailwindcss.com)
[![Vite](https://img.shields.io/badge/Vite-7.0-646CFF?style=for-the-badge&logo=vite&logoColor=white)](https://vitejs.dev)
[![Inertia.js](https://img.shields.io/badge/Inertia.js-2.0-9553E9?style=for-the-badge&logo=inertia&logoColor=white)](https://inertiajs.com)
[![Stripe](https://img.shields.io/badge/Stripe-635BFF?style=for-the-badge&logo=stripe&logoColor=white)](https://stripe.com)

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

Plateforme de mise en relation entre clients et freelances pour la gestion de projets. Les missions qui matchent vos besoins.

## Description

Jobs404 est une plateforme française permettant aux clients de publier des annonces de projets et aux freelances d'y répondre. Le système inclut une messagerie privée, un système d'abonnement freemium, et des crédits pour booster les annonces.

## Stack technique

- **Backend** : Laravel 12
- **Admin panel** : FilamentPHP
- **Frontend** : Vue 3 avec Inertia.js
- **Styling** : TailwindCSS
- **Paiements** : Stripe via Laravel Cashier
- **Gestion documents** : Filament Curator
- **Modération** : Filament Flagable
- **Permissions** : Filament Shield
- **Historique** : Filament Activitylog

## Fonctionnalités principales

### Pour les clients

- Publication d'annonces avec description, documents et fourchette tarifaire
- Réception de propositions de freelances
- Messagerie privée avec les freelances intéressés
- Abonnement gratuit (4 annonces par mois) ou payant (illimité)
- Système de boost pour mettre en avant les annonces

### Pour les freelances

- Consultation des annonces publiées
- Envoi de propositions aux clients
- Messagerie privée avec les clients
- Dashboard avec historique des annonces et crédits disponibles
- Achat de crédits pour booster les annonces

### Modération

- Panel d'administration via FilamentPHP
- Système de signalement et modération des annonces
- Vérification des reposts
- Expiration automatique des annonces sans réponse (7 jours)

## Modèles de données

### User
Gestion des utilisateurs (clients et freelances) avec abonnement, crédits et informations de profil.

### Project
Annonces de projets avec titre, description, documents, fourchette tarifaire et statut.

### Proposal
Réponses des freelances aux annonces. Le contenu est visible uniquement par le propriétaire de l'annonce.

### Message
Messagerie privée entre clients et freelances, liée aux propositions.

### Boosts
Système de mise en avant des annonces avec limite de 4 boosts par annonce.

### Payments
Gestion des transactions Stripe pour abonnements et crédits.

## Abonnement et crédits

### Abonnement
- **Gratuit** : 4 annonces par mois
- **Payant** : annonces illimitées, 15-20€/mois

### Crédits pour boosts
- 5 crédits : 5€
- 10 crédits : 8€
- 1 boost = 1 crédit
- Maximum 4 boosts par annonce

## Design

Le design suit un système de couleurs cohérent avec support du mode clair et sombre. La palette principale utilise le bleu (#3B82F6) comme couleur d'accent. La typographie utilise Inter pour une lisibilité optimale.

## Installation

```bash
# Cloner le projet
git clone [url-du-repo]

# Installer les dépendances PHP
composer install

# Installer les dépendances Node
npm install

# Copier le fichier d'environnement
cp .env.example .env

# Générer la clé d'application
php artisan key:generate

# Configurer la base de données dans .env
# Puis exécuter les migrations
php artisan migrate

# Compiler les assets
npm run build
```

## Configuration

### Variables d'environnement importantes

- `STRIPE_KEY` : Clé publique Stripe
- `STRIPE_SECRET` : Clé secrète Stripe
- `STRIPE_WEBHOOK_SECRET` : Secret pour les webhooks Stripe
- `APP_URL` : URL de l'application

### Configuration Stripe

Le projet utilise Laravel Cashier pour la gestion des paiements. Assurez-vous de configurer correctement les webhooks Stripe pour gérer les événements d'abonnement.

## Développement

```bash
# Démarrer le serveur de développement
php artisan serve

# Compiler les assets en mode watch
npm run dev
```

## Roadmap

### MVP
- Création et gestion des annonces
- Système de propositions
- Messagerie asynchrone
- Modération de base
- Abonnements free/paid
- Système de crédits et boosts
- SEO de base

### Second jet
- Éditeur WYSIWYG
- Preview instantanée
- Badges et labels
- Analytics avancées
- Recherche et filtres avancés
- Gamification (notations, avis, classements)
- Notifications email et dashboard
- Optimisation SEO complète

## SEO

Le projet intègre plusieurs optimisations SEO :
- Balises meta uniques par page
- URLs propres avec slugs
- Sitemap.xml et robots.txt
- OpenGraph et Twitter Cards
- Contenu structuré JSON-LD
- Lazy-loading des images
- Design responsive mobile-first

## Licence

