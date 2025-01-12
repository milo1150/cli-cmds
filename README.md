# Docker

- Force Logs to Be Visible and other examples

```bash
docker-compose build --no-cache --progress=plain
```

```bash
RUN echo "Checking watchexec version..." && watchexec --version && echo "Done checking watchexec version."
```

- To debug further, override the CMD and start a shell to run commands manually

```bash
docker-compose run --rm server sh
```

- Check OS Architecture
  
```bash
  uname -m
```

- if Docker & Postgres: Failed to bind tcp 0.0.0.0:5432 address already in use

``` bash
sudo lsof -i :5432
```

``` bash
sudo kill -9 <PID>
```

- Build specific image

```bash
 docker-compose -f deployments/docker-compose.production.yml up --build
```

- Remove xxx stuff

```bash
 docker image prune -a
```
```bash
 docker builder prune -a
```
```bash
 docker container prune -a
```

- Remove All Images Built by Docker Compose

```bash
docker-compose down --rmi all -v
```

--rmi all: Removes all images built by docker-compose. \
-v: Also removes volumes associated with the containers.

- Show docker disk usage
```bash
docker system df
```

# DB

- pgcli [Documentation](https://github.com/dbcli/pgcli)

``` bash
 pgcli postgres://postgres:postgres@0.0.0.0:5432/mydb
```

- mycli [Documentation](https://github.com/dbcli/mycli)

``` bash
 pgcli postgres://postgres:postgres@127.0.0.1:5432/mydb
```

# Python

- Change Poetry python version

```bash
pyenv install 3.11.11
```

```bash
pyenv local 3.11.11
```

```bash
poetry env use $(pyenv which python)
```

```bash
poetry run python --version
```

# Git

- Untrack file if init .gitignore in later project 

```bash
git rm -r --cached tmp
git rm --cached .env
```


