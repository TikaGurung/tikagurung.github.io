# Tika Ram Gurung — Personal Academic Website

Built with **Quarto** and deployed via **GitHub Pages**.

---

## 📁 Project Structure

```
tika-website/
├── _quarto.yml          # Site configuration
├── styles.css           # Custom Himalayan-themed CSS
├── index.qmd            # Homepage (hero + research + publications teaser)
├── research.qmd         # Research projects with figures
├── publications.qmd     # Full publication list
├── cv.qmd               # Timeline-style CV
├── contact.qmd          # Contact & links
└── docs/
    └── figures/
        ├── moisture_flux.png          # Project 1 figure
        └── glacier_mass_balance.png   # Project 2 figure
```

---

## 🚀 Step-by-Step: Build & Deploy to GitHub Pages

### 1. Install Quarto
Download from: https://quarto.org/docs/get-started/

### 2. Install R packages (optional, for R code chunks)
```r
install.packages("rmarkdown")
```

### 3. Preview locally
```bash
cd tika-website
quarto preview
```

### 4. Render the site
```bash
quarto render
```
This builds everything into the `docs/` folder.

### 5. Push to GitHub

```bash
git init
git add .
git commit -m "Initial website commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/YOUR_USERNAME.github.io.git
git push -u origin main
```

> **Tip:** Name your repo `tikargrg.github.io` (your GitHub username) for a clean URL like `https://tikargrg.github.io`

### 6. Enable GitHub Pages

1. Go to your repo on GitHub
2. Click **Settings** → **Pages**
3. Under **Source**, select **Deploy from a branch**
4. Branch: `main` · Folder: `/docs`
5. Click **Save**

Your site will be live at `https://YOUR_USERNAME.github.io` within a few minutes!

---

## 📸 Adding Your Own Figures & Photos Later

Put any new images in `docs/figures/` and reference them in `.qmd` files as:
```markdown
![Caption](figures/your_image.png)
```
or in raw HTML:
```html
<img src="figures/your_image.png" alt="Description" style="width:100%;"/>
```

---

## ✏️ Editing Content

Each page is a `.qmd` file. Edit the HTML inside the ` ```{=html} ` blocks.

- Update your name, email, links in `_quarto.yml` and each page footer
- Add new publications to `publications.qmd`
- Add field trip photos by dropping them in `docs/figures/` and adding an image card to `research.qmd`

---

## 🎨 Color Palette (Himalayan Ice & Earth theme)

| Variable | Color | Use |
|---|---|---|
| `--glacier-blue` | `#1a4a6e` | Headings, accents |
| `--nav-bg` | `#0d2b45` | Navbar, hero bg |
| `--accent-gold` | `#c9a84c` | Buttons, underlines |
| `--meltwater` | `#2e86ab` | Links, pub borders |
| `--ice-light` | `#d6eaf8` | Tags, section bg |

All colors are defined in `styles.css` as CSS variables — change them in one place to retheme the whole site.
