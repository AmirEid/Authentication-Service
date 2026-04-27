# Authentication Projects Hub

Two backend authentication implementations, one in Fastify and one in FastAPI, built to show how modern JWT and 2FA/session flows are designed in different stacks.

> The two project links are below. Open the cards to jump directly to each repository.

Quick jump:

- [Fastify Auth Service](#projects)
- [FastAPI Auth Service](#projects)

If you want to compare real auth architectures, this repository gives you two working projects side by side:

- JWT-based login and session handling
- Refresh-token rotation
- 2FA with TOTP
- Middleware-protected routes
- Clear, separate project docs for each stack

## Introduction

### What is JWT?

**JWT (JSON Web Token)** is a compact, signed token format used to securely transfer authentication and authorization claims between systems.

- It is stateless for access control checks
- It can include expiration (`exp`) and user identity claims
- It is signed (and optionally encrypted) to prevent tampering

In practical auth systems, JWT is often used for **short-lived access tokens** while refresh tokens are used to maintain sessions safely.

### What is 2FA?

**2FA (Two-Factor Authentication)** adds a second verification step after password login, usually a time-based one-time password (TOTP) from an authenticator app.

- Factor 1: something you know (password)
- Factor 2: something you have (authenticator app/device)

This significantly reduces account takeover risk, even if a password is leaked.

## What You’ll Find

- A Fastify + TypeScript authentication service
- A FastAPI + Python authentication service built around stateless JWT access tokens
- Project-specific README files in each repository

---

## Projects

<table>
  <tr>
    <td align="center" width="50%">
      <a href="https://github.com/AmirEid/Authentication-MicroService---Fastify">
        <img src="https://img.shields.io/badge/Fastify%20Auth%20Service-Click%20Me-000000?style=for-the-badge&logo=fastify&logoColor=white&cacheSeconds=0" alt="Fastify Auth Service" />
      </a>
      <br/><br/>
      <strong>Techs Used</strong>
      <ul align="left">
        <li>Node.js + TypeScript</li>
        <li>Fastify</li>
        <li>SQLite</li>
        <li>JWT</li>
        <li>Zod validation</li>
        <li>TOTP 2FA (Speakeasy + QRCode)</li>
        <li>Docker / Docker Compose</li>
      </ul>
      <strong>Services Provided</strong>
      <ul align="left">
        <li>User registration and login</li>
        <li>Access + refresh token flow</li>
        <li>Refresh token rotation</li>
        <li>Session idle timeout control</li>
        <li>2FA enable + verify endpoints</li>
        <li>Protected route middleware checks</li>
      </ul>
    </td>
    <td align="center" width="50%">
      <a href="https://github.com/AmirEid/Authentication-Service-FastAPI">
        <img src="https://img.shields.io/badge/FastAPI%20Auth%20Service-Click%20Me-009688?style=for-the-badge&logo=fastapi&logoColor=white&cacheSeconds=0" alt="FastAPI Auth Service" />
      </a>
      <br/><br/>
      <strong>Techs Used</strong>
      <ul align="left">
        <li>Python</li>
        <li>FastAPI</li>
        <li>Pydantic</li>
        <li>JWT access tokens</li>
        <li>Password hashing utilities</li>
        <li>Environment-based settings</li>
      </ul>
      <strong>Services Provided</strong>
      <ul align="left">
        <li>Account registration endpoints</li>
        <li>Login and stateless token issuance</li>
        <li>Token verification endpoint</li>
        <li>Account control routes</li>
        <li>Modular service architecture</li>
        <li>Config-driven security setup</li>
      </ul>
    </td>
  </tr>
</table>

---

## Goal of This Repository

Provide two implementations of secure authentication patterns in different ecosystems:

- **Fastify + TypeScript** for Node.js services
- **FastAPI + Python** for Python services using stateless JWT access tokens

This makes it easier to compare architecture decisions, security practices, and API design across frameworks.
