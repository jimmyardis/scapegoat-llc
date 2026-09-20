## Meta
| Field | Value |
| --- | --- |
| Project | Scapegoat LLC |
| Last Active | 2026-09-20 |
| Status | shipping |
| Repo | jimmyardis/scapegoat-llc (public) |
| Live | https://jimmyardis.github.io/scapegoat-llc/ |

## Current State
Marketing site for Scapegoat LLC, a Greenville SC landscaping company run by Jason Brown,
is live on GitHub Pages. The whole site is one self-contained `index.html` (~873 KB) with
inlined CSS and data-URI art, delivered as a finished file rather than built in the repo.
Repo created, committed, pushed, Pages enabled via API, and the live URL verified at 200.

## Next Action
Get contact details from the client — the page currently has no phone number, email, or
street address anywhere in it.

## Blockers
None.

## Open Questions
- Custom domain? Would need a CNAME file plus DNS, the way Lake Murray Tree Service was done.
- Should this live under the Telos-Digital account instead of jimmyardis, like Beauty by Olivia?

## Session Log
### 2026-09-20
- Took delivery of `index(1).html` from Windows Downloads, copied it in as `index.html`.
- Created `jimmyardis/scapegoat-llc` (public), committed with a README, pushed `main`.
- Chose `jimmyardis` over Telos-Digital so Pages could be enabled over the API — a
  Telos-Digital repo needs the browser-enables-Pages collaborator dance instead.
- Public on purpose: Pages on a private repo requires a paid plan.
- Enabled Pages (main, /root), polled the build, confirmed live at HTTP 200 with the
  full 873,379 bytes served.
- Noted the missing contact info; left it for the client rather than inventing details.
