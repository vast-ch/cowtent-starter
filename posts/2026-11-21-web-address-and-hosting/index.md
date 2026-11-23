---
title: "03 Your own web address and other hosts"
date: 2026-11-21
tags:
  - howto
---

After [01 Getting started](../2026-11-23-getting-started/index.md) your blog lives on GitHub Pages, at a `github.io` address. That's all a blog needs, and it can stay that way. This is for when you want your own address, or your blog on another host: Netlify is ready to go, Cloudflare, Vercel and Render take a few settings typed in once.

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

## On Cloudflare

[Cloudflare Pages](https://pages.cloudflare.com) is free too. It has no ready-made file yet, so you type two settings once:

1. Open the [Cloudflare dashboard](https://dash.cloudflare.com/sign-up) and make a free account.
2. Open **Workers & Pages**, click **Create**, choose **Pages** and **Connect to Git**. Connect GitHub and pick your blog.
3. Set **Framework preset** to **None**, **Build command** to `pnpm build` and **Build output directory** to `dist`. Click **Save and Deploy**.

A few minutes later your blog is online at `https://<project name>.pages.dev`. Cloudflare doesn't tell the blog its own address, so add it to `site.yaml` and commit, for its RSS feed and the links people share:

```yaml title="site.yaml"
url: https://my-blog.pages.dev
```

**Your own address on Cloudflare:** open your project, then **Custom domains** → **Set up a custom domain**, and follow the steps. Then change `url:` in `site.yaml` to the new address.

## On Vercel

[Vercel](https://vercel.com) is free for personal sites:

1. Open [Vercel](https://vercel.com/signup) and sign up with GitHub.
2. Click **Add New…** → **Project**, and **Import** next to your blog.
3. Set **Framework Preset** to **Other**. Open **Build and Output Settings**, switch on the overrides and type `pnpm build` as **Build Command**, `dist` as **Output Directory** and `pnpm install` as **Install Command**.
4. Open **Environment Variables** and add `ENABLE_EXPERIMENTAL_COREPACK` with the value `1`, so Vercel uses the right version of pnpm. Click **Deploy**.

Your blog is online at `https://<project name>.vercel.app`, and knows its address by itself. **Your own address on Vercel:** open the project's **Settings** → **Domains** → **Add Domain** and follow the steps; the blog uses it from its next update.

## On Render

[Render](https://render.com) has free static sites:

1. Open [Render](https://dashboard.render.com/register) and sign up with GitHub.
2. Click **New** → **Static Site** and pick your blog.
3. Type `corepack enable && pnpm install && pnpm build` as **Build Command** and `dist` as **Publish Directory**. Click **Deploy Static Site**.
4. For the maps: open **Headers** on the left and add a header with the path `/assets/*`, the name `Access-Control-Allow-Origin` and the value `*`. Without it, the swisstopo map can't load your route.

Your blog is online at `https://<name>.onrender.com`, and knows its address by itself. **Your own address on Render:** open **Settings** → **Custom Domains** → **Add Custom Domain**, then write the new address as `url:` in `site.yaml`.

## Other hosts

The blog is a plain website, so it can live almost anywhere that serves files: build it with `pnpm build` and put the `dist` folder online.
