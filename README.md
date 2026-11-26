# AI Spam Message Detector using Machine Learning

## 📌 Project Overview

The **AI Spam Message Detector** is a Machine Learning project that classifies SMS messages into two categories: **Spam** and **Ham (Legitimate Messages)**.

The project uses Natural Language Processing (NLP) techniques and Machine Learning algorithms to analyse message content, identify patterns and predict whether a message is spam or legitimate.

The primary objective is to build a text classification system that can detect unwanted messages and demonstrate how Machine Learning can be applied to real-world communication problems.

## 🎯 Objectives

- Analyse and understand SMS message patterns.
- Clean and preprocess the dataset.
- Perform Exploratory Data Analysis (EDA).
- Convert text messages into numerical features using TF-IDF.
- Train and compare different Machine Learning models.
- Evaluate model performance using classification metrics.
- Test the selected model with custom messages.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Programming language |
| Google Colab | Development environment |
| Pandas | Data manipulation and cleaning |
| NumPy | Numerical operations |
| Matplotlib | Data visualization |
| Scikit-learn | Machine Learning and evaluation |
| TF-IDF | Text feature extraction |
| NLP | Text classification |

## 📂 Dataset Information

The project uses an SMS Spam Collection dataset containing two categories:

- **Ham (0):** Legitimate messages.
- **Spam (1):** Unwanted or promotional messages.

### Dataset preprocessing

- Selected relevant message and label columns.
- Removed duplicate records.
- Converted categorical labels into numerical values.
- Checked for missing values.
- Created additional features for exploratory analysis.

**Dataset summary after cleaning:**

| Category | Number of Messages |
|---|---:|
| Ham | 4,516 |
| Spam | 653 |
| Total | 5,169 |

A total of 403 duplicate records were removed during preprocessing.

## 🔍 Exploratory Data Analysis (EDA)

EDA was performed to understand the distribution and characteristics of spam and legitimate messages.

The analysis included:

- Spam and Ham class distribution.
- Message length comparison.
- Word count analysis.
- Identification of frequently occurring words.
- Detection of URLs, long numerical sequences and money-related keywords.
- Baseline accuracy analysis.

One key observation was that spam messages were longer on average than legitimate messages in this dataset.

| Category | Average Characters | Average Words |
|---|---:|---:|
| Ham | 70.5 | 14.1 |
| Spam | 137.9 | 23.7 |

## ⚙️ Project Workflow

1. **Data Collection:** Load the SMS dataset.
2. **Data Cleaning:** Remove duplicates, rename columns and prepare labels.
3. **Exploratory Data Analysis:** Analyse message distribution and text patterns.
4. **Data Splitting:** Divide the dataset into 80% training and 20% testing data using stratified sampling.
5. **Feature Extraction:** Apply TF-IDF Vectorization with unigrams and bigrams.
6. **Model Training:** Train two Machine Learning classification algorithms.
7. **Model Evaluation:** Compare accuracy, precision, recall and F1-score.
8. **Error Analysis:** Examine false positives and false negatives.
9. **Feature Interpretation:** Identify important Spam and Ham indicators using Logistic Regression coefficients.
10. **Custom Testing:** Test the selected model using new SMS messages.

## 🧠 Machine Learning Algorithms

Two classification algorithms were implemented and evaluated.

### 1. Multinomial Naive Bayes
A probabilistic classification algorithm commonly used for text classification tasks.

### 2. Logistic Regression
A supervised Machine Learning algorithm used to classify messages into binary categories.

TF-IDF Vectorization was applied to transform text messages into numerical representations before classification.

## 📊 Model Performance Comparison

The models were evaluated using four performance metrics.

| Evaluation Metric | Naive Bayes | Logistic Regression |
|---|---:|---:|
| Accuracy | 99.03% | 98.36% |
| Spam Precision | 100% | 94.53% |
| Spam Recall | 92.37% | 92.37% |
| Spam F1-score | 96.03% | 93.44% |

### 🏆 Selected Model: Multinomial Naive Bayes

Based on the evaluation results, Multinomial Naive Bayes was selected as the final model because it achieved higher accuracy, precision and F1-score than Logistic Regression on the test dataset.

## 🔬 Error Analysis and Feature Interpretation

Additional analysis was performed to understand model behaviour.

**Error Analysis:**
- Identified false positives: legitimate messages incorrectly classified as spam.
- Identified false negatives: spam messages incorrectly classified as legitimate.
- Examined incorrectly classified messages to understand potential model limitations.

**Feature Interpretation:**
- Identified the strongest Spam-associated words.
- Identified the strongest Ham-associated words.
- Visualized Logistic Regression coefficients using horizontal bar charts.

## 🧪 Custom Message Testing

The selected Naive Bayes model was tested with custom SMS messages to demonstrate its prediction capability.

**Example input:**

```python
predict("gpay to 100 rupees 1234567890 this number to claim the prize")
```

**Output:**

```text
SPAM (spam probability: 99.5%)
```

The model classified this message as Spam with an estimated probability of approximately 99.53%.

The prediction function also supports a configurable classification threshold, with a default value of 0.5.

## 📈 Key Learnings

Through this project, I gained practical experience in:

- Data cleaning and preprocessing using Pandas.
- Exploratory Data Analysis and visualization.
- Text preprocessing and TF-IDF feature extraction.
- Implementing and comparing Machine Learning algorithms.
- Evaluating classification models using multiple metrics.
- Understanding confusion matrices and classification errors.
- Interpreting model coefficients.
- Testing trained models with custom text inputs.

## 🚀 How to Run the Project

1. Clone this repository:

```bash
git clone https://github.com/K-KARTHIKRAJA/AI-Spam-Message-Detector.git
```

2. Open the `.ipynb` notebook in Google Colab or Jupyter Notebook.

3. Upload the SMS dataset (`spam.csv`) when prompted.

4. Run the notebook cells sequentially.

5. Train the models and review the evaluation results.

6. Use the custom prediction function to test new messages.

## 📁 Project Structure

```text
AI-Spam-Message-Detector/
│
├── AI_Spam_Message_Detector.ipynb
├── spam.csv
├── eda_class_distribution.png
├── eda_message_length.png
├── confusion_matrices.png
├── model_comparison.png
├── top_words.png
└── README.md
```

*Include the dataset and generated chart images in the repository only if you intend to share them.*

## 🔮 Future Improvements

- Experiment with additional NLP techniques.
- Test other classification algorithms.
- Perform cross-validation for more robust evaluation.
- Experiment with different classification thresholds.
- Improve detection of difficult-to-classify spam messages.
- Develop a simple web application for real-time message classification.

## 👨‍💻 Author

**Karthikraja**

B.Tech Computer Science and Engineering

Interested in Data Analytics, Machine Learning, Python and Artificial Intelligence.

---

⭐ If you find this project interesting, feel free to explore the repository and share your feedback!

**Disclaimer:** The reported model metrics are based on the available dataset and a particular train-test split. Model predictions are text-based estimates and should not be treated as verification that a message or link is safe.
