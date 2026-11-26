---
title: "01 Getting started"
date: 2026-11-23
published: true
tags:
  - howto
---

Ten minutes from now you'll have a blog of your own on the web, a copy of this one, ready to make yours. You only need a web browser: there's nothing to install.

The blog is a folder of plain text files: one with the settings, and a folder for every post with its story and photos. **GitHub**, a free website, keeps the files and turns them into your website every time you change one. You write in an editor that GitHub opens for you in the browser, with your blog running right next to it.

## From zero to your blog

1. Sign in to [GitHub](https://github.com), or make a free account.
2. Open **[your blog's editor](https://codespaces.new/vast-ch/cowtent-starter?quickstart=1)**. Leave everything as it is and click **Create codespace**.

A new tab opens with the editor. When it asks whether you trust the authors of the files, click **Trust Folder & Continue**. The first time it then takes a minute or two to set itself up, and opens **the blog** in one more tab, exactly as it will look online. It changes every time you save: put the two tabs side by side, or switch between them. (Your browser blocked the tab? Click **Open in Browser** in the message at the bottom right of the editor.)

3. On the far left of the editor, click the files icon (two sheets of paper) and open `site.yaml`. Change `title: Bella's Cowtent` to the name of your blog.

There's no button to press: the editor saves as you type. A couple of minutes later it puts your change on GitHub by itself, and because it's your first one, GitHub makes you your own copy of the blog to put it in (a **fork**, GitHub says): `github.com/<your username>/cowtent-starter`. Everything you write from now on goes there.

4. Open your copy on GitHub. In its **Actions** tab, click **I understand my workflows, go ahead and enable them**.
5. Open its **Settings**, then **Pages** on the left, and set **Source** to **GitHub Actions**.
6. Back in the editor, change one more thing in `site.yaml`, say the `description:`.

Now watch the **Actions** tab of your copy: after two or three minutes the yellow dot turns into a green tick ✅, and your blog is online at:

```
https://<your username>.github.io/cowtent-starter
```

For the user `BellaTheCow`, that's `https://bellathecow.github.io/cowtent-starter`. You'll also find it under **Settings** → **Pages**. You made that! For another name at the end, rename your copy under **Settings** → **Repository name**: the address changes with it.

From now on, everything you change goes online by itself. If you see a red cross ❌ in the **Actions** tab instead, something in a file isn't right, and the old version simply stays online. Click the cross, then **build**, and the message tells you which file and what's wrong. Fix it, and it goes online by itself again.

## Coming back

Close the tab whenever you like: everything is saved. To write again, open [github.com/codespaces](https://github.com/codespaces) (bookmark it) and click your editor: it opens just as you left it. It's also under **Code** → **Codespaces** in your copy of the blog. Don't make a new one every time.

The editor runs on GitHub's computers, free for about 60 hours a month. It stops by itself half an hour after you stop writing, so it only counts the time you use it.

## What's next

Your blog still has Bella's posts, her About page and her photo. They show what a blog can have, and you can change or delete them whenever you like.

- **[02 Writing your blog](../2026-11-22-writing-your-blog/index.md)** - your settings and photo, writing posts, photos and galleries, maps, tags and filters.
- **[03 Your own web address and other hosts](../2026-11-21-web-address-and-hosting/index.md)** - an address like `bellascowtent.ch`, or your blog on Netlify instead of GitHub.
