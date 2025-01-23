# News Portal

A guide to setting up and running the News Portal application using Docker.

---

## Prerequisites

- **Docker**: Ensure Docker is installed and running on your system.

---

## Setup Instructions

### 1. Import the Database
Copy the SQL file to the MySQL container and import it:

```bash
docker cp newsportal.sql mysql_db:/newsportal.sql

# Access the MySQL container
docker exec -it mysql_db bash

# Import the SQL file inside the container
mysql -u root -p root
SOURCE newsportal < /newsportal.sql
```

---

### 2. Install Required PHP Modules
If the required PHP modules (e.g., `mysqli`) are missing, install them:

```bash
# Access the PHP container
docker exec -it php_app bash

# Update package lists
apt-get update

# Install the missing mysqli module
docker-php-ext-install mysqli

# Restart the container to apply changes
docker restart php_app
```

---

## Run The Application

### Start the application using Docker Compose:

```bash
docker-compose up -d
