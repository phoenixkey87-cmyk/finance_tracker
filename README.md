# 💰 Finance & Bill Balance Sheet

A single-file web app to track your accounts, balances due, amounts paid, and status —
with goals for paying down credit card debt, growing savings/checking, and improving your credit score.

Works in any browser on **phone or desktop**. No install, no login, no Kiro required to use it.

## Files

| File | Purpose |
|------|---------|
| `finance_balance_sheet.html` | The app. Open it in any browser. |
| `finance_data.json` | Your saved data (accounts + goals). Committed so it syncs across devices. |
| `.gitignore` | Keeps junk out of the repo. |

## How to use

1. Open `finance_balance_sheet.html` in a browser (double-click on desktop, or open the raw file on your phone).
2. Tap any cell to edit: account name, balance due, paid, min payment, due date, APR, status.
3. **Remaining** and the summary cards recalculate automatically.
4. Set targets under **Goals** — the progress bars show how close you are.
5. Edits save automatically in that browser (localStorage).

### Summary cards
- **Total debt remaining** — sum of unpaid balances on credit cards + loans (drive this down)
- **Paid toward debt** — how much you've knocked off
- **Cash** — checking + savings totals (build this up)
- **Net position** — cash minus debt

## Syncing across phone and desktop (the important part)

Your data lives in two places: the browser (auto-saved) and `finance_data.json` (in this repo).
To move data between devices, keep `finance_data.json` up to date in Git:

**Option A — GitHub (recommended, edit from anywhere):**
1. Create a repo on GitHub and push this folder (see below).
2. Turn on **GitHub Pages** (Settings → Pages → deploy from `main` branch, root).
   You'll get a URL like `https://<you>.github.io/<repo>/finance_balance_sheet.html`.
3. Open that URL on your phone or desktop. The app auto-loads `finance_data.json` from the repo.
4. After editing, click **Export data**, then commit the new `finance_data.json`:
   - On desktop: `git add finance_data.json && git commit -m "update balances" && git push`
   - On phone/browser: open `finance_data.json` on github.com, click the pencil ✏️, paste, commit.

Because it's a normal Git repo, you can update it from the GitHub website or mobile app — you are **not** limited to Kiro.

**Option B — Cloud drive:** put this folder in OneDrive/Google Drive/Dropbox and open the HTML from any device.

## Push this folder to GitHub

```bash
# from inside the finance_tracker folder
git remote add origin https://github.com/<you>/<repo>.git
git branch -M main
git push -u origin main
```
