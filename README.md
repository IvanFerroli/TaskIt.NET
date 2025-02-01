# TaskIt.NET

# Project Structure

This project is organized to support a microservices architecture with a .NET API backend, React frontend, PostgreSQL database, and RabbitMQ message broker.

## Folder Structure

```
AeC/
│
├── backend/               # .NET API Backend
│   ├── src/               # Source code
│   ├── tests/             # Unit and integration tests
│   ├── Dockerfile         # Dockerfile for backend
│   └── ...
│
├── frontend/              # React Frontend
│   ├── public/            # Public assets
│   ├── src/               # Source code
│   ├── tests/             # Unit and integration tests
│   ├── Dockerfile         # Dockerfile for frontend
│   └── ...
│
├── database/              # PostgreSQL Database
│   ├── migrations/        # Database migrations
│   ├── Dockerfile         # Dockerfile for database
│   └── ...
│
├── message-broker/        # RabbitMQ Message Broker
│   ├── Dockerfile         # Dockerfile for RabbitMQ
│   └── ...
│
├── docker-compose.yml     # Docker Compose file to orchestrate services
└── .gitignore             # Git ignore file
```

## Getting Started

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   ```

2. **Navigate to the project directory**
   ```bash
   cd AeC
   ```

3. **Build and run the services**
   ```bash
   docker-compose up --build
   ```

## Prerequisites

- Docker
- .NET SDK
- Node.js
- PostgreSQL
- RabbitMQ

## Contributing

Please read `CONTRIBUTING.md` for details on our code of conduct, and the process for submitting pull requests.

## License

This project is licensed under the MIT License - see the `LICENSE.md` file for details.
