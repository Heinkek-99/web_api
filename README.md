# web_api

API Symfony pour la gestion de données métier. Elle sert de socle : entités Doctrine, migrations,
authentification et rendu de pages.

## Contenu

- `src/` : contrôleurs, entités et logique applicative
- `templates/` : vues Twig
- `config/` : configuration Symfony (doctrine, sécurité, mailer, messenger, cache)
- `migrations/` : migrations Doctrine
- `compose.yaml` et `compose.override.yaml` : PostgreSQL 16 et services associés
- `assets/` : JavaScript et CSS via AssetMapper

## Stack

PHP 8.2 et plus, Symfony 7.2, Doctrine ORM 3, PostgreSQL 16, Twig, AssetMapper, Nelmio CORS,
PHPUnit, Docker Compose.

## Lancer le projet

```bash
composer install
docker compose up -d
php bin/console doctrine:migrations:migrate
php -S localhost:8000 -t public
```

## Avertissement

Le fichier `.env` est présent dans le dépôt. Il doit sortir du suivi de version et les valeurs
qu'il contient doivent être remplacées avant toute mise en ligne.
