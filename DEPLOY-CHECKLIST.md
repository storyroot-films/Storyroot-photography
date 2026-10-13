# Storyroot Photography — Deploy Checklist

This `website` folder is ready to publish. Everything the page needs is inside it.

## What's in here
- `index.html` — the page (loads at the site root)
- 9 images (logo, fingerprint, and the 7 session/portrait photos) with web-safe names,
  including `storyroot-films.jpg` for the Storyroot Films card

Keep all of these together — the page loads the images by relative name.

## Deploy to Vercel (pick one)
**Easiest — drag & drop**
1. Go to vercel.com → your project (or "Add New… → Project").
2. Drag this entire `website` folder into the deploy area.
3. After it builds, open Settings → Domains and attach `www.storyrootphotography.com`
   (and `storyrootphotography.com` redirecting to www).

**Git**
1. Put these files in your repo, commit, and push.
2. Vercel auto-deploys.

**CLI**
1. In this folder run `vercel`, then `vercel --prod`.

## Turn the inquiry form on (one time)
1. After the site is live, open it and submit the "Reserve Your Date" form once.
2. FormSubmit emails `photo@storyrootmemoryco.com` a confirmation link — click it.
3. From then on, every inquiry is delivered to that inbox automatically.
   (Optional: change the form's hidden `_next` field to your preferred "thank you" page URL.)

## Final check after it's live
- [ ] All photos load
- [ ] Logo shows, "Book Now" is white
- [ ] Nav links jump to the right sections
- [ ] Utah map renders
- [ ] A test inquiry lands in photo@storyrootmemoryco.com
- [ ] "Explore Storyroot Memory Co." opens www.storyrootmemoryco.com

## Portfolio page (added Oct 12, 2026)
- `portfolio.html` — the full gallery, served at /portfolio (cleanUrls in vercel.json)
- `portfolio-photos/` — 151 photos. Each has `name.jpg` (viewer), `name-sm.jpg` (grid),
  `name-card.jpg` (covers + previews, cropped around faces), `name-ring.jpg` (round buttons);
  the five homepage cards use `name-home.jpg`. Resized only, never graded.
- `portfolio-hero-lunt.jpg` — portfolio header photo
- `storyroot-fingerprint-green.png` — mark on the portfolio's closing section
- Home page now has a Portfolio nav link and a "Recent Work" strip above Sessions.
- To add or swap photos, ask Claude — the crops are generated around faces by script.
- [ ] After deploy: /portfolio loads, filter chips work, tapping a photo opens the viewer,
  swipe moves between photos on a phone.
