# A simple docker database config for localhost

This is a simple Repo that has most used databases configured to used as localhost via docker containers.

## How to use

1. Clone the repo
2. Run the following command to start the database container

```bash
docker-compose up -d <database-compose-file-path>
```


## How to run MySQL database
```bash
docker-compose -f ./mysql/docker-compose.yml up -d 
```


## How to run PostgreSQL database
```bash
docker-compose -f ./postgresql/docker-compose.yml up -d 
```


## Access Adminer
- Go to `http://localhost:8080` to access Adminer portal.
- Enter respective credentials after selecting system as MySQL and hit login
- You are connected to a GUI and good to go now!


## How to run MongoDB database
```bash
docker-compose -f ./mongodb/docker-compose.yml up -d 
```


## How to run Redis database
```bash
docker-compose -f ./redis/docker-compose.yml up -d
```

## Access Redis Insight dashboard
- Go to `http://localhost:8001` to access the Redis Insight.
- Accept the necessary T&Cs.
- Click on `"I already have a database"`
- Click on `"Connect to Redis database"`
- Enter the following configuration and click on `"Add Redis Database":`
- We have used `redis` as a `Host` because the `Redis Insight` container is also running on the docker, in the same network as the `redis` container.
- So, to access a services in the same network, we use their name as the `Host`. So, that's why we used `redis` (name of the service for redis container in the `docker-compose.yml` file)
- You are connected to the Redis database!