---
name: TicketSense Support Workspace
description: A clear routing workspace for customer-support agents.
colors:
  evergreen: "#124b45"
  ink: "#183e37"
  paper: "#e8f1e9"
  paper-raised: "#f7faf5"
  divider: "#ccdcd2"
  route-amber: "#e6bf5b"
  priority-coral: "#df715b"
typography:
  display:
    fontFamily: "Public Sans, sans-serif"
    fontSize: "30px"
    fontWeight: 700
    lineHeight: 1.2
  body:
    fontFamily: "Public Sans, sans-serif"
    fontSize: "14px"
    fontWeight: 400
    lineHeight: 1.6
  label:
    fontFamily: "IBM Plex Mono, monospace"
    fontSize: "11px"
    fontWeight: 500
rounded:
  sm: "6px"
  md: "8px"
  lg: "12px"
spacing:
  sm: "8px"
  md: "16px"
  lg: "24px"
  xl: "32px"
components:
  button-primary:
    backgroundColor: "{colors.route-amber}"
    textColor: "{colors.ink}"
    rounded: "{rounded.sm}"
    padding: "10px 16px"
  nav-item-active:
    backgroundColor: "{colors.paper}"
    textColor: "{colors.evergreen}"
    rounded: "{rounded.sm}"
    height: "44px"
  surface-card:
    backgroundColor: "{colors.paper-raised}"
    textColor: "{colors.ink}"
    rounded: "{rounded.md}"
    padding: "20px"
---

# Design System: TicketSense Support Workspace

## Overview

**Creative North Star: "Civic Wayfinding"**

TicketSense is an operational workspace, not a model demonstration. Its visual language borrows the legibility of civic route systems: an evergreen rail gives the app a stable home, a pale mineral surface keeps long work sessions comfortable, and warm markers distinguish the next step in a ticket's route.

The interface keeps standard web navigation and controls. Its signature route line links predicted intent, assigned team, and response target without competing with the customer message. One documentary support-team photograph appears on the overview only. The image is sourced from Unsplash photo `1521737711867-e3b97375f902` and loaded by `DashboardOverview.jsx`.

**Key Characteristics:**
- Evergreen navigation rail with a selected destination in pale green.
- Open, pale work surface with restrained borders and compact operational labels.
- Amber for primary action and route junctions; coral for urgent states.
- The API and model evaluation tools are outside the agent-facing navigation.

## Colors

The palette pairs deep evergreen with a cool, pale green ground; amber and coral are reserved for action and service meaning.

### Primary
- **Civic Evergreen** (#124b45): Main desktop navigation and the overview feature surface.
- **Route Amber** (#e6bf5b): Primary action and the junction marker in a ticket route.

### Secondary
- **Priority Coral** (#df715b): High-attention priority and error states.

### Neutral
- **Deep Ink** (#183e37): Primary text on light surfaces and text on amber actions.
- **Mineral Paper** (#e8f1e9): Main application ground and selected navigation background.
- **Raised Paper** (#f7faf5): Cards and the top workspace header.
- **Divider Green** (#ccdcd2): Structural borders and rules.

### Named Rules
**The Route Marker Rule.** Amber marks an action or an explicit route junction; coral is reserved for priority and error meaning.

## Typography

**Display Font:** Public Sans (sans-serif)
**Body Font:** Public Sans (sans-serif)
**Label/Mono Font:** IBM Plex Mono (monospace)

**Character:** Public Sans keeps messages and destinations plain at a glance. IBM Plex Mono is limited to identifiers, measurements, and compact technical values.

### Hierarchy
- **Display** (700, 30px, 1.2): Main workspace headline.
- **Headline** (700, 24px): Page heading and major result label.
- **Title** (700, 20px): Workbench sections and card titles.
- **Body** (400, 14px, 1.6): Descriptions and workflow copy.
- **Label** (500, 11px): Compact navigation group labels and measured values.

## Layout

On desktop, a 248px evergreen rail anchors the workspace beside a flexible content column. Main content is capped at 1500px and uses a 24px outer rhythm with 16px control spacing. At the 1024px Tailwind breakpoint, the rail gives way to a horizontally scrollable mobile navigation above the content. The overview feature stacks its image above its copy below 768px; other dense tables retain horizontal scrolling.

## Elevation & Depth

Depth is mostly tonal: the raised paper surface separates from the mineral ground with a fine green divider. Use no ambient shadow on routine cards. Keep the overview feature flat and use an offset only where a real floating layer is introduced.

### Named Rules
**The Surface Rule.** Separate work areas with surface tone and spacing before adding shadow.

## Shapes

Controls use compact 6px corners, repeated work cards use 8px corners, and the overview feature may use 12px corners. Route lines and service dots remain geometric and small; cards are not nested inside other cards.

## Components

### Buttons
- **Shape:** Compact rounded rectangles (6px).
- **Primary:** Amber fill (#e6bf5b), ink text (#183e37), 10px 16px padding.
- **Hover / Focus:** A brighter amber hover; a visible 2px coral keyboard outline with 3px offset.
- **Secondary / Ghost:** Text-forward actions use evergreen text and an arrow icon; avoid extra filled pills.

### Cards / Containers
- **Corner Style:** 8px for repeated work items; 12px for the overview feature.
- **Background:** Raised paper (#f7faf5) on the paper ground; evergreen for the overview feature.
- **Shadow Strategy:** Flat, separated by a fine divider.
- **Internal Padding:** 20px for summary and workbench items; 24px or more for the feature surface.

### Inputs / Fields
- **Style:** Dark evergreen-tinted field with light text, a fine border, and a 12px corner.
- **Focus:** Visible 2px coral keyboard outline.
- **Error / Disabled:** Coral communicates errors; disabled actions reduce opacity and remain visibly inactive.

### Navigation
- **Style:** Desktop uses a fixed evergreen side rail with grouped destinations and a pale selected row. Mobile uses a horizontally scrollable evergreen bar with the active destination reversed to pale paper. A compact live indicator describes classifier service availability.

### Ticket Route
- **Style:** A thin route line links Intent, Assigned team, and Response target. Each stage has a labeled marker, with amber identifying the handoff junction.

## Do's and Don'ts

### Do:
- **Do** keep classifier, batch triage, catalog, and SLA routing as distinct agent destinations.
- **Do** keep the support-team photograph on the overview only.
- **Do** preserve the model's result, assigned routing, confidence, and SLA values exactly.

### Don't:
- **Don't** bring model benchmarks or API controls into the agent navigation.
- **Don't** use route colors decoratively; keep amber and coral tied to their named jobs.
- **Don't** change the FastAPI contract from frontend presentation work.