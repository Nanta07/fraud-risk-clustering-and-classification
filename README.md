# fraud-risk-clustering-and-classification

# 📊 Machine Learning Project - Clustering and Classification
This repository showcases a complete machine learning workflow that integrates both **unsupervised (clustering)** and **supervised (classification)** learning approaches. The project was developed as part of my BMLP program (Basic Machine Learning Program).

---

## 🔍 Project Overview

This project is divided into two main phases:
1. **Clustering** – Identifying potential fraudulent patterns in banking transactions and labeling each record with a cluster ID.
2. **Classification** – Using the enriched dataset (which includes the cluster label) to build a model that predicts the cluster classification of new transaction records.

Together, this pipeline simulates a real-world use case where unsupervised learning helps reveal hidden patterns, which are then used as inputs for building more robust supervised models.

---

## 📊 Dataset Description

- **Source**: [Bank Transaction Dataset for Fraud Detection (Kaggle)](https://www.kaggle.com/datasets/valakhorasani/bank-transaction-dataset-for-fraud-detection)
- **Original Purpose**: The dataset was created to support machine learning models in detecting fraudulent banking transactions.
- **Features**: Includes various transactional attributes such as `step`, `type`, `amount`, `oldbalanceOrg`, `newbalanceOrig`, and `isFraud`.

### 🔁 Dataset Use in This Project

This project uses the dataset across two workflows: **clustering** and **classification**.

1. **Clustering Project**:
   - The dataset (`Dataset_clustering.csv`) is used to create clusters that represent transaction behavior patterns.
   - Unsupervised learning (e.g., K-Means) is used to assign each transaction a `cluster_id` to indicate possible risk or behavior categories.
   - The clustering does **not** use `isFraud` as a label, maintaining the unsupervised nature of the task.

2. **Classification Project**:
   - The dataset from the clustering phase is modified to include the `cluster_id` as a new target feature.
   - This modified dataset is saved as `Dataset_inisiasi.csv`, and used to train a supervised classification model.
   - The classifier learns to predict the correct `cluster_id` based on transaction features.

> 📝 **Note**:  
> - `Dataset_clustering.csv` is the **original dataset** obtained from the Kaggle source.  
> - `Dataset_inisiasi.csv` is the **processed dataset** that includes the new cluster label (as class target) used for the classification task.

---

## 🗂️ Project Structure

```

.
├── \[Classification]\_Submission\_Akhir\_BMLP\_Ananta\_Boemi\_Adji.ipynb   # Classification notebook
├── \[Clustering]\_Submission\_Akhir\_BMLP\_Ananta\_Boemi\_Adji.ipynb       # Clustering notebook
├── Dataset\_inisiasi.csv                                             # Original dataset for clustering
├── Dataset\_clustering.csv                                           # Dataset after clustering, used in classification
└── README.md                                                        # Project documentation

```

---

## 📌 Goals

- ✅ Identify clusters of transaction behavior that may indicate fraud.
- ✅ Add cluster labels as a new feature to enrich the dataset.
- ✅ Train a classification model to predict the cluster ID based on transaction features.
- ✅ Simulate a real-world pipeline that combines pattern discovery with classification logic.

---

## 🔧 Tools and Libraries Used

- Python
- Jupyter Notebook
- Pandas, Numpy
- Scikit-learn
- Matplotlib, Seaborn

---

## 🧪 How to Run This Project

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/ml-classification-clustering-project.git
   cd ml-classification-clustering-project
   ````

2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Open the Jupyter notebooks:

   * Run `Clustering` notebook first to generate and save cluster-labeled data.
   * Run `Classification` notebook using the updated dataset.

---

## Author

**Ananta Boemi Adji**
Machine Learning Enthusiast | Computer Engineering Student

---

## 📄 License

This project is intended for educational and research purposes. Feel free to use and reference with proper attribution.
