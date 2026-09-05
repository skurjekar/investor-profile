# saurabhkurjekar.com

Single-page personal site. No build step, no dependencies — one `index.html` plus images.

## Edit before deploying

Search the file for `TODO`. Five items:

1. **Door / market count** — hero and stats say 11 doors across 4 markets. Your deck said 4 assets. Pick the true number and use it everywhere.
2. **Contact email** — currently `saurabhkurjekar234@gmail.com`. Consider a dedicated address.
3. **X/Twitter** — no link included. Add one or leave it out.
4. **Writing section** — three placeholder entries. Replace with real posts as you publish them.
5. **Returns** — this file deliberately contains **no** financial returns. Add only numbers you'd defend in a due-diligence call.

## Deploy to GitHub Pages

The `investor-profile` repo is currently empty, so this is a clean first push.

```bash
cd website
git init
git add -A
git commit -m "Personal site"
git branch -M main
git remote add origin https://github.com/skurjekar/investor-profile.git
git push -u origin main
```

Then in the repo: **Settings → Pages → Source: `main`, folder `/ (root)`**.

Live within a minute or two at `https://skurjekar.github.io/investor-profile/`.

## Point a custom domain at it

Do this **before** you enable the LinkedIn custom button — that button may not be re-addable once removed, so it should point at a URL you will never need to change.

1. Buy `saurabhkurjekar.com`.
2. Add a `CNAME` file to this directory containing exactly:
   ```
   saurabhkurjekar.com
   ```
3. At your DNS provider, add four `A` records for the apex pointing to GitHub Pages:
   ```
   185.199.108.153
   185.199.109.153
   185.199.110.153
   185.199.111.153
   ```
   And a `CNAME` record for `www` → `skurjekar.github.io`.
4. Back in **Settings → Pages**, set the custom domain and tick **Enforce HTTPS** once the certificate provisions.

## Local preview

```bash
python3 -m http.server 8000
# http://localhost:8000
```

## Notes

- Design language matches the existing `re-investor-deck` (Playfair Display / Inter, brass `#c9a96e` on charcoal) so the site and the deck read as one brand.
- Property **markets** are named; addresses are not. Keep it that way — tenant privacy, and it avoids handing strangers your parcels.
- Footer carries an employer disclaimer and a not-investment-advice line. Don't remove them.
