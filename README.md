# What's in this folder

- `index.html` — the landing page. Copy is rewritten for clarity: big "FREE" messaging up top, plain-language benefit stats, a simple 3-step "how it works," and a strong CTA. Fifth-grade reading level on purpose — the goal is instant clarity, not clever writing.
- `assets/photos/` — the 20 real listing photos, downloaded and saved locally (not linked to the original site). This fixes the hotlinking issue that kept them from showing up before.
- `CLAUDE_CODE_PROMPT.md` — paste this into Claude Code to get the site tested and deployed to a live URL.

# What was actually broken before

1. **The photos were hotlinked** from franklinwest.com's image host, which blocks other sites from displaying its images directly. They're now downloaded into `assets/photos/` and referenced locally, so they'll load anywhere this folder is hosted.
2. **The video likely wasn't working because the file was opened directly** (double-clicked, showing a `file://` address instead of `http://`). Browsers block YouTube's embed API under `file://` for security reasons. Once this is served from an actual URL — even a local test server, and definitely once deployed live — the video will work normally.

# What changed in the copy

- Old version buried the free offer under a headline about the video itself. New version leads with "Get a FREE video" and repeats "free" multiple times (banner, headline, pill badge, steps, CTA button) so it's impossible to miss.
- Replaced abstract phrases ("virtual tour," "vacancy loss," "occupancy") with plain language a busy landlord skimming on their phone can understand in one pass.
- Stats are shown as big bold numbers with one plain sentence each, not paragraphs.
- The 3-step "how it works" exists specifically to make the process feel fast and effortless — removing that friction is what actually gets busy property managers to say yes, more than any amount of persuasive language.
