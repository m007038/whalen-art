# whalen.art

Static site for JohnDavid Whalen. Faithful rebuild of the original, self-contained for GitHub Pages, with an invisible machine-readable layer for AI discovery and commissioning.

## Structure
- `index.html` — the whole single-page site (inline CSS + JS)
- `assets/series/` — "A World Without End" series images (upload from Drive)
- `assets/reality-of-dreams/` — realized commission images + section icon (upload from Drive); Hope and Purpose are also the two featured works in "The Work"
- `assets/icon-a-world-without-end.jpg` — backdrop icon for the hero + series section
- `.well-known/ai-art.json` — machine-readable art/commission offer for AI agents
- `ai.txt`, `llms.txt` — plain-text agent invitations pointing to the manifest
- `robots.txt`, `sitemap.xml`
- `CNAME` — custom domain (whalen.art)
- `UPLOAD-CHECKLIST.md` — exact Drive-file → repo-path mapping

## Machine-readable layer (invisible to human visitors)
- JSON-LD in `<head>`: Person, the commission Offer (5000 EUR), and the two collections
- `/.well-known/ai-art.json`: the agent-facing offer (price, buyer-supplies-feeling, delivery, NFT certificate wallet)
- `ai.txt` / `llms.txt`: discovery entry points

None of this changes what a human sees.

## Deploy (GitHub Pages)
1. Push these files to the repo root of a GitHub repo.
2. Settings → Pages → Source: deploy from branch (root).
3. Keep the `CNAME` file (whalen.art).
4. Point GoDaddy DNS at GitHub Pages (final step).

## Notes
- Commission form has no backend on a static host; it opens a pre-filled email to johndavid@whalen.art.
- Images self-host once uploaded; a temporary Readdy fallback keeps the series visible until then.
