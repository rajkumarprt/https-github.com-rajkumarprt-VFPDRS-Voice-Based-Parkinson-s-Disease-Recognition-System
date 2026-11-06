# VFPDRS: Voice-Based Parkinson's Disease Recognition System

## Repository Overview

This repository contains the implementation of the **Voice-Based Parkinson's Disease Recognition System (VFPDRS)**, an intelligent machine learning framework for the early detection and classification of **Parkinson's Disease (PD)** using biomedical voice features.

The proposed framework integrates **Correlation-Based Feature Selection (CFS)** with a novel **Weighted Probabilistic Bagged k-Nearest Neighbour (WPB-k-NN)** classifier to improve prediction robustness, reduce overfitting, and enhance generalization performance for telehealth-oriented clinical applications.

The implementation utilizes the publicly available **Oxford Parkinson's Disease Dataset** from the **UCI Machine Learning Repository** and compares the proposed approach with several baseline machine learning models, including:

- Support Vector Machine (SVM)
- Logistic Regression
- Random Forest
- Conventional k-Nearest Neighbour (k-NN)
- PCA-based classifiers
- CFS-enhanced classifiers
- Proposed Weighted Probabilistic Bagged k-NN (WPB-k-NN)

---

# Proposed Methodology

The proposed **VFPDRS** framework consists of five major components.

## 1. Voice Acquisition Layer

The system accepts sustained vowel phonation recordings from subjects using mobile or clinical recording devices. Biomedical voice features are extracted from the Oxford Parkinson's Disease dataset, including:

- Fundamental Frequency (Fo)
- Jitter Measures
- Shimmer Measures
- Harmonic-to-Noise Ratio (HNR)
- RPDE
- DFA
- D2
- Pitch Period Entropy (PPE)

These features capture neuromotor speech impairments associated with Parkinson's Disease.

---

## 2. Multimodal Feature Extraction

The extracted biomedical voice features provide a comprehensive characterization of vocal biomarkers relevant to Parkinson's Disease diagnosis.

---

## 3. Correlation-Based Feature Selection (CFS)

To reduce redundancy and improve classification performance, the proposed framework employs **Correlation-Based Feature Selection (CFS)**. The objective is to maximize feature relevance while minimizing feature redundancy.

---

## 4. Weighted Probabilistic Bagged k-NN (WPB-k-NN)

The proposed **WPB-k-NN** classifier extends the traditional k-Nearest Neighbour algorithm through three mechanisms.

### Bootstrap Aggregation (Bagging)

- Multiple bootstrap datasets are generated.
- Each bootstrap sample trains an independent k-NN classifier.

### Distance-Based Weighting

- Neighbour contributions are weighted according to their Euclidean distances.

### Probabilistic Ensemble Aggregation

- Posterior probabilities of each class are estimated.
- Final class prediction is obtained using probabilistic ensemble voting.

This strategy improves robustness against noisy samples, reduces variance, and enhances prediction stability.

---

# Experimental Configuration

| Parameter | Value |
|------------|-------|
| Programming Language | Python 3.x |
| Environment | Jupyter Notebook |
| Operating System | Windows 10 (64-bit) |
| Base Learner | k-Nearest Neighbour |
| Distance Metric | Euclidean Distance |
| Number of Neighbours (k) | 5 |
| Number of Bootstrap Models | 50 |
| Hyperparameter Optimization | Grid Search + Cross Validation |

---

# Dataset

## Oxford Parkinson's Disease Detection Dataset

**Source**

https://archive.ics.uci.edu/dataset/174/parkinsons

### Dataset Characteristics

- 195 voice recordings
- 31 biomedical voice features
- 31 individuals
- 23 Parkinson's Disease patients
- 8 healthy controls

---

# Repository Structure

```text
VFPDRS/
│
├── NewPDmodels.ipynb
├── data.csv
├── README.md
├── requirements.txt
├── figures/
│   ├── architecture.png
│   ├── confusion_matrix.png
│   └── performance_comparison.png
│
└── results/
    ├── baseline_results.csv
    └── wpb_knn_results.csv
```

---

# Key Features

- ✔ Correlation-Based Feature Selection (CFS)
- ✔ Weighted Probabilistic Bagged k-NN (WPB-k-NN)
- ✔ Bootstrap Ensemble Learning
- ✔ Distance-Based Neighbour Weighting
- ✔ Parkinson's Disease Voice Biomarker Analysis
- ✔ Comparative Performance Evaluation
- ✔ Telehealth-Oriented Disease Monitoring
- ✔ Reproducible Experimental Framework

---

# Citation

If you use this repository in your research, please cite the associated publication.

```text
Sathya Bama B, Archana Sasi, Rajkumar Rajavel, Sathish Kumar Ravichandran, Santhosh Kumar C, Daniel Arockiam, "AI-Enabled Voice-Based Parkinson’s Disease Detection: A Feature-Weighted Probabilistic Ensemble Learning Approach", Humanities and Social Sciences Communications, 2026.
```

---

# Future Enhancements

Future extensions of the VFPDRS framework include:

- Deep Learning-based Voice Embeddings
- Multimodal Sensor Fusion
- LSTM-based Temporal Modelling
- Edge AI Deployment
- Real-time Mobile Health Applications
- Federated Learning for Privacy-Preserving Analytics
- Clinical Validation on Large-Scale Datasets

---

## License

This repository is intended for academic research and educational purposes.

---

## Contact

For research collaborations or queries, please contact the repository author.
