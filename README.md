
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
symfony new app --webapp
mv ./app/.env* ./
mv ./app/.gitignore ./
mv ./app/* ./
```

If you need a database, modify the .env file like this example:

```yaml
DATABASE_URL="mysql://user:password@127.0.0.1:3306/database?serverVersion=5.7&charset=utf8mb4"
```
