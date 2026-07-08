# nexpoint.tv

Landing page for NexPoint — Android + Linux TV boxes shipping the latest stable
Linux. A single
self-contained static HTML page (no build step, no dependencies), served by
GitHub Pages at https://nexpoint.tv.

- `index.html` — the page (inline CSS; animated gradient wordmark). Sections:
  hero, the S1 4K spotlight, why-NexPoint, the-hardware, contact.
  Copy is positioning-level only; the S1 hardware spec sheet is pending real
  numbers (no fabricated SoC/RAM/ports/price).
- `CNAME` — custom apex domain (nexpoint.tv).
- `.nojekyll` — serve files as-is, no Jekyll processing.

## Deploy

Pushed to `git@github.com:NEXPOINT/www.git` (branch `master`). To go live:

1. **Repo → Settings → Pages** → Source: `Deploy from a branch`, Branch: `master` / `/root`.
2. Set the custom domain to `nexpoint.tv` (the `CNAME` file already declares it).
3. DNS is already pointed at GitHub Pages (apex `A`/`AAAA` → the GitHub Pages IPs,
   `www` → `nexpoint.github.io`, DNS-only; done 2026-07-08 via Cloudflare, email
   + DDNS preserved).
