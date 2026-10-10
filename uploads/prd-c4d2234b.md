# PRD: Hajj & Umrah Platform — MVP

## Problem Statement

The agency runs Hajj and Umrah trips for many pilgrims. Today, most of the work runs on WhatsApp, phone calls, Excel sheets, and paper.

**For the agency staff:**
- Pilgrim details, documents, visa status, and payments sit in different places. It is hard to see who is ready and who is not.
- Documents come in on WhatsApp, often blurry or wrong. Nobody tracks what is missing.
- Staff get the same calls again and again: "Is my visa ready?", "What time is my flight?", "How much do I still owe?"
- Typing passport details again for the Saudi partner takes a lot of time and causes mistakes.

**For the pilgrims:**
- Their ticket, visa, hotel, and flight details come as separate PDFs and messages. These are hard to read on a phone, especially for older people.
- They do not know which documents are still needed, or why a document was not accepted.
- They do not know how much they have paid and how much is left.
- During the trip they often have weak or no internet, but that is exactly when they need their ticket, visa, and hotel details.
- Often one family member (for example, a son) handles everything for his parents, but no tool supports this.

## Solution

One system with three parts:

1. **Public website** — shows the agency's packages. Staff manage packages, photos, and FAQs themselves. Every enquiry goes to the admin panel as a lead.
2. **Admin panel** — staff manage pilgrims, family groups, packages and batches (departures), trip details, the document checklist, visa status, and offline payments. A dashboard shows the key numbers.
3. **Pilgrim portal** — each pilgrim logs in with email + OTP. They see their flight, hotel, visa, ticket, trip timeline, documents, and payment balance as clean, simple cards, in English, Hindi, or Urdu. They can upload their documents. A group leader can manage the whole family. Key trip details and an emergency card open even without internet.

The MVP is built for one agency, but every record carries an agency ID so it can become a multi-agency SaaS later.

## User Stories

### Login and accounts
1. As a pilgrim, I want to log in with my email and a one-time code, so that I don't need to remember a password.
2. As a pilgrim, I want to stay logged in on my phone, so that I don't have to log in every time I open the portal.
3. As a staff member, I want to create a pilgrim account from the admin panel, so that walk-in and phone bookings get portal access.
4. As a staff member, I want the system to email the pilgrim a welcome message with a login link when I create their account, so that they can start using the portal.
5. As a staff member, I want to log in to the admin panel with email + OTP, so that login is the same simple method for everyone.
6. As an owner, I want to add, disable, and change the role of staff accounts, so that I control who can use the admin panel.

### Family groups
7. As a staff member, I want to put pilgrims into a family group and pick a group leader, so that one person can manage the whole family.
8. As a group leader, I want to see every member's trip details, documents, and payments, so that I can manage everything for my parents or family.
9. As a group leader, I want to upload documents for any member of my group, so that members without a smartphone are still covered.
10. As an adult group member with my own email, I want to log in and see only my own details, so that I can open my ticket and visa on my own phone.
11. As a staff member, I want to add a pilgrim who has no email under a group leader, so that they are still fully managed.
12. As a staff member, I want to mark which male relative is the mahram for each woman in a group, so that the agency meets Hajj rules and can check it.
13. As a staff member, I want a warning when a woman who needs a mahram has none linked in the same batch, so that the problem is caught early.

### Packages and batches
14. As a staff member, I want to create a package template (name, Hajj or Umrah, duration, hotels, inclusions, photos, description), so that I describe a trip once and reuse it.
15. As a staff member, I want to create a batch (one departure) from a package, with its own dates, total seats, and prices, so that I can run the same package many times.
16. As a staff member, I want to set prices per room type (Quad, Triple, Double) and for child and infant, so that each pilgrim gets the correct price.
17. As a staff member, I want to add optional extras with prices (for example, wheelchair or an extra Ziyarat tour), so that I can charge for add-ons.
18. As a staff member, I want to create a private trip for one family with its own hotels, dates, and price, so that I can sell custom trips.
19. As a staff member, I want private trips hidden from the public website, so that custom deals stay private.
20. As a staff member, I want to see seats booked and seats left in each batch, so that I don't overbook.
21. As a staff member, I want to book a pilgrim into a batch with a room type and extras, so that the system knows their trip and their total price.

### Trip details (flights, hotels, tickets)
22. As a staff member, I want to enter flight details once per batch (airline, flight number, from, to, date, time), so that every pilgrim in the batch sees them without extra typing.
23. As a staff member, I want to enter hotel details once per batch (city, hotel name, address in English and Arabic, check-in, check-out), so that every pilgrim sees their hotels.
24. As a staff member, I want to add personal items per pilgrim (ticket PDF, PNR, seat, visa number, visa PDF), so that each person gets their own documents.
25. As a staff member, I want to override a batch flight or hotel for one pilgrim, so that special cases (for example, a different return date) are correct.
26. As a pilgrim, I want to see my flight as a clean card (for example, "SV-763, Mumbai → Jeddah, 12 Nov, 4:30 AM"), so that I can read it easily on my phone.
27. As a pilgrim, I want to open the original ticket or visa PDF below the card, so that I can show it at the airport or immigration.
28. As a pilgrim, I want a simple trip timeline (flight, Makkah hotel, Madinah hotel, return flight), so that I understand my whole journey at a glance.

### Document checklist
29. As a staff member, I want to set the required documents for each package (passport, photo, ID, vaccine certificate, etc.), so that every pilgrim knows exactly what to give.
30. As a pilgrim, I want to see my document checklist with a status for each item (Missing, Pending, Approved, Rejected), so that I know what is still needed.
31. As a pilgrim, I want to upload a document by taking a photo or choosing a file, so that I can submit from my phone.
32. As a staff member, I want to approve or reject each upload with a reason, so that the pilgrim knows what to fix.
33. As a pilgrim, I want to get an email when a document is rejected, with the reason, so that I can upload it again quickly.
34. As a staff member, I want to upload a document for a pilgrim, so that documents sent to us on WhatsApp are also in the system.
35. As a staff member, I want to see a list of all pending uploads waiting for review, so that I can work through them fast.
36. As a staff member, I want to see which pilgrims in a batch have all documents approved, so that I know who is ready for visa submission.
37. As an owner, I want passport and ID files kept private and opened only through short-lived links, so that sensitive data is not exposed.
38. As an owner, I want a record of who opened, uploaded, approved, or rejected each document, so that there is accountability.

### Visa
39. As a staff member, I want each pilgrim to have a visa status (Documents pending, Documents complete, Submitted, Approved, Rejected), so that everyone knows where the visa stands.
40. As a staff member, I want the status to move to "Documents complete" automatically when all required documents are approved, so that I don't have to update it by hand.
41. As a staff member, I want to update the visa status for many pilgrims in a batch at once, so that I save time.
42. As a pilgrim, I want to see my visa status as simple steps, so that I don't need to call the office.
43. As a pilgrim, I want an email when my visa is approved or rejected, so that I know straight away.
44. As a staff member, I want to download passport details for a batch as Excel in the Saudi partner's format, so that I don't retype them.
45. As a staff member, I want a warning when a pilgrim's passport expires too soon for travel, so that it is fixed before visa submission.

### Payments (offline only in MVP)
46. As an accounts staff member, I want to record a payment (cash, UPI, bank transfer, cheque) with date, amount, and reference, so that all money received is tracked.
47. As an accounts staff member, I want one payment to cover several members of a family group, so that a group leader's single payment is split correctly.
48. As a pilgrim, I want to see my total price, amount paid, and balance, so that I always know what I owe.
49. As a group leader, I want to see the total, paid, and balance for my whole family, so that I can plan payments.
50. As a pilgrim, I want to download a receipt for each payment, so that I have proof.
51. As a pilgrim, I want to see the agency's bank details in the portal, so that I can pay by bank transfer.
52. As an accounts staff member, I want every receipt to have a unique receipt number, so that accounts stay clean.
53. As an accounts staff member, I want to fix a wrong payment by reversing it (not deleting it), so that the history stays correct.
54. As an accounts staff member, I want to export payments as Excel, so that our CA can enter them in Tally.

### Cancellation (basic in MVP)
55. As a manager, I want to cancel a pilgrim's booking with a reason, so that the seat becomes free again.
56. As an accounts staff member, I want to record a refund against a cancelled booking, so that the balance is correct.

### Public website and leads
57. As a visitor, I want to see all open packages with photos, dates, hotels, and prices, so that I can choose a trip.
58. As a visitor, I want to see a package detail page with inclusions and FAQs, so that I understand what I get.
59. As a visitor, I want to send an enquiry with my name, phone, email, and interested package, so that the agency calls me back.
60. As a visitor, I want a WhatsApp button on each package, so that I can talk to the agency directly.
61. As a visitor, I want to view the website in English, Hindi, or Urdu, so that I can read it in my language.
62. As a staff member, I want to add and edit packages, photos, and FAQs from the admin panel, so that I don't need a developer.
63. As a staff member, I want each enquiry to appear as a lead with a status (New, Called, Interested, Booked, Not interested), so that no enquiry is forgotten.
64. As a staff member, I want to add a note to a lead, so that the team knows what was discussed.
65. As a staff member, I want to turn a lead into a pilgrim with one click, so that I don't retype their details.

### Languages
66. As a pilgrim, I want to choose English, Hindi, or Urdu in the portal, so that I understand everything.
67. As an Urdu reader, I want the screen to read right to left, so that it feels natural.
68. As a pilgrim, I want emails in my chosen language, so that I understand the message.

### Phone and offline use
69. As a pilgrim, I want to add the portal to my phone's home screen, so that it opens like an app.
70. As a pilgrim, I want my flight, hotel, visa, and ticket details to open without internet, so that I can use them at the airport or in Saudi Arabia.
71. As a pilgrim, I want an emergency card (guide or agency Saudi number, hotel address in Arabic) that works offline, so that I can get help if I get lost.
72. As a staff member, I want to enter the agency's Saudi contact number and each batch's guide name and phone, so that they appear on the emergency card.

### Admin roles and safety
73. As an owner, I want fixed roles (Owner, Manager, Documents staff, Accounts staff), so that each person sees only what they need.
74. As an accounts staff member, I want to see pilgrim names and payments but not passport files, so that sensitive data stays limited.
75. As a documents staff member, I want to manage documents, visa, and trip details but not payments, so that money stays with accounts.
76. As an owner, I want only the owner to delete records, and deletes to be soft (hidden, restorable), so that mistakes can be undone.
77. As an owner, I want every change to payments, documents, and visa status saved in an activity log, so that I can see who did what and when.

### Dashboard
78. As an owner, I want a dashboard with upcoming batches, seats booked and left, so that I see sales at a glance.
79. As a documents staff member, I want to see per batch how many pilgrims have pending or rejected documents, so that I know where to focus.
80. As a documents staff member, I want to see visa status counts per batch, so that I can track progress.
81. As an accounts staff member, I want to see total collected and total pending per batch, so that I can follow up on money.
82. As a staff member, I want to see new leads waiting for a call, so that we respond fast.

### Getting existing data in
83. As a staff member, I want to download an Excel template for pilgrims and family groups, so that I can fill in existing data.
84. As a staff member, I want to upload the filled template and see errors per row before saving, so that bad data doesn't get in.

## Implementation Decisions

### Architecture
- **Stack:** Next.js (App Router) + Supabase (Postgres, Auth, Storage). No separate backend server in the MVP.
- **Business logic lives in a separate domain layer**, not inside pages or route handlers. Pages and server actions call into this layer. This keeps logic testable and makes a later move to NestJS easy.
- **Multi-agency ready:** every business table has an `agency_id`. The MVP runs one agency, on the client's own domain.
- **Row Level Security (RLS)** on every table. Policies check `agency_id` and the user's role (staff) or group access (pilgrim).
- **PWA:** installable, with a service worker that caches the pilgrim's trip summary, emergency card, and the last-opened ticket and visa files for offline use.
- **Languages:** i18n setup (for example, next-intl) from day one for the website and pilgrim portal: English, Hindi, Urdu. Layouts use logical (start/end) spacing so Urdu RTL works. A proper Urdu font such as Noto Nastaliq Urdu. The admin panel is English only.
- **Email:** Supabase Auth email OTP for login. A transactional email provider (for example, Resend) for notifications. Every outgoing message is written to a message log with a status, so a later WhatsApp channel can plug into the same log.

### Main modules (deep modules marked ★)
- ★ **Access policy** — one place that answers "can this user do this action on this record?" Input: user (role or pilgrim + group), action, record. Used by server actions, with RLS mirroring the same rules. Covers staff roles, group-leader access, and self-only access.
- ★ **Booking & pricing** — given a batch, room type, traveller type (adult, child, infant), and extras, returns the total price. Handles seat counting (booked vs left) and cancellation (frees the seat).
- ★ **Ledger (payments)** — records payments, split allocations across group members, reversals, and refunds. Returns total, paid, and balance for a pilgrim or a group. Issues sequential receipt numbers per agency. Nothing is ever hard-deleted.
- ★ **Document checklist** — given a package's required list and a pilgrim's uploads, returns the status of each item and whether the pilgrim is "complete". Handles approve, reject with reason, and re-upload.
- ★ **Visa status** — a small state machine: Documents pending → Documents complete → Submitted → Approved / Rejected. It moves to "Documents complete" automatically from the checklist, supports bulk transitions, and blocks invalid jumps.
- ★ **Trip details resolver** — merges batch-level flights and hotels with per-pilgrim overrides and personal items. Returns one ordered timeline for the portal and the offline cache.
- ★ **Pilgrim import** — parses the Excel template, validates each row (required fields, date formats, passport number, duplicates, group-leader references), and returns a row-by-row error report before saving.
- ★ **Visa export** — turns a batch's pilgrims into rows in the Saudi partner's column format. The format is configurable once the client shares a sample.
- **Mahram & passport checks** — rules that return warnings (no mahram linked, passport expiring within the configured months).
- **Notifications** — builds messages from templates per language and sends by email. Writes to the message log.
- **Activity log** — records who did what, when, and on which record, for payments, documents, visa, and deletes.
- **CMS (website content)** — packages, photos, and FAQs for the public site, with a published/hidden flag. Private trips are never public.
- **Leads** — enquiry form intake, status, notes, and convert-to-pilgrim.
- **Dashboard queries** — counts per batch for seats, documents, visa, and money, shown by role.

### Data model (main entities)
- `agencies`, `staff_users` (role), `pilgrims` (profile, passport fields, language, optional auth user), `groups` (leader), `group_members`, `mahram_links`
- `packages` (template), `batches` (package optional; private flag; seats; prices per room type and traveller type), `batch_extras`
- `bookings` (pilgrim + batch + room type + extras + status + total)
- `batch_flights`, `batch_hotels`, `pilgrim_trip_items` (overrides and personal items like ticket, PNR, visa number)
- `document_requirements` (per package), `documents` (file ref, status, reason, reviewer)
- `visa_status` (per booking, with history)
- `payments`, `payment_allocations`, `refunds`, `receipts` (numbered)
- `leads`, `lead_notes`, `site_content` (FAQs, pages)
- `message_log`, `activity_log`
- All tables: `agency_id`, `created_at`, `updated_at`, `deleted_at` (soft delete where relevant)

### Files and privacy
- Passport, ID, visa, and ticket files are stored in a private bucket, organised by agency and pilgrim. They are opened only through short-lived signed URLs, and every open is logged.
- Accounts staff cannot open identity documents.

### Settings (editable by owner)
- Agency profile, logo, bank details for transfers, Saudi contact number, passport minimum validity (in months), receipt number prefix.

## Testing Decisions

- **What a good test is:** it checks what a module does from the outside (inputs → outputs, or allowed → denied), not how it does it inside. A test should still pass after a refactor if the behaviour didn't change.
- **Unit tests (Vitest) for every ★ module:**
  - Access policy — each role against each action, group leader vs member vs outsider, cross-agency access always denied.
  - Booking & pricing — room type × traveller type × extras, seat limits, cancellation frees the seat.
  - Ledger — split group payments, reversals, refunds, balance never drifts, receipt numbers unique and in order.
  - Document checklist — all status combinations, re-upload after rejection, "complete" only when all required items are approved.
  - Visa status — valid and invalid transitions, auto-move on checklist complete, bulk update.
  - Trip details resolver — batch data plus overrides give the correct ordered timeline.
  - Pilgrim import — good file, each type of bad row, duplicates, missing group leader.
  - Visa export — column order and formats match the sample.
- **RLS tests** against a local Supabase instance: a pilgrim cannot read another group's data, accounts staff cannot read identity files, and no user can read another agency's rows.
- **A few end-to-end tests (Playwright)** for the main flows: staff creates a pilgrim → pilgrim logs in → uploads a document → staff approves → visa moves to Documents complete → staff records a payment → pilgrim sees the balance and receipt. Also a check that the portal opens offline after the first visit, and that the Urdu layout renders RTL.
- **Prior art:** none yet (new codebase). These tests set the pattern.

## Out of Scope

These were agreed in planning but are **not in the MVP**. They come in later phases:
- Online payments (Razorpay), convenience-fee rules, and payment webhooks
- GST invoices and tax settings
- Automatic payment-due reminders
- Automatic WhatsApp messages (WhatsApp Business API). The MVP has email only, plus WhatsApp click-to-chat buttons on the website.
- Visitor self sign-up and booking requests from the website. In the MVP, staff create all pilgrim accounts; visitors send enquiries.
- Full refund rules engine and batch transfers. The MVP supports only basic cancellation and manual refund entry.
- During-trip management: room allocation, bus and seat allocation, day-by-day schedule, batch announcements, and room-mixing warnings. The MVP has only the offline emergency card and guide contact.
- Sub-agent tracking and commission
- Auto-delete of sensitive files after the trip. Files are stored privately in the MVP; the retention job comes later.
- Payment and family-group Excel import. The MVP imports pilgrims and groups only.
- Custom staff roles, multi-agency onboarding, subdomains, and custom domains for other agencies
- Native mobile apps
- Cost and profit reports

## Further Notes

- **Confirm with the client before build:**
  1. How many active pilgrims and batches they have, and where the data is now.
  2. The room types they offer, and their cancellation rules.
  3. A sample of the Saudi partner's Excel format for visa submission.
  4. The current passport validity rule for Saudi visas.
  5. The agency's bank details and Saudi contact number for the portal.
  6. Someone to check the Hindi and Urdu text before launch.
- Hindi and Urdu text must be checked by a native speaker, especially religious terms. Machine translation alone is not enough.
- Use a paid Supabase plan with daily backups from launch, because the system holds passport data and payment records.
- Keep message sending behind the message log, so adding WhatsApp later is only a new channel, not a rewrite.
- Keep `agency_id` on every record and in every RLS policy from day one, so the SaaS move later needs no data migration.
