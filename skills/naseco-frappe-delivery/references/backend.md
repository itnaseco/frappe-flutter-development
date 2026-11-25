# Frappe backend and delivery

- Reuse ERPNext masters and transactions when they match the business meaning. Model custom concepts with explicit ownership and lifecycle. Define DocTypes and child tables before the mobile API mapping. Use snake_case fieldnames and include name in DocType definitions.
- Enforce permissions, company scope, validation and state transitions on the site. Keep domain rules in services or controllers and API handlers thin. Use native document workflows for straightforward approvals.
- For material changes, specify current behavior, intended outcome, permissions, contract compatibility, migration impact and measurable acceptance criteria in the repository's OpenSpec workflow. Record exceptions and ownership.
- Target site-scoped bench operations explicitly. Prefer additive migrations and rehearse on an authorized non-production site with representative data. Compare critical records and business totals before and after. Document recovery and identify irreversible steps.
- Verify permitted and denied operations, business rules, and integration contracts. Report backend verification, mobile/device verification, release readiness, and deployment separately. For a requested Android release, report artifact location, version and compatibility evidence.
