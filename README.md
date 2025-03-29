# CIBC Quarterly Report Classification and Chatbot

## 📌 Project Overview
This project automates the classification of **CIBC quarterly financial reports** using **Natural Language Processing (NLP)** and **Machine Learning**. The goal is to categorize financial text into predefined classes using **TF-IDF and Word2Vec embeddings** and evaluate classification models like **Random Forest, Logistic Regression, and Naïve Bayes**. Additionally, a **rule-based chatbot** is integrated to provide financial insights.

## 🚀 Project Workflow
### **1. Data Collection & Preprocessing**
- Extracted **59 quarterly reports (2005-2024)** from CIBC’s investor relations page.
- Text extraction was performed using `pdfplumber`.
- Applied **data cleaning techniques** like stop-word removal, lemmatization, and punctuation removal.

### **2. Feature Extraction**
- **TF-IDF:** Converts text into numerical vectors based on term frequency.
- **Word2Vec:** Creates word embeddings to capture contextual meaning.

### **3. Text Classification Models**
- Implemented **Random Forest, Logistic Regression, and Naïve Bayes** for classification.
- Models were trained and tested using **TF-IDF and Word2Vec embeddings**.

### **4. Model Evaluation**
- **TF-IDF outperformed Word2Vec**, yielding better classification accuracy.
- **Random Forest with TF-IDF achieved 97% accuracy**, the best among all models.
- Word2Vec embeddings negatively impacted accuracy across all models.

### **5. Chatbot Development**
- Developed a **rule-based chatbot** to retrieve financial insights from reports.
- Users can query financial metrics like **Net Income, Revenue, EPS, and CET1 Ratio**.

## 📊 Results Summary
| Model | Feature Extraction | Training Accuracy | Test Accuracy |
|--------|------------------|----------------|-------------|
| Random Forest | TF-IDF | **97%** | **88%** |
| Logistic Regression | TF-IDF | **92%** | **79%** |
| Naïve Bayes | TF-IDF | 80% | 71% |
| Random Forest | Word2Vec | 91% | 71% |
| Logistic Regression | Word2Vec | 66% | 63% |

## 📌 Key Takeaways
- **TF-IDF was the best feature extraction method**, outperforming Word2Vec.
- **Random Forest provided the highest accuracy (97%)**, making it the most effective model.
- **Word2Vec embeddings negatively impacted performance**, likely due to financial text nuances.
- A **rule-based chatbot** was successfully implemented for financial insights.

## 🔮 Future Improvements
- **Handling Imbalanced Data:** Apply **SMOTE** or weighted loss functions.
- **Feature Selection:** Implement **Sequential Feature Selection** for better optimization.
- **Advanced Models:** Explore **XGBoost or Neural Networks** for enhanced accuracy.
- **Chatbot Enhancements:** Improve chatbot with **ML-driven responses**.

## 📂 Project Structure
```
├── data/
│   ├── raw_reports/        # Original PDF reports
│   ├── cleaned_text/       # Preprocessed text files
│
├── models/
│   ├── random_forest.pkl   # Trained Random Forest Model
│   ├── logistic_reg.pkl    # Trained Logistic Regression Model
│
├── scripts/
│   ├── data_preprocessing.py  # Cleaning and preprocessing
│   ├── feature_extraction.py  # TF-IDF & Word2Vec processing
│   ├── model_training.py      # Model training and evaluation
│   ├── chatbot.py             # Chatbot implementation
│
├── notebooks/
│   ├── EDA.ipynb          # Exploratory Data Analysis
│   ├── Model_Training.ipynb  # Model training insights
│
├── README.md              # Project documentation
├── requirements.txt       # Required Python libraries
```

## ⚙️ Installation & Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/cibc-nlp.git
   cd cibc-nlp
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the classification script:
   ```bash
   python scripts/model_training.py
   ```
4. Launch the chatbot:
   ```bash
   python scripts/chatbot.py
   ```

## 🤝 Contributors
- **Aditi Group**  
  - Aagam Shah  
  - Aditi Pithva  
  - Balavishak Mohandas  
  - Daivik Pelathur  

## 📜 References
- [CIBC Quarterly Reports](https://www.cibc.com/en/about-cibc/investor-relations/quarterly-results.html)
- [Stanford NLP Text Classification](https://nlp.stanford.edu/IR-book/information-retrieval-book.html)
