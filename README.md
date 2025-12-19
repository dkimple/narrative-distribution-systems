# Narrative Distribution – Systems Overview

## High-Level Systems Flow

```mermaid
flowchart LR

Outlook[Outlook<br/>External & Formal Communication]
Slack[Slack<br/>Internal Communication]

Monday[Monday.com<br/>Project Management & CRM]

LaunchBay[LaunchBay<br/>Client & Film Onboarding]
Molten[Molten<br/>Rights & Title Management<br/>Metadata • Contracts • Screening]
NexSpec[NexSpec<br/>Asset Delivery to Platforms]

AWS[AWS<br/>Film Assets<br/>Features • Trailers • Media]
Dropbox[Dropbox<br/>Documents & E-Signing<br/>Contracts • Avails • Sales History]

Outlook --> Monday
Slack --> Monday

Monday --> LaunchBay
Monday --> Molten

LaunchBay --> Dropbox

Molten --> NexSpec
Molten --> AWS
NexSpec --> AWS

Dropbox -.-> Molten

**Critical rules:**
- The Mermaid block must start with **three backticks + mermaid** on its own line:
  - ```mermaid
- It must end with **three backticks** on its own line:
  - ```
- Don’t indent the triple backticks.
- Don’t put the Mermaid block inside another code block that you *didn’t* intend.

---

### 5) Preview before committing (so you can confirm it renders)
1. Above the editor, click the **Preview** tab (it may say **Preview changes**)

What you should see:
- A rendered diagram (boxes and arrows)

If you **still see code** instead of a diagram, jump to the troubleshooting section below.

---

### 6) Commit the change
1. Scroll down to the **Commit changes** box
2. In the first field (“Commit message”), type something like:  
   `Add systems flowchart`
3. Choose either:
   - **Commit directly to the main branch** (most common), or
   - **Create a new branch…** (if your repo requires PRs)
4. Click **Commit changes** (or **Propose changes** if making a PR)

---

### 7) Confirm it works on the main repo page
1. Click the repo name (or click **Code** tab)
2. Scroll to the README section
3. You should see the rendered Mermaid diagram

---

# If it still isn’t working: the exact fixes

## Problem A: You see the Mermaid code, not a diagram
This usually means one of these:

### A1) The backticks are wrong
Fix:
- Make sure the opening line is exactly:
  - ```mermaid
- And the closing line is exactly:
  - ```
- Both must be on their **own** lines.

### A2) You accidentally nested code blocks
This is very common if you pasted the Mermaid block while already inside a Markdown code block.

Fix:
- Ensure there is **not** a line above your Mermaid block like:
  - ```markdown
  that never closes.
- In other words: only the Mermaid section should be a fenced block unless you intentionally want others.

### A3) You’re not actually editing a `.md` file
Mermaid rendering works in Markdown contexts.

Fix:
- Confirm the file ends in `.md` like:
  - `README.md`
  - `docs/systems-flow.md`

---

## Problem B: “Preview” renders nothing / shows an error
### B1) Special characters breaking parsing
Sometimes certain punctuation can cause issues depending on renderer.

Fix:
- Replace bullets `•` with normal text (hyphen or words).
- Here’s a safer version of the Molten label line if needed:
  - `Molten[Molten<br/>Rights & Title Management<br/>Metadata - Contracts - Screening]`

### B2) Mermaid syntax error
Fix:
- Try this ultra-minimal test to confirm Mermaid works in your repo:

Paste ONLY this in the README and preview:

```mermaid
flowchart LR
A --> B
