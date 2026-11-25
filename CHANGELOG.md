# Changelog

## v0.2.5 - 2026-11-25

- **02 Writing your blog** says where the route's download link is now
  (the facts), that the map opens big, and that a photo opened full
  screen can be shown on the map.
- cowtent-core v0.8.0

## v0.2.4 - 2026-11-24

- **The map is `route.gpx`**: a post's route named exactly that is on the
  map above the gallery by itself, with nothing to write. 02 Writing your
  blog says so, and how to put another route in the story. Bella's post
  doesn't embed hers any more.
- cowtent-core v0.7.0

## v0.2.3 - 2026-11-23

- **Bella's photos are on her map**: her gallery's photos have GPS along
  her route, so her post shows the photos on the map by themselves.

## v0.2.2 - 2026-11-23

- **Places and photos on the map** in 02 Writing your blog: a point's
  `latitude` and `longitude` and where to find them, and the gallery's
  photos with GPS on the map by themselves. Bella's points are on her map.
- cowtent-core v0.6.1

## v0.2.1 - 2026-11-23

- **Cloudflare, Vercel and Render** in 03 Your own web address and other
  hosts: the few settings to type in once, the blog's address and your
  own domain on each
- `engines` in `package.json`, for hosts that take Node's version from
  there (Vercel)

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
