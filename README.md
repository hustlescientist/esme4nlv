# Esmeralda Villeda | North Las Vegas Ward 1

Static **English/Spanish single-page website demo** for Esmeralda Villeda's North Las Vegas City Council Ward 1 campaign.

**Demo URL (after GitHub Pages is enabled):** https://hustlescientist.github.io/esme4nlv/

## Deployment (no custom GitHub Actions)

This repo uses the static **gh-pages branch**, deployed from its **/(root)** directory. No `.github/workflows` files or GitHub Actions-based site builders are required.

For initial setup in **Settings → Pages**:
1. Under **Build and deployment**, select **Deploy from a branch**.
2. Select **gh-pages** and **/(root)**, then **Save**.
3. Wait for GitHub Pages to finish publishing, then open the demo URL above.

Static assets are embedded or loaded from the campaign's existing image CDN; there is no build step.

## Site features

- Responsive sticky navigation and mobile menu
- Instant EN/ES switching via JavaScript (with URL/history support)
- Candidate story, issues, endorsement groups, campaign announcements and ActBlue links
- The supplied, real HighLevel opt-in iframe (form ID `bNfm16tjccR3VPuBa7u4`)
- Keyboard navigation and reduced-motion support

> **Demo caution:** The opt-in iframe is a real embedded campaign form. Submitting it may create or update a live campaign CRM contact. Do not use fake or unauthorized test contact details.

## Editing

- `index.html`: full standalone demo.
- `GHL-PASTE-IN.html`: version intended for a HighLevel Custom HTML element.
- `.nojekyll`: keeps Pages serving the static files directly.

The standalone demo includes `noindex, nofollow` metadata to avoid competing with the official campaign site.

Original campaign site: https://esmefornlv.com/
