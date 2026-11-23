---
title: How to make this blog your own
date: 2026-11-21
tags:
  - howto
---

This whole blog is a folder of plain text files: one file with the settings, and a folder for every post with its story and photos in it. You change a file, and a minute or two later the website shows the change. There's no app to install and no database to look after.

## A few words first

The steps below use **GitHub**, a free website that keeps your files and puts your blog online. It's just the easiest way to start: the blog isn't tied to it, and it works anywhere that can show a plain website.

GitHub has some words of its own. These are the only ones you need:

- **Repository** - your blog's folder on GitHub, with all its files.
- **Fork** - your own copy of someone else's repository. You'll fork Bella's blog and make it yours.
- **Commit** - GitHub's word for *save*. Every time you change a file you click **Commit changes**, and your blog updates with it.

## Getting started

Ten minutes from now you'll have a blog of your own on the web.

1. Sign in to [GitHub](https://github.com), or make a free account.
2. Open [Bella's blog on GitHub](https://github.com/vast-ch/cowtent-starter) and click **Fork** at the top right.
3. Under **Repository name**, write a short name for your blog, like `my-blog`. It becomes part of your blog's address. Click **Create fork**.
4. In your copy, open **Settings**, then **Pages** on the left, and set **Source** to **GitHub Actions**. (Actions is the part of GitHub that turns your files into the website.)
5. Open the **Actions** tab at the top and click the green button that turns them on.
6. Go back to the **Code** tab, open the file `site.yaml` and click the pencil ✏️ to edit it. Change `title: Bella's Cowtent` to the name of your blog, then click **Commit changes…** and **Commit changes** again.

Now look at the **Actions** tab. After two or three minutes the yellow dot turns into a green tick ✅, and your blog is online at `https://<your username>.github.io/<repository name>`. For the user `BellaTheCow` and the name `my-blog`, that's `https://bellathecow.github.io/my-blog`. You'll also find the address under **Settings** → **Pages**. You made that!

Every change you commit updates the site the same way. If you see a red cross ❌ instead, something in a file isn't right, and your old version simply stays online. Click the cross, then **build**, and the message tells you which file and what's wrong. Fix it and commit again.

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
5. Open your new folder, click **Add file** → **Upload files**, and drop in the photo for the top of the post. Name it `cover - ` and what's in it, like `cover - The fjord from the top.jpg`: that's the big photo at the top of the post and next to it on the front page, and the words after `cover - ` are read out to people who can't see it. Photos straight from your phone are fine, the blog makes smaller copies by itself.

### The photo gallery

The photos at the end of a post, in a grid that opens full screen when clicked, come from a folder called `gallery` inside the post's folder. There's nothing to write for them:

1. On your computer, make a folder called `gallery` and put the photos in it.
2. Name each photo after what's in it, like `The view from the top.jpg`. The name is shown under the photo, and read out to people who can't see it.
3. To put them in order, start the names with a number and ` - `: `01 - The view from the top.jpg`, `02 - Lunch by the lake.jpg`. Photos without a number come last.
4. Open your post's folder on GitHub, click **Add file** → **Upload files**, drag in the whole `gallery` folder and commit.

A photo's name can't have a `?` or `#` in it.

Not finished yet? Add `published: false` under the title, and the post stays off the site until you remove that line.

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

Recorded your route with a watch or an app like Strava or Komoot? Most of them can save it as a **GPX file**. Upload that file into the post's folder, the same way as the photos, and put it in your story like a photo, with a `!` in front:

```markdown title="posts/2025-06-01-my-first-trip/index.md"
![The way up](./route.gpx)
```

Your route then appears on the Swiss topographic map (swisstopo), with a link under it to download the file. Bella's looks like this:

![From the farm to the Bussalp](../2025-06-01-up-to-the-alp/route.gpx)

Without the `!` it's just a link to download the file:

```markdown title="posts/2025-06-01-my-first-trip/index.md"
[Download the GPX](./route.gpx)
```

The words in the square brackets are the map's name, and are read out to people who can't see it.

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

## Your own web address

Your blog keeps its `github.io` address for as long as you like. If you'd rather have your own, like `bellascowtent.ch`:

1. Buy the name from a domain seller (Infomaniak, Namecheap, Gandi…).
2. On GitHub, in your blog's **Settings** → **Pages** → **Custom domain**, type the name and click **Save**.
3. At the domain seller, find the domain's **DNS** settings (the address book that tells browsers where your blog lives) and add the entries [GitHub lists](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site): four `A` entries for `bellascowtent.ch` pointing to `185.199.108.153`, `185.199.109.153`, `185.199.110.153` and `185.199.111.153`, and a `CNAME` entry for `www` pointing to `<your username>.github.io`. The seller's help pages show where to click.
4. Wait until GitHub's check in **Settings** → **Pages** turns green (from a few minutes to a day), then tick **Enforce HTTPS** so the address is secure.
5. Update the blog once so its RSS feed uses the new address: **Actions** → **Publish** → **Run workflow**.

Visitors using the old `github.io` address are then sent to the new one automatically.
