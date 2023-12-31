# Start local Redis and Redis Insight client

### When `docker-compose.yml` is in the root folder

```bash
docker-compose up
```

### When `docker-compose.yml` is in the nested folders

```bash
docker-compose -f ./redis/docker-compose.yml up
```

# Access Redis Insight dashboard

- Go to `http://localhost:8001` to access the Redis Insight.
- Accept the necessary T&Cs.
- Click on **"I already have a database"**
- Click on **"Connect to Redis database"**
- Enter the following configuration and click on **"Add Redis Database"**:

  <img src="./redis-config.png"/>

  - We have used `redis` as a `Host` because the `Redis Insight` container is also running on the docker, in the same network as the `redis` container.

  - So, to access a services in the same network, we use their name as the `Host`. So, that's why we used `redis` (name of the service for redis container in the `docker-compose.yml` file)

- You are connected to the Redis database!

# `Set` and `Get` a key in the Redis

Now that you are connected to the Redis database through Redis Insight, let's set and get a key.

After connecting to the redis. Refer to the following video as a guide:

<video controls autoplay>
  <source src="https://github.com/hiteshchoudhary/docker-databases/blob/main/redis/redis-insight-guide.mov">
</video>

Now, you have a running redis instance!