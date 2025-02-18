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

### Was ist Redis
Redis ist eine In-Memory-Datenbank und ein Key-Value Store, der extrem schnelle Datenzugriffe ermöglicht. Es wird oft als Cache, Message Broker oder NoSQL-Datenbank genutzt und unterstützt Datenpersistenz, Skalierung und Pub/Sub-Kommunikation.

### Welche Ports werden genutzt?
8000 und 5000

### Was ist die Bedeutung von ENV im DOCKERFILE?
Das `ENV`-Kommando im **Dockerfile** setzt **Umgebungsvariablen**, die während der Laufzeit im Container verfügbar sind. Diese können für Konfigurationen, Pfade oder Zugangsdaten genutzt werden.

## **Beispiel**  
```dockerfile
ENV APP_ENV=production
```