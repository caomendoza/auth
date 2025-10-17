# Auth Service (Spring Authorization Server)

This microservice acts as the OAuth2 Authorization Server, issuing JWT access tokens and exposing a JWKS endpoint for public key verification. It supports the `client_credentials` grant type and is designed for secure, scalable authentication in a microservice architecture.

## 🔐 Features

- OAuth2 Authorization Server using Spring Authorization Server
- JWT access token issuance with RS256 signature
- JWKS endpoint at `/.well-known/jwks.json` for public key discovery
- In-memory registered clients with scoped access (`read`, `write`)
- Custom JWT claims (issuer: `carlo`)
- RSA key pair loaded via `RSAKeyProperties`

## 🚀 Getting Started

### Prerequisites

- Java 17+
- Maven or Gradle
- Spring Boot 3.x

### Run the service

```bash
./mvnw spring-boot:run

