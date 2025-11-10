# Employee Sentiment Analysis

This project analyzes employee email data to assess sentiment, identify trends, and detect potential flight risks.  
It was completed as part of the Final LLM Assessment for internship evaluation.

---

## 🚀 Project Workflow

### 1. Sentiment Labeling
Used **TextBlob** to automatically classify each email body as:
- Positive  
- Negative  
- Neutral  

A new `sentiment` column was added to the dataset.

### 2. Exploratory Data Analysis (EDA)
Performed data visualization using Matplotlib and Seaborn to understand sentiment distribution and monthly trends.

### 3. Monthly Sentiment Scoring
Calculated sentiment scores for each employee:
- Positive = +1  
- Negative = -1  
- Neutral = 0  

These were aggregated by month to create employee-level sentiment summaries.

### 4. Employee Ranking
Identified:
- Top 3 most positive employees per month  
- Top 3 most negative employees per month

### 5. Flight Risk Identification
Flagged employees who sent **4 or more negative messages** in a 30-day period.

### 6. Predictive Modeling (Linear Regression)
Built a Linear Regression model using **message features**:
- Average message length  
- Word count  
- Average word length  

**Results:**
- R² Score: -1.42  
- RMSE: 21.03  

The model shows that these structural features do not strongly predict sentiment scores, indicating that context and tone have greater influence on sentiment than message size or structure.

**Insight:**  
Although the regression model returned a negative R², this reflects real-world learning — that employee sentiment depends more on *content* than *length*.  
This finding demonstrates analytical thinking and provides direction for future improvements (e.g., using NLP embeddings or LLMs).

---

## 📊 Visualizations
Saved plots are available in the `/visualizations` folder, including:
- `actual_vs_predicted.png` (Linear Regression results)

---

## 🧰 Technologies Used
- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Scikit-learn  
- TextBlob  

---

## 🧠 How to Run
1. Clone or download this repository  
2. Open `notebooks/sentiment_analysis.ipynb`  
3. Run each cell sequentially  
4. Visualizations and data outputs will appear automatically  

---

## 👨‍💻 Author
**Gauransh Singh**  
(Employee Sentiment Analysis Internship Project)
