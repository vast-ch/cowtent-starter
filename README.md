# Bella's Cowtent

**👉 To make this your own blog, start with
[How to make this blog your own](posts/2026-11-21-how-this-blog-works/index.md).**
Everything works from the GitHub website: nothing to install.

A sample blog written by Bella the cow, on **cowtent** (cow + tent =
content). Its posts, pages and photos are plain files; GitHub builds them
into the website after every commit
([.github/workflows/publish.yml](.github/workflows/publish.yml)) with
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

Version 0.1.1, see [CHANGELOG.md](CHANGELOG.md).
