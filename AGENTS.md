# AGENTS.md

Instructions for any coding agent working in this repository. Read this before
touching anything.

---

## 1. What this repository is

The website for **UNIque Manzanita Company**, a California manzanita supply
business in Brownsville, Yuba County.

Live at **https://preview.uniquemanzanita.com**

This repository contains the website and nothing else. It is public. The
company's business records live in a separate private repository.

### What is deliberately not here, and why

Not included: the prospect register of named buyers and their contacts, unit
economics and margin structure, cost assumptions, the validation budget,
competitor assessments, parcel identifiers, and formation and legal papers.

That material is commercially sensitive and this repository is public. You do
not need it to build a web page. **Do not ask for it, do not try to infer it,
and do not put figures of that kind on the page.** If a task seems to require
it, say so and stop.

---

## 2. What the business is trying to achieve

### The material

Manzanita is a hard, dense, deep red-barked shrub and small tree. Cut and
prepared, its branches are sold as **hardscape**: the structure inside an
aquarium, a reptile enclosure or a bird cage. It is already a real category.
Specialist retailers stock it, and large chains carry manzanita perches.

The company owns roughly a hundred acres of it on one parcel. One owner, one
caretaker, one source. Nothing is bought in and relabelled.

### The problem with how the category sells today

Manzanita is sold as a pile of branches described by a single number: length.
That number is close to useless to a buyer, for two reasons.

**It does not tell you whether a piece fits.** Manzanita grows crooked. A
fourteen-inch branch might be four inches across or eleven. The buyer has a
tank with a bracing bar across the top and a specific interior height. Length
alone cannot answer the only question they have.

**It does not tell you what shipping will cost.** Parcel carriers bill on
dimensional weight, meaning the size of the box rather than the weight of the
contents. An eight-pound branch in a large carton can bill as thirty-four
pounds. A business selling a light, bulky, awkward product either understands
this or loses money on every order.

### Who the customer is

**Retailers. This is a wholesale business.**

The customer is the shop, not the person who walks into it. The goal is the
product on the shelf of every specialty pet, aquatic and reptile store that
will carry it, sold in cases a store can reorder. A store buys twelve pieces,
three sizes, four of each, and retails them out.

**The hero product is therefore the assortment, not the grade.** The case is
what a buyer purchases, so the case is what the site sells.

Direct-to-consumer exists but is deliberately **subordinate**, and must stay
that way. If a shop owner sees this site selling the same piece at retail price
next to the trade offer, U are their competitor and they hesitate. Never give
consumer purchase more prominence than the trade offer, and never undercut the
suggested retail position.

### The position this site takes

**Sell the envelope, not the length.**

Every piece is described by the maximum external box it occupies, measured at
the widest point on each axis rather than along its longest branch. Three
dimensions, published, in inches and centimetres.

That single decision is the spine of the whole site. It answers the buyer's
real question, it makes shipping honest, and it is something no competitor in
the category does. If you are ever unsure whether a change belongs, ask whether
it serves that idea.

The supporting claims are operational, not emotional: a written grade standard
a second worker can follow, so the second case matches the first; lot codes
tying every piece to the batch and the preparation record behind it; and serial
numbers on one-of-a-kind pieces so the item photographed is the item shipped.

### Who the retailer's customers are

Three end audiences who want different things from the same branch. The site
speaks to the **buyer** about all three, because a store needs to know the range
serves its whole aisle, not one shelf.

| Audience | What they are actually buying | What they judge it on |
|---|---|---|
| **Aquascapers** | Hardscape with a silhouette that carries a layout | Branching density, footprint, whether it clears the tank bracing |
| **Reptile keepers** | Climbing structure for arboreal species | Diameter at the trunk and at the fork, fork angle, not length |
| **Aviculturists** | Perch stock cut to a specification they set | Diameter band, bark on or off, squared ends |

**What the buyer themselves cares about** is different again, and it is the
question the site has to answer first: *what does this earn me per foot of
shelf per month.* Case packs, pallet dimensions, lead times, reorder
simplicity, margin, and whether the second shipment matches the first.

**One spec problem to know about.** Two of those three end audiences buy on
**diameter**, not length, and so does the small-mammal chew market if it opens. Only aquascaping leads on overall size. Bird perch
stock is sized to foot span, roughly 1.25 to 2.5 inches for the large parrots
manzanita actually suits; it is too hard for small beaks to work. Reptile
climbing stock runs roughly 0.5 to 3 inches. The published range is still
banded by length, which means a bird buyer cannot order from it. Fixing that is
real work and needs Evan, because the diameter figures do not exist yet.

### Where the business actually is right now

**This is pre-launch. Understanding this explains every disclaimer on the page.**

- No legal entity has been formed.
- No product has been released or offered for sale.
- No customer has ever bought anything.
- No supplier or buyer has been contacted.
- No packaging, transit or product-safety testing has been done.
- The species growing on the parcel has not been determined by a botanist.
- Preparation costs have never been measured.

Everything on the page is therefore a **proposal**, not a fact. The prices are
test values used to size the offer. The grade envelopes are provisional and get
confirmed by a packing trial. The photographs are of manzanita growing wild,
licensed openly, and none of them shows this stand or a product.

The page says all of this plainly, in a banner at the top and five statements
in the footer. **That honesty is a design feature, not boilerplate to tidy
away.** It is what makes the precise claims elsewhere on the page believable.

### What this website is for

Not a store. Its jobs, in order:

1. **Get a trade buyer to ask for the line sheet.** That is the one conversion
   that matters commercially. Everything else serves it.
2. **Establish that this is a serious supplier** rather than someone selling
   yard clippings, in the ten seconds before a buyer decides.
3. **Teach the envelope idea**, so a buyer thinks in three dimensions and
   understands why the shipping is honest.
4. **Show the range covers the whole aisle**, so a store sees more than one
   shelf position.

### Where it goes next

This is a design preview. The functional store is planned on Shopify, with a
single inventory system and a verified trade-account workflow, once there is a
released product with measured costs behind it. Work done here should make that
transition easier: keep the content model clean and the copy reusable.

---

## 3. How the site is built

One self-contained file. `index.html` holds the styles at the top, the content
in the middle, and a small hash router at the bottom. `img/` holds six
photographs. No build step, no package manager, no framework, no dependency
beyond two typefaces from Google Fonts.

```
index.html    the entire site
img/          six photographs
AGENTS.md     this file
README.md     public-facing description
CNAME         custom domain for GitHub Pages
.nojekyll     stops Jekyll processing
```

Five pages live in one document as `<div class="page" id="page-...">` blocks,
shown and hidden by the router on the URL hash. Only the home page is visible
at load.

| Hash | Page | Covers |
|---|---|---|
| `#home` | Home | The position, and the three audiences |
| `#range` | The Range | Four size grades with published envelopes |
| `#exact` | Exact Pieces | One-of-a-kind serialised pieces |
| `#origin` | Origin | The stand, and the lot-code system |
| `#trade` | Trade | Wholesale, OEM and private label |

**Do not convert this to a framework or split it into separate HTML files
unless asked.** The single file is deliberate: it opens from the filesystem, it
deploys with no pipeline, and a non-technical owner can read the whole thing.

The grade table builds from the `GRADES` array in the script so the rows cannot
drift out of step. Edit the array, not the table markup.

### Running it locally

```
cd uniquemanzanita-site
python3 -m http.server 8000
```

Then open `http://localhost:8000`. Opening `index.html` directly from the
filesystem also works, but serve it if you are testing anything path-dependent.

### Checking your work before you open a pull request

- All five pages, reached from the nav, not just the one you edited.
- At 375px, 768px and 1400px wide. Below 600px has had the least attention.
- No horizontal scrolling on the body at any width.
- All six images still load.
- Keyboard only: tab through the nav and make sure focus is visible.

---

## 4. GitHub operation

**Repository:** `unitree-space-captain/uniquemanzanita-site` (public)
**Default branch:** `main`
**Live URL:** `https://preview.uniquemanzanita.com`

### How deployment works

GitHub Pages serves `main` from the repository root. There is no build, no
action, no deploy script. **A merge to `main` is live in about a minute.** That
is the entire pipeline, and it is why the branch discipline below matters: a
bad commit on `main` is a bad public website within sixty seconds.

Two files are load-bearing and must never be deleted:

- **`CNAME`** holds `preview.uniquemanzanita.com`. Delete it and the custom
  domain stops working.
- **`.nojekyll`** stops GitHub running Jekyll over the repository.

DNS is a CNAME at Cloudflare pointing `preview` at
`unitree-space-captain.github.io`, set to DNS-only rather than proxied.
**Do not touch DNS.** It shares a zone with live email.

### The workflow

**Never commit directly to `main`.** Evan reviews every change as a diff.

```
git checkout main
git pull
git checkout -b short-descriptive-branch-name

# make the change

git add -A
git commit
git push -u origin HEAD
gh pr create --fill
```

Then stop and report the pull request URL. Do not merge your own pull request.
Do not push to `main` to "fix it quickly". Do not force-push a shared branch.

### Commit messages

A subject line saying what changed and why in plain words, then a blank line,
then the detail. Explain the reasoning, not the mechanics: the diff already
shows what moved. Write in ordinary English and never use em-dashes.

Not "update index.html". Say what the change does for the reader of the page.

### Pull request descriptions

State what changed, why, and what you checked. If a change touches copy, say
explicitly which of the rules in section 5 you checked it against. If you could
not verify something, say that rather than implying you did.

### Things that are not yours to do

- Merging a pull request.
- Changing repository settings, visibility, or collaborators.
- Touching DNS, the `CNAME`, or anything in Cloudflare.
- Removing `noindex` from the page.
- Adding any analytics, tracking pixel, cookie or third-party script. None of
  that goes on before there is a privacy notice and a decision about consent.
- Adding dependencies, a package manager, or a build step.

---

## 5. Rules the copy must follow

These are not style preferences. They come from the company's own product
release gates, and breaking one creates a real legal or safety exposure for a
business that has not launched yet.

1. **No botanical name anywhere.** The species growing on the parcel has not
   been determined on the ground by a qualified botanist. A provisional read
   exists from photographs, and provisional is not good enough for a page a
   customer reads. Do not write *Arctostaphylos*, do not write "whiteleaf", do
   not name or imply a species.

2. **No safety, suitability, sterility or sinking claim**, for any animal,
   species or enclosure. Never write "non-toxic", "sterile", "safe for every
   pet", "aquarium safe", "reptile safe", "bird safe", "guaranteed to sink", or
   any fixed service life. No product-safety review has been done. Care
   instructions, when they exist, will describe what was actually done to the
   wood, not what it is guaranteed to do.

3. **No environmental or sustainability claim.** Private ownership and
   California origin do not prove sustainable harvesting, and unsubstantiated
   environmental claims are independently a regulatory problem.

4. **Every price and dimension is provisional.** They are planning values held
   until preparation costs are measured and packing trials are run. They are
   not quotations. Do not remove the wording that says so, and do not add a
   price presented as firm.

5. **No product photography claims.** The six photographs show manzanita
   growing wild, licensed openly from other photographers. None shows this
   stand and none shows a product. The footer says so and the credits must
   stay. Original product photography replaces them before anything is offered.

6. **The preview banner and the footer disclaimers stay** until there is a real
   released product. This is not a store, nothing can be ordered, and the page
   must keep saying so.

7. **No named buyer, retailer, distributor or brand appears on the page.** None
   of them has been contacted, and naming one would imply a relationship that
   does not exist.

**If a task would require breaking one of these, stop and say so instead of
doing it.** Flagging the conflict is the correct outcome, not a failure.

---

## 6. Writing style

- **Never use em-dashes.** Use colons, commas, parentheses or semicolons.
- The owner writes **"U" for "you" and "ur" for "your"**. That is deliberate,
  it is in the page copy, and it is part of his voice. Do not correct it.
- **Specific beats persuasive.** "18 x 11 x 9 in, measured at the widest point,
  not the longest" is the register. "Beautiful premium driftwood" is not.
- Write from the reader's side of the screen. Name things the way a buyer
  recognises them.
- Short sentences. No hype words, no filler, no exclamation marks.

The constraint in section 5 and the style here point the same direction. Copy
that cannot make a safety claim has to be precise instead, and precision is
what makes the page feel like it was written by someone who actually handles
the material.

---

## 7. Design constraints

- **One light look.** The page does not follow the viewer's system theme. The
  palette was sampled from the photographs, and the material reads on a pale
  ground the way it does in life. `color-scheme: light` is declared on purpose.
  **Do not add a dark mode.**
- **Three type roles.** The system stack carries the headlines, so it sets in
  SF on Apple hardware. Fraunces carries the eyebrows and the wordmark. IBM
  Plex Mono carries every measurement, lot code and serial, because on this
  site the numbers are the product.
- **Photographs dissolve into the page** through mask gradients on the
  containers (`.photo--hero`, `.photo--band`, `.photo--tall`, `.backdrop`), not
  on the images themselves. Swapping a photograph should need no other change.
  If you add one, sample a colour from its edge toward `--paper` and the seam
  disappears.
- **The dark section on Exact Pieces is a deliberate contrast, not a theme.** A
  dark ground is what makes a single serialised piece read as an object in a
  room. Leave it dark.
- **Every special character is an HTML entity or a JavaScript escape**, on
  purpose, so the page renders correctly however it is served. Write `&times;`
  and `&middot;`, never the literal character. This was a real bug once.
- Colours come from the custom properties at the top of the file. Do not
  introduce a literal colour value into a component.

---

## 8. Open work

Genuinely useful things, if you are looking for work rather than waiting for
instructions. Each is still a pull request.

- **Responsive behaviour below 600px** has had less attention than the desktop
  layout. This matters: a lot of this audience browses on a phone while
  standing in front of a tank.
- **The nav has no mobile treatment** beyond horizontal scroll.
- **No `og:image` or Twitter card metadata**, so the link previews as nothing
  when shared. It gets shared a lot right now.
- **Focus handling in the router.** Changing page does not move keyboard focus,
  so a keyboard or screen-reader user lands nowhere obvious.
- **Image weight.** Six JPEGs at roughly 3.4MB total. WebP with a JPEG fallback
  would cut that substantially without touching the design.
- **The Range page could carry the diameter figures** the terrarium and aviary
  audiences actually judge on. Section 2 says those two audiences care about
  diameter more than length, and the page publishes envelopes only. The numbers
  do not exist yet, so this one needs Evan before it can be built.
