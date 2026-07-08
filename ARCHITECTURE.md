# NIS Connect Architecture

Version: 0.1.0

---

# Purpose

This document describes the architecture of the NIS Connect platform.

All contributors (human and AI) should follow this architecture.

---

# High-Level Architecture

                        +--------------------+
                        |  Parent Portal UI  |
                        +---------+----------+
                                  |
                                  v
                        +--------------------+
                        |   NIS Connect UI   |
                        +---------+----------+
                                  |
                                  v
                        +--------------------+
                        |   Service Layer    |
                        +---------+----------+
                                  |
                                  v
                        +--------------------+
                        | Repository Layer   |
                        +---------+----------+
                                  |
                                  v
                        +--------------------+
                        |   PowerSchool DB   |
                        +--------------------+

PowerSchool remains the System of Record.

NIS Connect provides presentation, workflow, configuration,
and business logic.

---

# Layer Responsibilities

## Presentation Layer

Location

web_root/

Responsibilities

- HTML
- CSS
- JavaScript
- User interaction

No business logic.

---

## Service Layer

Responsibilities

- Validation
- Workflow
- Business rules
- Permissions

Examples

DashboardService

StudentService

ParentService

ConfirmationService

AuditService

NotificationService

---

## Repository Layer

Responsibilities

Read/write data.

No business logic.

Examples

StudentRepository

ParentRepository

SettingsRepository

AuditRepository

---

# Module Architecture

Every module follows the same structure.

Example

modules/

    dashboard/

        dashboard.html

        dashboard.js

        dashboard.css

        DashboardService.js

        DashboardRepository.js

        README.md

Each module is self-contained.

---

# Core Modules

Dashboard

Configuration

Theme

Logging

Settings

Audit

Notification

Security

These modules are loaded automatically.

---

# Feature Modules

Demographics

Emergency Contacts

Approval Workflow

Reports

Toddle

Calendar

Forms

Transportation

Feature modules may be enabled or disabled.

---

# Module Registration

Each module must register itself.

Example

Module Name

Description

Version

Dependencies

Navigation

Permissions

Feature Flag

This allows automatic discovery.

---

# Feature Flags

Every module has a feature flag.

Example

dashboard.enabled

true

If disabled

- Menu hidden

- Routes disabled

- Dashboard card removed

No hardcoded visibility.

---

# Configuration

All configuration is stored in

NIS_CONNECT_SETTINGS

Examples

School Name

Theme

Academic Year

Maintenance Mode

Toddle URL

Calendar URL

Menu Visibility

---

# Logging

Every important action is logged.

Examples

Login

Configuration changes

Parent submission

Approval

Rejection

Errors

---

# Audit Workflow

Parent edits information

↓

Pending Changes

↓

Registrar Review

↓

Approval

↓

PowerSchool Update

PowerSchool is never updated directly by parents.

---

# Security

Validate all input.

Escape all output.

Use least privilege.

Do not expose database schema.

Never trust client-side validation.

---

# User Roles

Parent

Student

Registrar

Administrator

ICT Administrator

Permissions are role-based.

---

# Database Strategy

Never modify PowerSchool tables.

Create separate plugin tables.

Examples

NIS_CONNECT_SETTINGS

NIS_CONNECT_AUDIT

NIS_CONNECT_PENDING

NIS_CONNECT_LOG

Future versions may add additional tables.

---

# Navigation

PowerSchool Navigation

↓

NIS Connect

↓

Dashboard

↓

Modules

Navigation is generated dynamically.

---

# Dashboard

Dashboard widgets are dynamic.

Widgets are loaded from enabled modules.

No hardcoded dashboard.

---

# Theme

Theme is configurable.

School Logo

Primary Color

Secondary Color

Fonts

Icons

---

# Mobile

Responsive first.

Desktop

Tablet

Phone

supported equally.

---

# Versioning

Semantic Versioning

0.x Development

1.x Stable

2.x Major Features

---

# Future Expansion

Possible future modules

Toddle

Transportation

Library

School Forms

Digital Consent

Payment Gateway

ID Card Requests

Visitor Registration

The architecture should support these without
major redesign.
