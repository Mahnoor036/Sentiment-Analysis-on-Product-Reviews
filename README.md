# Sentiment-Analysis-on-Product-Review

This project performs **sentiment analysis** on product/movie reviews using the **IMDB Dataset**.  
It uses **Natural Language Processing (NLP)** techniques for preprocessing, **TF-IDF vectorization**, and trains both **Logistic Regression** and **Naive Bayes** models.  
The project also visualizes **top positive/negative words** contributing to sentiment prediction.

---

## ✨ Features

- **Data loading from ZIP** (IMDB dataset)
- **Exploratory data analysis**:
  - Class distribution plots
  - Data samples & structure
- **Text preprocessing**:
  - Lowercasing
  - Removing punctuation, numbers, and special characters
  - Stopword removal
  - Lemmatization
- **Model training & evaluation**:
  - Logistic Regression
  - Naive Bayes
- **Visualization**:
  - Confusion matrices for both models
  - Top positive & negative words for each model

---

## ⚙ Requirements

### 📌 Install dependencies:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn nltk
```

### 📌 Download NLTK resources (first-time setup):
```python
import nltk
nltk.download('stopwords')
nltk.download('wordnet')
nltk.download('omw-1.4')
```

---

## 🚀 Usage

### 1️⃣ Prepare your dataset
- Download the **IMDB Dataset** from Kaggle (CSV format).
- Place the ZIP file in your working directory.

### 2️⃣ Extract the dataset
```python
import zipfile
with zipfile.ZipFile('/content/IMDB Dataset.csv.zip', 'r') as zip_ref:
    zip_ref.extractall('/content')
```

### 3️⃣ Run the script
```bash
python main.py
```

---

## 📊 Outputs

1. **Dataset info & statistics**
2. **Class distribution plot**  
3. **Confusion matrix** for Logistic Regression & Naive Bayes  
4. **Most important positive & negative words** for both models  

---

## 📝 Example Output

```
✅ Dataset loaded successfully!
📊 Logistic Regression Performance:
Accuracy: 0.8925
📊 Naive Bayes Performance:
Accuracy: 0.8573
```

Visualizations generated:
- Sentiment distribution bar chart
- Confusion matrices for both models
- Positive/negative word importance bar plots

---

## 💡 Notes
- **TF-IDF** is limited to `MAX_FEATURES=5000` to optimize performance.
- Stopwords are removed during preprocessing.
- Works for any binary sentiment dataset with `review` and `sentiment` columns.

---

## 📄 License
This project is licensed under the MIT License.
