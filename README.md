# Analysis of JM Similarity and Dirichlet Function for Query Similarity Scoring

## Overview

This project explores the performance of the JM Similarity and Dirichlet Smoothing functions for ranking documents based on three queries. By testing various parameter values (\(\lambda\) and \(\mu\)) and analyzing their effects on precision and similarity scores, the study identifies the optimal configurations for each method.

---

## Queries

1. **Economic Growth Policy**
2. **National Security Defense**
3. **God Bless America**

---

## Results Summary

### JM Similarity Function

#### Testing with \(\lambda = 0.3\) and \(\lambda = 0.7\)
- **Observation:**
  - Lower \(\lambda\) values (e.g., 0.3) yielded better similarity scores (closer to 0) than higher \(\lambda\) values (e.g., 0.7).
- **Example (Query: God Bless America):**
  - \(\lambda = 0.3\): Similarity scores: -14.45, -16.09, -16.14
  - \(\lambda = 0.7\): Similarity scores: -16.24, -17.35, -17.445
- **Conclusion:**
  - A lower \(\lambda\) (0.3) provides better similarity scores across all queries, making it the preferred setting for JM Similarity.

---

### Dirichlet Function

#### Testing with \(\mu\) (Mean vs. Standard Deviation)
- **Method:**
  - \(\mu\) based on mean length and standard deviation of documents.
- **Precision Values:**
  - Consistent across both mean and standard deviation:
    - **Economic Growth Policy:** 0.66
    - **National Security Defense:** 0.33
    - **God Bless America:** 1.0
- **Similarity Scores (Mean vs. Std Dev):**
  - Mean consistently outperformed standard deviation, although differences were minor.
  - Example (Query: God Bless America, Mean): 13.71, 13.67, 13.66.

---

### Comparative Analysis: JM Similarity vs. Dirichlet Function

- **Precision:**
  - JM Similarity: Perfect precision (1.0) across all queries.
  - Dirichlet Function:
    - **Economic Growth Policy:** 0.6
    - **National Security Defense:** 0.3
    - **God Bless America:** 1.0
- **Best Results:**
  - Both methods performed best for the "God Bless America" query.
  - JM Similarity provided superior relevancy and precision overall.

---

## Observations

1. **JM Similarity:**
   - Lower \(\lambda\) values improve similarity scores and precision.
   - Best method for high relevancy across all queries.

2. **Dirichlet Function:**
   - Precision varies across queries.
   - Performance is better when \(\mu\) is set to the document mean length.

3. **Vector Space Analysis:**
   - The "God Bless America" query consistently produced the best similarity scores for both methods.

---

## Conclusion

- **JM Similarity** is more precise and reliable than Dirichlet Function for document-query similarity scoring.
- Optimal parameters for both methods:
  - JM Similarity: \(\lambda = 0.3\)
  - Dirichlet Function: \(\mu\) set to mean document length.
- The "God Bless America" query consistently yielded the best results, showcasing the effectiveness of the vector space method.

---

## Code and Results

Detailed implementations and results are available in the accompanying notebook `ProbMeth.ipynb`.

---

## Questions?

Feel free to reach out for further information or collaboration opportunities.
