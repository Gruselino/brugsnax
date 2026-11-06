# Snack Bar Wishlist

A tiny shared list for the office snack bar. Anyone with the link can suggest a snack, vote for it, and see the running total in euros. No accounts, no build step, three files.

- `index.html` – the whole app
- `firebase-config.js` – your database connection (you fill this in once)
- `database.rules.json` – access rules to paste into Firebase

## How it works

- **Shared data** lives in a free Firebase Realtime Database. GitHub Pages only serves static files, so the list needs somewhere to live; Firebase gives you live updates for everyone and handles several people voting at the same time without overwriting each other.
- **Snack lookup** uses the Open Food Facts product search. Type "pretzel m&m", pick the matching product (e.g. M&M's Pretzel), and it is stored with its brand, size, barcode and picture.
- **Price** comes from Open Prices (Open Food Facts' crowd‑sourced price database): the page averages all EUR prices recorded for that barcode. If none exist, click the "—" and type a price yourself. Any price can be corrected by clicking it.
- **Votes**: one vote per browser per snack (click again to withdraw). The list is sorted by votes.
- **Total**: sum of all prices on the list, in euros.

