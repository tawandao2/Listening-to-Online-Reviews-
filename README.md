# Listening to Online Reviews: Consumer Sentiment & Brand Analytics

**Decoding brand equity and customer loyalty in prestige skincare through NLP and sentiment analysis**

---

## 📌 Project Summary

This project analyzes **1,500+ consumer reviews** for two prestige skincare brands, **L'Occitane** and **La Mer**, to uncover what drives customer satisfaction, loyalty, and brand perception. Using **VADER sentiment analysis** and **NLP techniques in R**, I extracted patterns that go beyond simple star ratings — revealing *why* customers feel the way they do, and how that translates into actionable brand strategy.

**Key finding:** While La Mer holds a slightly higher average rating (4.06 vs L'Occitane), L'Occitane wins on *sensory storytelling* — customers describe a ritualistic, comforting experience — while La Mer wins on *perceived performance and indulgence*. One-star reviews were also found to be significantly *longer* than five-star reviews, suggesting they act as a diagnostic blueprint for product improvement.

These insights culminate in a proposed **Starbucks x L'Occitane "Fast Beauty" subscription box** concept, using the STEPPS framework to translate seasonal drink rituals into skincare engagement moments.

---

## 🛠️ Tools & Methods

| Category | Tools |
|---|---|
| Language | R |
| Sentiment Analysis | VADER |
| NLP / POS Tagging | udpipe |
| Text Mining | tm, wordcloud, tidytext |
| Visualization | ggplot2, gridExtra |
| Statistical Testing | Welch two-sample t-tests |

---

## 📊 Key Findings

### 1. Review Length Reveals Emotional Nuance

![Review Length Distribution](figures/01_review_length_distribution.png)

The average review length is ~404 characters. Reviews longer than this are classified as "Long," shorter as "Short" — this distinction reveals a consistent pattern across sentiment.

- **1-star reviews:** Long reviews are *less* negative (compound ≈ 0.302) than short ones (≈ 0.098) — a statistically significant difference (Welch t-test, p = 0.029). Unhappy customers who write more tend to express dissatisfaction in a more balanced way.
- **5-star reviews:** Long reviews are *more* positive (≈ 0.832) than short ones (≈ 0.688), and highly significant (p ≈ 3.1e-11). Satisfied customers become even more enthusiastic when they write in detail.

![Sentiment: Long vs Short Reviews](figures/04_sentiment_long_vs_short.png)

**Business implication:** Long reviews — in both directions — carry richer signal. Brands should prioritize mining long-form reviews for both product improvement (negative) and marketing copy (positive).

### 2. Ratings Skew Positive, and Sentiment Tracks Cleanly

![Rating Distribution](figures/02_rating_distribution.png)
![Average Sentiment by Rating](figures/03_avg_sentiment_by_rating.png)

Sentiment increases steadily and predictably with star rating. This tight correlation means **sentiment monitoring can serve as an early-warning system** — a dip in review sentiment could signal emerging product issues before it shows up in the star-rating average.

### 3. Brand Comparison: L'Occitane vs La Mer

| Brand | Avg. Compound Sentiment | Positive:Negative Rating Ratio |
|---|---|---|
| L'Occitane | 0.619 | 3.03 : 1 |
| La Mer | 0.660 | 4.09 : 1 |

La Mer shows consistently stronger sentiment and a higher ratio of positive-to-negative reviews. However, both brands are well-liked — they simply occupy **different emotional territory**:

- **L'Occitane** wins on approachability, gentle formulas, and everyday comfort.
- **La Mer** wins on indulgence, luxurious texture, and perceived effectiveness.

![Word Clouds: High vs Low Ratings by Brand](figures/06_wordcloud_brand_comparison.png)

### 4. What Customers Actually Say (Word-Level Analysis)

Using POS tagging (udpipe), I extracted the adjectives most associated with high- and low-rated reviews per brand:

- **L'Occitane — High ratings:** *amazing, soft, great, smooth, worth*
- **L'Occitane — Low ratings:** *oily, thick, dry, strong, sensitive*
- **La Mer — complaints center on:** heaviness, greasiness, and price
- **La Mer — praise centers on:** rich texture, hydration, visible glow

This confirms the brand narrative from the word clouds and sentiment scores: L'Occitane's complaints are about **texture/skin-reaction fit**, while La Mer's are about **value perception**, not efficacy.

![Positive Review Word Cloud](figures/05_wordcloud_positive_reviews.png)

---

## 💡 Strategic Application: Starbucks x Fast Beauty

As a capstone extension of the analysis, I translated these consumer sentiment patterns into a seasonal subscription-box concept pairing Starbucks' seasonal drink rituals with skincare emotional states:

| Season | Drink Inspiration | Skincare Theme |
|---|---|---|
| Spring | Iced Matcha Latte | Fresh start, gentle detox, soft glow |
| Summer | Pink Drink | Bright, fruity, radiance-focused |
| Fall | Pumpkin Spice Latte | Cozy, barrier-repair, comfort |
| Winter | Peppermint Mocha | Indulgence, hydration, holiday sparkle |

This concept demonstrates how sentiment-driven consumer insight can extend beyond diagnostics into **new product and marketing strategy**.

---

## 📁 Repository Structure

```
├── README.md
├── analysis/
│   └── sentiment_analysis.R      # Full VADER + NLP analysis pipeline
├── data/
│   ├── authors.csv
│   ├── products.csv
│   └── reviews.csv
└── figures/
    ├── 01_review_length_distribution.png
    ├── 02_rating_distribution.png
    ├── 03_avg_sentiment_by_rating.png
    ├── 04_sentiment_long_vs_short.png
    ├── 05_wordcloud_positive_reviews.png
    └── 06_wordcloud_brand_comparison.png
```

## ▶️ Reproducing the Analysis

```r
install.packages(c("tidyverse", "vader", "ggplot2", "gridExtra", 
                    "tm", "wordcloud", "RColorBrewer", "tidytext", "udpipe"))
```

Run `analysis/sentiment_analysis.R` from the project root after placing the data files in `data/`. Note: the udpipe English model (`english-ewt-ud-2.5-191206.udpipe`) is downloaded automatically via `udpipe_download_model()` on first run.

---

## 👤 Author

**Tawanda Matiashe**
M.S. Business Analytics, Lehigh University
📫 tam325@lehigh.edu
