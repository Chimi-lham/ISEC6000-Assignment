# ISEC6000-Assignment

this repository will be used for saleor is an open‐source, Python‐based platform that represents a real‐world e‐commerce solution. Saleor is built on a microservices
architecture, utilizing a robust backend API, a dynamic React frontend with a dashboard, a PostgreSQL database, and an in‐memory Redis cache. we will secure this application using industry‐
standard tools like Docker, Kubernetes, and Google Kubernetes Engine (GKE) 

Services
Saleor API: Backend logic, runs on port 8000.
Saleor Dashboard: Admin interface, runs on port 9002.
PostgreSQL: Database for Saleor.
Redis: Caching and background tasks.
Mailpit: Captures application emails.
Jaeger: Tracing service.

Volumes
saleor-db: Persistent storage for PostgreSQL.
saleor-redis: Persistent storage for Redis.
saleor-media: Shared media volume between API and Worker.

Network
API ↔ PostgreSQL: Port 5432
API ↔ Redis: Port 6379
Dashboard ↔ API: Port 8000

Security
Non-root Users: Containers run as non-root users.
Resource Limits: Set for each service to optimize resource usage.
Network Isolation: Services use isolated Docker networks.

Running the Application
Start the application in the background:
docker-compose up -d
Stop the services:
docker-compose down
