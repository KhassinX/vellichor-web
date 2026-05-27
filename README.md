# vellichor-www

Public web property for [Vellichor](https://vellichor.khassinx.com) — KhassinX commercial app.

Static Jekyll site served via GitHub Pages, proxied through Cloudflare for security headers (HSTS, CSP, X-Frame-Options, etc.). DNS: `vellichor.khassinx.com` CNAME → `khassinx.github.io` (proxy ON).

## Pre-reads

- `~/KhassinX/_template/web/WEB_PROPERTY_SPEC.md` — canonical spec for KhassinX web properties
- `~/KhassinX/_template/web/EMAILS.md` — email aliases canon

## Local preview

```bash
bundle install
bundle exec jekyll serve
```

## Deploy

Push to `main` → GitHub Pages builds + serves automatically. CF proxy ON injects the umbrella's Transform Rule security headers.

## OPSEC

- Zero PII in copy (no founder name, no Tampa/Florida/USA, no "solo dev")
- Bug bounty / responsible disclosure visible (`/security/` + `/.well-known/security.txt`)
- Audit before each deploy: `bash ~/KhassinX/_template/_scripts/audit_web_properties.sh vellichor.khassinx.com`
- Audit per `khassinx-web-audit` skill (responsive + a11y WCAG AA)
