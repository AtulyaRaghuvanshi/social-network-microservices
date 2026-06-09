## Distributed Social Platform

This project is a distributed social media backend built with multiple services. The application is split into separate services for the main social platform, authentication, email verification, and backend-for-frontend communication. This makes the system easier to manage, scale, and extend.

## Main Features

- User authentication and authorization using Keycloak and token-based security.
- Main social platform APIs for handling users, posts, feeds, and social interactions.
- Email verification service for validating user accounts.
- Backend-for-frontend service to simplify communication between clients and backend services.
- Request logging with unique request IDs for easier debugging across services.

                     +------------------+
                     |      Client      |
                     +--------+---------+
                              |
                              v
                   +----------------------+
                   | Backend For Frontend |
                   |      (BFF)           |
                   +----------+-----------+
                              |
          +-------------------+------------------+
          |                                      |
          v                                      v

+-------------------+             +----------------------+
|   Auth Service    |             |   Main Service       |
| (Keycloak Based)  |             | Social Features      |
+---------+---------+             +----------+-----------+
          |                                   |
          v                                   v

+-------------------+             +----------------------+
|    Keycloak       |             | PostgreSQL           |
| Identity Provider |             | Posts / Users / etc  |
+-------------------+             +----------------------+

          |
          v

+-------------------+
| Email Service     |
| Verification      |
+---------+---------+
          |
          v
+-------------------+
| MongoDB           |
+-------------------+

## Tools and Technologies

- Python
- FastAPI
- PostgreSQL
- MongoDB
- Keycloak
- RabbitMQ
- Redis
- SQLAlchemy
- Alembic
- Docker
- Docker Compose
- Kubernetes
- Helm
- Uvicorn
- Gunicorn
- Pytest

## Deployment

The project can run locally using Docker Compose. It also includes Kubernetes and Helm deployment files in the `devops_repo` folder, which can be used to deploy the services in a Kubernetes environment.

## Resume Summary

Built a distributed social media backend using FastAPI microservices, PostgreSQL, MongoDB, Keycloak, RabbitMQ, Docker, and Kubernetes, with separate services for authentication, email verification, core social features, and client-facing API communication.
 