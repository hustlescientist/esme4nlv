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
