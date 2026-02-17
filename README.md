# ✦ My Diary

A minimal, modern personal diary that lives entirely in your GitHub repository. No backend, no database — just a single HTML file and your own GitHub account.

---

## 🚀 Setup (5 minutes)

### 1. Create a GitHub Repository

Create a new repo (can be **private**) — e.g. `my-diary`. You don't need to add anything to it yet.

### 2. Enable GitHub Pages

In your repo → **Settings → Pages**:
- Source: **Deploy from a branch**
- Branch: `main` / root `/`

Your diary will be live at: `https://YOUR_USERNAME.github.io/YOUR_REPO/`

### 3. Add `index.html`

Commit the `index.html` file (from this project) to the **root** of your repo.

### 4. Create a Personal Access Token

Go to: [GitHub → Settings → Developer settings → Personal access tokens → Tokens (classic)](https://github.com/settings/tokens/new)

- Give it a name like `diary-token`
- Set expiration as desired
- Check the **`repo`** scope (full control of private repositories)
- Click **Generate token** and copy it

### 5. Open Your Diary

Visit your GitHub Pages URL. On first load, a setup screen will appear — enter:
- Your GitHub username
- Your repository name
- Your Personal Access Token

Your credentials are stored **only in your browser's `localStorage`** — they are never sent anywhere except directly to GitHub's API over HTTPS.

---

## 📁 Entry Storage Structure

Entries are saved as Markdown files, organised by year and month:

```
entries/
  2026/
    02/
      2026-02-17.md
      2026-02-14.md
    01/
      2026-01-30.md
  2025/
    12/
      2025-12-25.md
```

---

## ✨ Features

- **Date picker** — defaults to today, pick any date to write or review
- **Auto-load** — opens existing entries when you select a date
- **Save** — commits directly to your GitHub repo via the API
- **Delete** — removes the file from the repo
- **Sidebar** — lists all entries grouped by month
- **Sync button** — refreshes the entry list from GitHub
- **Word count** — live word counter in the editor footer
- **Offline-friendly** — credentials persist in localStorage

---

## 🔒 Privacy

- Use a **private** GitHub repository for full privacy
- Your token is stored locally in your browser only
- All API calls go directly from your browser to `api.github.com`

---

## 🛠 Customisation

The entire app is a single `index.html` file with embedded CSS and JS. Feel free to tweak colours (CSS variables at the top), fonts, or layout to your liking.
