# emartapp
# Containerizing Microservice Project

This project demonstrates the containerization of a microservice-based application, consisting of an Angular client app, Java API, Node.js API, and Nginx as a Api Gateway.

## Project overview
![EMart App Architecture](https://github.com/MhmdAbdo74/Containerizing-Microservice-Project/assets/94086189/27421cc2-daf0-458b-bf77-9a4bcde39543)


## Project Structure

The project structure is organized as follows:

```
.
├── angular-client-app
├── java-api
├── node-api
└── nginx
```

- `angular-client-app`: Contains the source code for the Angular client application.
- `java-api`: Contains the source code for the Java API.
- `node-api`: Contains the source code for the Node.js API.
- `nginx`: Contains the configuration files for Nginx.

## Prerequisites

Before running this project, ensure you have the following dependencies installed on your machine:

- Docker: [Install Docker](https://docs.docker.com/get-docker/)
- Node.js: [Install Docker Compose](https://docs.docker.com/compose/install/)

## Getting Started

To get started with this project, follow the steps below:

1. Clone the repository:

   ```bash
   git clone https://github.com/MhmdAbdo74/Containerizing-Microservice-Project.git
   ```

2. Build and run the images:

   ```bash
   docker compose up -d
   ```

   The client app will be available at `http://localhost:4200`.

   Nginx will be available at `http://localhost`.

## Additional Configuration

If you need to modify the configuration of Nginx, you can edit the `nginx.conf` file located in the
