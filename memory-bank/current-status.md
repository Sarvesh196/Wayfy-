# Current status

## Repository baseline

- Spring Boot Maven backend starter exists under `backend/`.
- The backend uses Java 21 and Spring Boot 4.
- Docker Compose defines PostgreSQL/PostGIS and Redis for local development.
- Git ignore rules cover common Java, Node, Angular, and environment files.

## Not implemented yet

- Angular application
- MVP domain entities, database migrations, and REST APIs
- OTP authentication and user profiles
- Trip rooms, chat, status reports, and report confirmations
- Notifications and moderation
- CI/CD and deployment environments

## Setup notes

At the last environment check, Java, Node.js, and Docker were not available on
the command-line PATH. Recheck tool availability before trying to build or run
the project; this note may become stale.
