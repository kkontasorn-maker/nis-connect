# NIS Connect

## Overview

NIS Connect is a modern family portal built on top of PowerSchool SIS for
Nakornpayap International School.

PowerSchool remains the System of Record.

NIS Connect provides the user experience.

The project is designed to be:

- Modular
- Upgrade-safe
- Configuration-driven
- Easy to maintain
- Easy to extend

---

# Objectives

Primary objective

Allow parents to review and confirm demographic information once per academic year.

Secondary objectives

- Improve parent engagement
- Reduce registrar workload
- Improve data quality
- Provide a modern portal experience
- Centralize family services

---

# Architecture

PowerSchool SIS

↓

NIS Connect Core

↓

Modules

↓

Dashboard

Demographics

Emergency Contacts

Approval Workflow

Reports

Notifications

---

# Guiding Principles

1. Never modify PowerSchool core files.

2. Never replace existing PowerSchool pages.

3. All customizations must reside inside the plugin.

4. Every feature must be configurable.

5. Every important action must be logged.

6. Every database change must be versioned.

7. All code must be documented.

8. Every release must be upgrade-safe.

---

# Modules

Core

Dashboard

Settings

Theme

Logging

Configuration

Audit

Notifications

Demographics

Emergency Contacts

Approval Workflow

Reports

Future Modules

Toddle

Calendar

E-Canteen

Transportation

Digital Forms

Library

---

# User Roles

Parent

Student

Registrar

Administrator

ICT Administrator

Each role has independent permissions.

---

# Database Philosophy

PowerSchool remains the source of truth.

Parents never write directly to core student tables.

Workflow

Parent edits

↓

Pending Changes

↓

Registrar Approval

↓

PowerSchool Update

---

# Design Goals

Modern

Responsive

Fast

Accessible

Minimal clicks

Mobile friendly

---

# Technology

HTML5

CSS3

Vanilla JavaScript

PowerSchool Plugin Framework

Git

GitHub

---

# Release Strategy

Semantic Versioning

0.x Development

1.0 Production

Future releases:

1.1

1.2

2.0

---

# Long-term Vision

NIS Connect becomes the central family portal for

Parents

Students

Teachers

School Services

without replacing PowerSchool.
