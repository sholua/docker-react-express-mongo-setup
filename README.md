# Multi container application
Make sure that docker and docker-compose are installed on your computer

## Development flow
Run frontend and backend servers in containers with command:
```bash
docker-compose up -d
```

Run app in containers and rebuild images:
```bash
docker-compose up -d --build
```
### Request in development
**frontend** http://localhost:3000
**backend** http://localhost:3000/api/

## Production flow
```bash
docker-compose -f docker-compose.yml up -d --build
```

This project needs a file **.env** with environment variables which has to be excluded from source control:
```
MONGO_USERNAME=dbUserName
MONGO_PASSWORD=you_password
MONGO_PORT=27017
MONGO_DB=dbName
```