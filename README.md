# docker-lamp(PHP:7.4-Apache/MariaDB:latest/phpMyAdmin)

- Let's change .env file as you like.
- then execute `docker-comose up -d`

## php-apache

```bash
  docker-compose exec php-apache bash
  apach2 -t
```

- If the Syntax error occured as below,

```bash
apache2 -t
Config variable ${APACHE_RUN_DIR} is not defined
apache2: Syntax error on line 80 of /etc/apache2/apache2.conf: DefaultRuntimeDir must be a valid directory, absolute or relative to ServerRoot
```
- execute this command
```bash
source /etc/apache2/envvars
```
- When you customize the Dockerfile.

#### For instance,add an php-extention(bcmath)
```dockerfile
RUN docker-php-ext-install bcmath
```
```bash
docker-compose build --no-cache
```