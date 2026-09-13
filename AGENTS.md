# AGENTS.md

Instructions for any coding agent working in this repository.

## What this is

The website for **UNIque Manzanita Company**: a California manzanita supply
business selling graded hardscape branches for aquarium, terrarium and
bird-habitat use. Brownsville, Yuba County, California.

Live at **https://preview.uniquemanzanita.com**

This repository contains the website and nothing else. The company's business
records live in a separate **private** repository and are deliberately not here.
Do not ask for them and do not reproduce anything from them.

## How it is built

One self-contained file. `index.html` holds the styles at the top, the content
in the middle, and a small hash router at the bottom. `img/` holds six
photographs. There is no build step, no package manager, no framework, and no
dependency beyond two typefaces loaded from Google Fonts.

To see it: open `index.html` in a browser, or

```
python3 -m http.server 8000
```

Serve it rather than opening the file directly if you are testing anything that
depends on paths.

Five pages live in one document as `<div class="page" id="page-...">` blocks,
shown and hidden by the router on the URL hash. Only the home page is visible
at load. Do not convert this to a framework or split it into separate HTML
files without being asked.

The grade table builds from the `GRADES` array in the script so the rows cannot
drift out of step with each other. Edit the array, not the table.

## Deploying

`main` is deployed by GitHub Pages automatically. A push to `main` is live in
about a minute. `CNAME` and `.nojekyll` are load-bearing: do not delete them.

**Open a pull request rather than pushing to `main`.** Evan reviews the diff.

## Rules the copy must follow

These are not style preferences. They come from the company's own product
release gates, and breaking one creates a real legal or safety exposure.

1. **No botanical name anywhere.** The species growing on the parcel has not
   been determined on the ground by a qualified botanist. Whiteleaf manzanita
   is the current working read, not a fact. Do not write *Arctostaphylos*, do
   not write "whiteleaf", do not imply a species.
2. **No safety, suitability, sterility or sinking claim**, for any animal,
   species or enclosure. Never write "non-toxic", "sterile", "safe for every
   pet", "aquarium safe", "guaranteed to sink", or any fixed service life.
3. **No environmental or sustainability claim.** Private ownership and
   California origin do not prove sustainable harvesting.
4. **Every price and dimension is provisional.** They are planning values held
   until preparation costs are measured and packing trials are run. They are
   not quotations. Do not remove the wording that says so.
5. **No product photography claims.** The six photographs show manzanita
   growing wild. None shows this stand and none shows a product. The footer
   says so and the credits must stay.
6. **The preview banner and the footer disclaimers stay** until there is a real
   released product. This is not a store, nothing can be ordered, and the page
   must keep saying that.

If a change would require breaking one of these, stop and say so instead.

## Writing style

- **Never use em-dashes.** Use colons, commas, parentheses or semicolons.
- The owner writes "U" for "you" and "ur" for "your". That is deliberate and it
  is in the page copy. Do not correct it.
- Specific beats persuasive. "18 x 11 x 9 in, measured at the widest point, not
  the longest" is the register. "Beautiful premium driftwood" is not.

## Design

- **One light look.** The page does not follow the viewer's system theme. The
  palette was sampled from the photographs and the material reads on a pale
  ground. Do not add a dark mode.
- **Three type roles.** System stack for headlines, Fraunces for eyebrows and
  the wordmark, IBM Plex Mono for every measurement and lot code.
- **Photographs dissolve into the page** through mask gradients on the
  containers (`.photo--hero`, `.photo--band`, `.photo--tall`, `.backdrop`), not
  on the images. Swapping a photograph should need no other change.
- The dark section on the Exact Pieces page is a deliberate contrast, not a
  theme. Leave it dark.
- Every special character is written as an HTML entity or a JavaScript escape,
  on purpose, so the page renders correctly however it is served. Keep it that
  way: write `&times;` not the literal character.

## What would actually improve this

If you are looking for useful work rather than waiting for instructions:

- Responsive behaviour below 600px has had less attention than the desktop
  layout.
- The nav has no mobile treatment beyond horizontal scroll.
- There is no `og:image` or Twitter card metadata.
- Focus order and keyboard navigation through the page router could be tighter;
  the router does not move focus when a page changes.
