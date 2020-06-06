# docker-lamp(php:7.4-apache-mysql8.0-phpmyadmin)

- Let's change .env file as you like.

- then execute `docker-comose up -d`

## php-apache

```bash
  docker-compose exec php-apache bash
  apach2 -t
```

- if the Syntax error:${APACHE_RUN_DIR} is not defined occured,

```bash
source /etc/apache2/envvars
```
