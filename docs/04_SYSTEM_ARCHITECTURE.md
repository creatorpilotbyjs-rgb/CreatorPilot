# CreatorPilot - System Architecture

| Property | Value |
|----------|-------|
| Document ID | CP-ARCH-004 |
| Status | Draft |
| Version | 0.1.0 |
| Owner | CreatorPilot Technologies Pvt. Ltd. *(Working Name)* |
| Last Updated | 04-Aug-2026 |
| Document Type | System Architecture |

---

# Executive Summary

This document defines the high-level architecture of CreatorPilot.

The architecture is designed to be scalable, modular, secure, maintainable, and AI-provider agnostic.

The goal is to support millions of creators without requiring major architectural redesign.

---

# Architecture Goals

The system must be:

- Modular
- Scalable
- Secure
- Provider Agnostic
- API First
- Mobile First
- Cloud Ready
- Easy to Maintain
- Cost Efficient

---

# High Level Architecture

```

```
                +---------------------------+
                |      React Native App     |
                +------------+--------------+
                             |
                             |
                +------------v--------------+
                |        Next.js Web        |
                +------------+--------------+
                             |
                             |
                     HTTPS / REST API
                             |
                             |
                +------------v--------------+
                |      ASP.NET Core API     |
                |     (Modular Monolith)    |
                +------------+--------------+
                             |
          +------------------+-------------------+
          |                  |                   |
          |                  |                   |
+---------v--------+ +--------v---------+ +-------v--------+
| AI Provider Layer| | Business Domains | | Infrastructure |
+------------------+ +------------------+ +----------------+
          |                  |                   |
          |                  |                   |
   OpenAI / Gemini /     PostgreSQL        Storage
   Claude / Runway       Supabase          Supabase
   Kling / Veo

```

---

# Core Principles

## API First

Every client communicates only with the backend API.

Clients never communicate directly with AI providers.

Benefits:

- Security
- Billing
- Monitoring
- Logging
- AI Switching
- Caching

---

## Modular Monolith

Phase 1 architecture:

Single API

Multiple independent modules.

Advantages:

- Faster development
- Easier debugging
- Lower hosting cost
- Easier deployment

Future:

Convert modules into microservices only when required.

---

# System Layers

## Presentation Layer

Applications:

- React Native
- Next.js

Responsibilities:

- UI
- User Interaction
- Local Cache
- Authentication

---

## API Layer

Technology:

ASP.NET Core

Responsibilities:

- Authentication
- Authorization
- Routing
- Validation
- Rate Limiting
- Logging

---

## Application Layer

Responsibilities:

- Use Cases
- Business Workflows
- DTO Mapping
- Service Coordination

---

## Domain Layer

Contains:

- Business Rules
- Entities
- Interfaces
- Domain Events

This layer must never depend on infrastructure.

---

## Infrastructure Layer

Contains:

- Database
- AI Providers
- Storage
- Email
- Notifications
- Third Party APIs

---

# Domain Architecture

The backend is divided into business domains.

Identity

Workspace

Project

Research

Knowledge

Script

Prompt

Generation

Assets

Publishing

Analytics

Billing

Notification

Administration

Each domain should own its:

- Entities
- Services
- Repositories
- Business Rules

---

# AI Provider Layer

CreatorPilot must never depend on a single provider.

Architecture:

```

```
Prompt Engine

↓

AI Orchestrator

↓

Provider Interface

↓

OpenAI

↓

Gemini

↓

Claude

↓

Runway

↓

Kling

↓

Future Providers
```

Adding a new provider should require minimal changes.

---

# Workspace Architecture

Workspace

↓

Projects

↓

Research

↓

Scripts

↓

Prompts

↓

Assets

↓

Exports

↓

Analytics

A creator may own multiple workspaces.

Each workspace may contain multiple projects.

---

# Request Flow

User

↓

React Native

↓

ASP.NET Core API

↓

Application Service

↓

Domain Service

↓

Repository

↓

Supabase

↓

Response

---

# AI Request Flow

User

↓

Prompt Engine

↓

AI Orchestrator

↓

Provider Selection

↓

Provider API

↓

Response Formatter

↓

Project Assets

---

# Authentication Flow

User

↓

Google / Apple / Email

↓

JWT Authentication

↓

Refresh Token

↓

Secure API Access

Future:

OAuth Providers

Enterprise SSO

---

# Storage Strategy

Database

Supabase PostgreSQL

Stores:

- Users
- Workspaces
- Projects
- Scripts
- Prompts
- Metadata

Storage

Supabase Storage

Stores:

- Images
- Videos
- Audio
- Documents

---

# Caching Strategy

Future:

Redis

Used for:

- AI Responses
- Trending Topics
- Frequently Used Prompts

---

# Logging

Every important action should be logged.

Examples:

Login

Project Created

Prompt Generated

AI Request

Export

Publish

Errors

---

# Security

Never expose API Keys.

Encrypt sensitive information.

Validate all requests.

Use HTTPS everywhere.

---

# Scalability Strategy

Phase 1

Modular Monolith

↓

Phase 2

Background Workers

↓

Phase 3

Microservices

↓

Phase 4

Global Scaling

---

# Folder Structure

```

```
src/

Core/

Application/

Infrastructure/

API/

Shared/

Modules/

Identity/

Workspace/

Projects/

Research/

Knowledge/

Script/

Prompt/

Generation/

Assets/

Publishing/

Analytics/

Billing/

Notifications/

Admin/
```

---

# Future Architecture

Future additions:

- AI Agents
- Event Bus
- Queue Processing
- Plugin Marketplace
- Cloud Rendering
- AI Memory
- Creator Knowledge Graph

---

# Technology Summary

Mobile

React Native

Web

Next.js

Backend

ASP.NET Core

Database

Supabase PostgreSQL

Storage

Supabase Storage

Authentication

JWT + OAuth

AI Providers

OpenAI

Gemini

Claude

Runway

Kling

Google Veo

---

# Architecture Decisions

Decision 001

Use Modular Monolith.

Reason:

Lower cost.

Simpler deployment.

Faster development.

---

Decision 002

API First.

Reason:

Better security.

Provider abstraction.

---

Decision 003

Provider Agnostic.

Reason:

Future flexibility.

---

# Approval

| Property | Value |
|----------|-------|
| Status | Draft |
| Reviewed By | |
| Approved By | |
| Approval Date | |

---

# Related Documents

Previous:

02A_COMPETITOR_ANALYSIS.md

Next:

05_TECH_STACK.md
