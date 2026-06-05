# Mousumi Das — Portfolio (GitHub Pages)

A modern, responsive, single-page academic/research portfolio built with plain
HTML, CSS, and JavaScript — no build step, no dependencies. Designed for PhD
applications in robotics / reinforcement learning.

🔗 **Live site (after setup):** `https://MousumiDas625.github.io/portfolio_mdas/`

---

## 📁 Project structure

```
mousumi_portfolio/
├── index.html          # The whole page (all content lives here)
├── css/
│   └── style.css       # Styling, colors, layout, dark/light themes
├── js/
│   └── main.js         # Theme toggle, mobile menu, scroll animations
├── assets/
│   ├── profile.jpg          # (add) your photo — optional
│   └── Mousumi_Das_CV.pdf   # (add) your CV for the download button
├── .nojekyll           # Tells GitHub Pages to serve files as-is
└── readme.md
```

---

## ✅ Before you publish — quick checklist

Edit these in `index.html` (search for the placeholder text):

1. **Add your photo** → drop `profile.jpg` into `assets/`.
   (If you skip it, the site shows your "MD" initials automatically.)
2. **Add your CV** → drop `Mousumi_Das_CV.pdf` into `assets/`.
3. **Fix the links** (currently placeholders):
   - Google Scholar URL (search `scholar.google.com/`)
   - LinkedIn URL (search `linkedin.com/in/mousumi-das`)
   - Publication paper link (search `pub__link`)
   - Project links (search `card__link`)
4. **GitHub username** is set to `MousumiDas625`.

---

## 🚀 Deploy to GitHub Pages

This repo (`portfolio_mdas`) is already created and pushed to:
`https://github.com/MousumiDas625/portfolio_mdas`

### Push new changes
Run these in `/Users/mousumi/mousumi_portfolio`:

```bash
git add .
git commit -m "Update portfolio"
git push
```

### Turn on Pages
On GitHub: open the repo → **Settings → Pages → Build and deployment →
Source: "Deploy from a branch"**, pick branch `main`, folder `/ (root)`, and **Save**.

Your site goes live in ~1 minute at **`https://MousumiDas625.github.io/portfolio_mdas/`**.

---

## 👀 Preview locally

Just open `index.html` in a browser, or run a local server:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

---

## ✏️ How to edit content later

- **Text / experience / projects / publications:** all in `index.html`,
  organized into clearly commented `<section>` blocks.
- **Colors / fonts / spacing:** `css/style.css` — change the CSS variables
  at the very top (`:root { ... }`) to recolor the whole site instantly.
- **Behavior (theme, menu, animations):** `js/main.js`.

To add a new publication, copy an existing `.pub` block. To add a project,
copy a `.card--project` block. To add an experience, copy a `.tl-item` block.
