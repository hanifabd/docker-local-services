# Docker Compose
Linux Terminal / Gitbash : `docker-compose up -d`<br>
List Container: `docker container ls`<br>
Inspect Container: `docker inspect <container_id>`

## Postgres Services
- PgAdmin4: `http://localhost:5050/`
- Database: `172.18.0.2`
    - username: `root`
    - password: `root`

## Ports
- "5000:3030"
- "{VPS_PORT}:{CONTAINER_PORT}"
- Notes:
    - VPS PORT - 5000
    - CONTAINER PORT - 3030

```
ports:
  - "8080:5000"

Internet → VPS:8080 → Container:5000

http://IP_VPS:8080
```

atau

```
expose:
  - "5000"

nginx → app:5000
```