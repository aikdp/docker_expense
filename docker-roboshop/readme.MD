1. Create mongoDB and run
```

craete docker network:
docker network create roboshop

docker build -t mongodb:v1 .
docker run -d --name mongodb --network roboshop mongodb:v1
```

2. Catalogue

```
docker build -t catalogue:v1 .
docker run -d --name catalogue --network roboshop catalogue:v1 
docker exec -it catalogue bash
curl http://localhost:8080/health
docker logs catalogue
```

3. For completion - frontend

```
docker build -t frontend:v1 .
docker run -d -p 80:80 --name frontend --network roboshop frontend:v1 
