# NorCal EV Runs Website Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Build and publish-ready a responsive one-page Astro site for NorCal EV Runs on GitHub Pages.

**Architecture:** Astro generates static HTML from a single page and a small set of reusable layout and navigation components. Plain CSS provides the complete visual system, responsiveness, and accessible motion. Heylo remains the source of truth for runs, membership, and joining.

**Tech Stack:** Astro 6, TypeScript, plain CSS, GitHub Actions, GitHub Pages

## Global Constraints

- Do not use em dashes in copy, code, or comments.
- Use semantic CSS tokens rather than raw color values inside components.
- Use `community`, `members`, and `join us` in public copy.
- Do not use `club`, `users`, `sign up`, `revolution`, `disrupting`, `game-changing`, `premier`, `EV lifestyle`, or `tribe` in public copy.
- Every run must be described as a group drive, never a race.
- Event registration and membership remain on Heylo.
- The site must work without client-side JavaScript.

---

### Task 1: Project foundation and design assets

**Files:**
- Create: `package.json`
- Create: `astro.config.mjs`
- Create: `tsconfig.json`
- Create: `.gitignore`
- Create: `public/CNAME`
- Create: `public/robots.txt`
- Create: `public/assets/images/norcal-ev-runs-logo.png`
- Create: `public/assets/images/norcal-road-hero.webp`

**Interfaces:**
- Consumes: the approved logo and original hero art.
- Produces: an Astro 6 static project and public assets used by the page.

- [ ] **Step 1: Define package scripts and dependencies**

Create scripts for `astro dev`, `astro build`, `astro preview`, and `astro check`. Pin Astro to the current major version and add the sitemap integration.

- [ ] **Step 2: Configure the production domain**

Set Astro `site` to `https://norcalevruns.com`, output to `static`, and create the `CNAME` and `robots.txt` files for the same domain.

- [ ] **Step 3: Add brand assets**

Copy the approved transparent logo and save the generated road image as optimized WebP.

- [ ] **Step 4: Install and verify the empty project**

Run: `npm install && npm run build`

Expected: Astro completes with exit code 0 and writes `dist/`.

### Task 2: Shared layout and metadata

**Files:**
- Create: `src/layouts/BaseLayout.astro`
- Create: `src/components/Nav.astro`
- Create: `src/components/Footer.astro`

**Interfaces:**
- Consumes: page `title`, `description`, and optional social image properties.
- Produces: semantic page shell, navigation landmarks, metadata, and footer links.

- [ ] **Step 1: Build the document shell**

Add canonical, Open Graph, Twitter, theme color, icon, and JSON-LD organization metadata. Include a skip link and semantic header, main, and footer landmarks.

- [ ] **Step 2: Build responsive navigation**

Add anchor links to Runs, Experience, Membership, and Safety, plus direct Instagram and Heylo actions. Implement the mobile menu with a native `details` element so navigation remains functional without JavaScript.

- [ ] **Step 3: Build the footer**

Include NorCal EVs parent attribution, contact email, social link, Heylo link, and dynamic copyright year.

- [ ] **Step 4: Run a type check**

Run: `npm run check`

Expected: 0 errors.

### Task 3: One-page narrative

**Files:**
- Create: `src/pages/index.astro`

**Interfaces:**
- Consumes: `BaseLayout`, the hero asset, and public destination URLs.
- Produces: all launch content and section anchors.

- [ ] **Step 1: Build the hero and route ribbon**

Use the approved headline, introductory copy, primary Heylo CTA, secondary experience anchor, and route-region labels.

- [ ] **Step 2: Build the experience sequence**

Create four accessible cards for meet, drive, charge, and arrive. Explain that details and expectations are shared before departure.

- [ ] **Step 3: Build the upcoming-runs CTA**

Create a single Heylo source-of-truth card with `See Upcoming Runs` and clear language that event registration is handled there.

- [ ] **Step 4: Build membership and safety sections**

Present monthly and yearly options, benefits, annual savings, separate event registration, and the `Runs, not races` safety statement.

- [ ] **Step 5: Build the closing community CTA**

Use `Good roads. Good people.` and provide Heylo, Instagram, and NorCal EVs links.

### Task 4: Visual system and responsive polish

**Files:**
- Create: `src/styles/global.css`

**Interfaces:**
- Consumes: semantic class names in the layout and page.
- Produces: the Road Atlas visual system across desktop, tablet, and mobile.

- [ ] **Step 1: Define semantic tokens and typography**

Create tokens for surface, ink, muted text, forest, teal, borders, shadows, type scales, spacing, radii, and content widths.

- [ ] **Step 2: Implement layout and route motifs**

Style the hero grid, waypoint labels, route line, experience cards, membership pricing, safety card, and closing CTA.

- [ ] **Step 3: Add interaction states**

Add visible focus, hover, active, and native details-menu states. Keep transitions below 300ms and disable nonessential movement for reduced-motion users.

- [ ] **Step 4: Add responsive rules**

Support wide desktop, tablet, and mobile widths down to 320px with no horizontal overflow.

### Task 5: Secondary routes and deployment

**Files:**
- Create: `src/pages/404.astro`
- Create: `.github/workflows/deploy.yml`
- Create: `README.md`

**Interfaces:**
- Consumes: the shared layout and GitHub Pages environment.
- Produces: a branded not-found page, automated static deployment, and setup documentation.

- [ ] **Step 1: Create the 404 page**

Provide a route-themed error message and links back home and to upcoming runs.

- [ ] **Step 2: Create the Pages workflow**

Use Node 24, `npm ci`, `npm run build`, `actions/upload-pages-artifact`, and `actions/deploy-pages` on pushes to `main`.

- [ ] **Step 3: Document launch steps**

Explain local commands, repository Pages settings, custom-domain configuration, and content destinations.

### Task 6: Verification and release

**Files:**
- Verify: all project files and built output

**Interfaces:**
- Consumes: complete site source.
- Produces: fresh evidence that the launch build and user experience meet the design.

- [ ] **Step 1: Run static validation**

Run: `npm run check && npm run build`

Expected: both commands exit 0 with no errors.

- [ ] **Step 2: Scan prohibited copy and raw component colors**

Run: `rg -n "—|revolution|disrupting|game-changing|premier|EV lifestyle|tribe|sign up|users" src public README.md`

Expected: no public-copy matches.

- [ ] **Step 3: Test rendered links and metadata**

Run a local preview and verify the title, canonical URL, main CTA destination, section anchors, image loads, and 404 response.

- [ ] **Step 4: Verify responsive layouts visually**

Capture desktop and mobile screenshots. Confirm readable content, visible controls, no overlap, and no horizontal scrolling.

- [ ] **Step 5: Create and push the GitHub repository**

Create the public `ZakWinnick/NorCalEVRuns` repository, push `main`, and confirm the remote contains the workflow and `CNAME`.

