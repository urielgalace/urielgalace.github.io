# Personal website - Uriel N. Galace

A dependency-free static website (plain HTML + CSS, no build step) served by GitHub Pages
at <https://urielgalace.github.io>. Five pages: About (landing), Research, Projects,
Teaching, CV.

## How it deploys

Every commit to the `main` branch of `urielgalace/urielgalace.github.io` redeploys the
site automatically, usually within a minute or two.

**The repository must be public for the site to be live.** On GitHub's free plan, Pages
only builds public repositories. Toggle it in **Settings → Danger Zone → Change
visibility** (GitHub may ask for your password). Two things to know:

- Making the repository private takes the site offline (it returns 404).
- Commits pushed *while private* do not get built. After switching back to public, push
  one more commit (or re-save the source in **Settings → Pages**) so a build runs against
  the latest code — otherwise the site keeps serving the last build from when it was public.

Publishing source lives in **Settings → Pages**: *Deploy from a branch*, branch `main`,
folder `/ (root)`.

## Common edits

| Task | How |
|---|---|
| Replace the photo | Overwrite `assets/img/profile.jpg` (a 2:3 portrait works well; the CSS crops it to a circle anchored at the top) |
| Adjust the photo crop | `.avatar { object-position: … }` in `assets/css/style.css` — `center top` keeps the head fully in frame |
| Update the CV | Replace `assets/pdf/Galace_CV.pdf` with a new file of the same name |
| Add a paper | In `research.html`, copy an existing `<article class="pub">…</article>` block and edit the title, status line, and abstract |
| Add a project | In `projects.html`, copy a `<div class="card">…</div>` block |
| Link a paper PDF | Put the PDF in `assets/pdf/`, then link it from the paper's status line, e.g. `<a href="assets/pdf/paper.pdf">Draft PDF</a>` |
| Change colors | Edit the variables at the top of `assets/css/style.css` (accent is Duke navy `#012169`) |
| Add a GitHub link | In `index.html`, uncomment the block inside `contact-links` |

Edits can be made directly on github.com: open the file, click the pencil icon, change the
text, and press **Commit changes**. Dark mode follows each visitor's system setting
automatically.

## Preview locally

From this folder:

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000>.
