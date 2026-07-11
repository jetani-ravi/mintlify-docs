# EzyText Documentation

Customer-facing help center for the EzyText text-campaign platform, built with
[Mintlify](https://mintlify.com). Every page is grounded in the actual product
modules (backend `src/modules/*`, frontend `src/features/*`).

## Local preview

```bash
npm i -g mint      # Mintlify CLI
mint dev           # serves docs at http://localhost:3000
```

Validate links and structure before pushing:

```bash
mint broken-links
```

Publishing is automatic: pushing to the default branch deploys via the Mintlify
GitHub app.

## Information architecture

Navigation lives in [`docs.json`](./docs.json) as `navigation.tabs → groups → pages`.
Each nav leaf maps to one `.mdx` file (extensionless, root-relative).

| Tab | Covers | Backing modules |
| --- | --- | --- |
| Getting Started | Onboarding, workspace, team, auth | `auth`, `organization`, `invitation`, `user/role/permission` |
| Channels | SMS / Email / Advertising overview | `channel-core`, `sms-channel`, `email-channel`, `advertising` |
| Providers | Twilio, Telnyx, Gmail, M365, SMTP, Google/Meta Ads | `sms-channel/providers`, `email-settings`, `advertising/providers` |
| Compliance | A2P 10DLC, toll-free, opt-in, opt-out | `channels` 10DLC, `opt-in`, `opt-out` |
| Contacts | Contacts, import, custom fields, tags, segments | `contacts`, `contact-import`, `tags`, `segments` |
| Campaigns | Campaigns, templates, quick messages, polls, links | `campaigns`, `*-templates`, `polls`, `short-links`, `join-links` |
| Automation & AI | Workflow builder, AI agent, knowledge base, module builder | `workflows`, `ai-agents`, `knowledge-base`, `module-builder` |
| Inbox | Unified inbox, tickets | `inbox`, `tickets` |
| Scheduling | Calendar, meeting types, availability, bookings | `calendar*`, `meeting-types`, `bookings` |
| Analytics & Billing | Dashboard, analytics, attribution, wallet/billing | `dashboard`, `advertising`, `platform-billing` |
| Developers | API keys, webhooks, API reference | `api-keys`, `webhooks` |
| Support | FAQ, troubleshooting, release notes | — |

## Page template

Every module page follows the same shape so customers learn one layout:

1. **Overview** — what it is, when to use it (+ difficulty/time hints).
2. **Before you start** — prerequisites and permissions.
3. **How-to** — `<Steps>` grounded in the real UI route.
4. **FAQ** — `<AccordionGroup>`.
5. **Troubleshooting** — common errors and fixes.

## Screenshots

Images are referenced as `/images/<section>/<name>.png` inside `<Frame>` blocks.
Drop real captures into `images/` matching those paths and they resolve. Pages
currently ship without images; add them incrementally — see `images/README.md`.

## Content status

Pages carrying a `This guide is being expanded` `<Note>` are structural stubs
awaiting full content. Track progress by phase in the project plan.
