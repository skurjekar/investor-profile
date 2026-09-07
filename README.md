# saurabhkurjekar.com

Single-page personal site. No build step, no dependencies — one `index.html` plus images.

## Edit before deploying

Search the file for `TODO`. Five items:

1. **Unit count** — hero and stats say 12 units across 4 markets. Keep this consistent with your LinkedIn and investor deck.
2. **Contact email** — currently `saurabhkurjekar234@gmail.com`. Consider a dedicated address.
3. **X/Twitter** — no link included. Add one or leave it out.
4. **Calendly** — `calendly.com/saurabhkurjekar234`, linked from the hero button and both contact cards.
5. **Returns** — this file deliberately contains **no** financial returns. Add only numbers you'd defend in a due-diligence call.

## Status — LIVE

- **https://saurabhkurjekar.com** (apex, HTTPS enforced)
- `www.saurabhkurjekar.com` → 301 → apex
- `skurjekar.github.io/investor-profile/` → 301 → apex
- Hosted free on GitHub Pages from `skurjekar/investor-profile`, branch `main`, root.
- Domain at Cloudflare Registrar, auto-renew on, expires 7 Sep 2027.
- TLS: Let's Encrypt, auto-renewing, covers apex + www.
- DNS: 4 A records (185.199.108–111.153) + `www` CNAME, all **DNS only** (grey cloud).
  Do not enable the Cloudflare proxy — it breaks GitHub's certificate renewal.

## To publish a change

```bash
cd website
git add -A && git commit -m "..." && git push
```

Live within ~1 minute. Do not delete the `CNAME` file — it is what binds the domain.
