# Samado Juice website (عصير صمدو)

## Put it online with GitHub Pages
0. (Pages CMS) After uploading, see "Edit offers with Pages CMS" below.
1. Create a new public repository on github.com (for example `samado-juice`).
2. Upload `index.html` and `offers.json` (Add file → Upload files → Commit).
3. Settings → Pages → Source: "Deploy from a branch" → Branch: `main` / `(root)` → Save.
4. After about a minute the site is live at `https://YOUR-USERNAME.github.io/samado-juice/`.

## Change offers (only you can — you own the repository)
Open `offers.json` on github.com → pencil icon (Edit) → change → "Commit changes".
The site updates within about a minute.

Each offer:
```json
{
  "id": "o1",
  "active": true,
  "title_ar": "اثنين صمدو جامبو",
  "title_en": "Two Samado Jumbo",
  "text_ar": "وصف قصير",
  "text_en": "Short description",
  "price": "18",
  "old_price": "20",
  "img": "samado",
  "ends": "2026-12-31"
}
```
- `active`: `true` shows it, `false` hides it.
- `ends`: optional (YYYY-MM-DD). After this date the offer hides by itself. Use `""` for no end date.
- `img`: `samado`, `maldives`, `cocktail`, `fanoos`, `avocado`, `watermelon`, `lemon-mint`, `areeka`, or any Arabic drink name from the menu (e.g. `مانجو`).
- No active offers → the offers section disappears from the site.
- Several offers: put them in the list separated by commas: `{"offers":[ {...}, {...} ]}`

## Edit offers with Pages CMS (a simple form, works on phone)
1. Upload `.pages.yml` to the repository too (it may be hidden on your computer; turn on "show hidden files", or create it on github.com: Add file → Create new file → name it `.pages.yml` and paste its contents).
2. Go to https://app.pagescms.org → Sign in with GitHub → install the GitHub App on your account → open the `samado-juice` repository.
3. Tap **العروض / Offers** → add, edit or remove offers → **Save**. The site updates in about a minute.
4. Remove all offers (or switch "Visible" off) and the offers section disappears from the site.
