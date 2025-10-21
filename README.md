# 🔐 Auth Service — Spring Authorization Server

⚠️ **Status: In Progress**
> This project is currently under development. Hopefully I can finish it soon :)

## 🎯 Project Intent

The intent of this microservice is to **abstract the authentication and authorization layer** for applications. By centralizing token issuance, client registration, and public key exposure, it allows downstream services to delegate security concerns and focus on business logic.

This service acts as a dedicated OAuth2 Authorization Server, issuing JWT access tokens and exposing a JWKS endpoint for resource servers to validate signatures. It is designed to be modular, standards-compliant, and extensible for enterprise-grade identity flows.

## 🚀 Features

- OAuth2 Authorization Server using `spring-boot-starter-oauth2-authorization-server`
- Supports `client_credentials` grant type
- JWT access tokens signed with RSA private key
- Custom token claims (`scope`, `issuer`)
- JWKS endpoint at `/.well-known/jwks.json`
- In-memory registered clients
- RSA key configuration via `application.yml` or environment variables

---

## 🧱 Tech Stack

- Java 17
- Spring Boot 3.5.6
- Spring Authorization Server
- Nimbus JOSE + JWT
- H2 (runtime only)
- Maven

## 🛠️ Getting Started

### Prerequisites

- Java 17+
- Maven 3.8+
- RSA key pair (public/private)

### 1. Clone the project

```bash
git clone https://github.com/your-org/auth-service.git
cd auth-service