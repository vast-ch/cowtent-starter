---
title: "01 Getting started"
date: 2026-11-23
tags:
  - howto
---

Ten minutes from now you'll have a blog of your own on the web, a copy of this one, ready to make yours. You only need a web browser: there's nothing to install.

The blog is a folder of plain text files: one with the settings, and a folder for every post with its story and photos. **GitHub**, a free website, keeps the files and turns them into your website every time you change one.

## Three GitHub words

- **Repository** - your blog's folder on GitHub, with all its files.
- **Fork** - your own copy of someone else's repository. You'll fork Bella's blog and make it yours.
- **Commit** - GitHub's word for *save*. Every time you change a file you click **Commit changes**, and your blog updates with it.

## From zero to your blog

1. Sign in to [GitHub](https://github.com), or make a free account.
2. Open [Bella's blog on GitHub](https://github.com/vast-ch/cowtent-starter) and click **Fork** at the top right.
3. Under **Repository name**, write a short name for your blog, like `my-blog`. It becomes part of your blog's address. Click **Create fork**.
4. In your copy, open **Settings**, then **Pages** on the left, and set **Source** to **GitHub Actions**.
5. Open the **Actions** tab at the top and click the green button that turns them on.
6. Go back to the **Code** tab, open the file `site.yaml` and click the pencil ✏️ to edit it. Change `title: Bella's Cowtent` to the name of your blog, then click **Commit changes…** and **Commit changes** again.

Now watch the **Actions** tab. After two or three minutes the yellow dot turns into a green tick ✅, and your blog is online at:

```
https://<your username>.github.io/<repository name>
```

For the user `BellaTheCow` and the name `my-blog`, that's `https://bellathecow.github.io/my-blog`. You'll also find it under **Settings** → **Pages**. You made that!

Every change you commit updates the site the same way. If you see a red cross ❌ instead, something in a file isn't right, and the old version simply stays online. Click the cross, then **build**, and the message tells you which file and what's wrong. Fix it and commit again.

## What's next

Your blog still has Bella's posts, her About page and her photo. They show what a blog can have, and you can change or delete them whenever you like.

- **[02 Writing your blog](../2026-11-22-writing-your-blog/index.md)** - your settings and photo, writing posts, photos and galleries, maps, tags and filters.
- **[03 Your own web address and other hosts](../2026-11-21-web-address-and-hosting/index.md)** - an address like `bellascowtent.ch`, or your blog on Netlify instead of GitHub.
