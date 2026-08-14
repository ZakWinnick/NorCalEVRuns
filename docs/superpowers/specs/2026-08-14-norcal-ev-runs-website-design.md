# NorCal EV Runs Website Design

## Purpose

Launch `norcalevruns.com` as the public front door for NorCal EV Runs, a cross-brand driving community from NorCal EVs. The site should turn social interest into attendance at upcoming paid runs and supporting membership while making the safety culture clear.

## Product direction

The launch is a focused one-page site with expansion-ready Astro structure. The page has one dominant action, `See Upcoming Runs`, which leads to the NorCal EV Runs Heylo group. `Join the Community` and Instagram are secondary actions.

The site is informational. Event registration, supporting memberships, community administration, and waiver acceptance stay in Heylo.

## Audience

- Northern California EV owners who want scenic drives and destination meetups.
- Drivers of every EV brand, including people new to group drives.
- Existing NorCal EVs members who want a more drive-focused experience.

## Experience principles

1. **The road comes first.** Scenic routes, shared stops, and thoughtful pacing lead the story.
2. **Cross-brand by design.** No single vehicle marque dominates the imagery or copy.
3. **Energetic, not aggressive.** Runs are clearly described as group drives, never races.
4. **Useful at a glance.** Visitors can understand the format, membership value, and next action in one scroll.
5. **Connected but distinct.** The site visibly belongs to the NorCal EVs family while retaining the green and teal NorCal EV Runs identity.

## Visual concept: The Road Atlas

The visual system combines an editorial Northern California road photograph with route-map graphics, waypoint labels, hairline grids, and compact mono typography. A continuous teal route line moves through key sections. Forest green carries the brand, teal marks decisions and waypoints, and warm off-white keeps the page outdoorsy rather than clinical.

The logo appears as the primary identity. It is not recreated or altered. Supporting typography uses a confident condensed display face for headlines, a neutral sans serif for body copy, and a mono face for route labels.

## Page structure

1. **Navigation:** Logo, Runs, The Experience, Membership, Safety, Instagram, and a compact Heylo CTA.
2. **Hero:** `Northern California looks better in motion.` Supporting copy explains scenic, all-EV group drives. Primary CTA is `See Upcoming Runs`; secondary CTA is `How Runs Work`.
3. **Route ribbon:** A visual strip establishing coast, redwoods, foothills, and Sierra destinations.
4. **The experience:** Four stages, meet, drive, charge, arrive, each explained with a route-style card.
5. **Upcoming runs CTA:** A high-contrast card directing visitors to current Heylo events without duplicating live event data.
6. **Membership:** Supporting membership at $5 monthly or $50 yearly, including 10% off paid events, a sticker, and future merchandise discounts. Event registration remains separate.
7. **Safety:** Clear `Runs, not races` statement, lawful driving expectations, and participant responsibility.
8. **Community close:** `Good roads. Good people.` with links to Heylo, Instagram, and NorCal EVs.
9. **Footer:** Parent identity, contact email, privacy note, and copyright.

## Responsive behavior

- Desktop uses an asymmetric editorial grid with the hero image occupying the right side.
- Tablet collapses route cards into two columns.
- Mobile becomes a single-column journey with large tap targets, compact navigation, and no horizontal overflow.
- Motion is subtle and respects `prefers-reduced-motion`.

## Accessibility and quality

- WCAG AA contrast for text and controls.
- Semantic headings, landmarks, labels, and visible keyboard focus.
- Informative images have descriptive alt text. Decorative route graphics are hidden from assistive technology.
- No essential information depends on animation.
- The site renders without client-side JavaScript. A small progressive enhancement script may control mobile navigation and reveal effects.

## Technical approach

- Astro 6 static output.
- Plain CSS with semantic custom properties, no Tailwind and no component library.
- GitHub Actions deployment to GitHub Pages.
- `public/CNAME` contains `norcalevruns.com`.
- SEO metadata, Open Graph metadata, structured data, sitemap, robots file, and a custom 404 page ship at launch.
- Live event data remains on Heylo to avoid stale information on the website.

## Links

- Upcoming runs and community: `https://heylo.group/norcalevruns`
- Parent community: `https://norcalevs.org`
- Contact: `mailto:info@norcalevs.org`
- Instagram: `https://www.instagram.com/norcalevruns/`

## Launch acceptance

- Production build succeeds with no errors.
- Every internal anchor and external CTA resolves to the intended destination.
- Desktop and mobile screenshots show no clipping, overlap, or horizontal scrolling.
- Page metadata and structured data contain the final domain and community name.
- The GitHub repository contains the complete source, deployment workflow, and domain file.

