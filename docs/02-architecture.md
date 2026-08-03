# Architecture

## Purpose

This document defines the conceptual architecture of the Analytical Design System.

It describes the hierarchical organization of analytical interfaces independently of any implementation technology or user interface.

---

## Description

The architecture is organized according to conceptual responsibilities rather than interface implementation.

Each level represents a different scope of analytical organization, from business domains to individual analytical elements.

| Level | Purpose |
|-------|---------|
| Analytical Module | Represents an analytical domain. |
| Dashboard | Represents an analytical topic. |
| Section | Represents one aspect of the analytical topic. |
| Analytical Unit | Represents the smallest independent piece of analytical information. |

---

## Relationships

- An **Analytical Module** contains one or more **Dashboards**.
- A **Dashboard** contains one or more **Sections**.
- A **Section** contains one or more **Analytical Units**.

---

## Elements

### Section

A Section represents a self-contained analytical area within a Dashboard.

A Section consists of:

- Header
- Body
- Footer (optional)

The Body contains the analytical content of the Section.

---

### Section Header

Every Section includes a Header composed of two areas.

#### Identification

The identification area contains either:

- a **Title** (single-view Sections), or
- a **View selector** (Tabs or another selector) for Sections with multiple Views.

#### Contextual Actions

Actions always apply to the active View.

Actions are grouped by responsibility:

- **Content selection**
  - Controls which information is visible in the active View.

- **Other actions**
  - Display options
  - Sorting
  - Export
  - Other contextual operations

The interaction pattern (icons, popovers, dialogs, side panels, etc.) is implementation-specific and is not defined at the architectural level.

---

### Section Body

The Body contains one or more Analytical Units.

The internal organization of Analytical Units depends on the selected visualization and is outside the scope of the architectural model.

---

### Section Footer (optional)

The Footer contains complementary information related to the Section.

Typical examples include:

- Data source
- Last update
- Methodological notes
- Additional context
