## Project Based Internship Bank Muamalat : Sales Analysis PT Sejahtera Bersama

### Preview Dataset 
- In this project, the dataset is about sales data in PT Sejahtera Bersama which contains 4 table (Customer, Products, Orders and ProductCategory).
- Link dataset : [https://drive.google.com/file/d/1RwsBQ1FriNfz6qiq0V5nD7gF7jO81To3/view?usp=sharing]
- This is name of column for each table :
    a. Customers
        - CustomerID      - CustomerAddress
        - FirstName       - CustomerCity
        - LastName        - CustomerState
        - CustomerEmail   - CustomerZip
        - CustomerPhone
    b. Orders
        - OrderID         - ProdNumber
        - Date            - Quantity
        - CustomerID
    c. Products
        - ProdNumber      - Category
        - ProdName        - Price
    d. ProductCategory
       - CategoryID
       - CategoryName
       - CategoryAbbreviation

### Case Study
1. To find primary key of Customer, Products, Orders and ProductCategory table !
2. To find relationship of 4 table !
3. To made master table which contains :
    - CustomerEmail (cust_email)
    - CustomerCity (cust_city)
    - OrderDate (order_date)
    - OrderQty (order_qty)
    - ProductName (product_name)
    - Productprice (product_price)
    - ProductCategoryName (category_name)
    - TotalSales (total_sales)
  Sort by ascending order_date !
4. To made data visualization report !
5. Recommendation for maintain and increase sales 

## Tools
In this project is used :
1. Google Big Query : to made master table
2. Looker Studio : to made data visualization report

## Case Study Answer
1. This is primary key each table 
   - Primary key of Customer table : CustomerID
   - Primary key of Products table : ProdNumber
   - Primary key of Orders table : OrderID
   - Primary key of ProductCategory table : CategoryID

2. This is relationship of 4 table with STAR SCHEMA
![image](https://github.com/gadingkusumaanggraeni/portfoliogadingkusumaanggraeni/assets/150303416/8d9ac623-7f13-486d-9906-56a63459d63e)

3. This is the steps for made master table :
    - From STAR SCHEMA, we know that the primary key of ProductCategory table is CategoryID which refers to   Category column in Products table. So, first step is join 2 table with LEFT JOIN and named product_order.
    - Second step, we know that the primary key of Customer table is CustomerID which referes to CustomerID column in Orders table. So, join 2 column with LEFT JOIN and named customer_order.
    - End step, join product_order table and customer_order table with primary key is product_number.
This is link Google Big Query to made master table : [https://console.cloud.google.com/bigquery?   sq=91576120964:5c5734d0f6734dd3b6b63b14213038af]

4. This is Looker Studio link to know about Product Sales Report in PT Sejahtera Bersama [https://lookerstudio.google.com/reporting/f87de00e-5a48-44e8-9889-5bb30ce91572]
![DASHBOARD_PRODUCT_SALES (2)](https://github.com/gadingkusumaanggraeni/portfoliogadingkusumaanggraeni/assets/150303416/69dd1310-80ef-4a6c-b54c-52a3e1f9cdfb)
- Overall, total quantity of products sold is 11654 products and total sales is 1,754,750.57
- From the total sales trend graph, it can be seen that the total sales trend in January 2020-October 2021   fluctuative. But, in October 2021 the trend have increased.
- The product category with the highest total sales is Robots which has total sales of 743,505 with total quantity of products sold is 1053. While the most low are the Blueprints with total sales 16,434.61.
- The product category has the highest total product quantity sold is 3123 eBooks with total sales is 58,968.41. While the lowest is Robot Kits, only 1037 products is sold.
- Washington is a city with the highest total product sales was 55381.94 with the total quantity of products sold being 308 products. Meanwhile, the city with the lowest total product sales is Philadelphia is only 23,845.26 with 139 products sold.

5. We know that in October 2021, total sales have increased. So, for maintain or increase sales, the recommendation strategy are :
- Made engagement with old customer by giving interested promotions which can make customer intersting to buy again the produt and make bundling package which customer often buy.
- Then, we can make advance analysis to learn about old customer behavior to make cluster. When we know the cluster, we can make interested promotions package and relate with customer needed. 
