# Personal academic website — Uriel N. Galace

A dependency-free static website (plain HTML + CSS, no build step) for GitHub Pages.
Five pages: About (landing), Research, Projects, Teaching, CV.

## Publish on GitHub Pages

1. Create a GitHub account at <https://github.com/signup>. Your username becomes your
   site address (`https://USERNAME.github.io`), so choose it carefully.
2. Create a new **public** repository named exactly `USERNAME.github.io`
   (replace USERNAME with your actual username). Do not add a README when creating it.
3. On the new repository page, click **"uploading an existing file"**, then drag in
   everything inside this folder (the five `.html` files, `404.html`, `README.md`,
   and the `assets` folder — use Chrome, which supports dragging whole folders).
   Click **Commit changes**.
4. Wait 1–3 minutes, then visit `https://USERNAME.github.io`. Done.

Every later edit committed to the repository redeploys the site automatically within
about a minute.

## Common edits

| Task | How |
|---|---|
| Add your photo | Put a square-ish headshot at `assets/img/profile.jpg`, then in `index.html` change `src="assets/img/profile.svg"` to `src="assets/img/profile.jpg"` |
| Update the CV | Replace `assets/pdf/Galace_CV.pdf` with a new file of the same name |
| Add a paper | In `research.html`, copy an existing `<article class="pub">…</article>` block and edit the title, status line, and abstract |
| Add a news item | In `index.html`, copy one `<li>` inside `<ul class="news">` |
| Add a project | In `projects.html`, copy a `<div class="card">…</div>` block |
| Link a paper PDF | Put the PDF in `assets/pdf/`, then link it from the paper's status line, e.g. `<a href="assets/pdf/paper.pdf">Draft PDF</a>` |
| Change colors | Edit the variables at the top of `assets/css/style.css` (accent is Duke navy `#012169`) |
| Add Google Scholar / GitHub links | In `index.html`, uncomment the block inside `contact-links` and fill in your profile URLs |

Edits can be made directly on github.com: open the file, click the pencil icon,
change the text, and press **Commit changes**. Dark mode follows each visitor's
system setting automatically.

## Preview locally

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000>.
