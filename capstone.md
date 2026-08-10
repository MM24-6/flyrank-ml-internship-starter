---
layout: default
title: Applied Search Intelligence | Madiha Manzoor
description: A machine learning research project exploring search performance signals and content optimization using a Decision Tree model.
---

# Applied Search Intelligence: Google Search Ranking & Discoverability

**Machine Learning Capstone — FlyRank ML Internship**

**Author:** Madiha Manzoor

---

## Abstract

This research investigates whether a Decision Tree model can identify content pages that may benefit from optimization using search performance signals.

A sample of 50,000 rows from the FlyRank ML Internship dataset was analyzed using impressions, average position, and scroll events.

The Decision Tree model was compared with a simple Week 4 baseline using the same evaluation split.

The Decision Tree achieved a measured accuracy of **0.8907**, compared with **0.50** for the baseline.

These findings are observational and are intended to support human decision-making rather than automated publishing or claims about search-engine causation.

---

# 1. Introduction / Problem Statement

Content teams need practical ways to identify pages that may deserve further review.

This project explores whether machine learning can help prioritize content pages using observed search performance signals.

The goal is not to predict or prove how Google's ranking algorithm works. Instead, the model is used as a decision-support tool to highlight pages that may benefit from further human review.

The decision supported by this research is:

> Which content pages may deserve attention for possible optimization based on observed search performance?

---

# 2. Data

## Dataset

The analysis uses the **FlyRank ML Internship dataset**, specifically the:

`fact_content_daily_performance`

table.

A sample of **50,000 rows** was loaded for this analysis.

The resulting dataset contained:

- 50,000 rows
- 30 columns
- 3 anonymized client identifiers
- 5,887 anonymized content identifiers

## Data Signals

The analysis used search and engagement signals including:

- GSC impressions
- Average position
- Scroll events
- GSC clicks for calculating CTR

## Date Window

The available report dates in the selected dataset sample were used for the analysis.

## Public-Safety Exclusions

No client names, domains, URLs, private search queries, credentials, or confidential identifying information were included in the published research paper.

The identifiers available in the dataset are anonymized hashes.

---

# 3. Methodology

## Model

A **Decision Tree classifier** was selected because it is an interpretable machine learning model that works well with structured tabular data.

## Features

The model used:

- GSC impressions
- Average position
- Scroll events

## Label Definition

Click-through rate (CTR) was calculated using GSC clicks and GSC impressions.

Pages with CTR below the average CTR in the analyzed sample were labeled as requiring further optimization review.

This label represents an analytical rule created for this project. It does not represent a business-approved classification or a guaranteed outcome.

## Baseline

The model was compared with the Week 4 baseline.

Both approaches were evaluated on the same test split.

## Validation

The dataset was divided into training and test sets using an 80/20 train-test split with a fixed random seed of 42.

The Decision Tree was trained on the training portion and evaluated on the held-out test portion.

## Leakage Check

The model features did not directly include the CTR label or the GSC clicks used to calculate the label.

No future information or private client information was intentionally included in the model features.

The results should therefore be interpreted as measured results from this analysis rather than proof of future performance.

---

# 4. Results

The Decision Tree model achieved higher measured accuracy than the Week 4 baseline on the same evaluation split.

| Method | Accuracy |
|---|---:|
| Week 4 Baseline | 0.50 |
| Decision Tree | 0.8907 |

The measured accuracy difference shows that the Decision Tree performed better than the simple baseline on this particular evaluation sample.

However, accuracy alone does not establish that the model will perform equally well on future or different datasets.

## Honest Interpretation

The result is:

- **Observed** on the analyzed sample
- **Measured** using the stated evaluation split
- **Directional** rather than guaranteed
- Intended for **decision-support**

It should not be interpreted as evidence that the model can predict Google's ranking algorithm or guarantee improved search performance.

---

# 5. Limitations

This project has several limitations.

### Sample Size

The analysis used a 50,000-row sample rather than the complete warehouse.

### Limited Features

Only a small number of search and engagement signals were used.

### Business Context

The model does not include all business, editorial, technical, seasonal, or content-quality factors that may influence optimization decisions.

### Generalization

The measured result may not generalize to other datasets, time periods, clients, or content types.

### Human Review

Model recommendations require human review before any content or SEO changes are made.

### No Causal Claim

The analysis does not prove that changing a page will cause better search performance.

---

# 6. Ranked Recommendations

The analysis suggests prioritizing pages showing a combination of:

1. **High impressions**
2. **Low click-through rate**
3. **Lower engagement signals**

These pages may deserve additional human review.

## Recommended Action Order

### 1. Review Page Titles

Check whether titles clearly communicate the page's topic and match likely search intent.

### 2. Review Meta Descriptions

Check whether descriptions accurately summarize the page and provide useful context for searchers.

### 3. Review Content Freshness

Identify pages where information may be outdated and determine whether a content refresh is appropriate.

### 4. Review Search Intent

Compare the page's purpose and content with the search intent it is intended to serve.

### 5. Validate Before Publishing

Human reviewers should evaluate recommendations before making changes.

These recommendations are decision-support actions, not guaranteed optimization outcomes.

---

# 7. Reproducibility

The research was developed as part of the FlyRank ML Internship repository.

The main capstone notebook is:

**Capstone Notebook:** `work/notebooks/capstone.ipynb`

The repository also contains the earlier notebooks used throughout the internship, including work related to:

- Research question
- ML task framing
- Data contract
- Baseline scoring
- Model development
- Validation audit
- Action playbook

The analysis uses a fixed random seed of **42** for the train-test split.

The published methodology, assumptions, model features, label definition, and evaluation approach are documented so that the work can be inspected and reproduced from the repository.

---

# 8. Artifacts

The capstone work produced the following artifacts:

### Dataset Summary

A summary of the analyzed dataset including rows, columns, anonymized clients, and anonymized content pages.

### Baseline Comparison

A comparison between the Week 4 baseline and the Decision Tree model.

### Recommendation Queue

A ranked set of pages based on search-performance signals and a review-priority score.

### Methodology Documentation

A written description of the research question, data, features, label definition, validation approach, leakage checks, and limitations.

---

# 9. Acknowledgments & Data Credit

Built on the **FlyRank ML Internship dataset**.

Data credit: FlyRank.

This work was completed as part of the FlyRank Machine Learning Internship using anonymized data and public-safe reporting practices.

The findings are presented as educational and decision-support analysis rather than as claims about private client performance or Google's ranking algorithm.

---

# 10. Five-Minute Demo Outline

## 1 Minute — Problem

Explain that the project investigates whether machine learning can help identify content pages that may deserve optimization review.

## 1 Minute — Data

Explain that a 50,000-row sample of the FlyRank ML Internship dataset was analyzed using search performance and engagement signals.

## 1 Minute — Method

Explain the Decision Tree model, the CTR-based label, the baseline comparison, and the train-test validation approach.

## 1 Minute — Result

Show that the Decision Tree achieved measured accuracy of **0.8907**, compared with **0.50** for the Week 4 baseline.

## 1 Minute — Recommendation

Explain that pages with high impressions and low CTR can be prioritized for human review, followed by title, meta description, content freshness, and search-intent checks.

---

# Employer-Facing Summary

I built an end-to-end machine learning capstone using an anonymized FlyRank search-performance dataset. I developed and evaluated a Decision Tree model using search and engagement signals, compared it with a baseline, and created ranked recommendations for content optimization review. The project demonstrates practical skills in data analysis, feature selection, model evaluation, validation, responsible ML, and decision-support reporting.

---

# Social Post

I completed my Machine Learning Capstone as part of the FlyRank ML Internship.

For the project, I analyzed anonymized search-performance data, developed a Decision Tree model, compared it with a baseline, and created practical recommendations for content optimization review.

The project focused on reproducibility, validation, leakage checks, and responsible reporting rather than making unsupported claims about search-engine algorithms.

#MachineLearning #DataScience #Python #AI #FlyRank

---

## Conclusion

This project demonstrates how a machine learning workflow can be used to turn observed search-performance signals into a structured review process.

The Decision Tree performed better than the simple baseline on the analyzed evaluation sample. However, the result should be treated as directional decision-support evidence rather than a guarantee of future performance.

Human judgment remains an important part of interpreting and acting on the recommendations.

---

© 2026 Madiha Manzoor
