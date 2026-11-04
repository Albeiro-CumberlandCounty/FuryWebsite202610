# FuryWebsite202610
Pages in HTML for the Fury Website

## Project references

- [Content, merchandise, and image guidelines](CONTENT_GUIDELINES.md)

## SoccerShift page mapping

- `CodeOfConduct` is the page content for `/code-of-conduct`.
- `ResourcesMenu` is the Resources submenu markup for SoccerShift. It preserves Player Registration and Financial Assistance and adds Code of Conduct; it does not add a new top-level menu.
- `Contact` is the page content for `/contact`; its form submits inquiries to `info@fayettevillefury.com` through FormSubmit.

## Argentina 2028 campaign (review branch only)

- `Argentina2028`: approved cinematic, fully scoped HTML/CSS fragment for a dedicated SoccerShift page, actual SoccerShift URL `/argentina2028`. Three CTA buttons open the [December 1, 2026, 7:00 PM Eastern Zoom webinar](https://us06web.zoom.us/webinar/register/WN_yKdBqIioQfqL6hirVjIMrw).
- `Home`: now includes the Argentina webinar announcement below the hero, scoped under `.fury-ar28-promo`. Updating this HTML fragment in GitHub does not automatically update the SoccerShift homepage.
- `Argentina2028HomePromo`: standalone copy of the announcement for reuse; it links to `/argentina2028`.
- `seo/argentina-2028-head.html`: metadata and WebPage JSON-LD **for SoccerShift's head/SEO controls**, never the page body.
- `seo/robots.txt` and `seo/sitemap.xml`: **reference templates**, not automatically deployed to the SoccerShift site root.
- [SEO rollout and QA checklist](seo/SOCCERSHIFT_DEPLOYMENT.md).

No production deployment is part of the GitHub review branch. **Merging this branch does not publish the site:** SoccerShift content and settings are updated separately after approval.
