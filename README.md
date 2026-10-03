# CarePoint Hospital Management System

A responsive, browser-based hospital operations dashboard built with plain HTML, CSS, and JavaScript. Open `index.html` to use the demo. No package install or build step is needed.

## Included workflows

- Overview dashboard with patient, appointment, bed capacity, revenue, activity, and department summaries.
- Patient records: search, filter, add a patient, view a record summary, and export CSV.
- Appointments: booking, search, date filtering, and status updates.
- Medical staff directory with availability updates and staff creation.
- Ward and bed occupancy dashboard.
- Laboratory orders with priority and workflow status updates.
- Pharmacy inventory with low stock indications and restocking.
- Billing with invoice creation and payment status updates.
- Reports with CSV export and hospital profile settings.
- Responsive layout for desktop, tablet, and mobile.

Data is stored in browser `localStorage`, so changes remain on that device and browser. Seed data illustrates the screens; summary totals also include illustrative baseline values to make the dashboards feel populated. This is a front-end MVP, not a production clinical record system.

## Scaling beyond 2,000 users

HTML/CSS/JavaScript can implement the interface, but browser storage cannot safely share or synchronize records among 2,000 users. For a real multi-user rollout, connect this UI to an API and shared database. Recommended foundations:

1. A versioned REST API (for example, Node.js with Fastify or Express) and PostgreSQL as the authoritative store.
2. Authentication, role-based access control, and least-privilege permissions for administrators, clinicians, reception, lab, pharmacy, and billing.
3. Server-side validation, audit trails, backups, encryption in transit and at rest, and secure handling of patient data appropriate to the deployment jurisdiction.
4. Pagination, indexed search, connection pooling, rate limits, observability, and load testing at expected peak concurrency.
5. Replace localStorage reads/writes with authenticated API calls; keep only non-sensitive UI preferences in browser storage.

The current demo has no server, authentication, access control, shared data, or clinical compliance guarantees. Do not enter real patient information until those are implemented and reviewed.
