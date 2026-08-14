# Nium Docs Style Guide

Reference for anyone writing or editing pages in the Nium developer documentation. Derived from existing pages in the docs repo.

---

## Voice and tone

- **Second person, active voice** — "You can fund a wallet using..." not "Wallets can be funded by..."
- **Present tense** — "The API returns..." not "The API will return..."
- **Plain English** — avoid jargon when a simpler word works. When a Nium-specific term must be used, bold it on first mention and define it immediately: `**Virtual account numbers (VANs)** are unique identifiers that...`
- **No filler** — remove "please note that", "simply", "just", "it is important to"
- **Direct** — lead with what the reader can do, not with background

## Headings

- **H1** (`#`): page title only; matches the `title` frontmatter field
- **H2** (`##`): major sections — "Understanding X", "How X works", "Get started", "Supported X"
- **H3** (`###`): subsections within H2
- Never skip a heading level
- No trailing punctuation on headings

## Frontmatter (required for every page)

```mdx
---
title: <Page title — matches H1>
slug: /<section-slug>/<page-slug>
description: <One sentence. What can the reader do after reading this page?>
---
```

- `slug` uses kebab-case and matches the URL path on docs.nium.com
- `description` is used in search results and link previews — make it specific

## Formatting

- **Bold** (`**text**`): Nium terms on first use, UI element names, key concepts in bullet lists
- **Code** (`` `text` ``): API fields, parameter names, values, endpoints, file paths, HTTP methods
- **Tables**: use for structured data — supported values, field definitions, comparison of options
- **Numbered lists**: use only for sequential steps. Everything else is a bullet list
- **Bullet lists**: use `-` not `*`; capitalise first word; no trailing period for fragments, period for full sentences

## Callouts (MDX admonitions)

Use Docusaurus admonitions for supplementary information:

```mdx
:::note
Use for important context that doesn't fit in the main flow.
:::

:::tip
Use for optional best practices or shortcuts.
:::

:::warning
Use for things that can go wrong or require caution.
:::
```

Do not use HTML `<div>` or `<blockquote>` for callouts — always use the `:::` syntax.

## Links

- Descriptive anchor text: `[Virtual Accounts](/docs/payins/virtual-account-number)` not `[click here](...)` or `[here](...)`
- Internal links: use the slug path — `/docs/<slug>` or `/api#tag/...`
- API reference links: `[Endpoint name](/api#tag/<tag>/METHOD/path)`

## Tables

Every table must have a header row. Use sentence case for column headers. Keep cell content concise — link out for detail rather than expanding inline.

```mdx
| Method | Description |
|--------|-------------|
| **Bank transfer** | Transfer funds to a bank account. |
| **Card** | Use a debit or credit card. Must be enabled by Nium. |
```

## MDX components

### RunInPostman
Add to API pages that have a corresponding Postman collection. Place immediately after frontmatter:

```mdx
<RunInPostman href="https://www.postman.com/nium-api/workspace/nium/folder/..." size="sm" />
<br></br>
<br></br>
```

### Tabs / TabItem
Use for content that varies by region, method, or category:

```mdx
import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

<Tabs groupId="region">
  <TabItem value="sg" label="Singapore">
    ...
  </TabItem>
  <TabItem value="eu" label="Europe">
    ...
  </TabItem>
</Tabs>
```

## File naming

- Files in `docs/` use numbered prefixes: `01-Page Name.md`, `02-Other Page.md`
- Numbers determine sidebar order — insert at the correct position; renumber following files if needed
- Use title case for the file name: `01-Fund Wallet.md` not `01-fund-wallet.md`
- Use `.md` for standard pages, `.mdx` for pages that use JSX components (Tabs, RunInPostman, etc.)
- Changelog files use `.mdx` and date-based names: `2026-08-13.mdx`

## Changelog format

Each entry belongs to one of three `<TabItem>` groups:

| TabItem value | label | Use for |
|---------------|-------|---------|
| `core-platform` | Core Platform | Wallets, onboarding, compliance, general platform |
| `issuance-and-cards` | Issuance and Cards | Card issuance, card controls, spend limits |
| `payouts-and-payins` | Payouts and Payins | Payouts, payins, VANs, transfers |

A changelog entry should:
- Start with a bold H3 heading: `### Feature Name`
- Describe what changed in 1–3 short paragraphs, plain English
- Mention new fields, endpoints, or parameters in inline code
- End with a link to the relevant docs page: `For more information, see [Page Title](/docs/slug).`
- Note enablement requirements if applicable: "Requires enablement by your Nium account manager."

## Terms

| Use | Avoid |
|-----|-------|
| virtual account number (VAN) | virtual account (alone, without specifying VAN) |
| wallet | account (for Nium wallet) |
| client | merchant, partner |
| customer | end user, consumer |
| corridor | route, channel (for currency/country pairs) |
| enable | turn on, activate |
| payout | withdrawal, transfer out |
| payin | deposit, transfer in |
