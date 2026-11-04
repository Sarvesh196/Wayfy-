# Architecture

## Direction

Start with a modular monolith: one Spring Boot backend with clear domain
modules, so modules can be split into services later if justified. The
Angular PWA communicates with the backend over REST and WebSocket.

The planned data and live-services layer is PostgreSQL/PostGIS plus Redis.
Kafka and a separately deployed Python prediction service are future additions,
not requirements for the initial MVP.

## Planned backend modules

- Auth and users: OTP login, JWT, profiles, reputation
- Routes and trips: routes, stops, scheduled trips, follows
- Status reports: quick reports, confirmations, status aggregation
- Chat: messages scoped to a trip room
- Tracking: live positions and route matching (later)
- Notifications: push alerts through Firebase
- Prediction: Python service integration (later)

## Main domain entities

User, Route, Stop, Trip, Follow, StatusReport, and ChatMessage. Location is
planned for tracking; Operator and Rating may be added for later phases.

## Current implementation boundary

The repository is currently a Spring Boot backend starter with PostgreSQL and
Redis services in Docker Compose. The Angular app and domain modules have not
yet been implemented. Treat this section as intended architecture, not a
description of working features.
