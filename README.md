# Social Media Microservices
 A Dockerized microservices-based social media platform with User, Auth, Post, and Notification services.
# Prerequisites
Docker and Docker Compose installed.
Ports 3001–3004 free
# Setup
Clone Repository:
git clone <repository-url>
cd social-media-platform
# Start Services 
docker-compose up --build
# Verify Containers 
docker ps
# Test APIs 
  # User Service:
  curl -X POST http://localhost:3001/users -H "Content-Type: application/json" -d '{"name":"Aarti","email":"aarti@gmail.com","password":"aarti123"}'
  # Auth Service:
  curl -X POST http://localhost:3004/auth/login -H "Content-Type: application/json" -d '{"email":"aartishakya@gmail.com","password":"aarti123"}'
  # Post Service:
  curl -X POST http://localhost:3002/posts -H "Content-Type: application/json" -d '{"content":"Hello World","userid":1}'
  # Notification Service:
  curl -X POST http://localhost:3003/notifications -H "Content-Type: application/json" -d '{"userid":1,"message":"New post created"}'
# Stop Services:
docker-compose down
