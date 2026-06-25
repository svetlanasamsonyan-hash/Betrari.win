# Betrari.win

External UI customization for the **betrari.win** casino / iGaming site.

The stylesheet here is injected into the live site and served through the
**GitHub → jsDelivr CDN** pipeline. There is no build step or framework — the
deliverable is the raw CSS file itself.

## Layout

```
betrari.win/
  betrari.win.css   # main stylesheet injected into the site
```

## CDN delivery (jsDelivr)

Served from jsDelivr using the GitHub `gh` path:

```
https://cdn.jsdelivr.net/gh/svetlanasamsonyan-hash/Betrari.win@<ref>/betrari.win/betrari.win.css
```

- `@main` — tracks the branch (jsDelivr caches aggressively, up to ~7 days).
- `@<commit-sha>` — pins to an exact commit. **Preferred for production** —
  immutable and cache-busts automatically.

## Workflow

1. Edit `betrari.win/betrari.win.css`.
2. Commit and push to `main`.
3. Use the pinned jsDelivr URL (`@<new-commit-sha>`) on the site.
