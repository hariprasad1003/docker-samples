## Exercise - 

To Connect a Node.js Application Container and Mongo Container

### Run using compose

```
docker-compose up 
```

### If made any changes, build container
```
docker-compose up --build
```

### Connecting MongoDB URL

```
mongodb://localhost:27017

or

mongodb://mongo:27017

```

### Using env 

```

Method 1 - .env

.env 

CONTAINER_NAME="mongo"

docker-compose.yml

    environment:
        - CONTAINER_NAME

Method 2 - Compose environment

    environment:
        - CONTAINER_NAME=mongo

Method 3 - Using .env with compose

.env 

CONTAINER_NAME="mongo"

    environment:
        - CONTAINER_NAME=${CONTAINER_NAME}

```

### List env file

```
docker-compose run web env
```