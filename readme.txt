Docker Compose + Todolist

ToDoList - A task management application.

Features:

- Add new tasks;
- View the list of all tasks;
- Mark tasks as completed;
- Delete tasks.

Preview:
https://github.com/sudolicious/todolist/blob/main/frontend/public/Screenshot.png?raw=true

Technologies:
Frontend: React with TypeScript
Backend: Golang
Database: PostgreSQL
Containerization: Docker

Requirements:
Docker (version 20.10.0+)
Docker Compose (version 1.29.0+)
Git (for cloning the repository)

Installation and setup:

    1. Clone the repository
    git clone https://github.com/sudolicious/todolist-docker-compose.git

    2. Copy .env files and configure them
    cd todolist-docker-compose
    cp .env.example .env # fill in database variables
    cd backend
    cp .env.example .env # fill in backend environment variables

    3. Build and run the application
    cd todolist-docker-compose
    docker-compose up --build -d

    4. Open the application
    Frontend: http://localhost:3000
    Backend API: http://localhost:3000/api/tasks

Project structure:
todolist-docker-compose/
├── backend/ # Go backend
│ ├── Dockerfile # Backend Dockerfile
│ └── .env.example # Backend environment variables template
│ └── migrations/ # Database migrations
│
├── frontend/ # React frontend
│ ├── src/ # Frontend source files
│ ├── public/ # Static files
│ ├── Dockerfile # Frontend Dockerfile
│ └── package.json # React dependencies
│
├── openapi.yml # OpenAPI specification
├── docker-compose.yml # Main Docker Compose configuration
└── README.md # This file
