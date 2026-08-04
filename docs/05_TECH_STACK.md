# CreatorPilot - Technology Stack

| Property | Value |
|----------|-------|
| Document ID | CP-TECH-005 |
| Status | Draft |
| Version | 1.0.0 |
| Owner | CreatorPilot Technologies Pvt. Ltd. *(Working Name)* |
| Last Updated | 04-Aug-2026 |
| Document Type | Technology Stack |

---

# Executive Summary

This document defines the official technology stack for CreatorPilot.

Every technology has been selected based on scalability, maintainability, developer productivity, cost, community support, and long-term sustainability.

The objective is to build a platform that can support millions of users without requiring major architectural changes.

---

# Technology Selection Principles

Before selecting any technology, it must satisfy the following criteria:

- Production Ready
- Large Community
- Long-Term Support (LTS)
- Cloud Friendly
- Well Documented
- Strong Security
- High Performance
- Easy Hiring
- Active Development

---

# Frontend

## Mobile

Framework

React Native

Reason

- Cross-platform
- Excellent ecosystem
- Large community
- JavaScript/TypeScript support
- Native performance

Future

Android

iOS

Tablet Support

Desktop (Optional)

---

## Web

Framework

Next.js

Reason

- Excellent SEO
- SSR Support
- Fast
- React Ecosystem
- Enterprise Ready

---

# Backend

Framework

ASP.NET Core (.NET LTS)

Reason

- Excellent performance
- Enterprise ready
- Strong security
- Clean Architecture
- Dependency Injection
- Cross-platform

Architecture

Modular Monolith

Future

Microservices

---

# Programming Languages

Frontend

TypeScript

Backend

C#

Database

SQL

Scripts

PowerShell / Bash

---

# Database

Provider

Supabase PostgreSQL

Reason

- PostgreSQL
- Free tier
- Easy scaling
- Managed backups
- Excellent developer experience

Future

Dedicated PostgreSQL Cluster

---

# Storage

Provider

Supabase Storage

Stores

Images

Videos

Documents

Audio

Exports

---

# Authentication

JWT

OAuth

Google Login

Apple Login

Email Login

Future

Microsoft

GitHub

Enterprise SSO

---

# AI Providers

Text

OpenAI

Google Gemini

Claude

Image

OpenAI

Google

Future Providers

Video

Runway

Kling

Google Veo

Future Providers

Architecture Rule

Never depend on a single provider.

---

# API Style

REST API

Versioning

/api/v1/

Future

GraphQL (If Required)

---

# Caching

Phase 1

In-Memory Cache

Phase 2

Redis

---

# Background Jobs

Future

Hangfire

or

Quartz.NET

Purpose

- AI Processing
- Email
- Notifications
- Scheduled Jobs

---

# File Processing

Image Processing

ImageSharp

Video Processing

FFmpeg

PDF

QuestPDF

---

# Logging

Serilog

Structured Logging

Future

OpenTelemetry

---

# Monitoring

Health Checks

Application Insights (Future)

Grafana (Future)

Prometheus (Future)

---

# Validation

FluentValidation

---

# Object Mapping

Mapster

Reason

Better performance than AutoMapper

---

# ORM

Entity Framework Core

Reason

Excellent productivity

Future

Dapper (Performance Critical Queries)

---

# Dependency Injection

Built-in ASP.NET Core DI

---

# API Documentation

Swagger / OpenAPI

---

# Testing

Unit Testing

xUnit

Mocking

Moq

Integration Testing

ASP.NET Core Test Host

Frontend

Jest

React Native Testing Library

---

# Version Control

Git

Hosting

GitHub

Branch Strategy

GitFlow (Modified)

---

# CI/CD

GitHub Actions

Future

Azure DevOps

---

# Cloud Hosting

Phase 1

DigitalOcean

Future

Azure

AWS

Google Cloud

---

# CDN

Cloudflare

---

# Security

HTTPS

JWT

OAuth

Rate Limiting

API Validation

Encryption

Secret Manager

---

# Notifications

Firebase Cloud Messaging

Email

SMTP

Future

SMS

WhatsApp

---

# Analytics

Google Analytics

PostHog (Future)

---

# Development Tools

Visual Studio

VS Code

Cursor AI (Optional)

GitHub Copilot (Optional)

---

# Package Management

Frontend

npm

Backend

NuGet

---

# Documentation

Markdown

Mermaid Diagrams

GitHub Wiki (Future)

---

# Future Technologies

Redis

Kafka

RabbitMQ

ElasticSearch

Vector Database

AI Memory

Plugin SDK

---

# Technology Decision Summary

| Area | Technology |
|-------|------------|
| Mobile | React Native |
| Web | Next.js |
| Backend | ASP.NET Core |
| Database | PostgreSQL (Supabase) |
| Storage | Supabase Storage |
| Authentication | JWT + OAuth |
| AI | Multi Provider |
| Cache | Redis (Future) |
| Logging | Serilog |
| Monitoring | OpenTelemetry |
| Testing | xUnit + Jest |
| CI/CD | GitHub Actions |

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
04_SYSTEM_ARCHITECTURE.md

Next:
06_DATABASE_DESIGN.md
