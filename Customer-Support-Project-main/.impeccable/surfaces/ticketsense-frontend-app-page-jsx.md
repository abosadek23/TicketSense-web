---
version: 1
slug: "ticketsense-frontend-app-page-jsx"
primary_target: "TicketSense/frontend/app/page.jsx"
related_targets: []
---

# TicketSense Support Workspace

Scope: Customer-support web app shell and all agent-facing pages. Visitor mode: Operate.

Audience and job: Support agents classify incoming inquiries, review the assigned intent, department, priority, and SLA, process batches, and look up intent or routing rules.

Content and constraints: Keep single and batch classification, CSV import/export, routing rules, and the 27-intent catalog. Keep the FastAPI service and prediction contracts unchanged. Hide Benchmark and API Playground from the agent-facing navigation. Use one verified support-team photo on the home screen only.

## Direction contract

THESIS: TicketSense routes a customer inquiry to the team that can resolve it. Refuse six equal, unrelated top-level tool tabs.

OWN-WORLD: Civic transit wayfinding lends TicketSense deep evergreen navigation, a pale mineral work surface, warm amber and coral state markers, concise workhorse typography, and one clear route line. Standard app navigation and controls remain familiar.

STORY: Agents start at one useful workspace, classify a message, and read the predicted intent, department, priority, and response target as one connected route. Batch, intent lookup, and SLA rules are separate destinations.

FIRST VIEWPORT: A fixed evergreen sidebar groups Overview and Classify, Batch Triage, Intent Catalog, and SLA Routing. The main workspace opens on a compact overview with one documentary support-team photo, clear counts drawn from the existing catalog, and direct actions. The classifier page presents the input and result side by side; a route connector links intent to assigned team and SLA.

FORM: Civic Wayfinding, assigned direction index 3, seed key 046aea2e. Code-led app build. The roll service was unavailable; the user chose this direction over Customer Care Desk.

FINISH: unreviewed and undocumented is unfinished; this build ends with the finish review, the verdict, DESIGN.md, and every shipping raster carrying its provenance

Unresolved: Whether Benchmark and API Playground should return in a separately authenticated developer workspace is outside this scope.
