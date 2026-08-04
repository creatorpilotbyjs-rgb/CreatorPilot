# CreatorPilot - Database Design

| Property | Value |
|----------|-------|
| Document ID | CP-DB-006 |
| Status | Draft |
| Version | 1.0.0 |
| Owner | CreatorPilot Technologies Pvt. Ltd. *(Working Name)* |
| Last Updated | 04-Aug-2026 |
| Document Type | Database Design |

---

# Executive Summary

This document defines the logical database architecture of CreatorPilot.

The database is designed around business domains instead of technical modules. This allows the application to scale while maintaining clean separation of concerns.

The primary database engine is PostgreSQL (Supabase).

---

# Database Goals

The database should be:

- Scalable
- Secure
- Highly Normalized
- Easy to Maintain
- AI Friendly
- Audit Friendly
- Cloud Ready

---

# Database Strategy

Database Engine

PostgreSQL

Hosting

Supabase

ORM

Entity Framework Core

Migration

EF Core Migrations

Soft Delete

Enabled

Audit Tracking

Enabled

UUID

Primary Keys

UTC

All timestamps

---

# High-Level Entity Relationship

```

Users

↓

Workspaces

↓

Projects

↓

Knowledge Base

↓

Research

↓

Scripts

↓

Scenes

↓

Prompts

↓

AI Requests

↓

AI Responses

↓

Assets

↓

Exports

↓

Publishing

↓

Analytics

```

---

# Domain Overview

Identity

Workspace

Project

Research

Knowledge

Script

Prompt

Generation

Asset

Publishing

Billing

Analytics

Notifications

Administration

Each domain owns its own tables.

---

# Identity Domain

Tables

Users

UserProfiles

RefreshTokens

OAuthAccounts

UserSettings

---

# Workspace Domain

Tables

Workspaces

WorkspaceMembers

WorkspaceInvitations

WorkspaceSettings

WorkspaceActivity

---

# Project Domain

Tables

Projects

ProjectTags

ProjectCategories

ProjectStatus

ProjectHistory

ProjectFavorites

---

# Research Domain

Tables

ResearchTopics

ResearchSources

ResearchNotes

ResearchBookmarks

ResearchFacts

ResearchMedia

---

# Knowledge Domain

Tables

KnowledgeCollections

KnowledgeArticles

KnowledgeReferences

KnowledgeCategories

KnowledgeTags

KnowledgeAttachments

---

# Script Domain

Tables

Scripts

ScriptVersions

ScriptComments

ScriptTemplates

ScriptSections

---

# Scene Domain

Tables

Scenes

SceneAssets

ScenePrompts

SceneTransitions

SceneTimeline

---

# Prompt Domain

Tables

PromptTemplates

GeneratedPrompts

PromptVariables

PromptHistory

PromptRatings

PromptCategories

---

# AI Generation Domain

Tables

AIProviders

AIModels

AIRequests

AIResponses

GenerationJobs

GenerationLogs

GenerationErrors

---

# Asset Domain

Tables

Assets

Folders

AssetTags

AssetVersions

AssetMetadata

Downloads

---

# Voice Domain

Tables

VoiceProjects

VoiceTracks

VoiceRecordings

VoiceEffects

BackgroundMusic

---

# Publishing Domain

Tables

PublishingProfiles

PublishingHistory

PlatformAccounts

ExportHistory

Captions

Hashtags

---

# Analytics Domain

Tables

ProjectAnalytics

AIUsage

UserActivity

PromptAnalytics

GenerationAnalytics

StorageAnalytics

---

# Billing Domain

Tables

Plans

Subscriptions

Invoices

Payments

UsageRecords

Credits

---

# Notification Domain

Tables

Notifications

NotificationTemplates

NotificationHistory

---

# Administration Domain

Tables

SystemSettings

FeatureFlags

AuditLogs

ErrorLogs

APIKeys

---

# Shared Tables

Countries

Languages

Currencies

TimeZones

Categories

Tags

FileTypes

Platforms

---

# Relationships

User

↓

Workspace

↓

Project

↓

Research

↓

Script

↓

Scene

↓

Prompt

↓

Generation

↓

Asset

Every project belongs to one workspace.

Every workspace belongs to one user or organization.

---

# Naming Convention

Tables

PascalCase

Columns

PascalCase

Primary Key

Id

Foreign Key

<Entity>NameId

Created Date

CreatedAtUtc

Updated Date

UpdatedAtUtc

Deleted

IsDeleted

---

# Audit Columns

Every table should include:

Id

CreatedAtUtc

UpdatedAtUtc

CreatedBy

UpdatedBy

IsDeleted

Version

---

# Indexing Strategy

Primary Keys

Clustered

Foreign Keys

Indexed

Search Fields

Indexed

Project Name

Indexed

Workspace Id

Indexed

Created Date

Indexed

---

# File Storage

Database

Stores metadata only.

Supabase Storage

Stores actual files.

Database Example

Asset

↓

FileName

↓

StoragePath

↓

FileSize

↓

MimeType

↓

CreatedAt

Actual binary files are never stored inside PostgreSQL.

---

# AI Storage Strategy

Every AI request must be stored.

Includes

Prompt

Provider

Model

Input Tokens

Output Tokens

Cost

Duration

Response

Status

This enables future analytics and billing.

---

# Future Database Features

Vector Database

Semantic Search

Knowledge Graph

Embedding Storage

AI Memory

Recommendation Engine

---

# Backup Strategy

Daily Backup

Point-in-Time Recovery

Disaster Recovery

Multi Region (Future)

---

# Security

Encryption at Rest

HTTPS

JWT

Role Based Access

Audit Logs

Soft Delete

No Hard Delete

---

# Database Decisions

Decision 001

Use PostgreSQL

Reason

Enterprise Ready

---

Decision 002

Use UUID

Reason

Better distributed systems support

---

Decision 003

Store files in object storage

Reason

Better scalability

---

Decision 004

Every table must support audit tracking

Reason

Enterprise compliance

---

# Related Documents

Previous

05_TECH_STACK.md

Next

07_API_SPECIFICATION.md
