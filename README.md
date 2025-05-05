# User Service

## Overview
This microservice handles user registration, login, deletion, and listing. It is developed using Flask and SQLite for simplicity and lightweight deployment.

## Features
- Register new users
- Login with username and password
- Delete a user by username
- List all registered users

## API Endpoints

### 1. Register a User
- **URL**: `/users/register`
- **Method**: `POST`
- **Request Body**:
```json
{
  "username": "admin",
  "password": "root123"
}
```

### 2. Login
- **URL**: `/users/login`
- **Method**: `POST`
- **Request Body**:

{
  "username": "admin",
  "password": "root123"
}


### 3. Delete a User
- **URL**: `/users/<username>`
- **Method**: `DELETE`

### 4. List Users
- **URL**: `/users`
- **Method**: `GET`

## Technology Stack
- Python 3.9
- Flask
- Flask-SQLAlchemy
- SQLite

## How to Run with Docker

docker build -t user-service:latest .
docker run -p 5000:5000 user-service:latest


## How to Deploy to Kubernetes

kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml


## Default Credentials
- Username: `admin`
- Password: `root123`



