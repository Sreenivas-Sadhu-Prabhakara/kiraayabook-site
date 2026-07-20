# KiraayaBook — explainer site

A standalone marketing/explainer page for **KiraayaBook**, the rent-collection
tool for small Indian landlords and PG owners.

> **Rent that collects itself.** — pricing on discovery, subscription basis

This is *not* the product UI. It is a polished, self-contained landing page that
makes the idea instantly clear to a non-technical SMB owner and to an investor
skimming for 30 seconds.

## What the product does

Rent is the most predictable recurring payment there is, yet every month it gets
chased by hand on WhatsApp. KiraayaBook turns that into an automatic cycle:

- **Monthly rent cycle** — one invoice per active lease, raised on its due day.
- **Dues & arrears roll-up** — a running balance per tenant, carried forward.
- **Staged WhatsApp reminders** — T-3 days, due day, and overdue, to the outbox.
- **Digital receipts** — issued automatically the moment a payment lands.
- **Electricity split by meter reading** — added straight onto the invoice.
- **Vacancy flag** — empty units drop out of billing and show as lost income.
- **Dashboard** — collected vs pending this month, plus the arrears list.

## Files

| File | Purpose |
|------|---------|
| `index.html` | Page markup — all 9 sections, inline SVG only. |
| `styles.css` | All styling. Palette built around the teal accent `#0F766E`. |
| `app.js` | Sticky-nav highlight, smooth scroll, and the animated hero "rent register" that collects itself. No dependencies. |
| `favicon.svg` | Ledger-book mark. |

## Design notes

- Palette: teal accent `#0F766E`, deep teal-black ink, off-white ledger paper,
  a muted sage tint, and a burnt-sienna warning colour for overdue/arrears.
- **Signature:** money is always set in tabular monospace, so the whole page
  reads like an accounts book (bahi-khata). The hero widget is a live rent
  register where a tenant's overdue rent visibly moves reminder → paid → receipt.
- Fully self-contained: no CDNs, no external fonts, images or scripts. System
  font stack only. Renders correctly opened as a local `file://` and deploys to
  any static host unchanged.
- Responsive down to mobile with no horizontal page scroll; the wide dashboard
  table scrolls inside its own container.
- Respects `prefers-reduced-motion` (the hero animation freezes on its end-state).

## Run it

Just open `index.html` in a browser. No build step. To serve locally:

```sh
python3 -m http.server 8080
# then visit http://localhost:8080
```

## Deploy

Upload the folder to any static host (Netlify, Cloudflare Pages, GitHub Pages,
S3). No configuration required.

---

A **KARYA** studio build · sreeni.nintendo@gmail.com
