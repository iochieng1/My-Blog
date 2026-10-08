# Ian Ochieng — Portfolio

The personal portfolio site of **Ian Ochieng**, a full-stack and backend developer in Kisumu, Kenya, and an apprentice at **Zone01 Kisumu**.

**Live site:** https://iochieng1.github.io/My-Blog/

It's a static site: plain HTML and CSS, with no build step, framework or JavaScript. It's hosted on GitHub Pages from the `main` branch.

## What's on the site

- **About**, with a professional photo
- **Stack**: languages, frameworks, infrastructure and tools
- **Experience**: freelance client work and the Zone01 Kisumu apprenticeship
- **Projects**:
  - **Personal projects**
    - SemaKazi, a skills-verification platform for informal-sector workers ([source](https://github.com/iochieng1/SemaKazi))
    - Duka POS, point of sale and inventory for small shops ([source](https://github.com/iochieng1/duka-pos))
    - AuraRisk, a flood-risk and early-warning platform ([source](https://github.com/iochieng1/Aura-Risk))
  - **Internal projects (Zone01 Kisumu)**: Flexi-Ride, DawaTrace, Clonernews, Sortable and [go-reloaded](https://github.com/iochieng1/go-reloaded)
  - **Client work**: Duka Ledger and Ben's Tailoring
- **Articles**:
  - engineering notes on real issues, in [`articles/`](articles/)
  - posts on [Dev.to](https://dev.to/iochieng1)
- **Hobbies**, **Education** and **Contact**, with links to LinkedIn, GitHub, Dev.to and X
- **Resume**: [`resume.html`](resume.html), plus a downloadable [`resume.pdf`](resume.pdf)

## Repository structure

```text
.
├── index.html              # the home page
├── style.css               # design tokens, layout, print styles
├── resume.html             # printable resume
├── resume.css
├── resume.pdf              # generated from resume.html (see below)
├── articles/               # engineering notes, one page each
├── img/ian-ochieng.jpg     # profile photo
├── favicon.svg
├── 404.html                # GitHub Pages "not found" page
├── robots.txt
├── sitemap.xml
├── .nojekyll               # serve files as-is, skip Jekyll
└── .htmlvalidate.json      # HTML lint rules
```

## Running locally

```bash
git clone https://github.com/iochieng1/My-Blog.git
cd My-Blog
python3 -m http.server 8000
```

Then open http://localhost:8000. You can also open `index.html` directly in a browser, but `404.html` uses absolute `/My-Blog/` paths, so it only renders correctly when served from GitHub Pages.

## Adding an engineering note

1. Copy `.github/templates/article.html` to `articles/<slug>.html` and fill in every `{{...}}` placeholder.
2. Add the note to the top of the "Engineering notes" list in `index.html`.
3. Add its URL to `sitemap.xml`.

## Regenerating the resume PDF

After editing `resume.html`, serve the site locally (see above), then run:

```bash
chromium --headless --no-pdf-header-footer --print-to-pdf="$PWD/resume.pdf" http://localhost:8000/resume.html
```

## Checking the HTML

To catch broken markup, such as unclosed tags, run:

```bash
npx html-validate index.html 404.html resume.html articles/*.html
```

## Accessibility

- Text colours meet WCAG AA contrast (4.5:1) against the dark background.
- There's a skip link, labelled navigation and visible focus outlines.
- Links that open in a new tab say so to screen readers.
- Animation is disabled when the visitor prefers reduced motion.

## Contact

- Email: ochieng1044@gmail.com
- GitHub: https://github.com/iochieng1
- LinkedIn: https://www.linkedin.com/in/ian-ochieng/
- Dev.to: https://dev.to/iochieng1

## License

[MIT](LICENSE)
