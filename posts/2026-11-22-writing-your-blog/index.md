---
title: "02 Writing your blog"
date: 2026-11-22
tags:
  - howto
---

Everything on your blog is a file you can change right on GitHub: open it, click the pencil ✏️, change it and commit. This is everything you can write, from your blog's name to a post with its photos, map and tags. Your blog isn't online yet? Start with [01 Getting started](../2026-11-23-getting-started/index.md).

## Your blog's settings

The file **`site.yaml`** holds the settings of the whole blog. Each line is a name, a colon and a value, like `title: My trips`, and the file explains every line above it:

- `title` - the name of your blog
- `short-title` - optional, a shorter name shown under the icon when someone adds your blog to their phone's home screen
- `description` - one line about your blog, shown under its name
- `owner` - your name, shown as "by …"
- `colour` - the colour of links and buttons, written like `"#b45309"`. [htmlcolorcodes.com](https://htmlcolorcodes.com) helps you pick one.
- `email` - optional. With it, every post ends with a "Send me a comment" button.
- `language` - `en` for English or `de` for German: the language of everything around your posts, like "Explore", "The facts" and the dates
- `theme` - the look of your blog: `alps` (the one you're looking at), `basecamp` or `night`
- `theme-switcher` - with `true`, visitors can pick a theme themselves at the end of the sidebar. Try it on this blog!

The pictures and the About page are files too:

- **`cover.jpg`** - your photo, shown next to the blog's name. To change it, click **Add file** → **Upload files**, drop in your own photo named `cover.jpg` and commit: it replaces Bella's. A square photo works best.
- **`favicon.svg`** - optional, the little icon in the browser tab.
- **`pages/about/index.md`** - your About me page. Change the text, then upload your own photo into the same folder, named `cover - ` and what's in it, like `cover - Me on the summit.jpg`, and delete Bella's.

**Every word around your posts** can be changed too, in `languages/en.yaml` (or `de.yaml` for German). For example, to say "All my trips" instead of "All adventures" in the sidebar, add:

```yaml title="languages/en.yaml"
sidebar:
  all-posts: All my trips
```

The file says where to find the list of every word you can change.

## Writing your first post

Every post is its own folder inside the `posts` folder. In it is a file called `index.md` with the text, and the photos sit right next to it.

1. Open the `posts` folder and click **Add file** → **Create new file**.
2. For the name, type `2025-06-01-my-first-trip/index.md`. Typing the `/` creates the folder. The folder's name becomes the post's address on the web, so keep it short, in lower case, with `-` instead of spaces. Starting it with the date keeps your posts in order.
3. Write the post. The part between the two `---` lines at the top describes the post (its title, date, tags and so on), and everything below is the story:

```markdown title="posts/2025-06-01-my-first-trip/index.md"
---
title: My first trip
date: 2025-06-01
tags:
  - hiking
  - country/norway
---

The story. A blank line starts a new paragraph.

## A heading

**Bold**, *italic*, and [a link](https://example.com).
```

4. Commit.

A minute or two later the post is on your blog.

### The photo on top

The big photo at the top of a post, also shown next to it on the front page, is the photo in the post's folder named `cover - ` and what's in it:

```
posts/2025-06-01-my-first-trip/cover - The fjord from the top.jpg
```

Open your post's folder, click **Add file** → **Upload files**, drop the photo in and commit. The words after `cover - ` are read out to people who can't see the photo. Photos straight from your phone are fine, the blog makes smaller copies by itself. The About page gets its photo the same way, in `pages/about`.

### Photos in the story

Upload a photo into the post's folder and put it in the story with a `!`, its description in the square brackets and its name in the round ones:

```markdown title="posts/2025-06-01-my-first-trip/index.md"
![Lunch by the lake](./lunch.jpg)
```

### The photo gallery

The photos at the end of a post, in a grid that opens full screen when clicked, come from a folder called `gallery` inside the post's folder. There's nothing to write for them:

1. On your computer, make a folder called `gallery` and put the photos in it.
2. Name each photo after what's in it, like `The view from the top.jpg`. The name is shown under the photo, and read out to people who can't see it.
3. To put them in order, start the names with a number and ` - `: `01 - The view from the top.jpg`, `02 - Lunch by the lake.jpg`. Photos without a number come last.
4. Open your post's folder on GitHub, click **Add file** → **Upload files**, drag in the whole `gallery` folder and commit.

A photo's name can't have a `?` or `#` in it.

### Links to your other posts

Link to another post by its `index.md`, and the link takes your readers to that post:

```markdown title="posts/2025-06-01-my-first-trip/index.md"
Like on [Bella's trip to the alp](../2025-06-01-up-to-the-alp/index.md).
```

### Not finished yet?

Add `published: false` under the title, and the post stays off the site until you remove that line.

[Bella's alp post](../2025-06-01-up-to-the-alp/index.md) shows everything else a post can have, like the table of facts. Open its `index.md` on GitHub and copy whatever you need.

## Checklists

A list in your story can show a little badge in front of each line instead of a dot: a green plus for what went well, a red minus for what didn't, a question mark, a star. Write the symbol in square brackets after the `-`:

```markdown title="posts/2025-06-01-my-first-trip/index.md"
## What I learned

- [+] **Started at sunrise**
  The ridge was ours alone until ten.
- [-] **Only one litre of water**
  No streams above the tree line.
- [?] Is the north ridge easier?
```

A bold first line works as the heading of the point, and the next line, starting with two spaces, as its text.

| You write | You get |
|---|---|
| `- [+]` | <span class="check-mark" data-check="plus" role="img" aria-label="Plus"></span> |
| `- [-]` | <span class="check-mark" data-check="minus" role="img" aria-label="Minus"></span> |
| `- [x]` | <span class="check-mark" data-check="done" role="img" aria-label="Done"></span> |
| `- [ ]` | <span class="check-mark" data-check="todo" role="img" aria-label="To do"></span> |
| `- [?]` | <span class="check-mark" data-check="question" role="img" aria-label="Question"></span> |
| `- [!]` | <span class="check-mark" data-check="important" role="img" aria-label="Important"></span> |
| `- [i]` | <span class="check-mark" data-check="information" role="img" aria-label="Information"></span> |
| `- [*]` | <span class="check-mark" data-check="star" role="img" aria-label="Star"></span> |

## Maps

Recorded your route with a watch or an app like Strava or Komoot? Most of them can save it as a **GPX file**. Name it `route.gpx` and upload it into the post's folder, the same way as the photos. There's nothing to write: your route appears on the Swiss topographic map (swisstopo) after the story, above the photo gallery, with a link under it to download the file.

```
posts/2025-06-01-my-first-trip/index.md
posts/2025-06-01-my-first-trip/route.gpx
```

Bella's post has one, have a look at [Up to the alp for the summer](../2025-06-01-up-to-the-alp/index.md).

### Places on the map

The `points` of a post's `facts:` (see [Filters](#filters)) get a dot on the route's map when you give them a `latitude` and `longitude`. Hover a dot and it shows the point's name and altitude:

```yaml title="posts/2025-06-01-my-first-trip/index.md"
facts:
  points:
    - name: The Bussalp
      altitude: 1790
      latitude: 46.65099
      longitude: 7.99203
```

To find them, right-click the place on [Google Maps](https://maps.google.com): the first line it shows, like `46.65099, 7.99203`, is the latitude and the longitude. On [map.geo.admin.ch](https://map.geo.admin.ch) they are the line next to **WGS 84**. A point without them is still in the table, just not on the map. A place you pass twice only needs them the first time.

### Photos on the map

There's nothing to write for these. Phones and many cameras save where a photo was taken inside the photo itself (its GPS, in the EXIF). Every photo in the post's `gallery` folder that has it appears on the route's map as a small round photo where it was taken, and a click on it opens it in the gallery.

Your photos don't show up on the map? The GPS was taken out on the way: some apps remove it when they export or resize a photo (Apple Photos: in the export, turn on **Include location information**). The photos on your blog never have it, only the ones you upload: the blog makes its own copies of them without it. Mind that the ones you upload are in your blog's repository, which anyone can see.

### Another map in the story

Want a second route somewhere in the story, say the way to the hut the day before? Upload it with any other name and put it in the text like a photo, with a `!` in front:

```markdown title="posts/2025-06-01-my-first-trip/index.md"
![The way to the hut](./hut.gpx)
```

It's a map right there, with its download link, but only of its own route: the points and the photos are on the map of `route.gpx`. The words in the square brackets are the map's name, and are read out to people who can't see it. Without the `!` it's just a link to download the file.

## Tags

Tags are short words you give your posts, like `hiking` or `winter`. They're listed in the sidebar, and clicking one shows only the posts that have it. Click two, and you get the posts that have both.

Write a tag in lower case, with `-` instead of spaces: `trail-running`. The sidebar shows it as **Trail Running**. To show it differently, give it a name in `languages/en.yaml`:

```yaml title="languages/en.yaml"
tags:
  trail-running: Trail running
  via-ferrata: Via ferrata
```

Tags can also be sorted into a **group**, like files in a folder. A group gets its own heading in the sidebar with its tags under it. For the country of each trip, write the tags as `country/…`:

```yaml title="posts/2025-06-01-my-first-trip/index.md"
tags:
  - country/norway
```

The sidebar then shows:

> **COUNTRY**
> Norway · Scotland · Switzerland

Names work the same way here: `country/new-zealand` shows as **New Zealand** by itself. A German blog can name them all in `languages/de.yaml`:

```yaml title="languages/de.yaml"
tags:
  country: Land
  country/norway: Norwegen
  country/scotland: Schottland
  country/switzerland: Schweiz
```

## Filters

Under the tags are the **filters**: Rating, Altitude gain, Distance, Time and Gradient. You don't write these yourself. They come from the numbers you give a post under `facts:`, which also appear as a table at the start of the post:

```yaml title="posts/2025-06-01-my-first-trip/index.md"
facts:
  rating: 4           # 1 to 5 stars
  distance: 12.5      # km
  ascent: 1070        # m
  movingTime: "6:30"  # hours:minutes
```

**Rating** is simply the stars: a post with `rating: 4` is under ★★★★☆.

The other four sort every post into a range, like "less than 1500 m":

| Filter | Comes from | Bella's alp post |
|---|---|---|
| Altitude gain | `ascent` | 1,180 m → **< 1500 m** |
| Distance | `distance` | 11.2 km → **< 15 km** |
| Time | `duration` (the whole day), or else `movingTime` | 6 h 30 → **< 10 h** |
| Gradient | `ascent` divided by `distance` | 1,180 m in 11.2 km = 10.5 % → **< 15 %** |

The ranges aren't fixed: they adapt to your posts. Say you have three posts with an ascent of 800 m, 1,180 m and 2,300 m. Altitude gain then shows:

- **< 1000 m** - the 800 m post
- **< 1500 m** - the 1,180 m post (everything from 1,000 to 1,500 m)
- **> 1500 m** - the 2,300 m post, and anything bigger

Write a fourth post with 1,800 m and a new range **< 2000 m** appears, while the last one becomes **> 2000 m**. Each range ends at a round number, and a filter never has more than 5 of them. A post without that number simply isn't in that filter.
