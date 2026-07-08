# AI Development Rules

These rules apply to ALL AI-generated code.

Failure to follow these rules is considered a bug.

---

# General

Always write production-quality code.

Do not generate placeholder code unless explicitly requested.

Do not generate duplicated code.

Prefer reusable components.

Document all public methods.

Keep files small and focused.

---

# PowerSchool

Never modify PowerSchool core files.

Never overwrite guardian pages.

Never edit existing PowerSchool HTML.

Always extend rather than replace.

Use supported PowerSchool extension points.

---

# Architecture

Business logic must never live inside HTML.

Configuration must never be hardcoded.

Separate

HTML

CSS

JavaScript

Configuration

Database

Logging

Services

Repositories

---

# JavaScript

Use modern ES6.

No jQuery unless PowerSchool requires it.

No inline JavaScript.

Use modules where possible.

Avoid global variables.

---

# CSS

No Bootstrap dependency.

No external CSS frameworks.

No inline CSS.

Use CSS variables.

Prefer Flexbox and Grid.

Responsive by default.

---

# HTML

Semantic HTML only.

Accessible forms.

Labels for every input.

Keyboard accessible.

Mobile friendly.

---

# Database

Never modify PowerSchool tables directly.

Use migration scripts.

Every schema change must be versioned.

Store plugin configuration separately.

Store audit logs separately.

---

# Logging

Every important action must be logged.

Examples

Login

Configuration changes

Parent submission

Approval

Rejection

Errors

---

# Security

Validate every input.

Escape all output.

Never trust client-side data.

Follow least-privilege principles.

Protect against CSRF and XSS where applicable.

---

# Feature Flags

Every module must support enable/disable.

Never hardcode visibility.

Dashboard must read enabled modules dynamically.

---

# Configuration

All configurable values belong in Settings.

Examples

School name

Theme

Academic year

URLs

Menu visibility

Maintenance mode

---

# Documentation

Every new feature must update

README

CHANGELOG

Developer Guide

Database documentation

---

# Version Control

Every feature must have

Git branch

Commit message

Release notes

---

# Performance

Avoid unnecessary database queries.

Reuse components.

Minimize JavaScript.

Optimize CSS.

---

# Code Review Checklist

Before completing any task

✔ Compiles

✔ Responsive

✔ Accessible

✔ Upgrade-safe

✔ Documented

✔ Logged

✔ Configurable

✔ Tested

If any item fails, the task is not complete.
