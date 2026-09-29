# Privacy Policy — Adnihilator

Effective 2026-09-24.

Adnihilator hides ads in the Facebook feed. It has no server of its own, no analytics, no account and no advertising. This policy covers everything the extension reads, stores and sends.

## What it reads

On `facebook.com` pages only, for each feed post, it reads:
- the author name, the header label (for example "Ad" or "3 hours ago") and call-to-action button text;
- external link domains, media counts and Facebook's ad-slot markers;
- up to 300 characters of post text, and the ad's title and description.

## What it sends, to whom, and when

Posts are sent only to the API providers whose keys **you** enter in settings:

| Recipient | Host | When | What |
|---|---|---|---|
| TypeSafe (Jev) | `api.typesafe.ai` | each new post, if a Jev key is set | the features above |
| Anthropic (Claude) | `api.anthropic.com` | every 5 minutes, only borderline posts, if a Claude key is set | the features above plus Jev's scores |

**Redaction rule:** author, post text and ad creative are sent only for posts with ad evidence: an ad label, a call-to-action button, an external link, or Facebook's ad slot. For every other post (for example a friend's photo), those fields are blanked before anything leaves the browser.

Each provider handles the data under its own terms: [TypeSafe](https://typesafe.ai) and [Anthropic](https://www.anthropic.com/legal/privacy). Without keys, nothing is sent anywhere.

## What it stores (on your device only, in `chrome.storage.local`)

| Data | Retention |
|---|---|
| Your settings and API keys | until you remove them |
| Classification cache (a hash of each post → verdict) | 7 days |
| Accuracy telemetry: numbers and flags only, never post text | 30 days |
| Your audit-mode Right/Wrong verdicts | 30 days |

Stored data never leaves your browser. The dashboard's **Export JSON** writes a file only when you click it, and **Clear log** deletes the telemetry.

## What it never does

- It doesn't collect, sell or share personal data for advertising or any other purpose.
- It doesn't read pages other than facebook.com.
- It doesn't track browsing history.
- It doesn't send data to the developer.

## Contact

Use the support tab of the extension's Chrome Web Store listing.
