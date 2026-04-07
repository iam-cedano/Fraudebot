# Fraudebot

Fraudebot is a platform that helps people to search through a database data related to
known scammers on the web. It's important to note that this project is targeting to **Mexico** clients. I'm not discarding to embrace other latin american countries, this will depend on the project's reception and support.

## History

Fraudebot is being developed due to the increase on online scams advertised mostly on Facebook where customers contact with the scammers through Messenger, then the victims may post their experience and cancel the thief's account which sometimes it was stolen or using personal information from other people.

Why bothering to create a platform like this? When people have the courage to upload their experiences, their posts mostly don't have the impact that they must have. Most of the time other customers wouldn't be aware of the post if they don't explicitly search them and even when they do, Facebook's algorithm do not show them either the post do not contain the necessary inforamtion to link it with the scammer or simply just because.

It's important to note the importance of [Estafabot] (https://www.facebook.com/estafabotmx), which is/was a project with the same objectives as this one. Sadly, the project stopped being developed for unknown reasons, its web and Whatsapp Bot were removed, even its domain name was expired (which I'm thinking to buy).

## Set up the project with [Docker] (https://www.docker.com/)

I'm a big fan of Docker, so to make the process easy, I uploaded a **docker-compose** YAML file, but before you do a ```docker-compose up -d```, you have to do certain steps before:


1. Complete the .env files in the project

There are two environment files: .env.database.example and .env.php.example

```.env.database.example
MYSQL_DATABASE={database-name}
MYSQL_ROOT_PASSWORD={root-account-passsword}
MYSQL_USER={account-name}
MYSQL_PASSWORD={account-password}
```

The project runs on MySQL version 8.0.37 (as of April 2026). You have to follow the image's [guidelines] (https://hub.docker.com/_/mysql).


```.env.php.example
DB_HOST=db
DB_USER={db-user}
DB_PASSWORD={db-password}
DB_DATABASE={db-database}
DB_PORT=3306
```

These values must match with the ones you used in the database's environment file.

2. Execute ```docker-compose up -d``` to have the project running.

