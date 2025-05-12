# 📊 Data-Driven Insights into Consumer Electronics Adoption & Recommendation Behaviors

This project explores customer recommendation behavior and seasonal trends in the consumer electronics market using structured product data from Best Buy (Databricks). It combines interactive visualizations, statistical modeling, and sentiment analysis to answer two key research questions.

---


## 🧪 Project Goals

1. **Identify factors that influence product recommendation percentage**
2. **Uncover seasonal patterns and forecast product trends**

---

## 📚 Dataset

- **Source**: Best Buy Product Data via Databricks Public Dataset
- **Size**: ~1000 rows × 35+ features
- **Features Used**:
  - Pricing: `initial_price`, `final_price`, `discount_percentage`
  - Feedback: `rating`, `reviews_count`, `questions_count`, `recommend_percentage`
  - Categorical: `root_category`, `esrb_rating`, `availability`
  - Text: `product_description`, `features_summary`, `q_a`

---

## 🧹 Data Preprocessing

- Cleaned prices and converted to floats
- Parsed `release_date` into `year` and `month`
- Created `discount_percentage` and `description_length`
- Handled missing values using median/mode
- Flattened JSON fields like `availability`

---

## 📊 Dashboards & Key Visuals

### ✅ [Dashboard 1 – Recommendation Behavior](./dashboards/recommendation_dashboard_2x2.html)

- Correlation Heatmap
- Rating vs Recommendation %
- Price vs Rating (by category)
- Sentiment-aware Bubble Chart

### ✅ [Dashboard 2 – Seasonal & Forecasting](./dashboards/full_dashboard_q2_split.html)

- Monthly and Yearly Trends in Product Releases
- Yearly Average Price & Rating
- ARIMA Forecasting with Confidence Intervals

---

## 📈 Models Used

| Model              | Purpose                        | Metrics Used            |
|-------------------|--------------------------------|-------------------------|
| OLS Regression     | Predict recommendation %       | R², MSE, p-values       |
| Ridge & Lasso      | Regularized regression models   | R², MSE                 |
| ARIMA              | Forecast product releases       | Confidence Intervals    |
| HuggingFace BART   | Sentiment Analysis (Zero-Shot) | Text classification     |

---

## 🧠 Key Findings

- **Rating is the strongest predictor** of recommendation percentage
- **Review count amplifies trust** but has weaker direct correlation
- **Price doesn't significantly affect recommendations**
- **Product launches peak in April & November**
- **ARIMA shows stable future trendlines**
- **Negative sentiment** in descriptions aligns with low recommendation %

---

## 🚀 Future Work

- Sentiment modeling on customer reviews
- Real-time dashboard using Streamlit
- Product clustering and persona detection
- Vendor comparison for price vs trust trends

---

## 📌 Author

**Sai Hemanth Kilaru**  ,
**Sri Ram THeerdh Manikyala**  
MS Data Science, University of Arizona  






