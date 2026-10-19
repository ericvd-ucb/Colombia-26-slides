# Slide decks: style and voice

Decks are Quarto reveal.js (`.qmd`), rendered with `quarto render deck.qmd`.

## Setup

- Theme: `cdss-slides.scss` in the deck folder. Front matter:

```yaml
format:
  revealjs:
    theme: [default, cdss-slides.scss]
    embed-resources: true
    slide-number: true
    footer: "Event | Venue | Eric Van Dusen, UC Berkeley"
    title-slide-attributes:
      data-visibility: hidden
```

- Images: the shared kit is at `~/Documents/Vibecoding/slide-kit/images/` (`logos/`, `screenshots/`, `figures/`), indexed in `slide-kit/README.md`. Copy only the images this deck uses into the deck's own `images/` folder so the deck stays self-contained. The title slide needs `uc-berkeley.svg` and `cdss.svg`. When a deck uses a new reusable image, also save it to the kit and add a line to the README index.
- Put all styling in the theme file. Don't add `<style>` blocks to the `.qmd` header. If a slide needs a one-off tweak, add a slide class to the theme (for example `.reveal .myslide-slide ...`).
- Use only the theme's colors. Don't introduce new ones. Navy `#061436` is the one dark blue, with the lighter blues in the theme ramp, plus gold `#FDB515` and orange `#F58B1F` as accents.

## Look

- **Title slide:** `## Title {.title-dark background-color="#061436"}`, with a `.subtitle` span, a `.byline` div (name, date, link; no affiliation text, since the logos show it) and a `.title-logos` div containing both logos. CDSS branding appears on the title slide only. The footer shows only there.
- **Content slides:** a short `##` title and the content. No numbered part labels or category tags above the content (such as `[1. Transferable skills]{.kicker}`); they read as AI-generated. If the talk has parts, show them once on an overview slide or with a `.section-dark` divider slide.
- **One idea per slide.** At most 5 or 6 bullets. If it doesn't fit, split the slide; don't shrink the font.
- **Components in the theme:** pick the one that fits the content, not for decoration.
  - `.statement`, `.statement-2`: lead sentence and supporting note
  - `.big-idea`: navy banner for the slide's main point, at most one per slide
  - `.bottom-question`: light callout for a question or takeaway
  - `.cards` around `.columns`: two to four parallel points
  - `.flow .flow-navy` / `.flow-grey`: vertical process; grey for the contrasting option
  - `.hflow`: left-to-right sequence
  - `.chips`: grid of short items
  - `.stairs` with `.rung .r1/.r2/.r3`: three levels
  - `.build-wrap` / `.build-stack` / `.layer .l1-.l6`: layered stack
  - `.outcome-grey` / `.outcome-navy`: outcome box under a flow
  - `img.shot`: framed screenshot
  - `.caption`: sources and URLs
- Cite sources in a `.caption` on the slide where the claim appears.

## Voice

Academic and professional, in Eric's own plain practitioner register. Not punchy, not conversational, not hot takes.

**Do:**

- Use descriptive titles that name the content: "Onboarding workflow via ACCESS", "Data 8 at scale", "Three levels of compute". Practical questions are fine as titles: "How does a campus get a JupyterHub?"
- Prefer specifics over adjectives: numbers, named courses, tools, programs, partners. "1,500 students per semester" rather than "massive scale".
- Explain systems by roles (instructor, student, administrator) and by numbered steps.
- Write short, complete, plain statements with consistent capitalization.
- Hedge where the evidence is thin. Leave open questions open: "Is notebook-based instruction a change in how we teach?"
- State values plainly: "Open source matters. Public infrastructure matters."
- Credit collaborators and partner institutions by name.
- Use first person sparingly and modestly. "My experience is in scaling infrastructure, not in training models."

**Don't:**

- Write slogans, aphorisms or punch lines ("...stops looking like magic").
- Use rhetorical triplets ("No account. No server. No cost.").
- Set up dramatic binaries with bolded contrasting words ("**consume** vs **build**").
- Make confident predictions, use superlatives, or "here's the thing" constructions.
- Use exclamation points or emdashes.
- Bold more than a word or two per slide.

When unsure, write the version a careful colleague would put in a program report.

## Speaker notes

Brief reminders of what to mention, as short bullets: points to raise, a figure to cite, "live demo, have fallback", a rough time. No prose and no voice needed.

## Before finishing

Render the deck and check every slide for overflow, then fix it by splitting or trimming. Don't shrink the text.
