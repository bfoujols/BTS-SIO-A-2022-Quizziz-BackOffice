![separe](https://github.com/studoo-app/.github/blob/main/profile/studoo-banner-logo.png)
# APP WEB ARCHI MVC
[![Codacy Badge](https://app.codacy.com/project/badge/Grade/df1ed0cf2b5a46e68a822e674ca8e671)](https://www.codacy.com/gh/bfoujols/BTS-SIO-Web-Archi-MVC/dashboard?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=bfoujols/manage-student-cli&amp;utm_campaign=Badge_Grade)
![CI](https://github.com/bfoujols/BTS-SIO-Web-Archi-MVC/actions/workflows/codacy.yml/badge.svg)
![CI](https://github.com/bfoujols/BTS-SIO-Web-Archi-MVC/actions/workflows/testing.yml/badge.svg)

Voici une proposition d'architecture MVC pour l'élaboration d'un projet ou de TP en cours \
L'objectif pédagogique est :
- Appréhender un projet par couche via MVC
- Faire un projet "full POO" et dans les "best practices" attendu par les entreprises
- Orchestrer via un gestionnaire de package (composer)
- Développement de test unitaire
- Début d'approche pour l'enseignement d'une framework (symfony, slim, Laravel ...)

Cible :
- Première année / 2e semestre
- Deuxième année / 1re semestre

## SETUP PROJET

### 1. Fork du projet 
Installation du projet se fait via les outils composer et git. \
Dans un premier temps, il faut faire un fork du repository sur votre espace de travail
Puis cloner le projet sur votre machine

### 2. Fichier de configuration
Une fois que la commande "git clone" est effectué, vous devez créer votre fichier de configuration projet (dotenv) \
Ce fichier doit s'appeler ".env", vous pouvez partir du fichier exemple nommé ".env-exemple"

````shell
cp .env-exemple .env
````

### 3. Installation des librairies
La prochaine étape concerne l'installation des librairies du projet. Cette installation se fait par l'outil "composer". \
Composer est un gestionnaire de package. Son utilité est assurée la compatibilité et l'installation entre les différentes versions de librairie.

````shell
composer install
````

### 4. Installation de la base de donnée
La base de donnée est un fichier sql. Elle se trouve dans le répertoire "docs/bddqcm.sql" 

### 5. Démarrage du projet
Demarrer ton projet
````shell
$ composer start
````
______

### DEV PROJET
En cas de création ou de mise a jour des classes du projet, faire la commande de autoloader
````shell
$ composer dump-autoload 
````

#### DEV STACK
| Version | Service                                                             | DESCRIPTION                      |
|:--------|:--------------------------------------------------------------------|:---------------------------------|
| ^5.5    | [vlucas/phpdotenv](https://packagist.org/packages/vlucas/phpdotenv) | Loads environment variables      |
| ^3.5    | [twig/twig](https://packagist.org/packages/twig/twig)               | Template Engine (VIEW couch)     |
| ^1.3    | [nikic/fast-route](https://packagist.org/packages/nikic/fast-route) | Router Engine (CONTROLLER couch) |
| ^8.0    | [PHP Engine](https://www.php.net/downloads.php)                     | Engine PHP                       |  
| ^2.0    | [Composer](https://getcomposer.org/download/)                       | Dependency Manager               | 
| ^9.5    | [PHPUnit](https://phpunit.de/)                                      | Testing Engine                   |

______
### TESTING
Les tests unitaires sont réalisés via PHPUnit. 

```shell
composer test
```
