# docker-lamp(PHP:7.4-Apache/MariaDB:latest/phpMyAdmin)

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
