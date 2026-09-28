# orbios.info — Orbios Agency (two doors)

Two pages. One design system. Static. No build step, no framework, no CMS, no tracking.

`index.html` + `hire.html` + `styles.css` + `favicon.svg` — that is the whole site.

| | |
|---|---|
| Domain | `orbios.info` (Namecheap) |
| Host | Vercel, static, Production branch `main` |
| Live | https://orbios.info |
| Client door | `/hire.html` — hero + 5 badge tabs + what stays forever (Discord, prompt stack, GitHub) + operator #01 / waitlist + booking `<dialog>`. No intern copy, no `$100` split. Mailto `contact@orbios.io`; Telegram `@lika_orbios` |
| Intern door | `/` `index.html` — 5-day intensive, terms (`$100` + up to `$100`), 5 track requirements, cohort 01.10 apply form. Header link: «Клиентам / Нанять оператора →» `/hire.html` |
| Links out | Camp https://www.orbios.org · Agency https://orbios.io |
| UI | Dark `#080c14`. Accents: emerald `#10b981` (primary), cyan `#38bdf8`, amber `#fbbf24`; badge colours violet `#a78bfa` (Thai Ops), rose `#f472b6` (Personal). Plus Jakarta Sans + JetBrains Mono |

## Run

No install. Open `index.html` or `hire.html`, or:

```bash
npx serve .
```

## Ship

```bash
git push origin main
```

Push is **not** shipped. Vercel builds, then the fingerprint must pass on the live URL —
`sops/website_deploy_verify.md` in `orbios-os`. Fingerprint strings for this site:

Homepage `https://orbios.info` (intern door):

- `5 дней боевого интенсива`
- `BUILT WITH AGENTS. RUN BY HUMANS.`

Client door `https://orbios.info/hire.html`:

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

- Client page shows `$199` as a finished service. Do not put the `$100` operator pay, internships, training, or the apply form on `hire.html`.
- Intern pay on `index.html` is `$100` base + up to `$100` bonus. Change either number only from the agency model doc.
- Only operators who passed certification go on the hire showcase as available. Everyone else is waitlist.
- Mobile floor 375px: no horizontal scroll, tap targets ≥ 44px.
- Client copy: plain commercial language, no officialese (`AGENTS.md` §6 stop-list).
- No secrets, tokens, or registrar credentials in this repo. `orbios-os` is private — do not link to it.
