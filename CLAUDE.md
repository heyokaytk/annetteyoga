# Yoga With Annette Website

## What This Is

Website for Annette Opas, a yoga instructor in Halifax, NS offering private classes and corporate bookings.

Website: yogawithannette.com
Repo: heyokaytk/annetteyoga (GitHub)
Hosting: GitHub Pages (`CNAME` file sets custom domain), fronted by Cloudflare DNS.

This top-level project folder IS the live repo (confirmed remote: `heyokaytk/annetteyoga.git`, up to date with `origin/main`). A previous, disconnected local copy with no remote existed nested inside it (`Yoga Website/`) — archived to `_archive-stale-yoga-site/` on 2026-07-22, confirmed superseded (the live site had already moved past everything in it, including two sections — video, bookshelf — deliberately removed later per the live repo's own commit history).

---

## Stack

Static HTML (`index.html`), no build step. No JS framework — vanilla JS for nav, scroll reveal, contact form AJAX, and the reflections "read more" accordion.
SEO files: `sitemap.xml`, `robots.txt` (already clean, no Cloudflare Managed-robots.txt injection as of 2026-07-22).

After any site change: push to `main` on GitHub (Pages rebuilds automatically). If the change doesn't appear live, purge Cloudflare cache in addition to the push — same as Golden Service and Bump & Grind.

---

## Pre-Commit / Pre-Push Audit

Before every `git commit` + `git push` on this site, run this audit on the diff being shipped. Act as a Principal Web Developer, UX/UI Expert, and Technical SEO Strategist. Give a rigorous, customized audit based on the actual code, copy, and architecture changed — not generic advice.

Audit across four pillars:

1. **UX/UI & Conversion Flow** — Does the change help or hurt the path to the primary CTA (contact form for private/corporate booking inquiries)? Any new friction points? Mobile responsiveness impact?
2. **Technical Architecture & Performance** — Is the code efficient? Any rendering roadblocks, bloated scripts, or structural issues introduced? Watch image weight in particular — the hero background is a full-viewport photo and directly affects load time.
3. **Technical & On-Page SEO** — Metadata, header hierarchy (H1/H2/H3), alt text — still optimized for target search intent after this change? Confirm canonical tag and www/non-www consistency aren't broken; confirm JSON-LD stays valid.
4. **Actionable Roadmap** — Prioritized checklist: Critical (fix before this push), High Impact (this week), Long-Term (this month).

Primary Goal: Convert visitors into private-class or corporate-booking inquiries via the contact form.
Target Audience: Individuals seeking private yoga instruction and Halifax-area businesses considering workplace wellness sessions.
Tech Stack Context: Static HTML on GitHub Pages, custom domain via Cloudflare DNS. No CI build step — what's pushed to `main` is what ships.

Scope the audit to the actual diff unless the change touches enough of the page to warrant a full-page pass. Present findings as a punch list. Don't block the commit — flag issues and let the site owner decide what to fix now vs. later.
