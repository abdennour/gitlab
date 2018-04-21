# Env files

- .env
- .env.postres

Do not forget

```sh
cp .env.dist .env
cp .env.postgres.dist .env.postres
```

# Start

```sh
docker-compose up -d
```

or

```sh
make up
```


# Deploy

**Build**

```sh
TAG=$(git rev-parse --short HEAD)
IMAGE=gitlab-abdennour;

docker build -t $IMAGE:$TAG .

```

**deploy**

Replace

```yml
gitlab:
  image: myrepository/${IMAGE}:${TAG}
```
