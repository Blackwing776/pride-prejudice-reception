# Data

## Tokenized Review Data

Due to copyright and platform terms of service, full review texts are not included in this repository. Instead, we provide:

- **Tokenized review data** (`.csv`) — morphologically analyzed tokens for Korean reviews (via kiwipiepy) and whitespace-tokenized text for English reviews
- **Original URLs** — each row includes a link to the original review where available

### File Format

| Column | Description |
|--------|-------------|
| `review_id` | Unique identifier (e.g., `WF_001` for Watchapedia Film, `AB_001` for Aladin Book, `IMDB_001` for IMDb) |
| `platform` | Source platform (`watchapedia`, `aladin`, `imdb`) |
| `type` | `film` or `book` |
| `tokenized_text` | Space-separated tokens (lemmatized for Korean) |
| `url` | URL to the original review (where available) |

### ID Prefixes

- `WF_` — Watchapedia, film reviews
- `WB_` — Watchapedia, book reviews
- `AB_` — Aladin, book reviews
- `IMDB_` — IMDb, film reviews

### Reproducing Full Texts

To reconstruct the full corpus, run the scraping notebook (`code/scraping.ipynb`) with a compatible ChromeDriver. Note that platform content may change over time; the data used in this study was collected in 2024.

## Corpus Statistics

| Platform | Type | Reviews |
|----------|------|---------|
| Watchapedia | Film | 3,527 |
| Aladin | Book | 647 |
| IMDb | Film | 1,099 |
