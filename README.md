# Architecture

![architecture](./arch.png)

# Inspection

## Redis

- `docker exec -it b922 redis-cli`
- `hgetall seen`

## Postgresql

- `docker exec -it <id> psql -U postgres`
- `select * from seen;`
