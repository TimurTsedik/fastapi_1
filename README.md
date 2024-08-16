### Dockerized Advertisement Application

- **Database**: Postgres
- **API**: FastAPI

- **Containers**: [db, web]  
- **Credentials**: Stored in `.env`

### 1. Starting the Containers

docker-compose up --build -d

### 2. Creating an Advertisement

curl -X POST "http://localhost:8000/advertisements/" -H "Content-Type: application/json" -d '{
  "title": "Selling a Bicycle",
  "description": "Mountain bike in excellent condition",
  "price": 10000,
  "author": "Ivan Ivanov"
}'

### 3. Retrieving an Advertisement by ID

curl -X GET "http://localhost:8000/advertisements/1"

### 4. Updating an Advertisement by ID

curl -X PATCH "http://localhost:8000/advertisements/1" -H "Content-Type: application/json" -d '{
  "price": 9000
}'

### 5. Deleting an Advertisement by ID

curl -X DELETE "http://localhost:8000/advertisements/1"

### 6. Viewing the Documentation

http://localhost:8000/docs
