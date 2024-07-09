# Backend - FastAPI with PostgreSQL

This directory contains the backend of the application built with FastAPI and a PostgreSQL database.

## Prerequisites

- Python 3.8 or higher
- Poetry (for dependency management)
- PostgreSQL (ensure the database server is running)

### Installing Poetry

To install Poetry, follow these steps:

```sh
curl -sSL https://install.python-poetry.org | python3 -
```

Add Poetry to your PATH (if not automatically added):

## Setup Instructions

1. **Navigate to the backend directory**:

   ```sh
   cd backend
   ```

2. **Install dependencies using Poetry**:

   ```sh
   poetry install
   ```

3. **Set up the database with the necessary tables**:

   ```sh
   poetry run bash ./prestart.sh
   ```

4. **Run the backend server**:

   ```sh
   poetry run uvicorn app.main:app --reload
   ```

5. **Update configuration**:
   Ensure you update the necessary configurations in the `.env` file, particularly the database configuration.

## Setting up the database locally

1. **Install postgres**

2. ```sh
   sudo -i -u postgres
   ```
3. ```sh
   psql
   ```
4. ```sh
   CREATE USER username WITH PASSWORD 'password';
   ```
5. ```sh
   CREATE DATABASE database;
   ```
6. ```sh
   GRANT ALL PRIVILEGES ON DATABASE database TO username;
   ```
7. ```sh
   ALTER USER username WITH SUPERUSER;
   ```

## Setting up adminer and NPM

1. **Start-up adminer**

   ```sh
   docker run --name adminer -p 8080:8080 -d adminer
   ```

2. **Start-up Nginx proxy manager:** Create a compose file with the container config then run:
   ```sh
   docker-compose up -d
   ```
