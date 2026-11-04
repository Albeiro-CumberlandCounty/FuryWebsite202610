# Fayetteville Fury: SoccerShift SEO deployment notes

**Status:** The user created `/argentina2028` in SoccerShift. This GitHub review branch contains fixes that have not yet been pasted or published to SoccerShift. The standalone page file is [`Argentina2028`](../Argentina2028); paste that full file into the custom HTML editor of the existing SoccerShift Argentina page.

## 1. Why the HTML and SEO files are separate

All existing repo pages (`Home`, `Nxt`, `AboutFury`, etc.) are independent HTML fragments, not `<!doctype html>` documents. SoccerShift owns the real HTML `<head>`, site navigation and server root. A title tag, canonical link, robots file, or sitemap **placed inside the page body or only in GitHub** does not necessarily affect the live site.

- Open the existing SoccerShift page at `https://www.fayettevillefury.com/argentina2028`. You do not need to create another page.
- Paste the full content of [`Argentina2028`](../Argentina2028) into **that page's HTML/body editor**. Do not paste it into a global theme file.
- If SoccerShift has native page SEO fields, enter the title and description there rather than injecting `<head>` markup. Add a canonical only if the actual published URL matches.
- If SoccerShift explicitly allows custom *head* markup for the page, use the reviewed [`argentina-2028-head.html`](argentina-2028-head.html) and verify it appears in the actual served `<head>` exactly once. The head snippet is not a body snippet.
- If SoccerShift already serves `/robots.txt` or `/sitemap.xml`, keep its generated configuration and request changes through its platform controls. The files here are **reference templates**, not deployed root files.

## 2. Recommended on-page configuration

- Existing SoccerShift route: `https://www.fayettevillefury.com/argentina2028`. Confirm the canonical on the rendered website after updating.
- Title: `Fayetteville Fury Argentina 2028 | Buenos Aires Soccer Tour`.
- Description: `Fayetteville Fury is heading to Buenos Aires in June 2028. Learn about the planned soccer tour and register for the December 1 family webinar.`
- H1: `Fury is going to Argentina.`
- Social preview: the approved, club-hosted image recorded in the head example; replace with a properly sized, approved Argentina campaign image if one is uploaded to SoccerShift.
- The page's Zoom CTA goes to `https://us06web.zoom.us/webinar/register/WN_yKdBqIioQfqL6hirVjIMrw`. It is **webinar registration**, not payment or confirmation of a trip reservation.

## 3. Proposed titles and descriptions for existing SoccerShift pages

These are settings to apply through each page's SEO interface only after checking the rendered page content. Avoid duplicates and verify the correct slug.

| URL | Suggested title | Suggested description |
| --- | --- | --- |
| `/` | Fayetteville Fury | Youth Soccer in Fayetteville, NC | Learn about Fayetteville Fury youth soccer, player development, coaching, and opportunities for players in the Fayetteville area. |
| `/about-fury` | About Fayetteville Fury | Our Soccer Club & Mission | Learn about Fayetteville Fury's player-first approach, club history, and commitment to soccer development. |
| `/coaching-staff` | Fayetteville Fury Coaching Staff | Meet the Coaches | Meet the Fayetteville Fury staff supporting youth soccer players and their development. |
| `/nxt` | Fury NXT | Fayetteville Fury Youth Soccer Program | Explore Fury NXT soccer development, training, competition, and player opportunities. |
| `/player-development` | Player Development | Fayetteville Fury Soccer | Learn how Fayetteville Fury approaches youth soccer training, competition, and long-term player development. |
| `/player-pathway` | Player Pathway to Success | Fayetteville Fury | Explore the Fayetteville Fury player pathway through high school soccer and possible next steps. |
| `/tournaments` | Youth Soccer Tournaments | Fayetteville Fury | Find out how competitive tournaments fit into the Fayetteville Fury player development experience. |
| `/code-of-conduct` | Code of Conduct | Fayetteville Fury | Read Fayetteville Fury expectations for players, families, and coaches, including respect and player welfare. |
| `/contact` | Contact Fayetteville Fury | Youth Soccer Questions | Contact Fayetteville Fury about club programs, player development, and general soccer questions. |

Because `/home` may render duplicate homepage content, use `/` as the preferred canonical if SoccerShift allows and the URL is confirmed. Never try to canonicalize with robots.txt.

## 4. XML and robots deployment

- [`robots.txt`](robots.txt) is a root-level **example** only. Check `https://www.fayettevillefury.com/robots.txt` first and do not accidentally overwrite the platform's instructions.
- [`sitemap.xml`](sitemap.xml) is a draft of expected page paths, including the existing Argentina page. Check each slug returns an indexable canonical page before applying any site-level change.
- If SoccerShift generates its own sitemap, update site routing through SoccerShift and submit the generated sitemap to Google Search Console instead of creating a second one.
- Do not add made-up `lastmod` timestamps; they should reflect real substantial updates.

## 5. Structured data and search eligibility

The separate head example uses a simple `WebPage` item with `WebSite` and `Organization` context. It intentionally does not use `Event` rich-result markup for the Zoom-only webinar, as Google's event search feature does not support virtual-only events. The June 2028 trip also must not be presented as a dated public booking event without validated dates and details.

Verify structured data using Google's Rich Results Test and the HTML source after publication. Schema does not guarantee ranking or special display treatment.

## 6. Images and SoccerShift CSS isolation

- All new landing-page CSS selectors are scoped under `.fury-ar28`. The optional homepage promo snippet has its own prefix `.fury-ar28-promo`.
- The landing page currently reuses two **existing Fury-hosted photographs** from the club's HTML. They are general Fury soccer imagery, not pictures of the future Argentina tour.
- Before live publication, the club may choose to upload the supplied Argentina campaign image to SoccerShift and use the resulting trusted public CDN URL. Do not put Drive viewer links, invented CDN names, or untested base64 images into production.
- The hero image uses `fetchpriority=high` and eager loading; the secondary photo is lazy-loaded.
- Keep any page-local H1 semantics; do not replace headings with divs simply to work around SoccerShift CSS.

## 7. Release and QA checklist

- [ ] Confirm the webinar URL works and its destination is the right event.
- [ ] Confirm date/time: Tuesday, December 1, **2026**, at 7:00 PM Eastern; trip: June **2028**.
- [ ] Confirm final trip itinerary, inclusions, costs, and image permissions with organizers.
- [ ] Replace the Argentina page's existing custom HTML with the updated `Argentina2028` standalone fragment, retaining the page URL `/argentina2028`.
- [ ] Test CSS against the SoccerShift theme with the exact page editor, on mobile and desktop.
- [ ] At 320, 375, 390, 768, and 1440 CSS px: no horizontal scroll, clipped copy, or unusable controls.
- [ ] Test keyboard-only navigation, visible focus, alt text, reduced motion, 200%/400% zoom and screen-reader reading order.
- [ ] Test the three CTA links and all FAQ disclosures.
- [ ] Confirm page-level SEO title, meta description, single canonical, Open Graph image, JSON-LD, sitemap and robots in the **rendered live HTML**.
- [ ] Measure image performance/LCP and confirm the hero is a suitable responsive crop.
- [ ] Replace the SoccerShift homepage HTML using the updated `Home` file; it now contains the scoped Argentina announcement immediately after the hero section. The `Argentina2028HomePromo` file is a reusable standalone copy, not an extra page.
- [ ] Submit the live canonical URL and sitemap in Search Console after publishing.

## References

- Google Search Central: [Specify a canonical URL](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls)
- Google Search Central: [Build and submit a sitemap](https://developers.google.com/search/docs/crawling-indexing/sitemaps/build-sitemap)
- Google Search Central: [Event structured data guidelines](https://developers.google.com/search/docs/appearance/structured-data/event)
