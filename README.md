# orbios.info — Orbios Agency (two-sided)

One page. Static. No build step, no framework, no CMS, no tracking.

`index.html` + `styles.css` + `favicon.svg` — that is the whole site.

| | |
|---|---|
| Domain | `orbios.info` (Namecheap) |
| Host | Vercel, static, Production branch `main` |
| Live | https://orbios.info |
| Client door | Hero + 4-asset fact grid + unit economics → 5 badges (tabs: pick a badge, see its 5-day scope, book / pre-order or join the track) → talent showcase. Book / pre-order opens a `<dialog>` that drafts a `mailto:contact@orbios.io` (plain `mailto` links without JS); Telegram fallback `@lika_orbios` |
| Intern door | 5-day intensive + apply form (5 tracks) → `mailto:contact@orbios.io` with the track in the subject. "Join track" links in the badge panels preselect the track |
| Links out | Camp https://www.orbios.org · Agency https://orbios.io |
| UI | Dark `#080c14`. Accents: emerald `#10b981` (primary), cyan `#38bdf8`, amber `#fbbf24`; badge colours violet `#a78bfa` (Thai Ops), rose `#f472b6` (Personal). Plus Jakarta Sans + JetBrains Mono |

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

- `Арендуй сертифицированного AI-оператора`
- `BUILT WITH AGENTS. RUN BY HUMANS.`

## Where this comes from (Orbios OS repo, private)

| What | Path in `orbios-os` |
|---|---|
| Agency model (badges, unit economics) | `context/company/agency-toptal-model.md` |
| B2B offer brief | `log/vector/research/2026-09-28-agency-toptal-model-and-b2b-offer-BRIEF.md` |
| Site unit (domain / host / manage) | `context/sites/orbios-info/site.yaml` |
| Deploy prove | `sops/website_deploy_verify.md` |

## Rules for edits

- Price is `$199` all-in (`$99` Orbios + `$100` operator), bonus up to `$100` is the client's call. Intern pay is `$100` base + up to `$100` bonus. Change both only from the agency model doc.
- Only operators who passed the sprint go on the showcase as available. Everyone else is pre-order.
- Mobile floor 375px: no horizontal scroll, tap targets ≥ 44px.
- Client copy: plain commercial language, no officialese (`AGENTS.md` §6 stop-list).
- No secrets, tokens, or registrar credentials in this repo. `orbios-os` is private — do not link to it.
