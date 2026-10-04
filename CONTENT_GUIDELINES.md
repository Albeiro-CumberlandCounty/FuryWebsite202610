# Fayetteville Fury content guidelines

This file records business and asset rules that must be followed when building future Fayetteville Fury pages. It is a development reference, not a public website page.

## Merchandise destinations

Fayetteville Fury has two separate merchandise destinations. They must remain clearly distinguished in page copy and calls to action.

### Player uniforms and team kits

- Destination: <https://diaza.com/collections/fayetteville-fury-team>
- Provider: DIAZA
- Use only for official player uniforms, player kits, and team uniform purchasing.
- Suitable CTA labels include `SHOP PLAYER UNIFORMS` and `SHOP TEAM UNIFORMS`.
- Do not describe DIAZA as the general Fury fan store.

### Parent, coach, and fan gear

- Destination: <https://www.soccer.com/club/#/2006784728/fanwear?category=Seasonal>
- Provider: Soccer.com
- Use for fanwear, parent gear, coach gear, supporter gear, Fury apparel, and general Fury merchandise.
- Suitable CTA labels include `SHOP FURY FANWEAR` and `SHOP FAN GEAR`.

### External-link implementation

Both merchandise destinations are external. Every merchandise CTA must:

- open in a new tab with `target="_blank"`;
- include `rel="noopener noreferrer"`;
- use descriptive visible text that identifies uniforms or fanwear; and
- never combine the DIAZA and Soccer.com purposes into one generic store link.

Do not create an internal `/store` or `/fan-store` route unless that route is explicitly approved later. Do not invent product or merchandise URLs.

## Website image management

Authentic Fayetteville Fury photography is the preferred source for the website. Do not substitute generic stock photography when suitable club photography is available, and do not invent or copy random external image URLs.

The known source library is organized in Google Drive under:

- `Fury Media/Pictures`
- `Website Items`
- `Fury NXT`

Original source photographs must remain untouched. Image work should maintain three distinct stages:

1. **Source photos** — the original, unmodified Google Drive library.
2. **Approved website photos** — reviewed assets approved for web use, including any non-destructive crops or corrected derivatives.
3. **Page-specific assignments** — the selected approved asset, intended section, crop/orientation, alt text, and rationale for a particular page.

## Image selection workflow

Before implementing imagery on a new page:

1. List the sections that need images and the purpose of each image.
2. Review the available Fury source photography rather than defaulting to URLs already used in existing HTML.
3. Compare candidates for subject matter, composition, action, emotional impact, lighting, image quality, and authentic Fury identity.
4. Consider player diversity, age group, gender representation, and whether the story calls for training, competition, a team, or an individual.
5. Check orientation, usable negative space, expected desktop crop, and expected mobile crop.
6. Select the strongest candidate for each specific section and avoid repeating an image on the same page without a clear design reason.
7. Record any needed crop, color correction, or background treatment before implementation; never overwrite the source photograph.
8. Implement only the approved asset and give it accurate, descriptive alternative text.

When candidates are otherwise comparable, prefer the photograph with stronger composition, better lighting, clearer Fury identity, more useful negative space, a better responsive crop, and more variety relative to imagery already used elsewhere. Do not select automatically by recency or file size.

## Site-wide image variety

Image assignments should intentionally rotate through the breadth of the organization, including:

- training and technical development;
- match action and tournament competition;
- team celebrations, awards, and championships;
- players with coaches;
- individual players and team photos;
- boys and girls;
- younger and high school players;
- goalkeepers;
- community moments;
- leadership and staff; and
- Fury identity and branding.

The goal is for the website to represent an active soccer organization rather than repeatedly presenting one photo session or a small group of familiar assets.

## Asset-access requirement

The Google Drive photo library is not stored in this repository. A developer must have access to the approved Drive folders—or receive exported approved assets and their final hosted URLs—before assigning new photography. Until that access exists, do not guess filenames, invent URLs, or download substitute stock images.
