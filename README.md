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
```
