
# Symfony 6 + PHP 8 + Docker

## Run Locally

Clone the project

```bash
  git clone https://github.com/sylvainnicolet/symfony6-php8-docker.git
```

Run the docker-compose

```bash
docker-compose build
docker-compose up -d
```

Log into the PHP container

```bash
docker exec -it app bash
```

Create your Symfony application and launch the internal server

```bash
symfony new new-project --full
cd new-project
symfony serve -d
```

Create an account (identical to your local session)

```bash
adduser username
chown username:username -R .
```

*Your application is available at http://127.0.0.1:8000*

If you need a database, modify the .env file like this example:

```yaml
DATABASE_URL="postgresql://user:password@database:5432/app?serverVersion=13&charset=utf8"
```