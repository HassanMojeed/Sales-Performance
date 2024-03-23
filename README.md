Python script by [__Hassan Mojeed__](https://linktr.ee/mhola)<br>
Email: mojeed.o.hassan@gmail.com<br>
[Linkedin Profile](https://www.linkedin.com/in/hassanmojeed/)



## View Dashbaord [here](https://app.powerbi.com/view?r=eyJrIjoiOTBiODkwYTYtMjk2MC00MzMzLWJkOGYtZWQzNGFiNTdjODZkIiwidCI6ImFlM2E5OTA2LTc4MWEtNDQ2YS1iZGI2LTYzNzdjMDllMmM2ZiIsImMiOjF9&pageName=ReportSectioneed2047ccf3ea2f7d6e8)

# Sales-Performance
Jumia Sales Performance


#### Introduction:
The Python code will extract, clean, and load sales data from Jumia Nigeria's sales department into a Microsoft SQL Server database. It will utilize various libraries and handle data processing tasks for sales data from March 2018.

#### Aim:
The objective is to analyze the sales performance of the Jumia Nigeria sales team for the specified period. This will involve extracting  relevant sales data, ensuring consistency and accuracy through cleaning, and finally loading it into an MSSQL Server database for further analysis.

#### Data Source:
Excel files stored in a directory named "Jumia" will serve as the data source. The code will locate these files using the glob function within the specified directory.

#### Data Extraction:
Using pd.read_excel(), the code will read data from the second Excel file found in the "Jumia" directory into a Pandas DataFrame.

#### Data Cleaning and Manipulation:

Column Removal: Unnecessary columns will be dropped from the DataFrame.<br><br>
Column Renaming: Columns will be renamed for clarity and consistency.<br><br>
Handling Missing Values: Missing values in specific columns ('Level', 'Region', and 'sub_category') will be filled with 'Unknown', and conditional replacements will be made based on certain criteria.<br><br>
Value Replacements: Various columns such as 'Region', 'category', 'sub_category', 'brand', and 'item_status' will undergo value replacements to ensure consistency and accuracy.<br><br>
Custom Function Application: The custom function replace_col1_with_col2 will be applied to perform specific replacements in the 'category' column.<br><br>
New Column Creation: A new column named 'final_delivered_date' will be created based on certain conditions, and additional columns will be created to calculate achieved, shipped, and delivered revenues.<br><br>
Data Type Conversion: Certain columns will be converted to appropriate data types.<br><br>
Date Formatting: Date-related columns will be formatted to the desired format.<br>

#### Data Export:
After processing, the DataFrame will be exported to an MSSQL database named 'JumiaDB_Project' and stored in a table named 'Sales_data'. The code will establish a connection to the database using PyODBC and SQLAlchemy, and then export the DataFrame to the specified table. A success message will be printed upon successful export.


