# Esmeralda Villeda — North Las Vegas Ward 1

Static, bilingual (English/Spanish) single-page website demo for the Esmeralda Villeda campaign.

**Demo URL once Pages is enabled:** https://hustlescientist.github.io/esme4nlv/

## GitHub Pages configuration — no custom GitHub Actions

This repository contains two branches:

- **`main`** — source HTML plus a reference `GHL-PASTE-IN.html` block for GoHighLevel.
- **`gh-pages`** — deployable static site in the branch root (`index.html` and `.nojekyll`).

**One-time setup:** Go to [Settings → Pages](https://github.com/hustlescientist/esme4nlv/settings/pages), under **Build and deployment** choose **Deploy from a branch**, select **`gh-pages`** and **`/(root)`**, then **Save**. GitHub will publish the static site. This project does **not** use a custom workflow, build system, or `.github/workflows` files. GitHub may still show its internally managed Pages deployment activity.

## Site

- Original campaign masthead, portrait, colors, endorsements, and announcement cards
- Responsive sticky header and mobile navigation
- Instant in-page English/Spanish toggle
- Integrated LeadConnector form `bNfm16tjccR3VPuBa7u4`
- Links to campaign information and ActBlue donation destination
- Demo marked `noindex, follow` to avoid search competition with the official campaign website

**Important:** The embedded LeadConnector form is live. Submitted contact details can be received by the actual campaign CRM. Its field labels are maintained in HighLevel.

## Updates

Update `index.html` on `main` and copy the revised static site to the root of `gh-pages` to update the public demo. The `GHL-PASTE-IN.html` file is a separate fragment for the HighLevel editor and is not the GitHub Pages entrypoint.

Original website: https://esmefornlv.com/

## Endorsements inventory (October 18, 2026)

The bilingual homepage and GHL custom-code fragment have the same expanded six-section endorsement wall: 5 leaders, 12 public-safety groups, 9 working-family and educator organizations, 5 veterans/community organizations, 3 businesses, and 3 local newspaper editorial boards (**37 named entries**).

Source and asset mappings are maintained in [`endorsements-manifest.json`](endorsements-manifest.json). The source CSV contains 73 media records, including duplicates, photos, unrelated organizational marks, and documents; it is not 73 distinct endorsers.

- NAPSO and Nevada Police Union appear as **text-only cards** because the CSV did not provide an unambiguous logo match.
- The earlier master endorsement sheet references eight leadership rows, but available source names/graphics identify only five. Three unnamed rows were **not fabricated**; provide their exact names/artwork to complete that part of the list.
- Unmatched Teamsters and unrelated regional-police logos were intentionally not published as endorsements.
- Newspaper cards link to the published editorial guides; a “Gun Sense Candidate” designation is not shown as an organizational endorsement.
- The site remains one GHL-ready static SPA; no GitHub Actions workflows were added.
