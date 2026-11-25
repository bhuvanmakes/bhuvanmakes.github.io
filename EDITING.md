# How to edit this site

Once this folder is on GitHub as the `bhuvanmakes.github.io` repository, GitHub Pages will build the site for free. You change a file in the repo, and after a minute or two the public site updates. You can edit here with me, or you can open the files on github.com and change them yourself.

Every project (and any later piece of writing, such as the novella) lives at `/projects/your-slug/`. There is no separate blog.

## Add a project

1. In `_projects/`, add a new file named something short, like `morse-monkey.md`.
2. Start the file with a front matter block (the bit between `---` lines), then write the page in ordinary Markdown underneath.

```yaml
---
title: The name people will see
order: 5
summary: One short line used if you don't write an intro.
intro: >-
  Two or three sentences for the home-page list.
lede: Optional short line at the top of the project page.
hero: /assets/img/your-slug/cover.jpg
hero_alt: A short description of the photo.
hero_credit: Optional, for example where the photo was first published.
instructable: https://www.instructables.com/your-write-up/
hackster:
github:
youtube:           # a YouTube video ID, for example dQw4w9WgXcQ
tags:
  - Arduino
  - 3D printing
---
```

`order` controls where the item sits in the home-page list. Lower numbers come first (1, 2, 3…).

`intro` is the short paragraph on the home page. If you leave it out, the list uses `summary` instead.

`instructable` is required for the project to show on the home page, in the sitemap and in the site feed. Only projects with a published Instructable are listed. If a project is not ready, set `published: false` or move the file into `_unpublished/` so it stays in the repo but off the public site.

`youtube` is optional. Put the video's ID (the part after `v=` in the YouTube link), and the project page will embed the video. A full YouTube URL also works.

`tags` is optional. These show as small quiet labels, in the same spirit as Instructables categories (for example Arduino, or 3D printing).

The other link fields are further reading. The page only shows the ones you fill in.

The usual recommendation is a cover photo plus a YouTube embed. You can also copy a fuller Instructables write-up onto the project page if you like, as long as the images are compressed (see below).

## Photos

Put a project's images in `assets/img/<slug>/`, for example `assets/img/algaesense/cover.jpg`, and point `hero` at that path.

Resize photos to about 1600 pixels on the long side, and keep each file under about 300 KB (JPEG is usually best). That keeps the site fast, and it also keeps you comfortably inside GitHub's free Pages hosting. A cover image is enough for most projects. If you want the full Instructables picture set on the page, that's fine too, as long as those images are compressed the same way.

The circular picture at the top of the home page is a placeholder until you add a profile photo (replace `assets/img/placeholder-portrait.svg`). The tab icon is `assets/favicon.png` — swap that file when you have a logo.

## Site-wide settings

A few things live in `_config.yml` instead of a project file:

- `about` — the intro text on the home page, under "About me,"
- `collab_url` — where the "Let's collaborate? :)" button and the footer Collaborate link go. It is a placeholder until you add a Google Form (or other) URL
- `instagram_url` and `donate_url` — leave these empty to keep Instagram and Patreon hidden in the footer; paste a URL to show them
- `links` — the other footer links (GitHub, Instructables, Hackaday, YouTube, X)

Don't add an email address or a `mailto:` link, and don't add LinkedIn. Project code links should be `github.com/bhuvanmakes/...` only, once those repos are public.

## After you edit

If you're changing the repo on GitHub, commit the file and wait for Pages to rebuild. If you're previewing on a computer:

```bash
bundle install
bundle exec jekyll serve
```

Then open http://127.0.0.1:4000. The generated `_site/` folder can be deleted; GitHub Pages will build its own copy.
