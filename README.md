# ETL_project_python_SQL
![ETL](https://github.com/Meetshah05-lab/ETL_project_python_SQL/assets/154343141/a7ae94a7-953f-4422-b90d-a3cf0a68f6d9)


Steps:
Import Libraries: Import necessary libraries including kaggle for downloading datasets.

Download Dataset: Use the kaggle library to download the dataset named orders.csv from the Kaggle dataset named retail-orders by running the command kaggle datasets download ankitbansal06/retail-orders -f orders.csv.
Extract Data from Zip File: Extract the contents of the downloaded zip file (orders.csv.zip) to the current directory.

Read Data and Handle Null Values:
Read the data from the orders.csv file into a Pandas DataFrame.
Handle null values by specifying ['Not Available','unknown'] as NaN values while reading the CSV file.

Rename Columns:
Rename columns to lowercase and replace spaces with underscores to ensure consistency and ease of access.

Derive New Columns:
Calculate additional columns like profit by subtracting cost_price from sale_price.

Convert Data Types:
Convert the 'order_date' column from object data type to datetime format using pd.to_datetime().

Drop Unnecessary Columns:
Remove unnecessary columns such as list_price, cost_price, and discount_percent from the DataFrame.

Load Data into SQL Server:
Connect to the SQL Server using SQLAlchemy.
Load the DataFrame into SQL Server with the name df_orders using the replace option.

Append Data into SQL Server:
Alternatively, load the DataFrame into SQL Server with the name df_orders using the append option to add data to an existing table.
