# lachlanewart.com (personal site)

A single-page personal website. No build step, no dependencies — it's one HTML file.

## Files

```
index.html      the whole site (text + styling)
cv.pdf          your CV, linked from the header
images/         put profile.jpg here
```

## Editing the text

Open `index.html` in any text editor (or edit it directly on GitHub — click the
file, then the pencil icon).

Every bit of text you need to write is wrapped like this:

```html
<p class="todo">Write your intro here — ...</p>
```

Replace the text with your own, then delete `class="todo"` so it stops rendering
as a greyed-out placeholder box:

```html
<p>I'm a second-year maths student at Warwick, currently ...</p>
```

That's the whole system. Anything not marked `todo` is factual detail pulled
from your CV — edit or delete it freely.

## Your photo

Save a square photo as `images/profile.jpg`. If you'd rather have no photo,
delete the `<img class="profile" ...>` line near the top of `index.html`.

## Adding an image

There's a commented-out block in `index.html` marked `OPTIONAL IMAGE`. Drop your
file in `images/`, delete the `<!--` and `-->` around the block, and update the
filename. You can copy that block as many times as you like.

## Links to fix

Three placeholder links point at generic URLs — search `index.html` for
`https://github.com/` and `https://www.linkedin.com/` and swap in your real
profile URLs (e.g. `https://github.com/yourusername`).

---

## Publishing on GitHub Pages

1. Create a new repository on GitHub. If you name it exactly
   `<your-username>.github.io`, the site lives at `https://<your-username>.github.io`.
   Any other name works too — it'll be at `https://<your-username>.github.io/<repo-name>`.
   Make it **Public**.

2. Upload these files. Easiest route: on the empty repo page click
   **uploading an existing file**, then drag in `index.html`, `cv.pdf`, `README.md`
   and the `images` folder. Commit.

   Or from the command line:

   ```bash
   git init
   git add .
   git commit -m "personal site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git push -u origin main
   ```

3. In the repo, go to **Settings → Pages**. Under "Build and deployment", set
   Source to **Deploy from a branch**, branch **main**, folder **/ (root)**. Save.

4. Wait a minute or two, then reload the Settings → Pages screen — the live URL
   appears at the top.

Every future edit you commit goes live automatically within a minute.

## Using your own domain (optional)

Buy a domain, then in **Settings → Pages → Custom domain** enter it and save.
GitHub will tell you which DNS records to add at your registrar. Tick
"Enforce HTTPS" once it's available.
