# Throughline — Phase 1 React prototype

An interactive, high-fidelity React wireframe for the confirmed Phase 1. The original compiled demo in `../throughline` remains available. This project contains editable React source.

## Start locally

```sh
npm ci
npm run dev
npm run build
```

The application uses hash navigation, so every screen is directly linkable. All data is synthetic. Changes are saved in this browser's localStorage under `throughline-p1-v1`. **Reset demo** restores the seeded workspace. This is a frontend prototype: Supabase and provider APIs have not been connected, no emails or messages are sent, and role settings do not enforce backend authorization.

## Included screens and working interactions

- **Overview:** customer counts, consent readiness, completed value, campaigns, return outcomes, business-unit summaries, actionable follow-ups.
- **Customers:** search, lifecycle and permission filters, CSV export, contact creation and exact-identifier duplicate checks. Customer drawer includes notes, permission evidence, follow-ups, source context and outcomes.
- **Data imports:** Sthalam / Shopify exports; Woodinc customer reports; Kreate / Petpooja reports. Customer CSV upload, sample report, field mapping, preview, skipped duplicates/invalid rows and local import history.
- **Campaigns:** list/calendar, status and search filters, a five-step wizard, recipient eligibility, approved-template selection, personalized WhatsApp preview, IST scheduling, draft saving and simulated execution.
- **Campaign reports:** sent/delivered/read/replied funnel, failures, recipient states, completed outcomes, repeat visits and matching-evidence labels.
- **Templates:** brand-specific marketing/utility examples, pending and approved sample states, message preview and simulated approval.
- **Audiences:** dynamic and snapshot audience creation, lifecycle/permission criteria and recipient preview.
- **Shared inbox:** thread filtering, assignment, sample replies, internal notes, resolve/reopen, customer context and booking-request capture.
- **Ad performance:** Meta/Google reports, spend, impressions, clicks, CTR, native form leads and CPL. Campaign details distinguish platform conversions from CRM captured leads and recorded outcomes. Ad creation stays in Ads Manager.
- **Lead pipeline:** board/list, source campaign/form/provider ID context, owner/stage changes, follow-ups, mark won and simulated native form capture. New contacts start with unknown marketing permission.
- **Orders & bookings:** completed value, repeat outcome indicators, manual recording, status updates, CSV export and outcome-report imports. Unmatched guest bills are retained without inferred identity or campaign attribution.
- **Connections:** separate sample WhatsApp sender accounts, Meta/Google reporting connectors and file-based source refresh history. Simulated reconnect/disconnect and sync controls.
- **Team & access:** sample team creation, roles and business scopes; no real invitations.
- **Shared UX:** business-unit filter, report-period selector, workspace search, notifications, feature overview, keyboard shortcut, accessible dialogs and responsive navigation.

## Sample data

180 customers, 5 WhatsApp campaigns, 5 templates, 3 audiences, 42 outcomes, 5 ad campaigns, 24 identifiable leads, 9 support conversations and 3 source imports. All contact emails use example.com. Report figures are illustrative, not client results. Reporting periods are fixed sample dates (7–13 October 2026 and 11–13 October 2026).

## Campaign design reference

The campaign workflow was informed by WATI's official documentation:

- [Guided first campaign setup](https://support.wati.io/en/articles/15165095-send-your-first-whatsapp-campaign-with-guided-setup): contacts, template selection/approval, scheduling and campaign overview.
- [Reusable custom segments](https://support.wati.io/en/articles/14192386-how-to-create-and-use-custom-segments-in-wati): dynamic/static audience groups and preview.
- [Campaign platform](https://www.wati.io/page/campaigns/): delivery/reply reporting and exportable results.

The design uses original Throughline styling and adds native CRM context, business-unit ownership, identifiable ad leads and customer-linked outcomes. Drip campaigns, omnichannel fallback, automated ad creation and anonymous visitor identification are not included in this Phase 1 prototype.

## Validation

Production build passed. Browser QA exercised all 14 routes, the campaign wizard and simulated run, customer import/review, inbox replies/notes/bookings, native form lead simulation, local persistence and four mobile screens. No page errors or page-level mobile overflow were detected. Sample campaign/lead business scopes and delivery totals were checked for consistency. Outcome-report import was separately checked for matched/guest/invalid results and idempotent reference handling.
