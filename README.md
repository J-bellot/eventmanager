# Eventmanager

Cette application de gestion d'événements a été développée en utilisant Symfony. Elle permet aux utilisateurs de créer, de modifier, et de supprimer des événements, ainsi que de s'inscrire à des événements. Cette documentation explique comment installer, configurer et utiliser l'application.

## Table des matières

1. [Prérequis](#prérequis)
2. [Installation](#installation)
3. [Utilisation](#utilisation)

## Prérequis

Avant de pouvoir installer et exécuter l'application, assurez-vous d'avoir les éléments suivants :

- [Composer](https://getcomposer.org/): Gestionnaire de dépendances PHP.
- [Symfony CLI](https://symfony.com/download): Outil en ligne de commande Symfony. (la dernière version de préférence)
- Une base de données MySQL (l'application a été développée avec une version 8)

## Installation

Suivez ces étapes pour installer l'application :

1. Clonez ce dépôt Git :

```
git clone https://github.com/J-bellot/EventManager.git
cd EventManager
```

2. Configurez la base de données en éditant le fichier .env avec vos paramètres de base de données.

3. Créez la base de données et appliquez les migrations :

```
symfony console doctrine:database:create
symfony console doctrine:migrations:migrate
```

4. Lancez le serveur de développement :

```
symfony serve
```

L'application devrait maintenant être accessible à l'adresse http://localhost:8000.

## Utilisation

Vous pouvez créer 3 utilisateurs :
- test qui aura ce nom, test@test.test pour adresse mail et "Azertyuiop8!" comme mot de passe
- 2 autres aux noms et identifiants aléatoires, leur mot de passe sera aussi "Azertyuiop8!"

```
symfony console doctrine:fixtures:load
```