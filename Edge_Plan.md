 Edge Deployment Plan

1. Overview
This system is designed to run efficiently in an edge environment (offline, low compute, CPU-only devices). The goal is to ensure fast, reliable, and lightweight inference without relying on external APIs or cloud services.

2. Constraints

The system is built under the following constraints:

- No internet access (fully offline)
- Low latency (<100ms per prediction)
- Limited memory (<100MB)
- CPU-only execution (no GPU)


3. Model Design

| Component            | Approach                          | Reason |
|---------------------|----------------------------------|--------|
| Text Processing     | TF-IDF                           | Lightweight, fast |
| State Prediction    | Logistic Regression              | Efficient on sparse data |
| Intensity Prediction| Random Forest Regressor          | Good performance with low complexity |
| Decision Engine     | Rule-based system                | Zero computational cost |
