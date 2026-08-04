# CreatorPilot - Project Rules

**Status:** Draft

**Version:** 0.1.0

**Owner:** CreatorPilot Team

**Last Updated:** 04-Aug-2026

---

# Purpose

This document defines the engineering, architecture, documentation, security, AI integration, and development standards for the CreatorPilot platform.

Every contributor must follow these rules to ensure the project remains scalable, maintainable, secure, and production-ready.

---

# Vision

CreatorPilot is not just another AI tool.

CreatorPilot is an AI Operating System for Content Creators.

The platform will help creators research, plan, generate, manage and publish high-quality content using multiple AI providers from a single workspace.

---

# Core Principles

## 1. Documentation First

No feature should be implemented before its documentation is approved.

Documentation always comes before code.

---

## 2. Provider Agnostic

CreatorPilot must never depend on a single AI provider.

Every AI integration must be replaceable.

Examples:

- OpenAI
- Google Gemini
- Claude
- Runway
- Kling
- Google Veo
- Future Providers

---

## 3. API First

All communication must go through the CreatorPilot Backend API.

The mobile and web applications must never communicate directly with AI providers.

Benefits:

- Security
- Billing
- Logging
- Rate Limiting
- Analytics
- Provider Switching

---

## 4. Clean Architecture

Backend must follow Clean Architecture principles.

Business logic must never depend on external services.

---

## 5. Modular Design

Every module should be independent.

Example:

Authentication

Research

Prompt Engine

Script Engine

Video Engine

Publishing

Analytics

Each module should be replaceable without affecting the rest of the system.

---

## 6. Security First

API Keys must never be stored in the client application.

Secrets must always remain on the backend.

---

## 7. Scalability

Every feature should be designed for future scaling.

Avoid temporary solutions that create long-term technical debt.

---

## 8. Reusability

Reusable code should always be preferred over duplicate implementations.

---

## 9. Performance

Every feature should be optimized for speed and low API usage whenever possible.

---

## 10. User Experience

Every feature must reduce the creator's manual work.

If a feature does not save meaningful time, it should be reconsidered.

---

# Documentation Standards

Every document must contain:

- Purpose
- Scope
- Goals
- Requirements
- Decisions
- Future Improvements

---

# Development Workflow

Every feature follows this order:

1. Requirement
2. Architecture
3. Database Design
4. API Design
5. UI Flow
6. Prompt Design
7. Backend Development
8. Frontend Development
9. Testing
10. Documentation Update

---

# Coding Standards

## Backend

- ASP.NET Core
- REST API
- Clean Architecture
- SOLID Principles

---

## Mobile

- React Native
- TypeScript

---

## Web

- Next.js
- TypeScript

---

## Database

- PostgreSQL (Supabase)

---

## Storage

- Supabase Storage

---

# AI Standards

All AI providers must be abstracted behind interfaces.

The application should never be tightly coupled with any AI provider.

---

# Git Standards

Main Branch

- production-ready code only

Develop Branch

- active development

Feature Branch

feature/<feature-name>

Bug Fix

bugfix/<issue-name>

Hotfix

hotfix/<issue-name>

---

# Commit Message Convention

Examples:

feat(auth): add Google authentication

fix(api): resolve prompt generation timeout

docs(vision): update project roadmap

refactor(ai): simplify provider selection

---

# Documentation Rules

Every major technical decision must be documented.

Architecture changes must be recorded.

Prompt changes must be versioned.

---

# Project Structure

The repository structure should remain clean and organized.

Documentation, prompts, architecture, APIs, and source code should always be separated.

---

# Definition of Done

A feature is considered complete only if:

✅ Requirements Approved

✅ Database Updated

✅ API Completed

✅ Mobile Completed

✅ Web Completed

✅ Documentation Updated

✅ Testing Completed

---

# Future Vision

CreatorPilot should evolve into a complete AI Creator Operating System capable of integrating with any AI provider while maintaining a consistent creator experience.

---

# Approval

Status: Draft

Reviewed By:

Approved By:

Approval Date:

---
