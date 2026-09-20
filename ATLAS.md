## Meta
| Field | Value |
| --- | --- |
| Project | Scapegoat LLC |
| Last Active | 2026-09-20 |
| Status | shipping |
| Repo | jimmyardis/scapegoat-llc (public) |
| Live | https://scapegoatsc.com |

## Current State
Marketing site for Scapegoat LLC, a Greenville SC landscaping company run by Jason Brown,
is live at **https://scapegoatsc.com** on GitHub Pages with HTTPS enforced. The whole site
is one self-contained `index.html` (~4.5 MB after the second delivery) with inlined CSS and
data-URI art, delivered as a finished file rather than built in the repo. Domain, TLS, and
all four URL variants (apex/www, http/https) verified serving the full file.

## Next Action
Get contact details from the client — the page still has no phone number, email, or
street address anywhere in it.

## Blockers
None.

## Open Questions
- Should this live under the Telos-Digital account instead of jimmyardis, like Beauty by Olivia?
- The page is now a ~4.5 MB first load; worth compressing the two PNGs if mobile speed matters.

## Session Log
### 2026-09-20 (cont.)
- Took a second delivery, `index(2).html`, and overwrote `index.html` wholesale. Grew from
  873 KB to 4.5 MB — two embedded PNGs account for the whole jump. Verified live byte-for-byte.
- Set the custom domain `scapegoatsc.com`. DNS was already done at Namecheap before this
  session: apex A records on all four Pages IPs, `www` CNAME to `jimmyardis.github.io`.
- API gotcha worth remembering: `PUT /pages` with `cname` and `https_enforced` together
  fails "The certificate does not exist yet". Set `cname` alone, wait for the cert to reach
  `approved`, then enforce HTTPS in a second call. GitHub writes the `CNAME` file into the
  repo itself, so pull afterwards.
- Verified apex and www, over both http and https, all 200 and all serving 4,491,608 bytes.

### 2026-09-20
- Took delivery of `index(1).html` from Windows Downloads, copied it in as `index.html`.
- Created `jimmyardis/scapegoat-llc` (public), committed with a README, pushed `main`.
- Chose `jimmyardis` over Telos-Digital so Pages could be enabled over the API — a
  Telos-Digital repo needs the browser-enables-Pages collaborator dance instead.
- Public on purpose: Pages on a private repo requires a paid plan.
- Enabled Pages (main, /root), polled the build, confirmed live at HTTP 200 with the
  full 873,379 bytes served.
- Noted the missing contact info; left it for the client rather than inventing details.
