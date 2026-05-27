# vellichor-www — TROUBLESHOOTING / TODO

## Pre-launch TODOs

### Favicons PNG (apple-touch + 32 + 16)

Status: SVG monogram (`assets/favicons/vellichor.svg`) está. Faltan los PNGs binarios:

- `assets/favicons/apple-touch-icon.png` (180×180)
- `assets/favicons/favicon-32.png` (32×32)
- `assets/favicons/favicon-16.png` (16×16)

Mientras no existan, los `<link rel="apple-touch-icon">` y `<link rel="icon" type="image/png">` del `_layouts/base.html` apuntan a archivos 404. Browser fallback al SVG. No es bloqueante para staging, pero ANTES DE APP STORE LAUNCH hay que generarlos.

**Cómo generarlos**:

Opción A — vía herramienta de design (Affinity Designer / Figma): exportar SVG a PNG en los tres tamaños.

Opción B — vía CLI (requiere `librsvg` instalado: `brew install librsvg`):

```bash
cd ~/KhassinX/vellichor-www/assets/favicons
rsvg-convert -w 180 -h 180 vellichor.svg -o apple-touch-icon.png
rsvg-convert -w 32  -h 32  vellichor.svg -o favicon-32.png
rsvg-convert -w 16  -h 16  vellichor.svg -o favicon-16.png
```

Verificar:
```bash
curl -sI https://vellichor.khassinx.com/assets/favicons/apple-touch-icon.png | head -1
# Debe ser HTTP/2 200
```

### Press alias

`press@khassinx.com` está enlazado desde `/press/`. Verificar en Proton Mail dashboard que el alias existe o crearlo antes de promocionar la página. Per `~/KhassinX/_template/web/EMAILS.md` canon.
