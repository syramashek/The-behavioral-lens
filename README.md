# The Behavioral Lens — website project

A mobile-friendly, research-informed blog by Syra Mashek. Built for Netlify with an optional browser-based editor through Pages CMS. **Your existing portfolio stays separate and unchanged.**

## What's included

- Home page, writing archive (searchable and filterable), individual article pages, About, and Connect/social links.
- Your first article, **Marriage Without Freedom**, with a link to your original academic PDF.
- A one-file site settings panel (publication name, copy, social links, portfolio link).
- Files arranged so a CMS can add and edit posts without changing the design.
- A generated `dist/` folder you can publish immediately, even before setting up the CMS.

## Option A — Publish immediately (simplest)

1. Download the separate **behavioral-lens-deploy-ready.zip** package.
2. Extract the ZIP into a folder on your computer.
3. Sign in at https://app.netlify.com/drop and drag the **extracted folder** into Netlify Drop. This creates a new Netlify site rather than overwriting your existing portfolio.
4. Netlify will display your new blog's web address. Use that address to add a link to the blog from your existing portfolio.

Important: Option A makes the website live, but it **does not activate the in-browser article editor**. For easy ongoing publishing, do Option B once.

## Option B — Enable “add new post” without touching the code

This needs a GitHub account and your Netlify account. The setup is one-time.

1. Create a new GitHub repository, for example `behavioral-lens-blog`.
2. Upload the **full project source** files from this folder to the repository root, including the hidden `.pages.yml` file, `build.mjs`, `netlify.toml`, `assets/`, and `content/`. Do **not** upload only `dist/`.
3. In Netlify: **Add new project → Import an existing project → GitHub** and choose that repository. Netlify should read `netlify.toml`: build command `node build.mjs`, publish directory `dist`.
4. After Netlify deploys, open https://app.pagescms.org/, sign in with GitHub, and authorize Pages CMS for that repository. Open the repo; Pages CMS will read `.pages.yml` and show **Blog articles** and **Site, socials, and portfolio links**.
5. To publish an article: **Blog articles → New article**, write/paste in the rich-text editor, set a category, date, and toggle **Published** on, then save. Pages CMS commits the change to GitHub; Netlify rebuilds the live blog automatically. To save a draft, leave **Published** off.
6. To update your social links or contact email: open **Site, socials, and portfolio links**, edit your details, and save. Blank social URLs are deliberately hidden from public pages.
7. Once Netlify gives you the final live address, enter it in the **site_url** setting (for example `https://YOUR-NEW-BLOG.netlify.app`). The build will then produce an RSS feed (`/feed.xml`) and a sitemap (`/sitemap.xml`) with correct public links.

You can manage the articles and socials from your phone using Pages CMS once it is connected.

**Important:** If the blog is connected to GitHub, publish new posts through Pages CMS / GitHub instead of drag-and-drop manual replacement. That keeps your edits in sync and avoids the next Git deployment overwriting manual changes.

Helpful references:
- Pages CMS editor setup: https://pagescms.org/docs/quick-start/
- Netlify and GitHub deployment: https://www.netlify.com/knowledge-base/how-to-deploy-a-site-to-netlify/
- Netlify Drop: https://docs.netlify.com/start/quickstarts/netlify-drop-quickstart/

## Editing files manually (optional)

- Add a post: copy `content/posts/marriage-without-freedom.json`, rename it to a concise URL slug such as `why-stigma-matters.json`, and change the content. **One JSON file = one article.** The `published` field controls visibility; `featured` controls the homepage feature.
- Update socials and portfolio link: `content/site.json`.
- Run `node build.mjs` from the project root to regenerate `dist/` (requires Node 18+).
- Deploy: upload the *entire `dist/` folder*, never a single page. The root of the uploaded folder must contain `index.html`.
- Original PDF: `assets/slave-marriage-original.pdf`.
- Color and layout: `assets/styles.css`.
- Site source generator: `build.mjs`.

## Editorial and professional notes

All academic adaptations should attribute their original research sources and distinguish interpretation from verified findings. This publication is educational, not a clinical service, and does not imply psychologist or independent-practice licensure. Do not publish identifying client information. Articles can be updated as scholarship evolves.

## Your supplied contact information

- Email: syramashekpsychology@gmail.com (publicly displayed on the Connect page and footer)
- Instagram: https://www.instagram.com/syramashekpsychology/
- TikTok: https://www.tiktok.com/@syramashekpsychology

These profile addresses were built from the handles you supplied; double-check they point to the intended profiles.

## Current launch checklist

- [x] Website layout and mobile navigation
- [x] Original article and original PDF
- [x] Professional portfolio link
- [x] Instagram, TikTok, and public contact email configured
- [x] Article creation support / CMS configuration
- [ ] You connect or create the GitHub repository and connect Netlify (required for automatic CMS publishing)
- [x] Your supplied Instagram and TikTok profile URLs are in site settings (confirm both links open your intended profiles after publishing)
- [ ] You set your new blog's live URL in Site Settings
- [ ] You add a link from your existing portfolio site to the new blog

No public blog has been deployed on your behalf yet. The package is yours to deploy.


### Psychedelic Art Deco edition
This edition uses custom editable SVG illustrations (`assets/deco-vision.svg`, `assets/deco-feature.svg`) and a jewel-toned Art Deco design system in `assets/styles.css`. It retains the same article data and Pages CMS settings. Publish `dist/` to Netlify, or publish the full repository with `npm run build`.
