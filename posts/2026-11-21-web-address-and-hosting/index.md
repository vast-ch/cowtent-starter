---
title: "03 Your own web address and other hosts"
date: 2026-11-21
tags:
  - howto
---

After [01 Getting started](../2026-11-23-getting-started/index.md) your blog lives on GitHub Pages, at a `github.io` address. That's all a blog needs, and it can stay that way. This is for when you want your own address, or your blog on another host.

## Your own web address on GitHub Pages

Your blog keeps its `github.io` address for as long as you like. If you'd rather have your own, like `bellascowtent.ch`:

1. Buy the name from a domain seller (Infomaniak, Namecheap, Gandi…).
2. On GitHub, in your blog's **Settings** → **Pages** → **Custom domain**, type the name and click **Save**.
3. At the domain seller, find the domain's **DNS** settings (the address book that tells browsers where your blog lives) and add the entries [GitHub lists](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site): four `A` entries for `bellascowtent.ch` pointing to `185.199.108.153`, `185.199.109.153`, `185.199.110.153` and `185.199.111.153`, and a `CNAME` entry for `www` pointing to `<your username>.github.io`. The seller's help pages show where to click.
4. Wait until GitHub's check in **Settings** → **Pages** turns green (from a few minutes to a day), then tick **Enforce HTTPS** so the address is secure.
5. Update the blog once so its RSS feed uses the new address: **Actions** → **Publish** → **Run workflow**.

Visitors using the old `github.io` address are then sent to the new one automatically.

## On Netlify

[Netlify](https://www.netlify.com) is another free host. Your blog is ready for it: its `netlify.toml` file tells Netlify how to build it, so there's nothing to fill in.

1. Open [Netlify](https://app.netlify.com/signup) and click **Sign up with GitHub**.
2. Click **Add new project** → **Import an existing project** → **GitHub**, let Netlify see your repositories, and pick your blog.
3. Netlify shows the settings it read from your blog. Leave them as they are and click **Deploy**.

Two or three minutes later your blog is online at an address like `https://wonderful-cow-1a2b3c.netlify.app`. For a nicer one, open **Project configuration** → **Change project name**. From now on, every commit updates the blog on Netlify too.

**Your own address on Netlify:** open **Domain management** → **Add a domain**, type the name you bought and follow the steps Netlify shows for its DNS. The blog uses the new address by itself from its next update: **Deploys** → **Trigger deploy** → **Deploy project**.

**GitHub Pages keeps running** next to Netlify. That does no harm, but to have the blog in one place only, open the **Actions** tab on GitHub, click **Publish** on the left, then **⋯** → **Disable workflow**.

## Other hosts

The blog is a plain website, so it can live almost anywhere. Ready-made setups like the one for Netlify are coming for more hosts.
