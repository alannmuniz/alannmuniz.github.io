# Alan Muniz — academic website

Source for [alannmuniz.github.io](https://alannmuniz.github.io), built with Jekyll and GitHub Pages.

## Publish for the first time

Create a **public** GitHub repository named exactly:

```text
alannmuniz.github.io
```

Then, from the folder containing these files:

```bash
git init
git add .
git commit -m "Initial academic website"
git branch -M main
git remote add origin https://github.com/alannmuniz/alannmuniz.github.io.git
git push -u origin main
```

In GitHub:

1. Open **Settings → Pages**.
2. Under **Build and deployment**, choose **Deploy from a branch**.
3. Select the `main` branch and the `/ (root)` folder.
4. Save.

The website will appear at:

```text
https://alannmuniz.github.io
```

## Edit the website

The most frequently updated information is stored under `_data/`:

- `_data/publications.yml`
- `_data/preprints.yml`
- `_data/events.yml`
- `_data/sagui.yml`
- `_data/talks.yml`

Add a new publication by inserting an item at the top of `_data/publications.yml`:

```yaml
- year: 2026
  title: "Paper title"
  authors: "Author One and <strong>Alan Muniz</strong>"
  venue: "Journal"
  note: "volume, pages"
  arxiv: "https://arxiv.org/abs/..."
  doi: "https://doi.org/..."
```

## Preview locally

Install Ruby and Bundler, then run:

```bash
bundle install
bundle exec jekyll serve
```

Open `http://localhost:4000`.

## Replace the profile photograph

Replace `assets/images/profile.jpg` with a higher-resolution image using the same filename.

## Main files

- `_layouts/` — page templates
- `_includes/` — reusable header, footer, and publication entry
- `assets/css/style.css` — visual design
- `*.md` — page content
- `_data/` — structured lists
