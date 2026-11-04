# Tech stack

## Application

- Backend: Java 21, Spring Boot 4, modular monolith
- Frontend: Angular and TypeScript, Angular Material, delivered as a PWA
- Database: PostgreSQL with PostGIS; schema changes managed by Flyway
- Cache and live data: Redis
- Maps: Leaflet and OpenStreetMap (planned)
- Authentication: Spring Security, JWT, phone OTP
- Real-time chat: Spring WebSocket
- Push notifications: Firebase Cloud Messaging (planned)
- API documentation: springdoc OpenAPI / Swagger (planned)

## Later services

- Kafka for messaging, when needed
- Python FastAPI prediction service
- LLM API for summaries, spam detection, and text-to-status parsing

## Development and delivery

- Maven; Node.js LTS and Angular CLI
- JUnit 5, Mockito, Testcontainers; Jasmine/Jest and Playwright or Cypress
- Docker Compose for local services
- GitHub Actions for CI/CD
- Kubernetes with Helm for a later deployment phase
- Prometheus, Grafana, and Spring Actuator for monitoring

## Environment notes

Local development uses Docker Compose. CI runs in GitHub Actions. Staging is
intended to deploy on merge, while production deployment requires manual
approval. Secrets belong in GitHub or Kubernetes Secrets, not in source files
or this memory bank.
