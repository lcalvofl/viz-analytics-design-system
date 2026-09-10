# Layout

## Purpose

This document defines how analytical content is organized within the available application space.

It describes the spatial organization of the Design System independently of the implementation technology.

---

## Scope

The initial layout specification is desktop-first.

The Design System supports different analytical content types while maintaining a consistent layout structure.

---

## Layout Hierarchy

```
Host Application (optional)

├── Navigation
└── Content Area
    ├── Dashboard
    └── Hybrid Analytical Content
   

Example of Dashboard:

┌──────────────────────────────┐
│ KPI │ KPI │ KPI │ KPI │ KPI  │
├──────────────────────────────┤
│ Line Chart (6) │ Map (6)     │
├──────────────────────────────┤
│ Table (12)                   │
└──────────────────────────────┘

Example of Hybrid Content

┌──────────────────────────────┐
│ Title                        │
│ Introductory text            │
├──────────────────────────────┤
│ Chart (6) │ Explanatory text │
├──────────────────────────────┤
│ Interactive infographic (12) │
├──────────────────────────────┤
│ Conclusions                  │
└──────────────────────────────┘

```

The Design System may be embedded inside a Host Application or run as a standalone web application.

Regardless of the hosting environment, the internal layout remains identical.

---

## Content Area

The Content Area is the workspace where analytical content is displayed.

It uses a common layout system shared by all supported content types.

---

## Grid

The Content Area uses a 12-column grid.

### Phase A — Top Navigation

The current layout uses a top navigation pattern. Since navigation does not occupy horizontal space, the grid uses the full viewport width.

At the 1280 px reference viewport:

- Columns: 12
- Column width: 85 px
- Gutter: 20 px
- Left margin: 20 px
- Right margin: 20 px

The grid spans the full 1280 px viewport.

## Column Spans

The initial layout supports the following column spans:

- 2
- 3
- 4
- 6
- 12

The two-column span is reserved for compact KPI containers.

Five- and seven-column layouts are intentionally excluded from the initial version.

---

## Rows

A row is composed of one or more Sections whose combined width occupies the twelve-column grid.

Examples include:

- 2 + 2 + 2 + 2 + 2 + 2
- 3 + 3 + 3 + 3
- 4 + 4 + 4
- 6 + 6
- 3 + 3 + 6
- 2 + 4 + 6
- 12

Sections belonging to the same row share the same height.

---

## Scrolling

The Design System never allows horizontal scrolling of the entire Content Area.

Vertical scrolling may be used when required.

The interface should clearly indicate when additional content exists below the visible area.

Selected Sections may remain fixed while the remaining content scrolls.

---

## Open Questions

- Final margin values.
- Final gutter values.
- Responsive adaptations.
- Sticky Section behaviour.
- Additional analytical content types.
