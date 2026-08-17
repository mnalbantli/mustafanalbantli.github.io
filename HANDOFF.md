# Handoff Brief — Portfolio Site → GitHub Pages Deployment

This project was designed and built in Claude.ai (chat) as static HTML/CSS/JS artifacts, iterating on content and visual direction with the site's owner (Mustafa Nalbantli, MS Data Analytics, job-searching for Analytics Engineer / Data Analyst roles). It's now ready to become a real deployed project. This doc gives you (Claude Code) the context needed to take it the rest of the way.

## What's already decided — please don't re-litigate these

- **Visual direction is locked.** Paper background, Fraunces serif headlines, IBM Plex Sans body, JetBrains Mono for stats/labels, navy/clay/gold accent palette. Don't redesign — just build/deploy what's here.
- **Content is locked and fact-checked.** Every number, tool name, and technical claim on these pages was sourced from the project owner's own detailed project documentation, with explicit "confirmed vs. unverified" discipline applied throughout the drafting process. Don't add, embellish, or "improve" any technical claims, stats, or tool names — if something looks incomplete, ask rather than filling gaps from assumption.
- **Deployment target: GitHub Pages.** Repo should be **public**. No custom domain yet — owner is undecided, so deploy to the default `*.github.io` subdomain and leave the door open for a custom domain later (a `CNAME` file can be added when they decide).

## What still needs doing

1. **Initialize the git repo** from these files, set up a clean commit history (not one giant initial commit — this person cares about clean git practice, it's literally a bullet point on their resume).
2. **Configure GitHub Pages** to serve from this repo (root or `/docs`, your call based on final repo structure) and confirm the live URL works end to end — homepage loads, all 4 project links work, back-links work.
3. **Mobile responsiveness check** — basic responsive rules exist in the CSS already (see `@media (max-width: 560px)` blocks in each file) but should be verified on an actual small viewport, not just assumed to work.
4. **Resume PDF — done.** `resume.pdf` is included in this repo and every "Download Resume" button already points to it. No action needed unless the owner sends an updated version.
5. **Optional, ask first:** light performance pass (Google Fonts are loaded via CDN `<link>` tags in each file's `<head>` — consider whether self-hosting or a shared stylesheet across pages is worth it, but don't do this without checking — the owner may prefer simplicity over a shared CSS file for now).

## Things to leave alone unless asked

- The scraper-resistant email pattern (JS assembles the mailto address at runtime rather than it appearing as plaintext in the HTML source) — this was a deliberate choice, not an oversight. Don't "simplify" it back to a plain `mailto:` link.
- The project ordering on the homepage (Mean Mug featured, then Retention Model, Student Success, Factbook) — deliberate, confirmed with the owner.
