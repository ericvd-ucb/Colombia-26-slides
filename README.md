# Colombia talks, October 2026

Slides for two talks at Universidad Externado de Colombia, Bogotá, October 2026. Eric Van Dusen, UC Berkeley College of Computing, Data Science, and Society.

In the HTML slides, press `S` for speaker notes and `F` for full screen.

## Keynote: Data Science in the AI Era (October 21, 2026)

How should data science education evolve? What a decade of teaching data science at Berkeley suggests for teaching AI, contributions from Colombia, and how courses can expand as AI tools change the work.

- **View the slides:** [ericvd-ucb.github.io/Colombia-26-slides/externado_keynote.html](https://ericvd-ucb.github.io/Colombia-26-slides/externado_keynote.html)
- **PDF:** [externado_keynote.pdf](externado_keynote.pdf)

Related materials:

- Notebooks for students: [github.com/ericvd-ucb/Colombia-26-NB](https://github.com/ericvd-ucb/Colombia-26-NB)
- Small models in the browser: [ericvd-ucb.github.io/small-models-lite](https://ericvd-ucb.github.io/small-models-lite/)

## Data Science Education and Workforce Preparation in the AI Era

- **View the slides:** [ericvd-ucb.github.io/Colombia-26-slides/data_science_ai_era_outline.html](https://ericvd-ucb.github.io/Colombia-26-slides/data_science_ai_era_outline.html)
- **PDF:** [data_science_ai_era_outline.pdf](data_science_ai_era_outline.pdf)

## Files

- `externado_keynote.qmd`, `.html`, `.pdf`: the keynote deck (Quarto reveal.js), rendered slides and PDF
- `data_science_ai_era_outline.qmd`, `.html`, `.pdf`: the workforce talk
- `cdss-slides.scss`: theme shared by both decks
- `CLAUDE.md`: style and voice rules for the decks
- `images/`: logos, screenshots and figures

To render:

```bash
quarto render externado_keynote.qmd
quarto render data_science_ai_era_outline.qmd
```
