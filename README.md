# DUWEI NIGHTS

DUWEI NIGHTS / 毒味夜 is a minimal Jekyll site prepared for Netlify deployment.

## Structure

- `_config.yml`: site settings and permalinks.
- `_layouts/`: page templates.
- `_includes/`: shared fragments.
- `_posts/`: Markdown posts.
- `index.html`: homepage.
- `posts/index.html`: archive page.
- `assets/css/site.css`: global styles.
- `assets/images/`: images and brand assets.
- `netlify.toml`: Netlify build settings.
- `.ruby-version`: Ruby version for local and hosted builds.

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

## Deploy on Netlify

1. Connect the GitHub repository to Netlify.
2. Keep the repository root as the site root.
3. Netlify will read `netlify.toml` automatically:
   - build command: `bundle exec jekyll build`
   - publish directory: `_site`
4. After the first deploy, note the Netlify site URL.
5. Put that URL in `_config.yml`:

```yml
url: "https://your-site.netlify.app"
baseurl: ""
```

The site already uses `relative_url`, so links and assets will work with `baseurl: ""`.

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
