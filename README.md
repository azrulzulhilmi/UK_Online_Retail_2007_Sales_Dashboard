# Association Rule: Market Basket Analysis Dashboard

## 📊 Project Overview

This project presents an interactive **Shiny dashboard** that performs **Market Basket Analysis** using **Association Rule Mining (ARM)** on an e-commerce dataset from a UK-based online novelty store. The goal is to identify product combinations frequently purchased together and extract actionable business insights for strategic decision-making.

## 🖥️ Dashboard Preview

![Dashboard](https://github.com/azrulzulhilmi/UK_Online_Retail_2007_Sales_Dashboard/blob/main/images/UK_Online_Retail_2017_Sales_Dashboard.png)


Dataset Source:  
[Kaggle - E-commerce Business Transaction](https://www.kaggle.com/datasets/gabrielramos87/an-online-shop-business)

---

## 📁 Dataset Description

- **Rows**: 536,350
- **Columns**: 8  
- **Key Features**:
  - `TransactionNo`: Unique identifier for each transaction
  - `ProductName`: Name of the purchased product
  - `Quantity`, `Price`: Units sold and product price
  - `Date`: Transaction date
  - `CustomerNo`, `Country`: Customer metadata

The dataset contains UK online retail transaction records for 2007, focused on gifts, homewares, and novelty items.

---

## 🎯 Objectives

1. Discover associations between items purchased together.
2. Generate rules with high support, confidence, and lift values.
3. Provide insights for:
   - Product bundling
   - Cross-selling strategies
   - Personalized recommendations

---

## 🔧 Technologies Used

- **R** (Shiny, arules, arulesViz, ggplot2, dplyr, tidyverse)
- **Shiny Dashboard** for UI/UX
- **Apriori Algorithm** for rule generation

---

## 🧹 Data Cleaning & Preparation

Steps included:
- Removing cancelled orders (identified by "C" in `TransactionNo`)
- Removing rows with missing data using `na.omit()`
- Standardizing `ProductName` to lowercase
- De-duplicating transactions
- Converting long format to basket format

---

## 📈 Dashboard Features

### 🔍 Sidebar Panel:
- Introduction and dataset summary
- Adjustable sliders:
  - **Support threshold**
  - **Confidence threshold**
- Rule sorting by **lift**
- Display:
  - Total rules generated
  - Top 10 rules (text output)

### 📊 Main Panel:
- **Scatterplot** of all rules (support vs. confidence, shaded by lift)
- **Graph visualization** of top 10 rules
- Creator credits

---

## 📌 Insights

- Products like *"herb marker rosemary"*, *"herb marker thyme"*, and *"herb marker parsley"* show **very high lift values**, indicating strong co-purchase behavior.
- Several **Jumbo bag** variants are commonly bought together, revealing bundling potential.
- Rules with high lift but low support can be used for **targeted promotions**.

---

## 📉 Challenges

- Large dataset size (536k+ rows) affecting performance
- Missing values and inconsistent data entries (e.g., cancelled transactions)
- Limited customer metadata (no age, gender, etc.)
- Product categories not explicitly defined

---

## 👨‍💻 Authors

- Azrul Zulhilmi bin Ahmad Rosli (P153478)

---

## 📚 References

- Agrawal, R., & Srikant, R. (1994). *Fast Algorithm for Mining Association Rules*
- Hahsler et al. (2005). *arules - An R Package for Association Rule Mining*
- Kaggle Dataset: [https://tinyurl.com/3sus65v9](https://tinyurl.com/3sus65v9)

---

## 🚀 How to Run the App

1. Install required R packages:
   ```r
   install.packages(c("shiny", "arules", "arulesViz", "tidyverse", "ggplot2", "dplyr", "plyr", "stringr", "RColorBrewer"))
