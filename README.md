# TIC-SYS2

Projet d'hébergement web réalisé par YACEF Souleyman et EDJAMTOLI Koboyo

## Usage

Afin de démarrer le projet, exécutez le script install_docker.sh:

./install_docker.sh

## Containers

### MariaDB

Dans le Dockerfile j'ai choisi la version 10.9 de debian avec le FROM puis avec le MANTAINER j'ai choisi deployer comme utilisateur.
Puis j'installer le server mariadb avec "apt-get install -y mariadb-server" et défini le 3306 avec EXPOSE 3306 et j'ai fini avec CMD ["mysqld_safe"] .

Dans le docker-compose.yml j'ai crée un service à partir du dossier mariadb et j'ai crée un volume pour stocker /var/lib/mysql

### Nginx

Dans le Dockerfile j'ai installer nginx puis j'ai copié mon fichier de configuration pour que l'image le mets dans le fichier de configuration de nginx et j'ai fini avec CMD ["nginx", "-g", "daemon off;"] pour le faire passer au premier plan.

Dans le docker-compose.yml j'ai crée un service à partir du dossier nginx pour monter en mode read-only le ./nginx/static

