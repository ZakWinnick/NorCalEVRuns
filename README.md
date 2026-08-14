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

Pushes to `main` build and publish the static site through GitHub Pages. Pages is configured to use GitHub Actions, and the custom domain is set to `norcalevruns.com`.

### Domain cutover

Remove the existing Cloudflare redirect to Heylo, then configure these DNS records:

| Type | Name | Value |
| --- | --- | --- |
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |
| CNAME | `www` | `zakwinnick.github.io` |

After DNS has propagated, confirm the domain check in GitHub Pages settings and enable HTTPS enforcement.

## Community destinations

- Heylo: <https://heylo.group/norcalevruns>
- Instagram: <https://www.instagram.com/norcalevruns/>
- NorCal EVs: <https://norcalevs.org>
