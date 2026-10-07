# Ian Ochieng — Portfolio

The personal portfolio site of **Ian Ochieng**, a full-stack and backend developer in Kisumu, Kenya, and an apprentice at **Zone01 Kisumu**.

**Live site:** https://iochieng1.github.io/My-Blog/

It's a single static page: no build step, framework or JavaScript. It's hosted on GitHub Pages from the `main` branch.

## What's on the site

- **About** — background and the kind of work I do
- **Stack** — languages, frameworks, infrastructure and tools
- **Experience** — freelance client work and the Zone01 Kisumu apprenticeship
- **Projects** — case studies and other work:
  - **SemaKazi** — a skills-verification and reputation platform for informal-sector workers (Node.js, Express, SQLite) · [source](https://github.com/iochieng1/SemaKazi)
  - **Duka POS** — point of sale and inventory for small shops (Node.js, Express, EJS, SQLite) · [source](https://github.com/iochieng1/duka-pos)
  - **Duka Ledger** — installment-payment tracking for shop owners (private client work)
  - **Ben's Tailoring Platform** — website and backend for a Qatar-based tailoring business (client work)
  - **DawaTrace** — a blockchain pharmaceutical-verification prototype (Solidity, Hardhat)
  - **Flexi-Ride** — a team-built ride-hailing platform (Go, SQL)
- **Education** and **Contact**

## Repository structure

```text
.
├── index.html              # the whole site
├── style.css               # design tokens, layout, print styles
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

## Checking the HTML

To catch broken markup, such as unclosed tags, run:

```bash
npx html-validate index.html 404.html
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

## License

[MIT](LICENSE)
