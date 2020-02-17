# Docker Development Environment

## Usage

Create a new environment file and name the project:

    cp .env.default .env

## TODO

General:

- composer; use `php -d memory_limit=-1 /usr/bin/composer`
- xdebug?
- Permissions so that apache can write to files
- Connect mailhog by default

`docker-compose.yml`:

- Add varnish
- Add memcache
- Add solr
- Add nginx as an alternative to Apache?
- Add MariaDB as an alternative to MySQL?
