# contribute

Create or update Nium documentation for a sprint. Handles new pages, updates to existing pages, and changelog entries — always in the same workflow.

---

## One-Time Setup (Prerequisites)

Before using this skill for the first time, make sure the following are in place:

### 1. Clone the docs repo and the skills repo

```bash
cd ~/Work   # or wherever you keep repos
git clone https://github.com/nium-global/docs.git
cd docs && npm install && cd ..
git clone https://github.com/saloni-nium/docs-skills.git
```

### 2. Install the contribute skill into Claude Code

```bash
mkdir -p ~/.claude/skills/contribute
cp ~/Work/docs-skills/skills/contributor/contribute.md ~/.claude/skills/contribute/SKILL.md
```

### 3. Authenticate with GitHub CLI

```bash
gh auth login
```

### 4. Verify you can build the docs locally

```bash
cd ~/Work/docs
npm run build
npm run start   # should open http://localhost:3000
```

### 5. Confirm the PPRCAMCP MCP server is connected

The skill uses it to pull Jira ticket details and Confluence PRD content. Verify it is listed under active MCP servers in your Claude Code session.

---

## Arguments

Pass all arguments inline when invoking the skill, or omit any and Claude will prompt you for it.

| Argument | Example | Description |
|----------|---------|-------------|
| `tickets` | `NIUM-123,NIUM-456` | Comma-separated Jira ticket IDs defining the feature |
| `prd` | `https://nium.atlassian.net/wiki/...` | Confluence URL of the PRD |
| `docs` | `https://docs.nium.com/payins/fund-wallet` | Comma-separated URLs of existing pages to update (omit if creating only new pages) |
| `sprint` | `14` | Sprint number |
| `pm` | `saloni` or `rana` | Your name — determines the feature branch name |

**Example invocation:**
```
/contribute tickets=NIUM-123,NIUM-456 prd=https://nium.atlassian.net/wiki/spaces/... docs=https://docs.nium.com/payins/fund-wallet sprint=14 pm=saloni
```

---

## Instructions

### Step 1 — Fetch the latest version of this skill

Pull the latest skill file from the skills repo so any updates are picked up before proceeding:

```bash
git -C ~/Work/docs-skills pull origin main --quiet
cp ~/Work/docs-skills/skills/contributor/contribute.md ~/.claude/skills/contribute/SKILL.md
```

This ensures the next time the skill runs it will use the latest version.

---

### Step 2 — Collect and validate inputs

Parse arguments from the invocation. For any missing argument, ask:

- **"What are the Jira ticket IDs? (comma-separated)"**
- **"What is the Confluence URL for the PRD?"**
- **"Are there existing doc pages to update? Paste the URLs or say 'no' for new page only."**
- **"What sprint number is this?"**
- **"Which PM is this for — saloni or rana?"**

Derive the feature branch name using whatever is available:
- If both sprint and PM name are provided: `sprint-release-<sprint>-<pm>` (e.g. `sprint-release-14-saloni`)
- If only sprint is provided: `sprint-release-<sprint>-<YYYY-MM-DD>`
- If only PM name is provided: `docs-update-<pm>-<YYYY-MM-DD>`
- If neither is provided: `docs-update-<YYYY-MM-DD>`

Always create a branch — never block on missing sprint or PM name.

Confirm with the user:
```
Feature branch: sprint-release-14-saloni
Based on:       staging (latest)
Proceeding...
```

---

### Step 3 — Set up the git workspace

Run these commands from the docs repo root (`~/Work/docs` or wherever it is cloned):

```bash
git fetch origin
git checkout staging
git pull origin staging
```

If the feature branch already exists remotely, switch to it and pull:
```bash
git checkout sprint-release-<sprint>-<pm>
git pull origin sprint-release-<sprint>-<pm>
```

If it does not exist yet, create it from the now-current staging:
```bash
git checkout -b sprint-release-<sprint>-<pm>
```

Report the current branch:
```
✓ On branch: sprint-release-14-saloni
  Based on:  staging (latest)
```

---

### Step 4 — Research: pull all source material

#### 3a. Fetch Jira tickets
For each ticket ID, use the `mcp__PPRCAMCP_PREPROD__get_jira_issue_details` tool. Extract:
- Summary (what changed / what is new)
- Description (technical details)
- Acceptance criteria (if present)
- Linked PRD or Confluence pages

#### 3b. Fetch the Confluence PRD
Use the `mcp__PPRCAMCP_PREPROD__get_confluence_page` tool with the provided Confluence URL. Extract:
- Feature scope and goals
- User-facing behaviour
- API changes, new fields, new endpoints
- Supported regions/corridors
- Any constraints or limitations

#### 3c. Read existing docs (if updating)
For each URL in `docs`, extract the path segment and find the local file by grepping frontmatter:
```bash
grep -rl "slug: /<path-segment>" docs/
```
For example, `https://docs.nium.com/payins/fund-wallet` → `grep -rl "slug: /payins/fund-wallet" docs/`
Read the matched file in full.

Produce an internal research summary (not shown to user unless asked):
```
Feature: <name from PRD>
Change type: [new page / update existing / both]
Affected sections: [e.g., 04-Payins]
API changes: [yes/no — list endpoints]
Changelog tab: [core-platform / issuance-and-cards / payouts-and-payins]
```

---

### Step 5 — Determine change type and plan the edits

**If `docs` argument was provided** → update those existing pages.

**If `docs` was not provided or user said "no"** → create a new page.

**In all cases** → create or update a changelog entry for today's date.

Ask the user to confirm the plan before making any changes:
```
Planned changes:
  [UPDATE] docs/04-Payins/01-Fund Wallet.md — add new funding method section
  [CREATE] changelog/2026/<today-date>.mdx  — new changelog entry
  
Does this look right? (yes / adjust)
```

---

### Step 6 — Write or update the docs

Apply all rules from `standards/nium-style-guide.md` throughout.

#### For an existing page update:

- Read the file in full first
- Make the targeted change: add a new section, update a table, add/revise steps
- Preserve all existing structure, frontmatter, and component usage
- Do not rename the file or change the `slug` unless explicitly asked
- Use the same MDX components already present in the file (`:::note`, `:::tip`, `<Tabs>`, etc.)

#### For a new page:

Determine where the new page belongs:
- Ask: **"Which section does this fall under?"** (show the numbered folder list)
- Name the file following the existing numbering convention in that folder: if the last file is `03-Something.md`, name the new one `04-New-Feature.md`

Create the file with this frontmatter:
```mdx
---
title: <Page Title>
slug: /<section-slug>/<page-slug>
description: <One sentence. What can the reader do after reading this?>
---
```

Structure the content following the patterns in the section:
- Lead with a bold definition of the feature: `**Feature name** is...`
- Use H2 (`##`) for major sections, H3 (`###`) for subsections
- Use tables for structured data (fields, parameters, supported values)
- Use `:::note` / `:::tip` / `:::warning` for callouts
- Include a "Get started" or equivalent practical section with API steps if applicable

If this is an API-related page, add the RunInPostman component below the frontmatter if a relevant Postman collection exists:
```mdx
<RunInPostman href="https://www.postman.com/nium-api/..." size="sm" />
<br></br>
<br></br>
```

#### For the changelog entry:

Check if a changelog file for today already exists at `changelog/2026/YYYY-MM-DD.mdx`.
- If yes → add the new entry inside the correct `<TabItem>` 
- If no → create a new file

Use this exact format:
```mdx
---
slug: /<month-name-dd-yyyy>
title: <Month DD, YYYY>
---

<Tabs groupId="changelog-category">
    <TabItem value="core-platform" label="Core Platform">
        ### <Feature Name>
        <What changed, in plain English. One short paragraph. Include the key behaviour, any new fields or endpoints, any enablement requirement.>

        For more information, see [<Page Title>](/docs/<slug>).
    </TabItem>

    <TabItem value="issuance-and-cards" label="Issuance and Cards">
        <p>There are no changes at this time.</p>
    </TabItem>

    <TabItem value="payouts-and-payins" label="Payouts and Payins">
        <p>There are no changes at this time.</p>
    </TabItem>
</Tabs>
```

Choose the correct `<TabItem>` for the feature based on which product area it belongs to. Use the Jira/Confluence research to determine this.

---

### Step 7 — Build and preview

```bash
npm run build
```

If the build fails, read the error output, fix the issue (usually a broken link, malformed MDX component, or frontmatter problem), and rebuild. Show the user what was fixed.

If the build passes:
```bash
npm run start
```

Tell the user:
```
✓ Build passed
✓ Preview running at http://localhost:3000

Please review the changes in your browser. 
Type 'approved' when ready to commit, or describe any changes needed.
```

---

### Step 8 — Wait for PM approval

Pause. Do not commit until the user explicitly types **approved** (or similar confirmation).

If the user requests changes, apply them, rebuild, and return to the preview step.

---

### Step 9 — Commit and push

Once approved:

```bash
git add <changed files>
git commit -m "docs: <concise summary of what changed>

Tickets: <JIRA-ID, JIRA-ID>
Sprint: <sprint number>
"
git push origin sprint-release-<sprint>-<pm>
```

Report the result:
```
✓ Committed and pushed

Branch:    sprint-release-14-saloni
PR target: staging

Summary of changes:
  - [UPDATED] docs/04-Payins/01-Fund Wallet.md — added direct debit section for EU
  - [CREATED] changelog/2026/2026-08-14.mdx — changelog entry under Payouts and Payins

Next: ask DevEx to open the PR from sprint-release-14-saloni → staging.
```
