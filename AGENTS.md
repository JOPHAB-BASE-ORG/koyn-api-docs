# Documentation project instructions

## About this project

- This is the Koyn API reference, built on [Mintlify](https://mintlify.com).
- Pages are MDX files with YAML frontmatter. Configuration lives in `docs.json`.
- The backend is a Laravel application. Production base URL is `https://api.getkoyn.com/api`; admin routes live under `/console`.
- Endpoint pages under `api-reference/` were generated from `GetKoyn.postman_collection.json`. Edit the MDX directly; the Postman export is kept only as a reference and is excluded from the build.

## Structure

- `guides/` holds concept pages: authentication, environments, response envelope.
- `api-reference/mobile/`, `api-reference/admin/`, `api-reference/public/`, `api-reference/webhooks/` map to the navigation tabs in `docs.json`.
- Each endpoint page uses `api:` frontmatter (`METHOD /path`) so Mintlify renders the interactive playground. Path parameters use `{param}` syntax.

## Terminology

- Use "wallet" for the naira balance and "crypto wallet" for on-chain addresses.
- Use "staff" for admin console accounts and "user" for app accounts.
- Use "signup bonus" for the credit new accounts receive.
- Use "withdrawal" (not "payout") and "swap" (not "trade") for crypto conversions. "Trade" refers to gift card trades only.

## Style preferences

- Use active voice and second person ("you").
- Keep sentences concise, one idea per sentence.
- Use sentence case for headings.
- Bold for UI elements: Click **Settings**.
- Code formatting for file names, paths, parameters and code references.
- Describe simulated or pending subsystems functionally; never label anything "demo", "mock", "stub" or "placeholder".

## Content boundaries

- Never commit real tokens, emails, phone numbers, BVNs or account numbers in examples. Use masked values.
- Pages under groups marked "Deprecated" stay for reference but must carry the deprecation warning.

## Checks

Run `npx mint validate` and `npx mint broken-links` before pushing.
