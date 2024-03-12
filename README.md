# Docker Compose for PrestaShop and MySQL

This repository contains a `docker-compose.yml` file that sets up a PrestaShop and MySQL environment using Docker Compose.

## Services

The `docker-compose.yml` file defines the following services:

`mysql`: This service uses the mysql:5.7 image and is named some-mysql.

`prestashop`: This service uses the latest stable version of the prestashop/prestashop image and is named prestashop. It depends on the mysql service. The PrestaShop installation is configured to connect to the `mysql` service with the database name `prestashop` and the root user credentials. The admin and install folders are named `admin4577` and `install4577` respectively.

### Credentials

```
server: some-mysql -> use it during prestahop configuration
user: root
pwd: admin
```

## Usage

To start the services, navigate to the directory containing the docker-compose.yml file and run the following command:

```
docker-compose up -d
```

To stop the services, run the following command:

```
docker-compose down
```

After starting the services, you can access the PrestaShop:

Shop: https://localhost:8080/install4577

Admin panel: https://localhost:8080/admin4577

## Note

Please ensure Docker and Docker Compose are installed on your machine before running these commands.
