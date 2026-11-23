# Bella's Cowtent

**👉 To make this your own blog, start with
[01 Getting started](posts/2026-11-23-getting-started/index.md).**
Everything works from the GitHub website: nothing to install.

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
[cowtent-core](https://github.com/vast-ch/cowtent-core).

```
site.yaml                    title, colour, menu, language, theme
languages/en.yaml            tag names, and any word of the blog to reword
cover.jpg                    the sidebar photo
posts/<name>/index.md        a post, its photos next to it
posts/<name>/cover - ….jpg   the photo on top: "cover - The view.jpg"
posts/<name>/gallery/        the photos at the end: "01 - The view.jpg"
pages/<name>/index.md        a page (About me), its "cover - ….jpg" next to it
```

Version 0.2.3, see [CHANGELOG.md](CHANGELOG.md).
