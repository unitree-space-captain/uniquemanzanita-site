# UNIque Manzanita: website

Design preview for **UNIque Manzanita Company**, Brownsville, Yuba County,
California. Graded California manzanita for aquarium, terrarium and
bird-habitat use.

Live at **https://preview.uniquemanzanita.com**

## This is a preview, not a store

Nothing has been released or offered for sale, no order can be placed, and
every price and dimension on the page is a working assumption rather than a
quotation. The page says so in its own banner and footer. It carries
`noindex, nofollow` so it stays out of search results until there is a real
product behind it.

## What is here

```
index.html     the entire site, one self-contained file
img/           six photographs
CNAME          the custom domain for GitHub Pages
```

No build step, no dependencies, no framework. Two typefaces load from Google
Fonts; everything else ships with the page. Open `index.html` in any browser
and it works, including straight off the filesystem.

## Structure

Five pages behind a sticky nav, routed on the URL hash so each has its own
address:

| Page | Covers |
|---|---|
| `#home` | The position, and the three audiences |
| `#range` | Four size grades with published envelopes |
| `#exact` | One-of-a-kind serialised pieces |
| `#origin` | The stand, and the lot-code system |
| `#trade` | Wholesale, OEM and private label |

## The idea it is built on

Buyers do not buy a length, they buy a shape that has to fit a space. So every
piece is described by its **envelope**, the maximum external box it occupies,
measured at the widest point on each axis rather than along its longest branch.
That is the number that decides whether a piece clears a bracing bar, and it is
the number that sets the shipping charge, because size rather than weight
prices most parcels.

## Design notes

- **Palette** sampled from the photographs: live mahogany bark, weathered
  silver heartwood, glaucous leaf, dry foothill grass. It commits to one light
  look rather than following the viewer's system theme, because the material
  reads on a pale ground the way it does in life.
- **Type in three roles.** The system stack carries the headlines, so it sets
  in SF on Apple hardware. Fraunces carries the eyebrows and the wordmark. IBM
  Plex Mono carries every measurement and lot code, because the numbers are the
  product.
- **Photographs dissolve into the page** through mask gradients on the
  containers, not on the images, so swapping a photograph changes nothing else.

## Rules the copy follows

These are not stylistic. They come from the company's own release gates.

1. **No botanical name anywhere.** The species has not been determined on the
   ground by a qualified botanist.
2. **No safety, suitability, sterility or sinking claim**, for any animal,
   species or enclosure.
3. **No environmental or sustainability claim.**
4. **Every price and dimension marked provisional.**

## Photography

None of these is a product photograph, and none shows this stand. They are
manzanita growing wild, licensed from the photographers below via Wikimedia
Commons. Original product photography replaces them before anything is offered.

| File | Photograph | By | Licence |
|---|---|---|---|
| `hero.jpg` | Curvy Curves | cogdogblog | CC0 |
| `branch.jpg` | The Manzanita Kink | cogdogblog | CC BY 2.0 |
| `tangle.jpg` | Manzanita texture | Aubrie Johnson | CC0 |
| `stand.jpg` | Manzanita | Katja Schulz | CC BY 2.0 |
| `peeling.jpg` | Manzanita bark | Alan Schmierer | CC0 |
| `limbs.jpg` | Common manzanita | Paul Asman and Jill Lenoble | CC BY 2.0 |

## Editing it

Everything is in `index.html`: styles at the top, content in the middle,
a small router at the bottom. Content lives in plain HTML except the grade
table, which builds from the `GRADES` array in the script so the four rows
cannot drift out of step.

Changes to the page must not break the four copy rules above.
