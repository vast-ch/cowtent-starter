# Changelog

## v0.2.0 - 2026-11-23

- **The guide in three parts**: 01 Getting started (from zero to your
  blog on GitHub Pages, nothing else), 02 Writing your blog (settings,
  posts, the cover photo, photos in the story, the gallery, links,
  checklists, maps, tags, filters) and 03 Your own web address and other
  hosts (a custom domain on GitHub Pages, Netlify)
- **Ready for Netlify**: `netlify.toml` is only the build command and the
  folder, everything else comes with cowtent-core's build, and the blog
  takes its address from Netlify
- Every build gets the newest cowtent-core, also where the host keeps
  `node_modules` between builds (`pnpm update cowtent-core` in the build
  script); pnpm and Node versions in `package.json` and `.node-version`

## v0.1.1 - 2026-11-23

- **Covers and galleries by file name**: the photo on top of a post or
  page is the one named `cover - <what's in it>.jpg` next to it, instead
  of `image:` in the front matter, and gallery photos are numbered with
  ` - `: `01 - Through town on the way up.jpg`

## v0.1.0 - 2026-11-23

The first version of Bella's Cowtent, the sample blog to fork.

- **site.yaml** with every setting explained, the `alps` theme and the
  theme switcher on
- **How to make this blog your own**: getting started on GitHub, the
  settings, writing a post, checklists, maps, tags, filters and your own
  web address
- **Up to the alp for the summer**: a post with everything a post can
  have: facts, a checklist, the GPX route on the map and a gallery
- An **About me** page, the cover photo, English words and tag names in
  `languages/en.yaml`
- Published to GitHub Pages on every commit, and every Monday, with the
  latest cowtent-core
