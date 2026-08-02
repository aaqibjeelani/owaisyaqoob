# Owais Yaqoob — Fan Site

A single-page site for MMA fighter Owais Yaqoob. Just one file: `index.html` (no build step, no dependencies to install).

## Deploy to GitHub Pages (free)

1. Create a new repository on GitHub, e.g. `owais-yaqoob-site`.
2. Upload `index.html` to the root of that repo (drag-and-drop on the GitHub web UI works fine, or `git push`).
3. Go to the repo's **Settings → Pages**.
4. Under **Build and deployment → Source**, choose **Deploy from a branch**.
5. Pick branch `main` and folder `/ (root)`, then **Save**.
6. Wait ~1 minute — GitHub will give you a live URL like:
   `https://<your-username>.github.io/owais-yaqoob-site/`

## Editing content later

Everything is in `index.html` — text, styles, and layout in one file, no build tools needed. Open it in any text editor.

- **Fight record table**: look for `<section class="section" id="record">` — each fight is one `.rt-row` block.
- **Instagram feed**: look for `<section class="section" id="instagram">`. Posts are loaded as live Instagram embeds from the `IG_POSTS` array near the bottom of `index.html`. To change which posts show:
  1. Find `const IG_POSTS = [...]` at the bottom of `index.html`.
  2. Add or remove `instagram.com/p/...` or `instagram.com/reel/...` URLs (newest first).
  3. Save — Instagram's official `embed.js` renders each post automatically. If a tile stays on "Loading post…", that URL was removed/deleted — swap it.
- **Link/social-share preview**: Open Graph and Twitter meta tags live in `<head>` (title, description, and `og:image` pointing at `assets/img/1.jpg`). After deploying, replace the placeholder `https://aaqibjeelani.github.io/owaisyaqoob/` base in the `og:url` and `og:image`/`twitter:image` tags with your real URL.
- **Colors/fonts**: all defined as CSS variables at the top of the `<style>` block (`--ink`, `--saffron`, `--oxblood`, etc.) — change once, updates everywhere.

## Notes on the design

- Palette draws on Pulwama's saffron fields (gold accent) and the oxblood of the fight game, on a near-black ground.
- The dashed-thread divider between sections is a nod to saffron stigma threads, Pulwama's signature crop.
- The "Walkout" card documents Owais's actual ring-entrance ritual (karakuli cap, pashmina, tricolour) rather than generic fighter-page filler.
- Fight record and stats current as of **August 2, 2026** (day after his BRAVE CF 107 win over Delyan Georgiev).
