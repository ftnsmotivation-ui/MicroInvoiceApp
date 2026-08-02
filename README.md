# MicroInvoice

A clean, zero-login, single-file invoicing app. No backend, no account, no database — everything runs client-side and autosaves to your browser's `localStorage`.

Live demo: open `index.html` directly in a browser, or deploy the file as-is to Vercel, Netlify, GitHub Pages, or any static host.

## Features

- **Zero-login, local-first** — your invoice drafts autosave to `localStorage`; nothing is sent to a server.
- **Live editable invoice canvas** — logo upload, business/client info, invoice #, dates, line items with auto-calculated subtotal/tax/total.
- **Multi-currency** — USD, EUR, GBP, CAD, INR, JPY, AUD, with correct decimal handling (e.g. JPY has no decimal places).
- **Reorderable line items** — move rows up/down, remove rows, everything recalculates live.
- **AI Magic Paste** — paste rough notes like `"5 hrs landing page dev at $80/hr, $100 server setup, fixed SSL bug for $50"` and it parses out structured line items automatically.
- **Payment link** — paste a Stripe/PayPal/Wise/Revolut link and a "Pay This Invoice Online" button appears on the invoice.
- **Export options:**
  - Download as a clean, single-page PDF
  - Copy as richly-formatted Email HTML (paste directly into Gmail/Outlook)
  - Export line items + totals as CSV
- **Built-in growth loop** — a discreet "Generated with MicroInvoice" footer badge links back to wherever you deploy the app.

## Tech stack

- Plain HTML + vanilla JavaScript (no build step, no framework)
- [Tailwind CSS](https://tailwindcss.com/) via CDN
- [html2pdf.js](https://github.com/eKoopmans/html2pdf.js) (html2canvas + jsPDF) for PDF export
- Inter / Plus Jakarta Sans via Google Fonts

## Running it

There's nothing to build or install. Either:

1. Open `index.html` directly in a browser, or
2. Deploy it to any static host (Vercel, Netlify, GitHub Pages, Cloudflare Pages, etc.) — it's a single file with no server-side dependencies.

## Deploying to GitHub Pages

1. Push this repo to GitHub.
2. In the repo settings, go to **Pages** and set the source to the `main` branch, root folder.
3. Your invoice tool will be live at `https://<username>.github.io/<repo-name>/`.

## Notes on data & privacy

All invoice data (business info, client info, line items, logo image) is stored only in the browser's `localStorage` on the device that created it. Clearing browser storage or using a different browser/device will not carry drafts over. There is no server component, so there is nothing to configure for privacy — the tradeoff is that drafts don't sync across devices.

## License

MIT — see [LICENSE](./LICENSE). Feel free to fork, modify, and rebrand.
