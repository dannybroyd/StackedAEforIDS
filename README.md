# StackedAEforIDS

An implementation of the **Stacked Autoencoder (AE)** method from the paper:  
**_"Exploring the boundaries of lateral movement detection through unsupervised learning"_**  
by Smiliotopoulos et al.

---

## 📌 Description

This project implements a Stacked Autoencoder architecture for unsupervised anomaly detection, inspired by the methodology proposed in the above paper. The model is trained exclusively on **normal traffic** samples and is evaluated on its ability to detect **lateral movement attacks**.

The dataset used is **LMD-2023**, a comprehensive benchmark dataset for intrusion detection.

---

## 📁 Dataset

> **Note**: The dataset files are **too large to upload to GitHub** directly.

To run this project, you must manually place the required files in a local `data/` directory in your project root.

**Required files:**

```
data/
├── LMD-2023 [2.3M Elements - EoHT]checked.csv
├── LMD-2023 [2.3M Elements - EoRS]checked.csv
└── LMD-2023 [2.3M Elements - Normal]checked.csv
```

And a checkpointing folder 
```
checkpointing/
```

Make sure the filenames match exactly, including spaces and brackets.

---

## 🧠 Model Overview

The Stacked Autoencoder is trained only on normal samples, following an unsupervised learning paradigm. It attempts to reconstruct input vectors and flags samples with high reconstruction error as potential anomalies.

---
