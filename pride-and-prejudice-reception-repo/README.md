# Pride and Prejudice Reception Study

**Patriarchal Myth in Adaptation: A Cross-Cultural Analysis of Reader/Viewer Reviews**

This repository contains the code and processed data for a study examining how Joe Wright's 2005 film adaptation of Jane Austen's *Pride and Prejudice* transforms the character of Mr. Bennet, and how Anglo-American and Korean audiences respond to this transformation.

## Repository Structure

```
├── README.md
├── code/
│   ├── scraping.ipynb          # Review collection from Watchapedia, Aladin, IMDb
│   ├── korean_analysis.ipynb   # Korean morphological analysis + collocation (kiwipiepy)
│   └── imdb_analysis.ipynb     # English tokenization + collocation analysis
├── data/
│   ├── README.md               # Data format description and reproduction instructions
│   ├── korean_reviews_tokenized.csv   # Tokenized Korean reviews (film + book)
│   └── english_reviews_tokenized.csv  # Tokenized IMDb reviews
└── results/
    ├── collocation_korean.csv         # Korean collocation tables (MI, T-score, LL)
    └── collocation_english.csv        # English collocation tables (MI, T-score, LL)
```

## Methodology

### Data Collection
- **Korean film reviews**: 3,527 reviews from [Watchapedia](https://pedia.watcha.com/)
- **Korean book reviews**: 647 reviews from [Aladin](https://www.aladin.co.kr/)
- **English film reviews**: 1,099 reviews from [IMDb](https://www.imdb.com/)

Reviews were collected using Selenium-based web scraping (see `code/scraping.ipynb`).

### Analysis
- **Korean**: Morphological analysis via [kiwipiepy](https://github.com/bab2min/kiwipiepy), followed by collocation analysis (log-likelihood, MI, T-score) with target lemmas "아버지" (father) and "아빠" (dad)
- **English**: Whitespace tokenization with stopword removal, followed by collocation analysis with target terms "father," "dad/daddy," and "Mr. Bennet/Bennett"
- **Parameters**: Window size L5–R5, minimum frequency threshold = 3

## Data Availability

Due to platform terms of service, full review texts are not redistributed. Tokenized versions are provided in `data/`. Full texts can be reconstructed by running the scraping scripts, though platform content may have changed since the original collection (2024).

## Requirements

```
pandas
selenium
kiwipiepy        # Korean morphological analysis
beautifulsoup4
html5lib
tqdm
```

## Citation

If you use this code or data, please cite:

```
[Author]. "Patriarchal Myth in Adaptation: A Cross-Cultural Analysis of 
Pride and Prejudice Reviews." [Journal/Institution], [Year].
```

## License

This project is for academic research purposes. Review data remains the property of its respective platforms and users.
