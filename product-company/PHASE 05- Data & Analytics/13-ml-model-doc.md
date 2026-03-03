# ml-model-doc.md

> **Skill:** Produces a machine learning model card that documents model purpose, training data, performance metrics, limitations, fairness assessment, and operational requirements.

---

## TLDR

An ML model card (Mitchell et al., 2019) is the standard documentation artifact for a machine learning model: what it does, what it was trained on, how it performs, where it fails, and what its operational requirements are. It enables informed deployment decisions and responsible use by making model behavior transparent to engineers, product managers, and stakeholders.

---

## Topic Explanation

### Why Model Cards Were Developed

Model cards were introduced by researchers at Google to address the common problem of ML models being deployed without clear documentation of their behavior, limitations, and potential for harm. A model without documentation is a black box: engineers deploying it do not know when it fails, on what groups it performs poorly, or what conditions it was not designed to handle.

The model card provides this transparency systematically.

### Performance Metrics Choice

The choice of performance metrics depends on the model type and the costs of different error types:

**Classification models:**
- Precision: of the predictions labeled positive, what fraction are actually positive? (Minimize false positives)
- Recall: of the actual positives, what fraction were correctly identified? (Minimize false negatives)
- F1: harmonic mean of precision and recall
- AUC-ROC: overall classification ability across thresholds

**Regression models:** RMSE, MAE, R²

**Recommendation models:** precision@k, recall@k, NDCG

The model card should document which metric was optimized during training AND how the model performs on other relevant metrics, because a model optimized for one metric often sacrifices others.

### Fairness Assessment

A model that performs well on aggregate metrics may perform significantly worse for specific demographic groups or data segments. The model card should document performance disaggregated by relevant slices, and explicitly assess whether the model produces unfair outcomes for any group.

---

## Output Format

```
1. MODEL CARD HEADER
   Model name, version, type, author, date, status.
   Model framework and version.

2. MODEL OVERVIEW
   What this model does.
   The prediction it makes and how it is used.
   The problem it solves and for whom.

3. INTENDED USE
   Primary intended use cases.
   Intended users (engineers / product features / analysts).
   Out-of-scope uses: what this model should NOT be used for.

4. TRAINING DATA
   Data sources and time period.
   Data size: rows, features.
   Target variable definition.
   Data preprocessing steps.
   Known biases or limitations in the training data.

5. MODEL ARCHITECTURE
   Model type: logistic regression / random forest / gradient boosting / neural network / etc.
   Key hyperparameters.
   Feature engineering approach.
   Training approach: cross-validation, train/test split.

6. PERFORMANCE METRICS

   Overall performance:
   | Metric | Value | Interpretation |

   Performance by key segment:
   | Segment | Metric | Value | Vs. overall |

   Baseline comparison:
   | Baseline | Metric | Value |

7. EVALUATION DATA
   How the model was evaluated.
   Test set description: size, time period, representativeness.
   Known differences between training and production distribution.

8. LIMITATIONS
   Known failure modes.
   Data distribution shifts that would degrade performance.
   Populations or scenarios the model was not trained on.
   Uncertainty quantification: how reliable are confidence scores?

9. FAIRNESS ASSESSMENT
   Relevant protected characteristics or sensitive segments.
   Performance disaggregated by relevant slices.
   Known disparate impact or bias issues.
   Mitigation steps taken.

10. OPERATIONAL REQUIREMENTS
    Inference latency requirements.
    Infrastructure requirements.
    Monitoring requirements: what to track in production.
    Retraining trigger: when does the model need to be retrained?
    Drift detection: how to detect model staleness.

11. CHANGELOG
    Version history with training data changes and metric changes.
```

---

## Starter Prompt

```
You are a machine learning engineer writing a model card.

Model: [name and what it predicts]
Use case: [how and where it is deployed]
Training data: [sources, period, target variable]
Model type: [algorithm]
Performance metrics: [results on test set]
Segment performance: [performance disaggregated by key groups]
Known limitations: [failure modes and out-of-scope uses]
Operational requirements: [latency, monitoring, retraining]

Produce a complete model card including intended use, training data,
performance metrics disaggregated by segment, limitations, fairness assessment,
and operational requirements.
```

---

*Skill file version: 1.0 | Phase: 06 - Data and Analytics | Company type: Product*
