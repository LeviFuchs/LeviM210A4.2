# LeviM210A4.2

### Set Github Login

1. Set a variable with your Github token

```html
export CR_PAT=<Github_Token>
```

2. Login to Github with your personal token

```html
echo $CR_PAT | docker login ghcr.io -u <githubusername> --password-stdin
```

### Set Docker Platform (for ARM)

1. Set a Docker Platform ARCH from ARM to AMD64

```html
export DOCKER_DEFAULT_PLATFORM=linux/amd64
```

### Docker Compose

1. Start

```html
docker-compose -p python-web up --build -d
```

2. Stop

```html
docker-compose -p python-web down
```

3. Delete

```html
docker image prune -a
docker volume prune
docker network prune
docker system prune -a --volumes
```