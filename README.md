# Recommendation Systems Portfolio

Two complementary Python notebooks that develop transparent recommendation-system baselines from Amazon product-review data.

## Notebooks

1. **Exploratory Data Analysis and Bayesian Popularity Recommender**
   - Cleans review data, measures user-item sparsity, explores rating and activity patterns, and ranks products with Bayesian-smoothed popularity scores.
   - Establishes a robust non-personalized baseline for new users and sparse interaction histories.

2. **Content-Based Filtering with TF-IDF**
   - Builds item text profiles from review content, computes TF-IDF features and cosine similarity, and generates personalized unseen-item recommendations from rating-weighted user profiles.
   - Includes an intra-list similarity measure to discuss recommendation diversity and filter-bubble risk.

## Setup

```bash
python -m venv .venv
# Windows
.venv\\Scripts\\activate
# macOS/Linux
source .venv/bin/activate
pip install -r requirements.txt
jupyter lab
```

## Dataset

The notebooks expect a compatible Amazon Reviews JSON-lines dataset at:

```text
data/Electronics_5.json.gz
```

The dataset is intentionally excluded from this repository. It can be large and may be subject to separate distribution conditions. No dataset-derived outputs are committed; run the notebooks locally after supplying the data.

## Methods

- Exploratory data analysis and temporal inspection
- User-item sparsity analysis
- Bayesian-smoothed popularity ranking
- TF-IDF text vectorization with unigrams and bigrams
- Cosine similarity for item and user-profile ranking
- Intra-list similarity as a simple diversity indicator

## Limitations

Popularity ranking is non-personalized and may overexpose mainstream items. Content-based filtering depends on descriptive text and can over-specialize. These notebooks are intended as explainable baselines before a hybrid or collaborative filtering model.
