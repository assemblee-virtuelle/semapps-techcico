[![SemApps](https://badgen.net/badge/Powered%20by/SemApps/28CDFB)](https://semapps.org)

# SemApps instance for Tech-CICO (UTT)

## Initial setup

### Install Docker

Install Docker engine:
https://docs.docker.com/engine/install/

Configure Docker user as root:
https://docs.docker.com/engine/install/linux-postinstall/#manage-docker-as-a-non-root-user

Install Docker-compose:
https://docs.docker.com/compose/install/

### Clone this repo

```
git clone https://github.com/assemblee-virtuelle/semapps-techcico.git
```

### Build the containers

```
cd semapps-techcico
docker-compose build
```

## Maintenance

### Upgrade the middleware

```
docker-compose build middleware
docker-compose up -d
```

> Note: A new version of the middleware is built only if a change in the selected Git branch is detected.

### Access the middleware REPL

```
docker exec -it middleware pm2 attach 0
```

### Follow the logs

```
docker exec -it middleware pm2 logs
```
