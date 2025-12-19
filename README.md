# narrative-distribution-systems
Systems Map for ND
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

4. Click **Commit changes**

### What you get
- GitHub will **render the diagram automatically**
- Anyone on the team can view it
- You can edit the diagram just by editing text

---

## Option 2: Dedicated `/docs` Folder (Best for Scaling Later)

If this will grow into onboarding docs, SOPs, etc.

### Steps
1. In the repo → **Add file → Create new file**
2. Name it:  
   `docs/systems-flow.md`

3. Paste:

```markdown
# Systems Flow – Narrative Distribution

```mermaid
flowchart LR
...diagram here...
