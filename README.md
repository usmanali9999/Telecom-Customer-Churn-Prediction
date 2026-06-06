# Telco Customer Churn Prediction Engine

An end-to-end machine learning pipeline leveraging **Decision Tree** and **Random Forest Classifiers**, optimized using a **Genetic Algorithm (GA)** for intelligent feature selection. This project targets binary classification of customer attrition using demographic, account, and billing attributes from the Telco dataset.

## 🚀 Key Features
* **Automated Data Processing**: Coercive data type conversion, null field verification, and continuous feature scaling.
* **Evolutionary Feature Selection**: Employs the `deap` framework to discover optimal feature chromosomes and eliminate noisy variables.
* **Comparative Evaluation**: Benchmarks single-tree logic against multi-tree ensemble architectures.

---

## 📊 Model Performance Metrics

The algorithms were evaluated using standard validation splits on the `WA_Fn-UseC_-Telco-Customer-Churn.csv` dataset. Below are the recorded metric baselines:


| Model Architecture | Feature Selection Mode | Accuracy | Precision | Recall | F1-Score |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Decision Tree** | All Raw Features | 72.8% | 49.3% | 48.7% | 49.0% |
| **Random Forest** | All Raw Features | 78.9% | 63.1% | 47.9% | 54.5% |
| **Random Forest + GA** | Optimized Feature Chromosome | **80.4%** | **65.8%** | **51.2%** | **57.6%** |

### Key Observations
* **Ensemble Superiority**: The Random Forest variant yields a significant drop in false-positive rates compared to the standalone Decision Tree.
* **Genetic Optimization**: Applying the Genetic Algorithm for feature selection prunes redundant attributes, boosting overall model accuracy and optimizing the F1-Score via improved recall balances.

---

## 🏃‍♂️ Execution Blueprint

Follow these steps to set up and run the environment locally:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/usmanali9999/Telecom-Customer-Churn-Prediction.git
   cd Telecom-Customer-Churn-Prediction
   ```

2. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Launch the Notebook**:
   ```bash
   jupyter lab
   ```
   Open the notebook workspace and execute the cells sequentially to visualize data preprocessing steps and view live genetic algorithm generations.
