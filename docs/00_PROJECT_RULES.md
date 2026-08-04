# CreatorPilot - Project Rules

| Property | Value |
|----------|-------|
| Status | Draft |
| Version | 0.1.0 |
| Owner | CreatorPilot Team |
| Last Updated | 04-Aug-2026 |
| Document Type | Engineering Standard |

---

# Executive Summary

This document defines the engineering principles, development standards, architecture rules, security guidelines, documentation standards, and product philosophy for the CreatorPilot platform.

Every contributor must follow these standards to ensure the platform remains scalable, maintainable, secure, and production-ready.

This document serves as the constitution of the CreatorPilot project.

---

# Purpose

The purpose of this document is to establish a single source of truth for engineering and development practices across the CreatorPilot platform.

It ensures consistency across architecture, backend development, frontend development, AI integrations, documentation, testing, and deployment.

---

# Scope

These rules apply to:

- Mobile Application
- Web Application
- Backend API
- AI Integrations
- Prompt Engine
- Database
- Infrastructure
- Documentation
- CI/CD Pipelines
- Future Contributors

---

# Vision

CreatorPilot is not just another AI tool.

CreatorPilot is an AI Operating System for Content Creators.

The platform enables creators to research, plan, generate, manage and publish high-quality content using multiple AI providers from one unified workspace.

---

# Product Philosophy

CreatorPilot does not compete with AI providers.

CreatorPilot orchestrates them.

AI models will continue to evolve.

CreatorPilot will remain the intelligent workflow platform that connects creators with the best AI technologies available.

Our value comes from:

- Workflow Automation
- Prompt Engineering
- Content Research
- AI Orchestration
- Productivity
- Quality

---

# Core Engineering Principles

## 1. Documentation First

No feature should be implemented before documentation has been approved.

Documentation always comes before code.

---

## 2. Provider Agnostic

CreatorPilot must never depend on a single AI provider.

Every provider must be replaceable.

Supported providers may include:

- OpenAI
- Google Gemini
- Anthropic Claude
- Runway
- Kling
- Google Veo
- Future Providers

---

## 3. API First

All requests must pass through the CreatorPilot Backend API.

Mobile and Web applications must never communicate directly with AI providers.

Benefits include:

- Security
- Billing
- Analytics
- Provider Switching
- Rate Limiting
- Logging
- Monitoring

---

## 4. Clean Architecture

Backend services must follow Clean Architecture principles.

Business logic must remain independent from frameworks and external services.

---

## 5. Modular Architecture

Every module must be independently replaceable.

Examples include:

- Authentication
- Research
- Prompt Engine
- Script Engine
- Image Engine
- Video Engine
- Publishing
- Analytics

---

## 6. Security First

No secrets shall ever exist inside client applications.

API keys must remain on the server.

Sensitive information must be encrypted.

---

## 7. Scalability

Every feature must be designed for future scaling.

Temporary solutions that introduce technical debt should be avoided.

---

## 8. Reusability

Reusable components are preferred over duplicate implementations.

---

## 9. Performance

Performance should always be considered during development.

Avoid unnecessary API requests and database operations.

---

## 10. Creator First

Every feature must reduce manual work for creators.

If a feature does not improve productivity, it should be reconsidered.

---

# Documentation Standards

Every document should contain:

- Executive Summary
- Purpose
- Scope
- Goals
- Functional Requirements
- Non Functional Requirements
- Risks
- Future Improvements
- Decision Log
- Approval

---

# Development Workflow

Every feature follows this lifecycle:

1. Requirement
2. Research
3. Architecture
4. Database Design
5. API Design
6. UI/UX Design
7. Prompt Design
8. Backend Development
9. Frontend Development
10. Testing
11. Documentation Update
12. Release

---

# Technology Standards

## Mobile

- React Native
- TypeScript

## Web

- Next.js
- TypeScript

## Backend

- ASP.NET Core
- REST API
- Clean Architecture

## Database

- PostgreSQL (Supabase)

## Storage

- Supabase Storage

---

# AI Development Standards

All AI providers must be abstracted through interfaces.

Business logic must never directly depend on a specific AI provider.

Provider replacement should require minimal code changes.

---

# Git Workflow

Main Branch

Production-ready code only.

Develop Branch

Active development.

Feature Branches

feature/<feature-name>

Bug Fixes

bugfix/<issue-name>

Hotfixes

hotfix/<issue-name>

Release Branches

release/<version>

---

# Commit Message Standard

Examples:

feat(auth): add Google authentication

feat(prompt): implement reusable prompt builder

fix(api): resolve timeout issue

docs(vision): update product vision

refactor(ai): simplify provider selection

---

# Definition of Done

A feature is complete only if:

- Requirements Approved
- Documentation Updated
- Database Updated
- API Completed
- Mobile Completed
- Web Completed
- Tests Passed
- Code Reviewed
- Deployment Ready

---

# Long-Term Vision

CreatorPilot will evolve into the world's leading AI Operating System for content creators.

The platform should support any AI provider while delivering a seamless and consistent creator experience.

---

# Approval

| Property | Value |
|----------|-------|
| Status | Draft |
| Reviewed By | |
| Approved By | |
| Approval Date | |
