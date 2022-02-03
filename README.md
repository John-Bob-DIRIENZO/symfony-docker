# Symfony x Docker
#### Avec MariaDB, PhpMyAdmin & MailDev

Pour lancer le projet
```shell
docker-compose up -d
docker exec symfony_docker composer create-project symfony/skeleton symfony_project
sudo chown -R $USER ./
```

Pensez ensuite à aller exécuter toutes vos commandes depuis l'intérieur
du container

Enfin, modifiez la config DB dans le fichier .env de Symfony
```dotenv
DATABASE_URL=mysql://root:ChangeMeLater@db:3306/symfony_db?serverVersion=mariadb-10.7.1
```