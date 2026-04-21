# Emotion-Aware Recommender System  
### A Stage-Wise Evaluation of Sentiment-Enhanced Recommendation Models

---

## Overview

This project investigates the role of sentiment-aware textual features in recommender systems and evaluates their effectiveness across different stages of user decision-making.

Unlike traditional recommender systems that rely primarily on behavioral data, this study integrates Natural Language Processing (NLP) techniques to extract sentiment from user-generated reviews and incorporates these features into the recommendation pipeline.

A key contribution of this work is a **stage-wise evaluation framework**, which examines how sentiment influences:
- Ranking performance
- Perceived relevance
- Purchase intention
- Model representation capability

---

## Research Objectives

- Analyze the impact of sentiment features on recommendation performance  
- Evaluate how sentiment affects different stages of user interaction  
- Compare baseline and enhanced feature representations  
- Quantify the relationship between sentiment and purchase behavior  

---

## Research Questions

### RQ1  
Does the integration of sentiment-based features improve recommendation ranking performance?

### RQ2  
To what extent does sentiment influence the perceived relevance of recommendations?

### RQ3  
What is the effect of sentiment on user purchase intention?

### RQ4  
Do enriched feature representations outperform traditional text encoding methods?

---

## Methodology

### Data Processing
- Text cleaning and preprocessing  
- Sentiment scoring using NLP techniques  
- Feature engineering (TF-IDF + sentiment features)

### Models Used
- TF-IDF based baseline model  
- Enhanced model with sentiment features  
- Logistic regression for classification tasks  
- Similarity-based recommendation approach  

### Evaluation Metrics
- **Precision@K** → Relevance of top recommendations  
- **Recall@K** → Coverage of relevant items  
- **NDCG@K** → Ranking quality  
- **Accuracy** → Classification performance  
- **T-test** → Statistical significance  
- **Correlation & Regression** → Relationship analysis  

---

## Dataset Description

- Total records: **500**  
- Source: API-based product and review data  
- Features:
  - `user_id`
  - `review_text`
  - `cleaned_text`
  - `product_id`
  - `title`
  - `price`
  - `category`

Sentiment scores were derived from review text and used as additional features in the modeling process.

---

## Key Results found after EDA

###  RQ1: Ranking Performance
- Precision@5: **0.169 → 0.208**  
- Recall@5: **0.0086 → 0.0106**  
- NDCG@5: **0.352 → 0.341**

**Insight:**  
Sentiment improves relevance selection but has limited impact on ranking order.

---

### RQ2: Perceived Relevance
- T-statistic: **-24.41**  
- p-value: **3.93 × 10⁻⁸⁷**

**Insight:**  
Sentiment has a **highly significant impact** on perceived recommendation relevance.

---

### RQ3: Purchase Intention
- Correlation: **0.738**  
- Logistic Regression Coefficient: **8.45**

**Insight:**  
Sentiment strongly influences purchase decisions and is most impactful at the decision stage.

---

###  RQ4: Model Performance
- TF-IDF Accuracy: **0.86**  
- Enhanced Model Accuracy: **0.99**

**Insight:**  
Richer feature representations significantly improve performance, though results should be interpreted cautiously due to potential feature overlap.

---

## Key Insight (Core Contribution)

The impact of sentiment is **stage-dependent**:

| Stage | Impact of Sentiment |
|------|--------------------|
| Ranking | Moderate |
| Relevance | Strong |
| Purchase Decision | Very Strong |

> Sentiment is most influential at later stages of user decision-making.

## Implementation Highlights

- End-to-end NLP pipeline  
- Integration of sentiment into recommendation logic  
- Stage-wise evaluation framework  
- Combination of statistical and machine learning techniques  

---

## Limitations

- Sentiment used as a proxy for emotional context  
- Limited dataset size and diversity  
- Potential overlap between features and target variables  
- Simplified recommendation architecture  

---

## Future Work

- Incorporate transformer-based embeddings (e.g., BERT)  
- Use real-world user interaction datasets  
- Improve ranking optimization techniques  
- Conduct user-based evaluation studies  
- Extend to multi-modal recommendation systems  

