# Bella's Cowtent

**👉 To make this your own blog, start with
[01 Getting started](posts/2026-11-23-getting-started/index.md).**
Everything works in your web browser: nothing to install.

1. **[Open your blog's editor](https://codespaces.new/vast-ch/cowtent-starter?quickstart=1)**
   (sign in to GitHub, or make a free account). Leave everything as it is
   and click **Create codespace**. In a minute or two the editor opens in
   your browser, with Bella's blog in a tab next to it.
2. **Make it yours:** open `site.yaml` and change `title:` to your blog's
   name. That first change makes your own copy of the blog on GitHub,
   `github.com/<your username>/cowtent-starter`.
3. **Put it online:** in your copy, open the **Actions** tab and click
   **I understand my workflows, go ahead and enable them**. Then
   **Settings** → **Pages** → **Source**: **GitHub Actions**.

From then on, write and save: everything you change goes online by itself
a couple of minutes later, at `https://<your username>.github.io/cowtent-starter`.
To come back, open [github.com/codespaces](https://github.com/codespaces)
and click your editor: it opens just as you left it.

The how-tos, on the blog and here:

1. [Getting started](posts/2026-11-23-getting-started/index.md) - from
   zero to your own blog on GitHub Pages, in ten minutes
2. [Writing your blog](posts/2026-11-22-writing-your-blog/index.md) - your
   settings, posts, photos and galleries, maps, tags and filters
3. [Your own web address and other hosts](posts/2026-11-21-web-address-and-hosting/index.md) -
   an address like `bellascowtent.ch`, or your blog on Netlify, Cloudflare,
   Vercel or Render

A sample blog written by Bella the cow, on **cowtent** (cow + tent =
content). Its posts, pages and photos are plain files; GitHub builds them
into the website after every commit
([.github/workflows/publish.yml](.github/workflows/publish.yml)), or
Netlify ([netlify.toml](netlify.toml)), with
[cowtent-core](https://github.com/vast-ch/cowtent-core). The editor is VS
Code on [GitHub Codespaces](https://github.com/features/codespaces)
([.devcontainer](.devcontainer/devcontainer.json)), with
[Front Matter CMS](https://frontmatter.codes) for the posts
([frontmatter.json](frontmatter.json)) and
[GitDoc](https://github.com/lostintangent/gitdoc) to save to GitHub
([.vscode/settings.json](.vscode/settings.json)).

```
site.yaml                    title, colour, menu, language, theme
languages/en.yaml            tag names, and any word of the blog to reword
cover.jpg                    the sidebar photo
posts/<name>/index.md        a post, its photos next to it
posts/<name>/cover - ….jpg   the photo on top: "cover - The view.jpg"
posts/<name>/gallery/        the photos at the end: "01 - The view.jpg"
posts/<name>/route.gpx       the route on a map above them
pages/<name>/index.md        a page (About me), its "cover - ….jpg" next to it
```

Version 0.3.0, see [CHANGELOG.md](CHANGELOG.md).
