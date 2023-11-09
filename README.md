## Project Based Internship Bank Muamalat : Sales Analysis PT Sejahtera Bersama

### Preview Dataset 
In this project, the dataset is about sales data in PT Sejahtera Bersama which 4 table (Customer, Products, Orders and ProductCategory)
Link dataset : [https://drive.google.com/file/d/1RwsBQ1FriNfz6qiq0V5nD7gF7jO81To3/view?usp=sharing]
This is name of column for each table :
1. Customers
    - CustomerID      - CustomerAddress
    - FirstName       - CustomerCity
    - LastName        - CustomerState
    - CustomerEmail   - CustomerZip
    - CustomerPhone
2. Orders
    - OrderID         - ProdNumber
    - Date            - Quantity
    - CustomerID
3. Products
    - ProdNumber      - Category
    - ProdName        - Price
4. ProductCategory
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
1.This is primary key each table 
   a. Primary key of Customer table : CustomerID
   b. Primary key of Products table : ProdNumber
   c. Primary key of Orders table : OrderID
   d. Primary key of ProductCategory table : CategoryID
2. This is relationship of 4 table with STAR SCHEMA
   ![image](https://github.com/gadingkusumaanggraeni/portfoliogadingkusumaanggraeni/assets/150303416/cef85e9d-98b9-424d-8294-4d39d97116c1)
3. This is steps for made master table
   a. From STAR SCHEMA, we know that the primary key of ProductCategory table is CategoryID which refers to Category column in Products table. So, first step is           join 2 table with LEFT JOIN and named product_order.
   b. Second step, we know that the primary key of Customer table is CustomerID which referes to CustomerID column in Orders table. So, join 2 column with LEFT JOIN       and named customer_order. 
   c. End step, join product_order table and customer_order table with primary key is product_number. 

   This is link Google Big Query to made master table : [https://console.cloud.google.com/bigquery?sq=91576120964:5c5734d0f6734dd3b6b63b14213038af]
4. This is    
