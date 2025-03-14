# Group 4
# Crowdfunding_ETL

### Group Members:
* Sofonias Abebe
* Jennifer Andrews
* Oliver von Mizener
* Lisa Tafoya 

In this ETL mini project, we worked in our group to practice building an ETL pipeline using Python, Pandas, and Python dictionary methods to extract and transform the data. After we transformed the data, we created four CSV files and used the CSV file data to create an ERD and a table schema. Finally, we uploaded the CSV file data into a Postgres database.

The instructions for this mini project are divided into the following subsections:
* Create the Category and Subcategory DataFrames
* Create the Campaign DataFrame
* Create the Contacts DataFrame
* Create the Crowdfunding Database

### Create the Category and Subcategory DataFrames

For this section, we performed the following tasks: 

1. Extracted and transformed the crowdfunding.xlsx Excel data to create a category DataFrame that has the following columns:
* A "category_id" column that has entries going sequentially from "cat1" to "catn", where n is the number of unique categories
* A "category" column that contains only the category titles
2. Exported the category DataFrame as category.csv and saved it to our GitHub repository.

3. Extracted and transformed the crowdfunding.xlsx Excel data to create a subcategory DataFrame that has the following columns:
* A "subcategory_id" column that has entries going sequentially from "subcat1" to "subcatn", where n is the number of unique subcategories
* A "subcategory" column that contains only the subcategory titles

4. Exported the subcategory DataFrame as subcategory.csv and saved it to our GitHub repository.

### Create the Campaign DataFrame

The following tasks were performed for this section of the project:

1. Extracted and transformed the crowdfunding.xlsx Excel data to create a campaign DataFrame has the following columns:
* The "cf_id" column
* The "contact_id" column
* The "company_name" column
* The "blurb" column, renamed to "description"
* The "goal" column, converted to the float data type
* The "pledged" column, converted to the float data type
* The "outcome" column
* The "backers_count" column
* The "country" column
* The "currency" column
* The "launched_at" column, renamed to "launch_date" and with the UTC times converted to the datetime format
* The "deadline" column, renamed to "end_date" and with the UTC times converted to the datetime format
* The "category_id" column, with unique identification numbers matching those in the "category_id" column of the category DataFrame
* The "subcategory_id" column, with the unique identification numbers matching those in the "subcategory_id" column of the subcategory DataFrame

2. Exported the campaign DataFrame as campaign.csv and saved it to our GitHub repository.

### Create the Contacts DataFrame

For this section, we performed the following tasks: 
We used Python dictionary methods for extracting and transforming the data from the contacts.xlsx Excel data. To be specific, we followed the following steps:
* Imported the contacts.xlsx file into a DataFrame.
* Iterated through the DataFrame, converting each row to a dictionary.
* Iterated through each dictionary, doing the following:
    * Extracted the dictionary values from the keys by using a Python list comprehension.
        * Added the values for each row to a new list.
        * Created a new DataFrame that contains the extracted data.
        * Split each "name" column value into a first and last name, and placed each in a new column.
        * Cleaned and exported the DataFrame as contacts.csv and saved it to our GitHub repository.

        ### Create the Crowdfunding Database

        In this section:

        1. We inspected the four CSV files, and then sketched an ERD of the tables by using QuickDBD.
        2. We used the information from the ERD to create a table schema for each CSV file.
        3. We saved the database schema as a Postgres file named crowdfunding_db_schema.sql, and saved it to our GitHub repository.
        4. Created a new Postgres database, named crowdfunding_db.
        5. Using the database schema, we created the tables in the correct order to handle the foreign keys.
        6. Verified the table creation by running a SELECT statement for each table.
        7. Imported each CSV file into its corresponding SQL table.
        8. We finally verified that each table has the correct data by running a SELECT statement for each.


        ### References
        *Data for this dataset was generated by edX Boot Camps LLC, and is intended for educational purposes only.*
