# ERP analysis

Use the relevant named companion skill if installed. Otherwise use the workflows below. These apply to ERP work with or without a mobile client.

## Requirements and edge cases — grill-me

Before coding or defining a schema for a material business change, inspect existing workflows, roles, DocTypes, reports, and specifications. Record what the evidence already answers. Interview the user on consequential gaps, starting with the highest-impact question and using concrete scenarios and a recommended default. Follow each answer to the rules it affects.

Confirm actors and approval limits, record ownership, sources of truth, lifecycle events, exceptions, and who handles recovery. Walk through relevant cases such as partial quantities, returns, cancellation, duplicate submissions, backdating, closed periods, concurrent edits, and intercompany transactions. Record decisions and examples as OpenSpec acceptance criteria where applicable. Pause dependent implementation when a missing business decision could change permissions, postings, or the data model. Proceed with independent design work and label provisional assumptions.

## Root cause and side effects — five-whys, systems-thinking, analytical-thinking

Define the discrepancy with an expected result, actual result, affected records, company, period, and units. For a stock-versus-ledger mismatch, reconcile the same transaction population and cut-off, then trace the originating voucher, stock movements, valuation, GL entries, and downstream reports. For a metric anomaly, verify the definition, filters, denominators, and time boundaries first.

Ask why at each causal step and attach evidence. Branch when multiple explanations fit. Stop at a verified cause or specify the smallest read-only check that would distinguish hypotheses. Map affected modules and consider reversals, reposting, integrations, permissions, and reporting. Propose the fix, any separate data repair, and regression evidence. Treat live corrections as a separate authorized operation.

## Rollout stress test — pre-mortem, first-principles-thinking

Start with business invariants such as authorized postings, auditable reversals, balanced accounting, and reconciled quantities and values. Challenge inherited defaults against policy and transaction evidence.

Assume the release failed. For each credible failure, record the trigger, impact, detection signal, preventive test, owner, and recovery or containment action. Rehearse applicable cases with representative data. Include interrupted migrations and reruns, tax rounding and invoice reversals, and concurrent peak activity or queue backlog. Define measurable go/no-go checks before rollout, using confirmed business tolerances and representative volumes. Record which checks passed, which remain unverified, and who accepts residual risk.
