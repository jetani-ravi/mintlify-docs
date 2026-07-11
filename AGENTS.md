# EzyText documentation — project instructions

## About this project

- Customer help center for **EzyText**, a multi-channel text-campaign platform (SMS, email, advertising).
- Built on [Mintlify](https://mintlify.com); pages are MDX files with YAML frontmatter.
- Navigation and settings live in `docs.json` (`navigation.tabs → groups → pages`).
- Content must reflect the **actual app** — cross-check the product repo
  (`text-campaign-ai`: backend `src/modules/*`, frontend `src/features/*` and routes)
  before documenting a flow. Do not document features that are not shipped.
- Use the Mintlify MCP server, `https://mcp.mintlify.com`, to edit content and settings via MCP.
- Use the Mintlify docs MCP server, `https://www.mintlify.com/docs/mcp`, to query Mintlify usage.

## Terminology

- Say **workspace** / **organization** for the tenant, **member** for a user in it.
- Say **channel** (SMS, Email, Advertising), **provider** (Twilio, Telnyx, Gmail, …).
- Say **contact** (not "lead" unless referring to ad Lead Ads), **segment**, **campaign**.
- Say **opt-in** / **opt-out** (hyphenated); **A2P 10DLC** (not "10dlc").

## Style preferences

- Use active voice and second person ("you").
- Keep sentences concise — one idea per sentence.
- Use sentence case for headings.
- Bold for UI elements and navigation: Click **Settings → Channels**.
- Code formatting for file names, commands, paths, keywords (`STOP`), and code references.
- Every module page follows: Overview → Before you start → How-to (`<Steps>`) → FAQ (`<AccordionGroup>`) → Troubleshooting.

## Content boundaries

- Document customer-facing features only. Do not document platform-admin,
  internal billing margin config, or unreleased modules.
- Never include real API keys, tokens, phone numbers, or customer data in examples.
