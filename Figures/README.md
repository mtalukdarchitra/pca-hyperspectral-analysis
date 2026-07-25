# PCA Hyperspectral Analysis — Figures

This directory contains the figures generated during the PCA-based hyperspectral data analysis. The experiments compare **Eigenvalue Decomposition (EVD)**, **Singular Value Decomposition (SVD)**, and **Power Iteration** in terms of reconstruction accuracy, runtime, compression, and computational complexity.

---

## Cumulative Explained Variance

![Cumulative Explained Variance](cumulative_variance.png)

The cumulative explained variance increases rapidly with the number of principal components. A relatively small number of components captures most of the variance in the hyperspectral data, demonstrating the effectiveness of PCA for dimensionality reduction.

---

## Figure 1 — Reconstruction Error vs. Number of Components

![Reconstruction Error vs Number of Components](figure1_reconstruction_vs_k.png)

The relative reconstruction error decreases as the number of retained principal components (`k`) increases.

EVD, SVD, and Power Iteration produce nearly overlapping reconstruction-error curves, indicating comparable reconstruction quality for the tested component counts.

---

## Figure 2 — Runtime Comparison

![Runtime Comparison](figure2_runtime_bar.png)

Runtime comparison of EVD, SVD, and Power Iteration at `k = 10`.

For this experiment, EVD has the lowest runtime, Power Iteration requires more computation time, and SVD has the highest measured runtime.

---

## Figure 3 — Compression Ratio vs. Reconstruction Error

![Compression Ratio vs Reconstruction Error](figure3_compression_vs_error.png)

This figure illustrates the trade-off between compression and reconstruction quality.

Higher compression ratios correspond to larger reconstruction errors, while retaining more principal components reduces compression but improves reconstruction accuracy.

The EVD, SVD, and Power Iteration results closely overlap, indicating similar reconstruction behavior across the three PCA approaches.

---

## Figure 4 — Computational Complexity / FLOP Comparison

![FLOP Comparison](figure4_flops_bar.png)

Estimated floating-point operation (FLOP) counts for EVD, SVD, and Power Iteration at `k = 10`.

EVD and SVD have similar estimated computational costs in this experiment, while Power Iteration shows a somewhat higher FLOP count.

---

## Summary

The results demonstrate the trade-offs involved in PCA-based hyperspectral dimensionality reduction:

- Increasing the number of principal components improves reconstruction accuracy.
- A relatively small subset of components captures most of the dataset variance.
- Greater compression results in higher reconstruction error.
- EVD, SVD, and Power Iteration provide similar reconstruction quality in these experiments.
- Their computational runtime and estimated complexity differ, making implementation cost an important consideration when selecting a PCA method.
