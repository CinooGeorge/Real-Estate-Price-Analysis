# Real-Estate-Price-Analysis
# 🏡 Real Estate Price Analysis – Palm Beach County (2023)

## 📌 Project Overview
This project investigates factors influencing the difference between **list and sold prices** in Palm Beach real estate.  
By analyzing property attributes, market conditions, and regional trends, we uncover **actionable insights** to refine pricing strategies, optimize sales, and improve transaction outcomes.

The analysis leverages **data analytics and machine learning** to identify key drivers of price discrepancies, helping **realtors, investors, and buyers** make data-driven decisions.

---

## 👥 Authors
- **Sara Martin**
- **Cinoo Bosco Thomas**

---

## 📂 Dataset
- **Source:** Provided by course instructor  
- **Size:** 6,600 rows × 81 columns  
- **Filtered:** 3,400 closed sales (rented properties excluded)  
- **Target Variable:** `Price_Difference = LIST PRICE - SOLD PRICE`  

### Key Features:
- **BEDS** – Number of bedrooms  
- **FBATHS** – Number of bathrooms  
- **TOT_SQFT** – Total square footage  
- **LOT_SIZE** – Lot size  
- **YEAR_BUILT** – Year the property was built  
- **POOL** – Pool availability (binary encoded)  
- **ZIP_CODE** – Property location  

---

## 🔍 Data Preparation
1. Removed rented properties to focus on sold homes  
2. Cleaned missing values in critical columns  
3. Encoded categorical features (e.g., Pool availability)  
4. Standardized ZIP codes for location-based analysis  
5. Created the target variable `Price_Difference`  

---

## 📊 Exploratory Data Analysis (EDA)
- **Descriptive statistics** revealed wide price variability with a **right-skewed distribution**.
- **Market trends** identified cities with the highest/lowest average price differences.  
- **Correlation analysis** showed:
  - `TOT_SQFT` and `SOLD_PRICE` strongly correlated (0.79)  
  - `YEAR_BUILT` negatively correlated with price differences (-0.30)  
  - `POOL` had minimal impact (0.05)  

---

## 🤖 Models Used
| Model                  | RMSE      | R² Score  |
|------------------------|-----------|-----------|
| **Linear Regression**  | 103,883   | 0.121     |
| **Random Forest**      | 95,136    | 0.263     |

✅ **Random Forest Regressor** performed better, capturing more complex relationships in the data.

---

## 🔑 Feature Importance (Random Forest)
1. **Total Square Footage (TOT_SQFT)** – 40.4%  
2. **Year Built (YEAR_BUILT)** – 23.6%  
3. **Zip Code (ZIP_CODE)** – 13.3%  
4. **Lot Size (LOT_SIZE)** – 9.8%  
5. **Full Bathrooms (FBATHS)** – 9.7%  
6. **Bedrooms (BEDS)** – 2.2%  
7. **Pool Availability (POOL)** – 0.9%  

---

## 📌 Key Findings
- **Larger homes** with more square footage and modern construction have smaller price differences.  
- **Location (ZIP_CODE)** plays a significant role in determining property prices.  
- **Pools** have minimal effect on price differences in this dataset.  
- **Luxury markets** (e.g., Manalapan, Palm Beach) experience larger negative differences due to overpricing or negotiation leverage.

---

## ✅ Recommendations
- **For Sellers:** Use accurate pricing, highlight property size, and invest in modern upgrades.  
- **For Buyers:** Negotiate in luxury markets, consider older properties for better deals.  
- **For Future Research:** Include external factors (amenities, school districts, crime rates) and test advanced ML models for better prediction accuracy.

---

## 🛠️ Technologies Used
- **Python** (Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn)
- **Machine Learning Models:** Linear Regression, Random Forest Regressor
- **Data Visualization:** Heatmaps, Bar Charts, Line Plots

---

## 📈 Visuals
The project includes:
- Correlation heatmaps
- Feature importance bar chart
- City-level pricing difference charts
- Model comparison line plots  

---

## 🚀 How to Run
```bash
# Clone the repository
git clone https://github.com/CinooGeorge/Real-Estate-Price-Analysis.git

# Navigate to the project directory
cd Real-Estate-Price-Analysis

# Install required packages
pip install -r requirements.txt

# Run the analysis
python analysis.py
