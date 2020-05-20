# Architecture

![architecture](./arch.png)

# Inspection

## Redis

- `docker exec -it b922 redis-cli`
- `hgetall seen`

## Postgresql

- `docker exec -it <id> psql -U postgres`
- `select * from seen;`

## AWS Deployment

- Dockerrun.aws.json has container definitions for multi-container setup.
- https://docs.aws.amazon.com/AmazonECS/latest/userguide/task_definition_parameters.html
- hostname - what containers look at to communicate with eachother
  - specified in `docker-compose.yml`
  - server was overriden in `nginx/default.conf` to `api`
