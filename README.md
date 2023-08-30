# Workshop

## Working with Docker compose

MySQL
```
$docker compose up -d
$docker compose ps 
$docker compose logs --follow
$docker compose down
```

## Read data from environment variables
docker-compose.yml
```
web:
    #docker image build -t demo:3.0 .
    image: demo:3.0
    environment:
      - PAYMENT_ENDPOINT=${URL:-http://dev.demo.com}
```

Run
```
$export URL=http://www.google.com
$docker compose up -d web
```