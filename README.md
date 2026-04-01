# DUWEI NIGHTS

DUWEI NIGHTS / 毒味夜 is a minimal Jekyll site for GitHub Pages.

## Structure

- `_config.yml`: site settings, permalinks, and GitHub Pages URL/base path.
- `_layouts/`: page templates.
- `_includes/`: shared fragments.
- `_posts/`: Markdown posts.
- `index.html`: homepage.
- `posts/index.html`: archive page.
- `assets/css/site.css`: global styles.
- `assets/images/`: images and brand assets.

## Preview Locally

Install Jekyll once, then run:

```bash
jekyll serve
```

Open `http://127.0.0.1:4000`.

## Push to GitHub

1. Create a GitHub repository.
2. Use a simple lowercase repository name such as `duwei-nights`.
3. Put this project at the repository root.
4. Commit and push your files to `main`.

Example:

```bash
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin git@github.com:YOUR-USERNAME/YOUR-REPO.git
git push -u origin main
```

## Enable GitHub Pages

1. Open the repository on GitHub.
2. Go to `Settings` -> `Pages`.
3. Under `Build and deployment`, choose `Deploy from a branch`.
4. Select the `main` branch and the `/ (root)` folder.
5. Save and wait for GitHub Pages to build the site.

## Configure `url` and `baseurl`

Edit `_config.yml` before deployment:

- If the repository is your user or organization site, for example `yourname.github.io`:

```yml
url: "https://yourname.github.io"
baseurl: ""
```

- If the repository is a project site, for example `yourname.github.io/duwei-nights`:

```yml
url: "https://yourname.github.io"
baseurl: "/duwei-nights"
```

The site already uses `relative_url`, so once `baseurl` is correct, internal links and assets will resolve correctly on GitHub Pages.

## Add a New Post

1. Create a file in `_posts/` named `YYYY-MM-DD-title.md`.
2. Add front matter:

```yaml
---
title: "Post Title"
date: 2026-04-01 23:40:00 +0800
dek: "Short line for homepage and archive."
---
```

3. Write the post body in Markdown.
4. Put any images in `assets/images/`.
5. Commit and push.

Posts appear automatically on the homepage and at `/posts/`.
