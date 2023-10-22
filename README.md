# Docker Compose for InJob Project
This Docker Compose configuration sets up a development environment for the InJob project. It includes a PostgreSQL database, a Keycloak identity and access management system, and an Adminer database management tool.

## Prerequisites
Docker installed on your machine.
How to Run
Clone the InJob project repository if you haven't already.

Run the following command to start the containers:

```bash
docker-compose up
```

Once the containers are up and running, you can access the services as follows:

Keycloak: http://localhost:8080
Adminer: http://localhost:8082
To stop the containers, press Ctrl+C in the terminal where the docker-compose up command is running, or run:

```bash
docker-compose down
```

1. injob-postgres
PostgreSQL database for the InJob project.
Exposes port 5432.
2. injob-keycloak
Keycloak identity and access management system.
Keycloak admin console: http://localhost:8080/auth
Imports the realm configuration from keycloak/realms/realm-export.json.
3. injob-adminer
Adminer, a database management tool for PostgreSQL.
Adminer web interface: http://localhost:8082
Connects to the PostgreSQL database.