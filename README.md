# 🛒 Amazon Sales Analysis – EDA

## 🔍 Project Overview
This project focuses on performing Exploratory Data Analysis (EDA) on Amazon India product data to uncover insights related to discounts, ratings, product categories, and customer behavior.

The analysis explores how pricing strategies and product categories influence customer ratings and marketplace trends.

---

## 📁 Dataset Information
- Source: Kaggle – amazon.csv  
- Total Products: 1,465  
- Unique Categories: 211  

### Key Features Used
- product_id  
- product_name  
- category  
- discounted_price  
- actual_price  
- discount_percentage  
- rating  
- rating_count  

### Engineered Features
- main_cat (main category extracted from hierarchical category structure)

- Dataset Type: Mixed (Numerical + Text/Categorical)  
- Nature: Real-world e-commerce dataset  

---

## 🧹 Data Cleaning & Preprocessing

### 💰 Price Column Cleaning
Columns:
```python
discounted_price
actual_price
```

contained:
- ₹ symbols  
- commas  

These were cleaned using:
```python
.str.replace()
```

and converted into float datatype.

### 📉 Discount Percentage Cleaning
Converted:
```python
"64%"
```

into numeric integer format.

### ⭐ Rating Column Fix
- One invalid rating value containing:
```python
"|"
```

was replaced and converted into numeric format.

### 📊 Rating Count Cleaning
- Removed commas from values like:
```python
"24,269"
```

- Filled 2 null values using:
```python
fillna(0)
```

### 🗂️ Category Parsing
The category column used hierarchical pipe-separated categories:
```python
Electronics|Accessories|Headphones
```

Extracted main category using:
```python
split('|')[0]
```

---

## 📊 Exploratory Data Analysis

### 🔹 Univariate Analysis
- Discount distribution  
- Rating distribution  
- Product category frequency  

### 🔹 Bivariate Analysis
- Price vs Rating  
- Category vs Average Discount  
- Category vs Average Rating  

### 🔹 Correlation Analysis
- Relationship between pricing and customer ratings  

---

## 📌 Key Insights

### 💰 Discount Analysis
- Average discount:
```python
47.7%
```

- Nearly half of all products were discounted above 50%.

➡️ Amazon India operates as a highly discount-driven marketplace.

### ⭐ Rating Distribution
- Average rating:
```python
4.09★
```

- Most products were rated between:
```python
4.0 – 5.0★
```

➡️ Low-rated products are relatively rare.

### 🔗 Price vs Rating Correlation
Correlation:
```python
r = 0.114
```

➡️ Product price has very weak impact on customer ratings.

### 🗂️ Category Insights
Top categories:
- Electronics  
- Computers & Accessories  
- Home & Kitchen  

Electronics showed the heaviest discounting patterns.

---

## 💡 Key Learnings

- String-to-numeric conversion is one of the biggest real-world data cleaning tasks  
- Hierarchical categories require parsing before analysis  
- Correlation does not always indicate strong business relationships  
- Customer review systems can introduce rating bias  
- EDA helps reveal hidden marketplace and pricing strategies  

---

## 🛠️ Tools & Technologies Used
- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Plotly  

Examples:
- Discount Distribution Histogram  
- Rating Distribution  
- Category-wise Discount Analysis  
- Correlation Heatmap  
- Category Frequency Charts  

---

## 🚀 How to Run the Project

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/your-username/amazon-sales-eda.git
```

### 2️⃣ Install Required Libraries
```bash
pip install pandas numpy matplotlib seaborn plotly
```

### 3️⃣ Run Jupyter Notebook
```bash
jupyter notebook
```

---

## 📌 Project Status
✅ Completed  
🔄 Open for improvements and feedback  

---

## 🤝 Connect With Me
I’m currently learning Data Analytics and building real-world projects.


## ⭐ If You Found This Useful
Give this repository a star ⭐ and share your feedback!
