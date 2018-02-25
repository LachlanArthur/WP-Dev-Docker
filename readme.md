# Superfast WordPress Dev Env in Docker

- Alpine
- Nginx
- PHP7.2
- MariaDB

## Instructions

0. Install [Docker](https://www.docker.com/get-docker)
1. Clone this repo somewhere
2. Change the domain in the `.env` file (eg. `"SITE=wp.test"`)
3. Start the containers with `docker-compose up -d`
5. Wait a few seconds for WordPress to be installed in `./wp` (this can be configured in `.env`)
4. Add the domain to your hosts file (eg. `"127.0.0.1 wp.test"`)
6. Check out your new site at `wp.test`

## Multiple Sites

This super-simple config only supports one site.  
But that's ok, just make another clone of this repo in a new folder.

Each site needs its own port to bind to, so change the port in the `.env` file (eg. `"PORT=8001"`).  

For example, you could have the sites `wp1.test:8001` and `wp2.test:8002`

## Todo

- Override PHP image script to install extra stuff, like XDebug
- Add option to skip WordPress installation

---

PS: Don't use this in production!
