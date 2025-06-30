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

snap_4 :
![image](https://github.com/user-attachments/assets/18900d62-ee8f-4fc2-9b59-805ec36d0318)

Step 6 : Write a Data query for Average Pizzas Per Order

5 .Average Pizzas Per Order SELECT CAST(CAST(SUM(quantity) AS DECIMAL(10,2)) / CAST(COUNT(DISTINCT order_id) AS DECIMAL(10,2)) AS DECIMAL(10,2)) AS Avg_Pizzas_per_order FROM pizza_sales

snap 5:

![image](https://github.com/user-attachments/assets/52b3a543-367c-44b9-a496-adf99e5098e9)


B. Daily Trend for Total Orders

Step 7 : Data query for Daily Trend for Total Orders
SELECT DATENAME(DW, order_date) AS order_day, COUNT(DISTINCT order_id) AS total_orders FROM pizza_sales GROUP BY DATENAME(DW, order_date)

snap 6 :

![image](https://github.com/user-attachments/assets/8e1b6b13-7044-4634-b1ce-ec7e35dec0c7)


Step 8 : Data query for Monthly Trend for Orders

select DATENAME(MONTH, order_date) as Month_Name, COUNT(DISTINCT order_id) as Total_Orders from pizza_sales GROUP BY DATENAME(MONTH, order_date)

snap 7 : 


![image](https://github.com/user-attachments/assets/cbf02908-50c2-40cf-b4ca-8dea9ff2ba37)


Step 9 : Data query for Pizza Category

% of Sales by Pizza Category

snap 8 :

![image](https://github.com/user-attachments/assets/1bd0b5ea-2bc6-40aa-a574-6cea865eadb2)

Step 10 : % of Sales by Pizza Size


SELECT pizza_size, CAST(SUM(total_price) AS DECIMAL(10,2)) as total_revenue, CAST(SUM(total_price) * 100 / (SELECT SUM(total_price) from pizza_sales) AS DECIMAL(10,2)) AS PCT FROM pizza_sales GROUP BY pizza_size ORDER BY pizza_size

snap 9 :
![image](https://github.com/user-attachments/assets/36233d14-227b-427d-baf1-7f3730f24b75)

Step 11 : Total Pizzas Sold by Pizza Category

SELECT pizza_category, SUM(quantity) as Total_Quantity_Sold FROM pizza_sales WHERE MONTH(order_date) = 2 GROUP BY pizza_category ORDER BY Total_Quantity_Sold DESC

snap 10 :

![image](https://github.com/user-attachments/assets/2a3e17d6-73e2-4b80-a38a-d22232d894ee)

Step 12 : Top 5 Pizzas by Revenue

SELECT Top 5 pizza_name, SUM(total_price) AS Total_Revenue FROM pizza_sales GROUP BY pizza_name ORDER BY Total_Revenue DESC

snap 11 :

![image](https://github.com/user-attachments/assets/06d8e44f-85b0-47c4-9e5f-a5b247ba3ae6)

Step 13 : Bottom 5 Pizzas by Revenue

SELECT Top 5 pizza_name, SUM(total_price) AS Total_Revenue FROM pizza_sales GROUP BY pizza_name ORDER BY Total_Revenue ASC

snap 12 :


















