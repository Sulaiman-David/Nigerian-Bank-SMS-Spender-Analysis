# Nigerian-Bank-SMS-Spender-Analysis

Overview
This project simulates, parses, cleans, and analyzes Nigerian bank debit SMS alerts.
The goal is to transform unstructured SMS text into structured financial data, allowing you to compute spending insights such as:
Categorized spending (Food, Transport, Groceries, etc.)
Total amount spent
Vendor-level analysis
Daily/weekly/monthly spending behavior
Visualizations of spending distribution

The dataset is synthetically generated but modeled after real SMS formats used by major Nigerian banks (GTBank, Access Bank, Zenith Bank, UBA, FCMB, etc.).
This makes the project excellent for data cleaning, regex extraction, feature engineering, and exploratory data analysis.





Features
This project includes:

1. Synthetic Data Generation
Creates hundreds of realistic SMS alerts with:
Vendor names
Debit amounts
Randomized timestamps
Multiple SMS formats (GTB-style, Access/Zenith-style)
Extra “noise messages” to simulate real inbox conditions


2. Data Cleaning & Parsing
Using Python and regex, the notebook extracts:
Debit amount
Vendor name
Transaction category
Transaction date
and removes irrelevant messages.


3. Categorization Logic
Vendors are mapped to spending categories using keyword-based rules.


4. Exploratory Data Analysis
Includes:
Total spending by category
Vendor frequency
Spending distribution plots
Bar charts, pie charts, and trend charts


5. Fully Modular Code
Every part of the pipeline—generation, cleaning, extraction, categorization, visualization—is reusable and easy to expand.

Project Structure
Bank-SMS-Spender/

bank_sms_analysis.ipynb       # Main notebook
nigerian_bank_sms_logs.csv    # Generated synthetic dataset
README.md                     # Project documentation
images/                       # (Optional) Saved charts



Tools & Libraries
This project uses:
Python 3.x
pandas
numpy
re (regex)
matplotlib
seaborn
datetime

All dependencies are standard.


How It Works
STEP 1 – Generate Dataset
The script:
Picks a random vendor
Picks a suitable amount
Creates a random date
Selects one of two SMS “formats”
Appends to dataframe
Adds noise messages
Saves the final CSV

STEP 2 – Extract Clean Fields
Regex is used to extract:
Amount
Vendor
Date
Non-transactional messages are removed.

STEP 3 – Categorize Spending
A custom function determines the spending category based on vendor keywords.


STEP 4 – Visualize Spending
A horizontal bar chart shows total spending by category.
You can add more visualizations later (e.g., monthly trends, vendor rankings).

Use Cases
This project is ideal for:
Data cleaning exercises
Regular expression practice
Building a portfolio-ready data science project
Financial analytics prototypes
Personal finance automation demos



How to Run (Jupyter Notebook)

Launch Jupyter Notebook
Open bank_sms_analysis.ipynb
Run the cells sequentially

The notebook will:
Generate the dataset
Parse and clean the data
Produce final structured data
Output visualizations



Next Steps (Future Enhancements)
Add real machine learning classification for vendor categorization
Build a dashboard using Plotly/Dash or Power BI
Detect potential fraud or unusual spending
Integrate with an SMS API (Twilio, Termii, etc.)
Build a personal finance recommender


