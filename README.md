# Moodle Docker Setup

This repository contains a Docker-based development environment for [Moodle](https://moodle.org/), using **PHP-FPM**, **Nginx**, and **MariaDB**.

It is designed for local development and testing of Moodle installations.

---

---

##  Run the Project

###  Prerequisites

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)
- [Git](https://git-scm.com/)

###  Steps

1. Clone the repository:


git clone https://github.com/YOUR_USERNAME/moodle-docker.git
cd moodle-docker


2. Start the containers:

   
docker compose up -d --build

3.Access Moodle in your browser:
  http://localhost:8081

Configuration Details
Docker Services
PHP-FPM: Handles backend PHP processing

Nginx: Serves Moodle using FastCGI

MariaDB: Stores Moodle database

Volumes:

moodledata/ → Stores Moodle's uploaded content and generated files

db_data/ → Persists MariaDB data across restarts


Useful Docker Commands

# Start the containers
docker compose up -d

# Stop the containers
docker compose down

# Rebuild containers after making config changes
docker compose up -d --build

# View real-time logs
docker compose logs -f

# Access PHP container shell
docker exec -it moodle-php bash

# Access MariaDB container
docker exec -it moodle-db mysql -u root -p



