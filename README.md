# HKSPCCM 2nd AGM & Annual Scientific Meeting — Landing Page

A single-file, responsive landing page for the Hong Kong Society of Paediatric
Critical Care Medicine's 2nd AGM & Annual Scientific Meeting.

## Overview

This is a self-contained `index.html` that renders two distinct layouts:

- **Mobile** — a compact, single-column view optimised for small screens.
- **Desktop** — a wider two-column hero layout with a footer illustration
  strip.

Both versions are embedded in the same file and swapped in based on a
`861px` viewport breakpoint, so the page can be hosted anywhere as a static
file with no build step or dependencies.

## Features

- Fully responsive mobile/desktop layouts in one file
- Hero section with event details (date, time, venue, CME points)
- "Reserve a Seat" call-to-action button linking to the RSVP section
- Sponsor / partner logo strip
- Footer illustration banner
- No external assets — all images are inlined as base64, so the page works
  offline and loads with a single HTTP request

## Getting Started

No build tools or dependencies are required.

```bash
git clone <this-repo-url>
cd <repo-folder>
open index.html   # or double-click the file in Finder/Explorer
```

To preview locally with a simple server (recommended for accurate mobile
testing):

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploying

Since this is a static single-file site, it can be hosted on any static
file host, for example:

- **GitHub Pages** — enable Pages on this repo (Settings → Pages), pointing
  to the branch/root containing `index.html`
- **Netlify / Vercel** — drag-and-drop deploy of the folder
- Any web server that can serve static files

## Project Structure

```
.
├── index.html   # Complete landing page (mobile + desktop layouts, styles, images)
└── README.md    # This file
```

## Editing

All markup, styles, and images live inside `index.html`:

- Mobile layout: first `<body>...</body>` block
- Desktop layout: second `<body>...</body>` block
- Shared event details (date, time, venue, CME) appear in the `.hero-meta`
  section of each layout and should be updated in both places
- Images are embedded as base64 `data:` URIs directly in the relevant
  `<img>` tags

## License

Internal use for HKSPCCM. Update this section with a license if the
repository will be made public.
