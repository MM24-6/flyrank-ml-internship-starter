# Applied Search Intelligence: Google Search Ranking & Discoverability

## Abstract

This research investigates whether a Decision Tree model can identify content pages that may benefit from optimization based on search performance signals. A sample of 50,000 rows from the FlyRank ML Internship dataset was used. The model was trained using impressions, average position, and scroll events, and compared with a simple Week 4 baseline. The Decision Tree model achieved a measured accuracy of approximately 0.89 compared with the baseline accuracy of 0.50. These findings are observational and are intended to support human decision-making rather than automated publishing.

---

# Introduction

The purpose of this project is to support content optimization using search performance data. Instead of replacing human judgment, the model highlights pages that may deserve further review. The recommendations are intended to assist SEO and content teams in prioritizing their work.

---

# Data

- Dataset: FlyRank ML Internship Dataset
- Table: fact_content_daily_performance
- Sample Size: 50,000 rows
- Features Used:
  - GSC Impressions
  - Average Position
  - Scroll Events
- Private client information was excluded.
- No URLs or confidential search queries were used.

---

# Methodology

The analysis used a Decision Tree classifier.

### Features
- GSC Impressions
- Average Position
- Scroll Events

### Label

The target was created from Click-Through Rate (CTR). Pages with below-average CTR were labeled as requiring optimization.

### Validation

A train-test split was used for evaluation.

### Leakage Check

No future information, client identifiers, or target-derived features were included.

---

# Results

| Method | Accuracy |
|---------|----------|
| Week 4 Baseline | 0.50 |
| Decision Tree | 0.8907 |

The Decision Tree model produced higher measured accuracy than the baseline on the evaluated sample.

---

# Limitations

- Uses a sample dataset.
- Limited feature set.
- Results may not generalize to every situation.
- Human review is required before making content changes.
- Findings should be interpreted as decision-support.

---

# Ranked Recommendations

Priority should be given to pages with:

- High impressions
- Low click-through rate
- Low engagement

Recommended actions:

1. Improve page titles.
2. Improve meta descriptions.
3. Refresh outdated content.
4. Review search intent.
5. Validate recommendations manually before publishing.

---

# Reproducibility

This project was completed using the notebooks included in the repository.

Main notebooks include:

- Week 5 Model
- Week 6 Validation Audit
- Week 7 Action Playbook
- Capstone Notebook

---

# Acknowledgments

Built on the FlyRank ML Internship Dataset.

Data Credit:
https://flyrank.ai

Special thanks to the FlyRank ML Internship team for providing the anonymized dataset used in this educational project.

---

© 2026 Madiha Manzoor
