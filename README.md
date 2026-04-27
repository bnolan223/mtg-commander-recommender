# ManaCurve Analytics - A MTG Commander Recommender System

This project develops a data-driven recommendation system for Magic: The Gathering Commander decks. The system analyzes a submitted decklist and suggests cards that improve the deck based on structural fit, color identity, mana curve alignment, and card co-occurrence patterns from real Commander decklists.

The project targets intermediate Commander players who understand deck construction basics but want data-driven guidance when refining their 99.

## Data

Three data sources are required to run the project. The raw data files are not stored in the repository due to size — download them and place them in the project root directory.

**AllPrintings.json** — MTGJSON full card dataset
https://mtgjson.com/downloads/all-files/#allprintings

**AllDeckFiles/** — MTGJSON Commander preconstructed decklists (used for co-occurrence matrix and evaluation)
https://mtgjson.com/downloads/all-files/#alldeckfiles

**oracle-cards.json** — Scryfall bulk oracle card data (includes EDHREC rank per card)
https://scryfall.com/docs/api/bulk-data

## Project Structure

```
notebooks/    – EDA, feature engineering, and recommender system notebooks
reports/      – Report files and presentations
```

## How to Run

1. Download the three data files listed above and place them one level above the `notebooks/` directory (i.e. in the project root).
2. Install dependencies: `pip install pandas numpy scikit-learn matplotlib seaborn`
3. Run the notebooks in order:
   - `01_eda.ipynb` – Basic metrics and exploratory data analysis
   - `02_feature_engineering_analysis.ipynb` – Feature engineering and correlation analysis
   - `03_recommender_system_final.ipynb` – Full recommender system, evaluation, and baseline comparison

## Recommender System

The recommender uses a hybrid approach:

- **Content-based similarity** — cosine similarity over a feature vector of card attributes (mana value, color identity, card types, rarity, power/toughness) and TF-IDF embeddings from card rules text
- **Co-occurrence scoring** — cards that frequently appear together in real Commander precon decklists receive a higher score
- **Color identity enforcement** — hard filter so only color-legal cards are recommended
- **Evaluation** — reconstruction-based Hit Rate@K and Recall@K on held-out MTGJSON decks, Precision@K against deck ground truth, and comparison against a popularity baseline

## Current Progress

- Data acquisition and preprocessing pipeline complete
- Exploratory data analysis and feature engineering complete
- Hybrid content-based + co-occurrence recommender implemented
- Reconstruction evaluation, Precision@K, and baseline comparison implemented
- EDA report complete
- Status presentation complete

## Team Members

Group 1 – ManaCurve Analytics

- Bennett Nolan
- Dominic Durning
- Darryl Fields
