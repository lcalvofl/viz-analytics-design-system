# Architecture

## Purpose

This document defines the conceptual hierarchy of the Analytical Design System.

The hierarchy organizes analytical information independently of any implementation technology or user interface.

---
| Level | Purpose |
|-------|---------|
| Analytical Module | Represents an analytical domain. |
| Dashboard | Represents an analytical topic. |
| Section | Represents one aspect of the analytical topic. |
| Analytical Unit | Represents the smallest independent piece of analytical information. |
---

## Description

The hierarchy is based on conceptual responsibilities rather than interface elements.

- An Analytical Module represents an analytical domain.
- A Dashboard represents an analytical topic.
- A Section develops one aspect of that topic.
- An Analytical Unit represents the smallest independent analytical information element.

---

## Relationships

- An Analytical Module contains one or more Dashboards.
- A Dashboard contains one or more Sections.
- A Section contains one or more Analytical Units.
