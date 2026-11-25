---
name: naseco-frappe-delivery
description: Design, build, review, and verify NASECO Frappe and ERPNext custom apps and Flutter field clients, including offline sync, shared UI, OpenSpec, BPMN, DMN, and Mermaid documentation.
---

# NASECO Frappe Delivery

Resolve reference links from this skill directory. Use the host agent's available tools to inspect project files and follow its permission model. Specialist skills are optional. When unavailable, continue with these references and identify any verification you cannot perform.

Identify the company objective, operational owner, users, success criteria, and applicable company policies. Treat missing policy as a decision to resolve, especially for approvals, stock, finance, and regulated records.

Choose the requested mode: explore, specify, implement, review, or release. Explore is read-only. Identify the app, repositories, target site and environment, existing conventions, and active OpenSpec change. Preserve existing edits in every repository. Use installed OpenSpec skills for their corresponding modes when available. Otherwise inspect the repository's specifications directly and report any unavailable validation.

- For Frappe work read [backend and delivery](references/backend.md). Use installed frappe-app-dev for framework mechanics.
- For Flutter or sync work read [field apps](references/field-apps.md). Use available approved Flutter skills for architecture, persistence, theming, responsive layout, accessibility, and testing as applicable.
- For process, decisions, or explanation read [models and diagrams](references/models.md). Use approved runtime-specific skills only for the selected runtime.

Every field app uses an identified Frappe site as its authoritative backend. Flutter owns local capture and feedback. Frappe owns authorization, business validation, and accepted records. Use approved specialist skills when available; these references provide the NASECO baseline when they are absent. Installation, live deployment, and production mutations require authorization.

Trace material changes from business requirement through OpenSpec, applicable model and code, and acceptance evidence. Report what passed and what remains unverified across the backend, field device, migration, and release.
