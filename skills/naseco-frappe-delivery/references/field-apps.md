# Flutter field applications

## Site and sync contract

- Identify the Frappe backend app, intended site, authenticated user, company scope, API version and capabilities. Prefer a single configured site unless switching is required. Isolate local records, credentials, cursors and queues by site and user and enforce company scope. Never replay queued writes across sites or accounts.
- Use the existing Flutter architecture and local store. Read from durable local state and atomically save an offline edit with its outbox entry. Track immutable external_id for offline-created records, a separate per-mutation idempotency key, and a server version for detecting conflicts. Map fields and child tables explicitly between Dart and Frappe.
- Persist queued writes across restarts. Retry transient failures with backoff, acknowledge only after server acceptance, and surface rejected or conflicted changes for recovery. Use stable incremental cursors and define deletion, stale data and conflict behavior per entity. Use a durable attachment queue where needed.
- Treat offline capture as provisional. The site confirms submissions, privileged approvals, reservations and stock or financial posting. Preserve authoritative server snapshots offline when applicable. Verify permission revocation and unsupported contract behavior on reconnect without silently discarding pending work.

## Shared UI

- Reuse the app's existing theme, design tokens and widgets first. Put proven cross-app primitives in a versioned shared package such as naseco_ui. Keep business rules, Frappe calls and sync execution outside presentation widgets.
- Standardize form fields, validation feedback, record lists, navigation, attachment capture and status components. Distinguish saved on device, waiting to sync, accepted by the site, action required and conflict. Pair status colors with readable labels and provide recovery actions.
- Check narrow screens, text scaling, keyboard insets, contrast, touch targets and screen-reader semantics. Exercise affected widgets and run device-to-site checks for offline capture, restart, replay without duplicates, rejection, conflicts and attachment recovery as applicable.
