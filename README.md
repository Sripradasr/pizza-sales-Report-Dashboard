# pizza-sales-Report-Dashboard
Dashboard Link :
(https://github.com/Sripradasr/pizza-sales-Report-Dashboard/blob/main/pizza%20sales%20Dashboard%20home.png)
(https://github.com/Sripradasr/pizza-sales-Report-Dashboard/blob/main/pizza%20sales%20Dashboard.png)
 
 Problem Statement
 This dashboard helps the Pizza Sales understand their customers better. It helps the Sales Report know if their customers are satisfied with their services. Through different ratings, they get to know their improvement area, & thus they can improve their services by identifying these area. It also lets them know the Average Order Values, Total Revenue, Total Pizza Sold, Total orders and Average Pizza Per Orders, thus since by using this dashboard they have identified this report, they can further work on factors responsible for the Sales.
 
Since, number of Total Revenue($817.9k),Average Order Values(38.31),Total Pizza Sold(50K), Total orders(21k), Average Pizza For order(2.32)

Steps followed
Step 1 : Create a New Database, Load data into Database, dataset is a csv file.

Step 2 : Create a Table and write a Data query for Total Revenue

for Total Revenue following query was written
1 . Total Revenue: SELECT SUM(total_price) AS Total_Revenue FROM pizza_sales;
