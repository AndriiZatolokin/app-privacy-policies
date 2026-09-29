# App sites

Static GitHub Pages site for apps by Andrii Zatolokin.

## Structure

```text
index.html                         App directory and language entry points
assets/                            Shared styles and RoadVolume brand assets
roadvolume/index.html              RoadVolume landing page (English)
roadvolume/privacy-policy.html     Stable English privacy-policy URL
roadvolume/uk/                     Ukrainian landing page and privacy policy
roadvolume/tr/                     Turkish landing page and privacy policy
robots.txt                         Search crawler rules
sitemap.xml                        Public page index
```

The existing `/roadvolume/privacy-policy.html` path remains the canonical English policy URL so Google Play links do not need to change.

When adding a language, add both the landing page and privacy policy, update the language navigation and `hreflang` links on all localized pages, then add the new URLs to `sitemap.xml`.

## RelayInbox

- English app page: `/relayinbox/`
- Stable English privacy policy: `/relayinbox/privacy-policy.html`
- Ukrainian app page: `/relayinbox/uk/`
- Ukrainian privacy policy: `/relayinbox/uk/privacy-policy.html`

RelayInbox policy content is maintained in the Android repository `SmsBot/privacy/policy.json`. Its `scripts/sync-privacy-policy.py --site-root <this-checkout>` generates these pages and the matching bundled Android policies. Run it with `--check` to verify parity before publication. This site remains static and requires no backend or build toolchain.
