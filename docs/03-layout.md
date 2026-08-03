# Layout

## Purpose

This document defines how analytical containers are distributed within a Dashboard.

It describes the relationship between the application shell, the dashboard content area and the layout grid. It does not define the internal layout of Sections, KPIs or visualization components.

---

## Scope

The initial layout specification is desktop-first.

Mobile, tablet and other device-specific adaptations are outside the current implementation scope, but the architecture must allow alternative layouts and visualization strategies to be introduced later.

---

## Application Shell

The Application Shell defines the highest-level structure of the analytical interface.

It may use top or side navigation, depending on the product or Analytical Module.

```text
Viewport
└── Application Shell
    ├── Global Navigation
    └── Main
        ├── Dashboard Header and global controls
        └── Content Area
```

Navigation is independent from the Dashboard grid.

The navigation placement should remain consistent across the Dashboards belonging to the same product or Analytical Module.

---

## Content Area

The Content Area is the space available for Dashboard content after accounting for global navigation, headers and other application-level elements.

The Dashboard grid is applied exclusively inside the Content Area.

Changes to navigation width or placement affect the available Content Area, but do not change the internal anatomy of Dashboard containers.

---

## Grid

The Dashboard uses a twelve-column fluid grid.

Initial desktop values:

| Property | Value | Status |
|---|---:|---|
| Columns | 12 | Accepted |
| Outer margin | 24 px | Provisional |
| Gutter | 20 px | Provisional |
| Minimum validation width | 1280 px | Provisional |

The margin and gutter remain constant within the initial desktop range. Additional available width increases the width of the grid columns.

The grid should also be validated at larger desktop widths, including 1400 px and 1920 px.

---

## Allowed Spans

Dashboard containers may initially use the following column spans:

```text
2, 3, 4, 6 and 12 columns
```

The two-column span is intended for compact analytical containers, typically KPIs.

The three-, four-, six- and twelve-column spans support standard analytical containers.

Five- and seven-column combinations are not part of the initial layout system.

---

## Composition Rules

Containers placed in the same row should collectively use the twelve-column grid.

Examples include:

```text
2 + 2 + 2 + 2 + 2 + 2
3 + 3 + 3 + 3
4 + 4 + 4
6 + 6
3 + 3 + 6
2 + 4 + 6
12
```

The examples describe valid span combinations, not fixed orders. Designers may reorder containers according to information hierarchy and reading flow.

A row composed exclusively of six two-column containers is reserved for homogeneous compact KPIs or equivalent compact analytical elements.

The grid defines available space. It does not determine which visualization type is suitable for that space.

---

## Height and Scrolling

Container height is not determined by its column span.

Dashboard containers may use different heights when required by their content and analytical purpose.

A visualization that requires more horizontal space may provide internal horizontal scrolling, provided that:

- scrolling remains contained within the analytical container;
- it does not create horizontal scrolling for the complete Dashboard;
- controls, identification and surrounding Dashboard content remain fixed and usable.

Dashboard-level scrolling behaviour will be defined separately from internal visualization scrolling.

---

## Responsive Behaviour

Responsive decisions should be based on the available Content Area rather than exclusively on the viewport width.

A side navigation, expanded panel or embedded context may reduce the Content Area even when the physical screen is large.

The initial system will be designed and validated for desktop. Smaller devices may require:

- rearranging containers;
- changing navigation behaviour;
- stacking content;
- or replacing a visualization with a device-appropriate alternative.

These adaptations will be specified in a later phase.

---

## Open Questions

- Final outer margin and gutter values.
- Minimum usable Content Area with expanded side navigation.
- Behaviour of the twelve-column grid when the Content Area becomes too narrow.
- Rules for collapsing or overlaying side navigation.
- Dashboard-level vertical scrolling policy.
- Final name and anatomy of compact KPI containers.
