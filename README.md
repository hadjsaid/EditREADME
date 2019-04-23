# EditREADME
                  Bienvenue sur le Blog DevWeb de Diallo Thierno & Kenza  Hadj Said !

#Description du projet :  http://localhost/blog3old/public/login 

DevWeb est un mini-site réalisé dans le cadre d’une formation sur le Framework LARAVEL. L’objectif, nous faire découvrir cette technologie à travers un projet concret afin que chaque participant puisse savoir y coder une application basique. Nous, notre projet est composé d’une page d’accueil, d’une page articles et d’une page contact. Ces rubriques sont dynamiques grâce à une base de données (PHPLITE) et au principe d’authentification. Pour avoir accès à l’ensemble au site, l’utilisateur ou visiteur doit préalablement créer son compte et ou s’identifier. 

#Guide d’installation Laravel: https://laravel.com/docs/5.8)

- Le début d’un projet Laravel commence par l’Installation de Composer pour la gestion des dépendances :
 - https ://getcomposer.org
- Ensuite deux manières de créer un nouveau projet sur Laravel :
- Via Laravel Installer : sur le terminal de votre repertoire, taper : composer global require laravel/installer ou Via Composer Create-Project: sur votre terminal taper : composer create-projet – prefer-dist laravel/laravel blog.

**Activer le serveur local** 
- Sur le terminal de votre projet, exécuter la commande : php artisan serve. L’URL généré http://localhost:8000 vous permettra d’afficher votre site sur le navigateur web.

#Quelques fichiers à créer et configurer lors des chacunes des implémentations : 

- routes[routes/web.php]
- controller[app/http/controller/...]
- modèles[app/modèles/..]
- vues[ressources/views/ welcome.blade.php]

#IMPLEMENTATION & FONCTIONNALITES:

Afin de personnaliser et dynamiser notre blog, nous avons réalisé quelques implémentations:

- Création d’une base de données phpLiteAdmin à l’aide des migrations de Laravel :
 https://laravel.com/docs/5.7/migrations pour créer puis configurer les tables de notre base de données : articles(post),  contacts et  utilisateurs. 
Exemple de commande sur le terminal : php artisan migrate & php artisan make:migration create_contact_table –create=contact.

- Création des fichiers Seeding pour insérer des données fictives dans la BD et tester sa connexion avec le blog:
  https://laravel.com/docs/4.2/migrations 

- Commandes à exécuter sur le terminal de votre projet :
        php artisan make:seeder UsersTableSeeder par exemple pour la table des utilisateurs
        php artisan migrate
- Création et ajout d’un formulaire de contact ;
- Création puis configuration des fichiers DatatbaseSeeder.php et PostFactory.php

#Création et gestion des commentaires :
- Création de la migration pour les tables de commentaires :
   Php artisan make:migration create_comments_table
- Ajout d’un formulaire et d’un modèle (comment.php) pour permettre à l’utilisateur de poster un commentaire sur l’article de son choix.

#Identification
- Ajout d’un système d’authentification pour limiter l’accès au blog aux personnes identifiées à travers un compte. https://laravel.com/docs/5.8/authentication 
- Commande à exécuter sur le terminal du projet : php artisan make:auth  
- Configuration des fichiers «auth» et fonctions « Middleware» dans les pages du site.

#Des tests à faire : Que pouvez-vous tester sur notre blog ?

                 1- L’authentification et l’oubli des mot de passe :
**Création d’un compte de connexion pour accéder au site**

                2- L’accès au contenu des articles:
Chaque titre d’un article constitue un lien qui renvoi sur le contenu complet de l’article***

               3- Possibilité de laisser des commentaires sur chaque article
Le clic sur le titre d’un article vous renvoie sur la page complète de l’article. Et en bas de chaque article, vous avez alors la possibilité de laisser un commentaire**

               4- La page contact:
Une page contact permet aux visiteurs du site de nous contacter. Et une fois le message soumis, va s’afficher la liste de toutes les personnes qui nous ont déjà écrit. ***

A rappeler que chacune des actions d’un utilisateur constitue un enregistrement de plus dans notre BD du blog. Par exemple, si quelqu’un nous soumet un message à travers le formulaire de contact, son nom, adresse mail et message s’enregistrent automatiquement sur notre Bases de données.
