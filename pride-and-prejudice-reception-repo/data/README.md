# Data

## Tokenized Review Data

Due to copyright and platform terms of service, full review texts are not included in this repository. Instead, we provide:

- **Tokenized review data** (`.csv`) — morphologically analyzed tokens for Korean reviews (via kiwipiepy) and whitespace-tokenized text for English reviews

### File Format

| Column | Description |
|--------|-------------|
| `review_id` | Unique identifier (e.g., `WF_001` for Watchapedia Film, `IMDB_001` for IMDb) |
| `platform` | Source platform (`watchapedia`, `imdb`) |
| `type` | `film` |
| `tokenized_text` | Space-separated tokens (lemmatized for Korean, stopword-removed for English) |

### ID Prefixes

- `WF_` — Watchapedia, film reviews (3,527 reviews)
- `IMDB_` — IMDb, film reviews (1,099 reviews)

### Korean Book Reviews (Aladin)

The 639 Aladin book reviews were examined qualitatively due to the small number of Mr. Bennet mentions. These are not included in the tokenized dataset but are discussed in the paper.

### Reproducing Full Texts

Reviews were collected using Selenium-based web scraping from each platform's public review pages. Platform content may change over time; the data used in  this study was collected in 2024.
