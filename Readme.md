# MongoDB ReplicaSet on Docker

![mongo logo](https://upload.wikimedia.org/wikipedia/commons/thumb/9/93/MongoDB_Logo.svg/2560px-MongoDB_Logo.svg.png)
Hello,

This small repository is only for simplify your life if you to need run a mongo db cluster on your localhost

## Setup

Probably you will to customize this files with your project and to run this service you need run a `docker-compose` with a little extra command:

```
docker-compose up --build -d --remove-orphans; sleep 5;  docker exec mongodb1 /scripts/rs-init.sh
```

I would like improve this and simplify without extra command, but I didn't make yet. So you need run the docker-compose, wait for 5 seconds (to container up) and to call the replica set script.

To manage the database I like to use the Mongo Compass, maybe you can want to use as well:

https://www.mongodb.com/try/download/compass

## Improve the repository

Feel free if you want improve something and send a PR :)

Exemple about what we can improve right now:

1. Simplify the command to up - Find some way to run the rs-init automatically;
2. Upgrade to the last mongodb version;
