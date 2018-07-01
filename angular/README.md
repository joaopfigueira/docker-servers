# Docker Angular development environment

## Instructions:

### 1. Name your new project
open `.env` file and edit `ANGULARPROJECTNAME` variable. That will be the name of the folder your new angular project will live in.

### 2. Create the new project
Make sure you are in the same folder of `docker-compose.yml` and:
```sh
$ docker-compose run --rm angular-dev install.sh
```

### 3. Serve your project
Make sure you are in the same folder of `docker-compose.yml` and:
```sh
$ docker-compose run --rm --service-ports angular-dev serve.sh
```
Your project will be available on `http://localhost:4200`

### 4. Enjoy

## Notes:
- `node_modules` are stored on a volume outside your host filesystem.
