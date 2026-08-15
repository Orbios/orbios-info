# orbios.info — Orbios 3.0 manifesto

One screen. Static. No build step, no framework, no CMS, no tracking.

`index.html` + `styles.css` + `favicon.svg` — that is the whole site.

| | |
|---|---|
| Domain | `orbios.info` (registrar TODO — Founder) |
| Host | Vercel, static, Production branch `main` |
| Live | https://orbios.info |
| Doors | `mailto:contact@orbios.io` with the door in the subject |
| Links out | Camp https://www.orbios.org · Agency https://orbios.io |

## Run

No install. Open `index.html`, or:

```bash
npx serve .
```

## Ship

```bash
git push origin main
```

Push is **not** shipped. Vercel builds, then the fingerprint must pass on the live URL —
`sops/website_deploy_verify.md` in `orbios-os`. Fingerprint strings for this site:

- `Camp. AI Agency. Governed by Founder OS.`
- `The Founder ratifies. He is not the factory.`

## Where this comes from (Orbios OS repo, private)

| What | Path in `orbios-os` |
|---|---|
| Build brief | `context/briefs/2026-08-16-architect-orbios-info-site-brief.md` |
| Copy source of truth | `log/vector/research/2026-08-15-orbios-info-manifesto-3.md` |
| Site unit (domain / host / manage) | `context/sites/orbios-info/site.yaml` |
| Craft rules for landings | `log/vector/research/2026-08-16-landing-anti-slop-craft.md` |
| Deploy prove | `sops/website_deploy_verify.md` |

## Rules for edits

- Copy changes come from the manifesto SoT above. Do not write a second manifesto here.
- One screen, one route. No blog, no i18n, no second page in v1.
- Public page: no book, no perimeter, no owner targets, no securities language.
  A market seat is a share of a closed paid order, not an investment offer.
- No secrets, tokens, or registrar credentials in this repo.
