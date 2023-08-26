# Customer Segmentation

## Project Overview
The project goal is to carry out segmentation of customers using the online transactions history of an ecommerce platform.


The projects contains the following files:
1. ``src/extract.py`` - a python script that contains instructions to connect to Amazon Redshift and to extract online_transactions_cleaned data
2. ``src/clean_data.py`` - a python script that contains instructions to preprocess the data
3. ``src/segment_data`` - a python script that contains instructions to segment the customers based on the preprocessed data
4. ``main.py`` - a python script that contains all instructions to execute all the steps to extract, clean and segment customers using the functions from extract.py, clean_data.py and segment_data.py
5. ``notebooks/1_data_preprocessing.ipynb`` - a note book that contains data exploration and data preprocessing tasks
6. ``notebooks/2_exploratory_data_analysis.ipynb`` - a notebook that contains exploratory data analysis on preprocessed data
7. ``notebooks/3_customer_segmentation_percentile_ranking`` - a notebook that contains customer segmentation using percentile ranking
8. ``notebooks/4_customer_segmentation_kmeans`` - a notebook that contains customer segmentation using Kmeans clustering
9. ``data/online_trans.pkl`` - the preprocessed data loaded as a .pkl file to data folder
10. ``data/customer_rfm.csv`` - the resulting dataframe where recency, frequency, and monetary value metrics are calculated per customer
11. ``data/customer_segments`` - the resulting dataframe that contains customer segments and campaign strategy
12. ``.env.example`` - a text document that contains the list of environment variables used in .env file
13. ``.gitignore`` - a text document that specifies intentionally untracked files that Git should ignore
14. ``requirements.txt`` - a text document that contains all the libraries required to execute the code

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
3. Alternatively, run the Jupyter notebooks in this order:
    - 1_data_preprocessing.ipynb
    - 2_exploratory_data_analysis.ipynb
    - 3_customer_segmentation_percentile_ranking
    - 4_customer_segmentation_kmeans