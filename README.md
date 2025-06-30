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
Snap_1 :
![image](https://github.com/user-attachments/assets/2fabcdf1-a8fe-4f06-8e0c-5dc464f08887)

Step 3 : Create a Table and write a Data query for Average Order Value

2 . Average Order Value SELECT (SUM(total_price) / COUNT(DISTINCT order_id)) AS Avg_order_Value FROM pizza_sales

Snap_2 :
![image](https://github.com/user-attachments/assets/cc374ff8-df89-45af-bb61-d5a3107641c4)


Step 4 :Create a Table and write a Data query for Total Pizzas Sold

3 . Total Pizzas Sold SELECT SUM(quantity) AS Total_pizza_sold FROM pizza_sales

Snap_3 :![image](https://github.com/user-attachments/assets/76e7f1fd-536e-4dc6-b135-b57c04d40c73)

Step 5 :Write a Data query for Total orders

4 .Total Orders SELECT COUNT(DISTINCT order_id) AS Total_Orders FROM pizza_sales
snap_4








