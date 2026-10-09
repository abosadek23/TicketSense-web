# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

Customer support agents handling incoming customer inquiries.

## Product Purpose

TicketSense classifies customer support messages so agents can identify the customer's intent and route the inquiry to the right department with a priority and service-level target.

## Positioning

TicketSense combines intent classification across 27 intents and 11 categories with department routing and SLA guidance in one workflow.

## Operating Context

Agents classify a single inquiry, process a batch of inquiries from text or CSV, look up intent definitions and example queries, and refer to departmental routing and SLA rules.

## Capabilities and Constraints

- The web frontend is a Next.js application and communicates with a separate FastAPI backend.
- Preserve the existing prediction and batch-prediction API contracts and all backend behavior.
- Keep single-ticket classification, batch triage, the intent catalog, and SLA routing available in the redesigned frontend.
- The user chose to hide model benchmarks and the API playground from the customer-support interface; do not delete or modify their backend services.

## Brand Commitments

The product name is TicketSense. The interface should read as a practical support-agent application.

## Evidence on Hand

- The trained classifier is in `TicketSense/backend/artifacts/bestmodel.pkl`.
- The existing project reports 99.84% held-out test accuracy and 0.9980 Macro-F1 in its benchmark content. Preserve these values as existing project claims; do not add new performance claims.
- Intent definitions and routing metadata are maintained in `TicketSense/frontend/lib/intents-data.js` and `TicketSense/backend/artifacts/intent_metadata.json`.

## Product Principles

- Make classification and the resulting route easy to act on.
- Keep support-agent workflows distinct from developer and model-evaluation tools.
- Preserve the existing classifier behavior while improving wayfinding and clarity.
- Present model and SLA facts accurately.