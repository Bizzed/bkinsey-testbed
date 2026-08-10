# bkinsey-testbed

Testbed repo for a sandbox landing page that simulates a standard marketing site, so Bizzed users can embed and pilot third-party vendors (chatbots, live chat, etc.) and test the end-to-end UX before rolling them out to real client sites.

The site itself is a fictional online tutoring business ("Bright Path Tutoring") built with [Astro](https://astro.build), styled in a stripped-down monochrome palette (white / dark grey). It's deployed via GitHub Pages.

## Adding a vendor embed for testing

All third-party embed snippets go in one place: [src/components/VendorEmbeds.astro](src/components/VendorEmbeds.astro). It's rendered on every page, right before `</body>`. Paste a vendor's install `<script>` snippet there, run the dev server, and test. Remove or comment it out when you're done so the testbed starts clean for the next test.

## Commands

All commands are run from the root of the project, from a terminal:

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `npm install`             | Installs dependencies                            |
| `npm run dev`             | Starts local dev server at `localhost:4321`      |
| `npm run build`           | Build your production site to `./dist/`          |
| `npm run preview`         | Preview your build locally, before deploying     |
| `npm run astro ...`       | Run CLI commands like `astro add`, `astro check` |

## Deployment

Pushes to `main` build and deploy automatically to GitHub Pages via [.github/workflows/deploy.yml](.github/workflows/deploy.yml), publishing to `https://bizzed.github.io/bkinsey-testbed/`. Enable Pages for this repo under Settings → Pages → Source: GitHub Actions.
