# Music Genre Classification: KNN with Feature Augmentation

---

# Project Overview

This project implements a **K-Nearest Neighbors (KNN)** classifier to predict the genre of music tracks. By strategically utilizing data augmentation on the **GTZAN Dataset**, the model achieved high accuracy, demonstrating the effectiveness of feature-based classification in Music Information Retrieval (MIR).

# Key Findings

| Metric | Result | Insight |
| :--- | :--- | :--- |
| **Final Accuracy** | **[0.8967]** | The model correctly classifies nearly 9 out of 10 unseen song segments. |
| **Optimal $K$** | **[Insert Your Optimal K Value, e.g., 7]** | This value minimized errors during hyperparameter optimization. |
| **Best Performers** | Metal, Hiphop, Classical ($\mathbf{F1 \ge 0.92}$) | Highly distinct genres are classified with near-perfect reliability. |
| **Main Challenge** | Country ($\mathbf{F1=0.81}$) | The model struggles most with Country, frequently confusing it with adjacent genres like Rock or Pop. |

# Dataset & Features

The model was trained on the **GTZAN Genre Collection**, using the **`features_3_sec.csv`** file.

* **Data Strategy:** We performed data augmentation by segmenting 30-second songs into ten 3-second clips, expanding the training dataset from $\approx 1,000$ to $\mathbf{10,000}$ samples.
* **Core Features:** The classifier used 58 extracted audio features, including **Mel-Frequency Cepstral Coefficients (MFCCs)**, **Spectral Centroid**, and **Chroma features**.

# Technology Stack

* **Language:** Python [Insert Version]
* **ML Libraries:** Scikit-learn (KNN, StandardScaler, Metrics)
* **Data Analysis:** Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn

# Next Steps

To improve performance, future work should include:
1.  **Model Comparison:** Implementing a **Random Forest** or a shallow **Neural Network** to compare against the KNN baseline.
2.  **Error Deep Dive:** Further analysis of the Confusion Matrix to find specific feature differences that could better separate Country from similar genres.