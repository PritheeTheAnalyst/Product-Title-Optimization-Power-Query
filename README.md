## 📌 Introduction

This project focuses on generating a shorter, optimized version of product titles from a dataset. The original Title column contains detailed product information, which can be lengthy and inconsistent.

The goal is to create a short_title feature that improves readability and supports better SEO while retaining essential product information.

## Dataset Image
<img width="1920" height="960" alt="Screenshot (487)" src="https://github.com/user-attachments/assets/e9b18820-0860-40a6-8aa5-2abd8c58bb6a" />


## 🧼 Data Cleaning

During the data cleaning process, several data quality issues were identified:

- Inconsistent formatting and special characters
- Mixture of digits and letters
- Missing values across multiple records
- Presence of unnecessary filler words

## 🔧 Cleaning Steps
To address these issues, the following steps were performed using Power Query:

1. Removed filler words and redundant text
2. Eliminated unnecessary spaces, symbols, and punctuation
3. Standardized text using trimming functions
4. Applied formatting functions to ensure consistency
5. Handled missing values and errors
   
## ✂️ Short Title Creation
A new feature, short_title, was engineered to produce concise and structured product titles.

## ⚙️ Methodology
Duplicated the original Title column
Applied Power Query transformations:
- Column splitting
- Split by position to extract the last characters
- Extracted last 8 characters (e.g., size or quantity)
- Removed fillers, punctuation, and applied trimming
- Created custom columns for transformation
- Combined columns using text functions
- Removed duplicate words using List.Distinct
- Ensured final title length falls between 30–50 characters

## 📊 Clean Dataset Overview
### 🧮 Key Formulas Used

1. Limit title length:

Text.Start([Title], 40)

2. Combine and remove duplicate words:

Text.Combine(
    List.Distinct(
        Text.Split([Column1] & " " & [Column2], " ")
    ),
" ")

## 🚀 Impact
1. Improved readability of product titles
2. Reduced redundancy and inconsistency
3. Created a structured feature for analysis and SEO
4. Enhanced overall data quality for downstream tasks

## 🛠️ Tools Used
Power Query (Excel)
Text functions 

## 💡 Key Takeaway
This project demonstrates how data cleaning and feature engineering can transform raw text data into structured, usable insights, improving both analytical efficiency and user experience.

