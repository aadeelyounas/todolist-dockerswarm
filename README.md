# Todo List Application with Docker Swarm

This is a simple Todo List application built with React, Node.js, Express, and PostgreSQL. It is designed to be easily deployed using Docker Swarm.

## Features

*   Create, read, update, and delete todos
*   Responsive user interface
*   Dockerized for easy deployment

## Prerequisites

*   Docker
*   Docker Compose

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/aadeelyounas/todolist-dockerswarm.git
cd todolist-dockerswarm
```

### 2. Build the Docker images

```bash
docker-compose build
```

### 3. Run the application using Docker Compose

```bash
docker-compose up -d
```

This will start the application in detached mode. The frontend will be accessible at `http://localhost:3000`, and the backend API will be accessible at `http://localhost:3001`.

### 4. Access the application

Open your web browser and navigate to `http://localhost:3000` to access the Todo List application.

## Docker Swarm Deployment (Optional)

To deploy the application using Docker Swarm, follow these steps:

### 1. Initialize a Docker Swarm

If you don't already have a Docker Swarm initialized, run the following command:

```bash
docker swarm init
```

### 2. Deploy the application to the Swarm

```bash
docker stack deploy -c docker-compose.yml todolist
```

This will deploy the application to the Docker Swarm.

## Environment Variables

The following environment variables are used by the application:

*   `DATABASE_URL`: The connection string for the PostgreSQL database. This is used by the backend API.
*   `POSTGRES_PASSWORD`: The password for the PostgreSQL database. This is used by the `db` service in the `docker-compose.yml` file.

## API Endpoints

The following API endpoints are available:

*   `GET /todos`: Get all todos
*   `POST /todos`: Create a new todo
*   `PUT /todos/:id`: Update a todo
*   `DELETE /todos/:id`: Delete a todo
*   `GET /health`: Health check endpoint

## Contributing

Contributions are welcome! Please feel free to submit a pull request.

## License

[MIT](https://opensource.org/licenses/MIT)
