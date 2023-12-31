# Customer Segmentation

## Project Overview
The project goal is to carry out segmentation of customers using the online transactions history of an ecommerce platform.
The project consists of 4 python scripts that extract (src/extract.py), preprocess (src/clean_data.py), segment the customers using the preprocessed data (src/segment_data.py), and execute all these steps (main.py).
It also consists of 4 Jupyter notebooks that demonstrate coding workflows for the data exploration, data preprocessing, exploratory analysis, and customer segmentation. 


## Project Scope
- Data Exploration (SQL)
- Data Preprocessing (Python)
- Exploratory Data Analysis (Python - seaborn and matplotlib)
- Customer Segmentation and Analysis (Python - seaborn and matplotlib, yellowbrick, sklearn)

## Dataset Overview
The dataset is the output of the [ETL Pipeline project](https://github.com/DSKunth/ETL-Pipeline) where the raw online transactions data was extracted from Amazon Redshift warehouse, transformed and loaded to S3 cloud object.
It contains 399841 transaction records from 01/12/2010 to 09/12/2011. The data has 9 attributes:
- invoice
- stock_code
- description
- price
- quantity
- total_order_value
- invoice_date
- customer_id
- country

## How to Run Customer Segmentation 
### Requirements:
- Python 3+
- Python IDE or Text Editor and Command Line Interface
- Jupyter notebook

### Instructions:
1. Copy the ``.env.example`` file to `.env` and fill out the environment variables.
2. Install the requirements
    ```
   pip3 install -r requirements.txt
   ```
3. Run the main.py script
   - For Windows:
   ```
   python main.py
   ```
   - For Mac:
   ```
   python3 main.py
   ```
4. Alternatively, run the Jupyter notebooks in this order:
    - 1_data_preprocessing.ipynb
    - 2_exploratory_data_analysis.ipynb
    - 3_customer_segmentation_percentile_ranking.ipynb
    - 4_customer_segmentation_kmeans.ipynb

### View [Executive Dashboard](https://public.tableau.com/app/profile/dorothy.kunth/viz/ExecutiveDashboard_16934981219780/ExecutiveDashboard) in Tableau