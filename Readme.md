# Hotel Booking Application

This is a Dockerized project for a Hotel Booking application, consisting of PostgreSQL for the database, Redis for caching, and the Hotel Booking service.

## Prerequisites

Make sure you have Docker and Docker Compose installed on your system.

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Usage

1. Clone this repository:

   ```bash
   git clone https://github.com/Athunlal/BookNow-microservices-infra-Git.git
   cd hotel-booking-docker

Create a .env file in the project root and set the required environment variables:

env

# .env file

POSTGRES_USER=postgres
POSTGRES_PASSWORD=postgres password
POSTGRES_DB=database name

REDIS_PASSWORD=redis password

Run the application:

bash

    docker-compose up -d

    This command will start the PostgreSQL, Redis, and Hotel Booking service containers in detached mode.

    Access the Hotel Booking service at http://localhost:3000.

Services
PostgreSQL

    Container Name: postgres
    Port: 5432

Redis

    Container Name: redis
    Port: 6379

Hotel Booking Service

    Container Name: hotel-booking
    Port: 3000
    Image: shakezidhin/hotelbooking:1.0

Network

The services are connected to an app-network bridge network.
Stop and Cleanup

To stop the application and remove containers, run:

bash

docker-compose down
