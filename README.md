# NorCal EV Runs

The website for NorCal EV Runs, a NorCal EVs community for scenic group drives across Northern California.

## Local development

```bash
npm install
npm run dev
```

The local site runs at `http://localhost:4321`.

## Quality checks

```bash
npm run check
npm run build
```

## Publishing

Pushes to `main` build and publish the static site through GitHub Pages. In the repository settings, set Pages to use GitHub Actions. The custom domain is defined in `public/CNAME` as `norcalevruns.com`.

When the Pages deployment is ready, update the domain DNS to the GitHub Pages records and enable HTTPS in the repository settings.

## Community destinations

- Heylo: <https://heylo.group/norcalevruns>
- Instagram: <https://www.instagram.com/norcalevruns/>
- NorCal EVs: <https://norcalevs.org>
