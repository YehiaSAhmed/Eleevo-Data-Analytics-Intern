The dataset used in this task is acquired from [kaggle](https://www.kaggle.com/datasets/rohitsahoo/sales-forecasting)


The excel file contains 4 sheets, the first one contains the original dataset (), the second contains the data results from preprocessing, the last two sheets contains the required in the task.

Data Cleaning:


data type of The original data set: it contained 8 categorical columns, 2 date columns, an ID column, 3 other ID columns , 2 numerical columns (one of them is sales, which is the core of the dataset), 2 text columns.

No ducplicates in the used dataset is found.

Performed Data cleaning on this dataset, the resulted data is have 10 columns out of 18 in the original.

The cleaned dataset contains 10 columns: ID columns, 3 numerical columns (two of them is a transformed values from the two data columns mentioned above, order ID column, 5 categorical columns).


The removed columns are: country column (as the data only cares about US), City (as we want to see the big picture and the trend in the whole state), Subcategory (as this will lead to more sophisticated analysis and the important one is the category not the subcatogery), Product Name, Postal code, Product ID ,Order and Ship Dates columns , Customer Name and Customer ID columns (as the customer could be known from the order ID).

Key metrics Sheet contains the number of the units sold and the total revenue and the montly trends (All of these are made by pivot tables) and Both YoY and MoM changes, that all of them have slicers that filter these metrics upon these slicers.

Overall Performance Sheet contains a map that shows the distribution of the overall sales done by each state in the US made from a pivot table but it is inserted in a seperate table to easily get this map as it require a static data, and two pie charts that made by pivot tables that checks the percentage of each category in the catogrical features/columns (segment, ship mode) and also these two are controled by slicers that fileter them and also filters the pivot chart that shows each state percentage from the sales.


Data Set Summary:
Data Source: [Kaggle - Sales Forecasting](https://www.kaggle.com/datasets/rohitsahoo/sales-forecasting)
Columns Count: 18
Rows Count: 9800
Duplicates: None (Verified using remove duplicates button in data tab in the menu bar)
Blank cells: 11 (All of them is in Postal Code column, checked by countblank formula)
