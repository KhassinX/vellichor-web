# vellichor-web

Source for **vellichor.khassinx.com** — the public web property for **Vellichor**, a PDF Q&A app powered by Apple Intelligence on-device, for iPhone, iPad, and Mac.

## What lives here

- `index.html` — landing page (EN)
- `legal/` — Privacy Policy, Terms of Use, Legal index
- `security/` — Security & Responsible Disclosure
- `press/` — Press kit (fact sheet, contact, brand assets)
- `es/` — natively written localized mirror (Spanish; neutral panhispanic). pt-BR/de-DE deferred to v1.x (ADR 0008)
- `_layouts/` — Jekyll base + prose layouts (shared with rest of KhassinX umbrella)
- `assets/css/` — Layer 3 primitives + Layer 2 Vellichor brand tokens (warm brown signature)
- `assets/favicons/` — V monogram favicons (parchment warm brown)
- `.well-known/security.txt` — RFC 9116 machine-readable security policy

## Stack

GitHub Pages (Jekyll) → Cloudflare proxy → `vellichor.khassinx.com`. Custom domain via `CNAME` file. SSL via Cloudflare Full (strict). Security headers via CF Transform Rules (HSTS, X-Frame-Options, X-Content-Type-Options, Referrer-Policy, Permissions-Policy, CSP).

Canonical spec: `~/KhassinX/_template/web/WEB_PROPERTY_SPEC.md`.
Brand origin: `~/KhassinX/_template/designs/2026-05-26-vellichor-design.md`.

## Localization

EN default (no prefix), ES under `/es/`. Each locale is **natively written**, not machine-translated. Per-page `lang:` front-matter + hreflang tags signal locale to crawlers. pt-BR + de-DE deferred to v1.x per ADR 0008 (v1 ships en-US + es only).

## Brand

"Vellichor" is from John Koenig's *Dictionary of Obscure Sorrows* (2014): *"the strange wistfulness of used bookstores"*. The warm brown accent reflects aged paper and parchment.

## Contact

- General: [hello@khassinx.com](mailto:hello@khassinx.com)
- Press: [press@khassinx.com](mailto:press@khassinx.com)
- Security: [security@khassinx.com](mailto:security@khassinx.com)
