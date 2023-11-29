# E-Commerce Shopping Platform

**Project Idea**
Our project idea is to design a shopping platform for E-commerce websites. Specifically, this platform will maintain a shopping cart system where users can add items, keep track of products being sold and their according prices and quanitites, check for specific items in the product inventory, and apply discounts and taxes after the user is finished adding items to their cart.

**Dataset**
To gain data about various products, and their quantities and prices, we decided to use a dataset found on Kaggle that contains sales data collected from a small business that sells women's clothing items. This dataset is a CSV file that has the following columns: InvoiceNo, StockCode, Description, Quantity, InvoiceData, UnitPrice, CustomerID, and Country. For the sake of our program, we kept the Description, Quanity, and UnitPrice columns to have a sample product inventory that a user can choose from. The initial dataset contained 541,910 rows of data, but we shortened it to 500 rows.

The dataset can be found here: https://www.kaggle.com/datasets/shilongzhuang/-women-clothing-ecommerce-sales-data

**Program Description**
This program mimics an E-Commerce platform that is able to read from a dataset containing information about items names, their corresponding prices, and their corresponding quantities.

The DataProcessor class is designed for efficient handling and preprocessing of tabular data sourced from a CSV file. Upon initialization, the class reads the CSV file into a Pandas DataFrame (self.df). The preprocess_data method allows truncation of the DataFrame to a specified length, removal of designated columns, and elimination of duplicate rows. The class also provides methods for extracting dictionaries: get_price_dictionary generates a dictionary mapping values from a specified description column to corresponding numeric values in a price column after coercion, while get_quantity_dictionary creates a dictionary mapping values from a description column to corresponding values in a quantity column. This class serves as a versatile tool for users to streamline data preprocessing tasks and extract specific information in a dictionary format from tabular datasets.

The ShoppingCart class represents an online shopping cart and supports operations like adding items, removing items, calculating the total cost, applying discounts, adding tax, and sorting items by price. The cart utilizes dictionaries to keep track of item quantities and prices.

The program reads input data from external text files (add_items.txt and remove_items.txt) to simulate the addition and removal of items from the shopping cart. Make sure that these files, in addition to the dataset, are all in the same directory. After performing these operations, it calculates and displays the total cost, discounted total, and total with tax. Additionally, it implements the merge sort algorithm to sort items in the cart based on their prices.

**Libraries**
We used the Pandas library on Python to conduct data cleaning on our dataset as well as convert the columns into dictionaries that store information about the products. If running the program on VS Code or any other IDE other than a Jupyter Notebook, install Pandas.

**Expectations & Weaknesses**
We expect that our software successfully responds to the user's commands to add items to the cart if the item exists in the product inventory, or remove items from the cart if the item exists in the cart. Moreover, we expect the cart to display the product's prices, any applied discounts, taxes, and the grand total correctly in ascending order of price.

Currently, this software is limited to specific catalog of products. Future improvements can be made to make it more dynamic and work on various datasets.
