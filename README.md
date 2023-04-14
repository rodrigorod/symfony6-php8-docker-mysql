
# Symfony 6 + PHP 8 + Docker + MySQL

## Run Locally

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
DATABASE_URL="mysql://user:password@127.0.0.1:3306/database?serverVersion=5.7&charset=utf8mb4"
```
