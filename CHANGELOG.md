# Changelog

## v0.2.15 - 2026-11-26

- cowtent-core v0.15.0: the maps are OpenStreetMap, worldwide, in 3D too;
  a post can have several routes (`01 - route.gpx`, `02 - route.gpx`, …),
  each in its colour on one map and one altitude profile; the gallery is
  in rows, in its order.

## v0.2.14 - 2026-11-26

- cowtent-core v0.14.0: each theme's seven colours, and your own in
  `colours:` in site.yaml. The blog's `colour:` is gone: Bella now wears
  the theme's colours.

## v0.2.13 - 2026-11-26

- cowtent-core v0.13.3: a tick every 5 km on the altitude profile, and the
  photos' pins on the map no longer grow under the mouse.

## v0.2.12 - 2026-11-26

- cowtent-core v0.13.2: the photos on the altitude profile are pins, like
  on the map, their tip on the relief where each was taken.

## v0.2.11 - 2026-11-25

- cowtent-core v0.13.1: the arrows of a full-screen photo show on a
  phone too.

## v0.2.10 - 2026-11-25

- cowtent-core v0.13.0: a post's title rises into the mountains at the
  top as you scroll, and the altitude profile is wider.

## v0.2.9 - 2026-11-25

- **02 Writing your blog** tells of the altitude profile under the map
  and the walk along the route.
- cowtent-core v0.12.0

## v0.2.8 - 2026-11-25

- cowtent-core v0.11.1: a link to the map or a photo opens it again, and
  the map in 3D shows the terrain from the first click.

## v0.2.7 - 2026-11-25

- **02 Writing your blog** tells of the 3D button, the enlarge button at
  the map's top right, and the photos on pins.
- cowtent-core v0.11.0

## v0.2.6 - 2026-11-25

- **The cover is the gallery's first photo**, and on the map with GPS.
  02 Writing your blog says so.
- cowtent-core v0.9.0

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
