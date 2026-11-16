# aquatic-api
A Spring Boot and PostgreSQL REST API that tracks aquariums and checks whether the animals in them are compatible.

## Goal

Build a production-style backend where the interesting part is the domain logic, not the CRUD. Given a tank and its stocking, the API answers: can these animals live together, and is the water keeping them healthy?

It flags:
- Mismatched water types (fresh, salt, brackish)
- Non-overlapping temperature or pH ranges
- Aggressive-versus-peaceful temperament conflicts
- Tanks that are too small for their stock
- Water readings that fall outside the range of the species in the tank

This project is also a deliberate exercise in building and defending a full backend end to end: schema design, test-first business rules, integration testing against real infrastructure, authentication, CI/CD, caching, and observability.

## Planned stack
Java, Spring Boot, PostgreSQL, Flyway, JUnit, Mockito, Testcontainers, JWT auth, OpenAPI, Docker, GitHub Actions, Redis, Prometheus, Grafana. A React and TypeScript front end will come later.

## Status
Work in progress. This section will be updated as each milestone lands.

## Definition of done
- Live deployment
- Architecture diagram and ERD in this README
- Decisions log
- Passing CI badge
- Test coverage reported as a measured number
- Load-test results (requests per second, p95 latency), added only once measured

## Data
The species dataset (50 to 100 species) will be assembled from cited sources, with licenses checked before any public dataset is used.
