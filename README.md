# nexpoint.tv

Landing page for NexPoint — a single self-contained static HTML page (no build
step, no dependencies), served by GitHub Pages at https://nexpoint.tv.

- `index.html` — the page (inline CSS; animated gradient wordmark). Currently a
  neutral holding page (wordmark + contact) pending final content.
- `CNAME` — custom apex domain (nexpoint.tv).
- `.nojekyll` — serve files as-is, no Jekyll processing.

## Deploy

Pushed to `git@github.com:NEXPOINT/www.git` (branch `master`). To go live:

1. **Repo → Settings → Pages** → Source: `Deploy from a branch`, Branch: `master` / `/root`.
2. Set the custom domain to `nexpoint.tv` (the `CNAME` file already declares it).
3. Point DNS for `nexpoint.tv` at GitHub Pages (apex `A`/`AAAA` records to the
   GitHub Pages IPs, or move the apex behind the Pages target). Note: the domain
   currently resolves to a Linode host — repointing replaces that.
