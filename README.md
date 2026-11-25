# Bhuvan Makes

Personal site for [Bhuvan Makes](https://bhuvanmakes.github.io), built with Jekyll so GitHub Pages can compile it from the default branch. There is no custom GitHub Actions workflow and no heavy JavaScript framework.

The public site is https://bhuvanmakes.github.io, built from this repository.

## Pages

- `/` — landing page (about, then one list of projects and writing)
- `/projects/algaesense/` — AlgaeSense write-up
- `/projects/morse-monkey/` — Morse Monkey
- `/blog/algaesense/` redirects to `/projects/algaesense/`
- `/blog/` and `/projects/` redirect to the home page so old addresses keep working
- Unpublished projects live in `_unpublished/` (currently BESOS and Small Beacon) and stay off the public site until they have a published Instructable
- Drafts in `_drafts/` are not built unless you pass `--drafts`
- `EDITING.md` — how to add or edit a project or write-up

Public identity is **Bhuvan Makes** only. There is no LinkedIn link. OpenExG-C5, AirCalibre and GoodOne are not on this site.

## Look

The site is dark only: black background, white text, yellow accents. Yellow rules sit under the header and above the footer only. Colours and fonts are CSS variables at the top of `assets/css/style.css`. There is no light theme, no location line, and no email address or `mailto:` link on the site.

The home page opens with Bhuvan's about text and a "Let's collaborate? :)" button (the URL is `collab_url` in `_config.yml`, a placeholder until a form link is added). Projects and writing share one list. To add or change work, see `EDITING.md`.


## Local preview

You need Ruby 3, Bundler, and (the first time) a network connection to install gems.

```bash
cd bhuvanmakes.github.io   # or this folder, /workspace/portfolio/site
bundle config set --local path vendor/bundle
bundle install
bundle exec jekyll serve
```

Then open <http://127.0.0.1:4000>. The compiled site is written to `_site/`, which is generated and can be deleted.

To preview unpublished drafts as well:

```bash
bundle exec jekyll serve --drafts
```

## How to publish (once bhuvanmakes access exists)

Do these steps only after Bhuvan grants access to the **bhuvanmakes** GitHub account and asks for the site to go live. The box `gh` CLI may still be signed in as another account; switch or authenticate as **bhuvanmakes** first. Do not push from the wrong account.

1. Sign in as `bhuvanmakes`. Confirm with `gh api user --jq .login`.
2. Create a **public** repository named exactly `bhuvanmakes.github.io` on that account (empty, no README or licence from the GitHub form, so this tree can be pushed as-is).
3. In this folder:

   ```bash
   git remote add origin git@github.com:bhuvanmakes/bhuvanmakes.github.io.git
   git branch -M main
   git push -u origin main
   ```

4. On the repository's Settings → Pages, set the source to **Deploy from a branch**, branch **main**, folder **/ (root)**. GitHub Pages will run Jekyll itself. Do not add a `.nojekyll` file.
5. Wait for the Pages build, then check <https://bhuvanmakes.github.io>.
6. Optional later: replace `assets/img/placeholder-portrait.svg` with the shared profile photograph once Bhuvan supplies it, and fill empty kit fields (see below) as each piece is published.

No custom domain is required. Do not reuse the existing `bhuvanmakes/portfolio` PDF repository as this site.

## Adding a project or a write-up

See `EDITING.md` for the short, plain-language version: which folder to use, the front matter fields, where images go, and how writing shows up in the same home-page list as projects.

## GitHub links

The footer links to the public profile <https://github.com/bhuvanmakes>.

Project and post `github` kit fields are intentionally empty until each repository is published under that account. When a repo goes public, add its `https://github.com/bhuvanmakes/...` URL to the matching project page and blog post, then rebuild.

## Portrait

`assets/img/placeholder-portrait.svg` is a temporary monogram. Bhuvan is taking a new photograph to use on this site and on the other public profiles. Do not invent a portrait.
