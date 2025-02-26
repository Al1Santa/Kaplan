# Création d'un projet skeleton (projet minimum)

```bash
composer create-project symfony/skeleton kaplan
```

On déplace les fichier du sous-dossier du projet, puis on supprime le sous-dossier

```bash
mv kaplan/* kaplan/.* .
```

## Lancer le projet

On utilise `php -S` pour ne pas être dépendant d'un serveur web

```bash
php -S 0.0.0.0:8080 -t public
```

## Création d'une route/controller

Pour pouvoir utiliser les annotations et que symfony les lise

```bash
composer require annotations
```

### cache:clear

Si j'ai une erreur `Script cache:clear returned with error code 1`

Bine lire les messages, il s'agit probablement de nom de fichier/nom de classe qui ne corresponde pas.

`Case mismatch between loaded and declared class names:`

Pour vérifier que tout est bon

```bash
bin/console cache:clear
```

## debug des routes

Pour voir la liste de toutes les routes du projet

```bash
 bin/console debug:router
```

on peut donc donner un nom à notre route

```php
/* @Route("/", name="default_page")
```

## Installation twig

```bash
composer require twig
```

# Connection BDD en local

Dans .env.local ajouter : 

```bash
DATABASE_URL="mysql://adminer:adminer@127.0.0.1:3306/adminer_spectacle?serverVersion=5.7&charset=utf8mb4"
```

## debug / profiler

```bash
composer require --dev symfony/profiler-pack
```

Var_dumper + gestion des dump dans la toolbar

```bash
composer require --dev symfony/var-dumper
composer require --dev symfony/debug-bundle
```

## Gestion des assets et de leur inclusion

```bash
composer require symfony/asset
```

## maker

```bash
composer require --dev symfony/maker-bundle
```

```text
          
 [ERROR] Missing package: to use the make:controller command, run:                    
                                                                                      
         composer require doctrine/annotations                                        

```


## make:controller

```bash
bin/console make:controller
```

```bash
bin/console m:cont
```
