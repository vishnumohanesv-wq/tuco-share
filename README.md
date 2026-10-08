# TUCO OPS – Share Message Pro

Screenshot / sheet cells → Row ID + PIN / PO number → WhatsApp-ready group message.

## Files
- `index.html` – the whole app (single file)
- `manifest.webmanifest`, `icon.svg` – lets you "Add to Home Screen" on mobile

## Put it on GitHub Pages (no coding needed)
1. Sign in at github.com → **New repository** → name it `tuco-share` → Public → **Create repository**.
2. Click **uploading an existing file** → drag in all 4 files → **Commit changes**.
3. **Settings → Pages** → Source: *Deploy from a branch* → Branch: `main`, folder `/ (root)` → **Save**.
4. Wait ~1 minute. Your app: `https://<your-username>.github.io/tuco-share/`
5. Mobile: open the link → browser menu → **Add to Home Screen**.

### Using git instead
```bash
git init && git add . && git commit -m "TUCO share pro"
git branch -M main
git remote add origin https://github.com/<your-username>/tuco-share.git
git push -u origin main
```
Update later: edit/upload the file again → Commit; the site refreshes in ~1 min.

## Screenshot reading (needs your own Claude API key)
1. Create a key at console.anthropic.com.
2. Open the app → **⚙ Image reading setup** → paste the key. It is stored **only in your browser** (localStorage), never in GitHub.
3. Paste / drop a sheet screenshot → rows appear → compare with the sheet → **Copy message**.

No key? Copy the "Po number" cells from the sheet → paste in the text box → set **Start serial** → **Parse text**. Always verify the characters before sending.

## Security notes
- NEVER type your API key into `index.html` or commit it to the repo.
- Pages sites are public. The page holds no data; screenshots go only to the Claude API when you press read.
- Use a key with a spend limit, and only on your own devices (the key sits in that browser).
