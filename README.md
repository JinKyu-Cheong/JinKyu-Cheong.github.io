# JinKyu-Cheong.github.io

Personal academic website built with Hugo and deployed on GitHub Pages.

## Quick Setup

### 1. Create GitHub Repository

Go to [github.com/new](https://github.com/new) and create a repo named:
```
JinKyu-Cheong.github.io
```
- Set to **Public**
- Do NOT initialize with README (we'll push our own)

### 2. Push this project

```bash
cd JinKyu-Cheong.github.io
git init
git add .
git commit -m "Initial academic site"
git branch -M main
git remote add origin https://github.com/JinKyu-Cheong/JinKyu-Cheong.github.io.git
git push -u origin main
```

### 3. Enable GitHub Pages

1. Go to repo **Settings → Pages**
2. Under **Source**, select **GitHub Actions**
3. The site will auto-deploy on every push to `main`

Your site will be live at: `https://jinkyu-cheong.github.io/`

## Local Development (optional)

```bash
# Install Hugo: https://gohugo.io/installation/
hugo server -D
# Open http://localhost:1313
```

## How to Edit

### Update your profile
Edit `hugo.yaml` — change name, bio, affiliation, social links, research interests.

### Add a publication
Create a new `.md` file in `content/publications/`:
```bash
cp content/publications/2024-example-paper.md content/publications/2025-your-new-paper.md
```
Then edit the front matter (title, authors, journal, doi, etc.).

### Add your photo
Replace `static/images/profile.jpg` with your photo (square crop recommended, ~400x400px).

### Add a CV download
Place your CV PDF in `static/uploads/CV.pdf`, then link to it from any page:
```markdown
[Download CV](/uploads/CV.pdf)
```

## Future Expansion (Lab Website)

When you become PI, uncomment these sections in `hugo.yaml`:
```yaml
menus:
  main:
    - name: "Team"
      url: "/team/"
    - name: "Research"
      url: "/research/"
    - name: "News"
      url: "/news/"
```

Then create corresponding directories under `content/`:
```bash
mkdir -p content/{team,research,news}
```

## Structure

```
.
├── hugo.yaml              # Main config (profile, social, menu)
├── content/
│   ├── _index.md          # Homepage
│   ├── publications/      # Paper entries
│   └── contact/           # Contact page
├── layouts/               # HTML templates
├── static/
│   ├── css/style.css      # Styles
│   ├── js/main.js         # Mobile nav
│   └── images/            # Profile photo, etc.
└── .github/workflows/     # Auto-deploy
```
