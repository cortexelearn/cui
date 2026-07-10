# CortexEdge — Controlled Unclassified Information (CUI) Track

A standalone Progressive Web App teaching the handling, transmission, and rules of
Controlled Unclassified Information (CUI) for aerospace/defense professionals.
15 lessons across 4 phases + a 53-question final exam pool + a certificate of completion.

**This is an information-awareness course for reference only — not legal or compliance
advice, and not an official CUI/CMMC certification.** See the disclaimer in-app and on
the certificate. Content reflects the regulatory landscape as of early 2026 and should
be reviewed by a subject-matter expert before operational reliance.

## Deploy to GitHub Pages

1. Create a repository named **`cui`** under the `cortexelearn` account.
2. Upload the **CONTENTS** of this folder (index.html, manifest.json, sw.js, icons/) to the repo **root** — not the folder itself.
3. Settings → Pages → Deploy from branch: `main`, folder `/ (root)`.
4. The course will be live at **https://cortexelearn.github.io/cui/**

## Structure

- `index.html` — the full app (React 18 + Babel via CDN, course data inlined)
- `manifest.json` — PWA manifest (scoped to `/cui/`)
- `sw.js` — service worker (network-first for HTML, cache-first for static/CDN). Cache: `cortexedge-cui-v2`
- `icons/` — app icons

## Features

- 15 lessons: 10 with verified videos, 14 with official .gov reference cards (34 authoritative links — NARA/ISOO, dodcui.mil, DoDI 5200.48, NIST, eCFR, CDSE, DCSA, FedRAMP, SPRS, DIBNet), and a capstone CUI-lifecycle infographic
- Per-lesson knowledge-check quizzes with explanations
- 53-question final exam (shuffled questions + answers), **85% to pass (46/53)**
- Certificate of completion (unlocks on passing; carries the awareness/disclaimer statement), printable to PDF
- Progress (exam result, certificate name) persists locally via localStorage
- "← All Courses" back link to the landing page
- Offline-capable, installable, ad-free, no account required

## Updating

1. Edit the course data (`CUI_LESSONS` / `CUI_FINAL_EXAM`) or component inside `index.html`.
2. Bump `CACHE_NAME` in `sw.js` (e.g., `cortexedge-cui-v1` → `-v2`) so clients refresh.
3. Re-upload to the repo root.

## Brand

CortexEdge E-Learning · CortexEdge@outlook.com · dark aerospace theme, burnt-orange/cream · ad-free.
