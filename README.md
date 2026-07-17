# Mapping Brexit Sentiment: Temporal SVO Networks from One Million Guardian Articles

**MSc Computer Science Dissertation** — Luis Eduardo Ballarati

This dissertation investigates the evolving sentiment of Brexit coverage in *The Guardian* from **2007 to 2024**. Using a dataset of **over one million articles**, it extracts **Subject–Verb–Object (SVO) triplets** to construct temporal sentiment networks centred on the term "Brexit", then analyses how sentiment shifted around key geopolitical events — the 2016 referendum, the invocation of Article 50, and the UK's official departure from the EU — and which words drove those shifts.

📄 **Full dissertation:** [`DissertationGH.pdf`](./DissertationGH.pdf)

## Methodology at a Glance

1. **Data collection** — All Guardian articles from 2007–2024 retrieved via The Guardian's Open Platform API (1M+ articles).
2. **Exploratory analysis** — Lexical diversity, readability, and volume-over-time analysis to validate the reliability and coherence of the corpus before modelling.
3. **SVO extraction** — A custom-built Subject–Verb–Object parser, supported by NLP filtering, converts raw article text into structured triplets.
4. **Network construction** — Triplets are assembled into temporal sentiment networks centred on "Brexit", one per time window, capturing how entities relate to the term over the years.
5. **Network analysis** — Centrality metrics (degree, betweenness, and related measures) identify the most prominent and influential entities in the Brexit discourse and how their roles change around major events.

## Repository Guide

The notebooks follow the pipeline order:

| Notebook | Role |
|---|---|
| `The_Guardian_Scraper_API.ipynb` | Collects the article corpus from The Guardian API |
| `Dataset_Overview_GH.ipynb` | First exploration of the dataset — volume, coverage, structure |
| `Dataset_Overview_2_GH.ipynb` | Deeper corpus statistics (lexical diversity, readability) |
| `Dataset_Overview_3_GH.ipynb` | Final dataset validation ahead of network construction |
| `svo_function_GH.ipynb` | The custom SVO triplet parser and NLP filtering functions |
| `Network_Generator_Testing&Training.ipynb` | Development and testing of the network construction approach |
| `Network_Generator_Final.ipynb` | Final pipeline: builds and analyses the temporal sentiment networks |
| `DissertationGH.pdf` | The full written dissertation |

## Key Findings

Media sentiment around Brexit shifted significantly during major events — most notably the referendum, Article 50, and the formal EU departure — with the sentiment networks revealing which entities and terms gained centrality in each period. The work demonstrates the utility of combining **SVO-based network analysis** with **NLP** for studying media sentiment dynamics at scale, contributing to the field of computational social science.

## Tech Stack

- **Python / Jupyter** — full pipeline
- **NLP** — custom SVO parsing and text filtering
- **Network science** — graph construction and centrality analysis
- **Data source** — The Guardian Open Platform API

## Notes on Reproduction

The raw article corpus is not included in the repo (1M+ articles; Guardian content is subject to their API terms). To reproduce, request a free API key from [The Guardian Open Platform](https://open-platform.theguardian.com/) and run `The_Guardian_Scraper_API.ipynb` first.

---

*Author: Luis Eduardo Ballarati — [Medium](https://medium.com/@luiseduardoballarati)*
