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

- NAPSO and Nevada Police Union now display their campaign-provided logos in the public-safety section (added October 18, 2026).
- The earlier master endorsement sheet references eight leadership rows, but available source names/graphics identify only five. Three unnamed rows were **not fabricated**; provide their exact names/artwork to complete that part of the list.
- Unmatched Teamsters and unrelated regional-police logos were intentionally not published as endorsements.
- Newspaper cards link to the published editorial guides; a “Gun Sense Candidate” designation is not shown as an organizational endorsement.
- The site remains one GHL-ready static SPA; no GitHub Actions workflows were added.

## Form embedding: October 18, 2026

The original inline HighLevel form (`bNfm16tjccR3VPuBa7u4`) was collapsing on the GHL-hosted live page. The form loader has been hardened in both `main/index.html` and `GHL-PASTE-IN.html`, and the same standalone fix has been published on `gh-pages`.

**Changes:** removed `loading="lazy"`, deferred the iframe's real `src` until after HighLevel's embed helper initializes, reserved at least 1090px, repaired vendor-enforced off-screen or hidden iframe styles, restored a missing iframe after GHL hydration, and placed a direct form link above the embed so visitors can still contact the campaign if an external blocker prevents loading.

**The GHL live page does not automatically sync from GitHub.** To update `esmefornlv.com/home`, replace the previous full Custom Code element with the current entire contents of [`GHL-PASTE-IN.html`](GHL-PASTE-IN.html) and republish. Keep a single widget/form ID and do not add the original iframe code separately.

If fields still fail to load after publishing, check the browser Network/Console for blocked `api.leadconnectorhq.com/widget/form` or `link.msgsndr.com/js/form_embed.js`, other copies of `form_embed.js`, and **Optimize JavaScript** (temporarily disable for verification if GHL delays hydration). Use the direct form link as a temporary fallback.

QA: Source and JS syntax were checked across both branches; in a controlled local Chromium reproduction, a mock HighLevel helper that hid the iframe did not collapse the frame, and simulated helper unavailability still produced a visible, 1090px container. Because external domain access is restricted in this test environment, the actual HighLevel form response and CRM submissions could not be verified here.

## Campaign videos (October 18, 2026)

The page now contains a **ten-video YouTube Shorts gallery** after Updates and before Get Involved, which keeps all videos downstream of the endorsement wall. Each video has a source-based English and Spanish summary, an EN/ES-aware title and accessible play label, filter chips for Candidate Story / Housing / Community / Healthcare, and a direct YouTube link.

The gallery displays lazy thumbnail images but does **not** create any YouTube player iframe until the visitor clicks Play. The player is loaded from `youtube-nocookie.com`; closing or filtering away from a video removes the player and stops playback. Filtering and language switching stay within the same SPA.

The upload provided visible on-screen video overlays, **not reliable word-for-word audio transcripts**. The website therefore uses brief descriptions rather than mislabeling overlays as closed captions. The two closely related public-safety videos are kept separately because their video IDs differ. The ten IDs, titles and displayed summaries are stored in [`videos-manifest.json`](videos-manifest.json).

For the live `esmefornlv.com` page, **republish** the entire [GHL paste-in file](GHL-PASTE-IN.html) in its existing sole Custom Code block. The GitHub Pages demo updates from `gh-pages` independently and does not synchronize edits into HighLevel.

## Ward 1 civic-resource area (October 19, 2026)

The bilingual SPA now includes five anchored destinations while retaining the full campaign pages:

- **`#e-ward1`**: North Las Vegas history (1946, 1972, 2000, 2011, 2025, 2026), official Ward 1 map, and three places with tap-to-call and directions.
- **`#e-ward1-resources`**: prominent Dolores Huerta Resource Center card and an English/Spanish resident service telephone guide (four quick lines plus eight detailed directory contacts).
- **`#e-civic-vote`**: six official-resource links for government election information, registration, site details, mail ballots, official guides, and help. Information is maintained by Clark County and Nevada election authorities.
- **`#e-ward1-meetings`**: an October 2026 curated snapshot of four public-meeting opportunities and direct official calendar and boards/commissions links. Dated meeting cards hide automatically when their day has passed (Nevada local timezone).
- **`#e-who-to-call`**: anchor directly to the resident help directory within the resource area.

The menu includes **Ward 1** in place of an Updates shortcut to avoid overcrowding; Updates remains available in the footer. History appears after Priorities, while the resource, voting, and meeting content appears after campaign videos and before Get Involved. All 37 endorsement cards, 10 videos, contact form, and ES/EN toggle remain.

The linked government resources are distinct from campaign operations. Reference numbers, links, and meeting dates are captured in [`ward1-resource-sources.json`](ward1-resource-sources.json). Civic information should be reviewed if city websites change.

To apply this update to `esmefornlv.com`, replace the **single** existing HighLevel Custom Code block with [`GHL-PASTE-IN.html`](GHL-PASTE-IN.html) and republish. The GitHub Pages branch is independent of the GHL live site; no custom GitHub Actions workflows are used.
