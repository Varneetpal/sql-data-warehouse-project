Data Dictionary for Gold layer 

Overview 

The Gold Layer is the business-level data representation, structured to support analytical and reporting use cases.
It consists of dimension tables and fact tables for specific business metrics. 

------------------------------------------------------------------------------------------------------------------ 

1. **gold.dim_customers **

  Purpose: Stores customer details enriched with demographic and geographic data. 
  
  Columns:
  Column Name 	Description 	Description 
  Customer_name 	INT 	Surrogate key uniquely identifying each customer record in the dimension table. 
  Customer_id 	INT 	Alphanumeric identifier representing the customer, used for tracking and referencing. 
  Customer_number 	NVARCHAR(50) 	The customer's first name, as recorded in the system. 
  First_name 	NVARCHAR(50) 	The customer's last name or family name. 
  Last_name 	NVARCHAR(50) 	The country of residence for the customer (e.g. 'Canada') 
  country 	NVARCHAR(50) 	The marital status of the customer (e.g., 'Married', 'Single'). 
  Marital_status 	NVARCHAR(50) 	The marital status of the customer (e.g., 'Married', 'Single'). 
  gender 	NVARCHAR(50) 	The gender of the customer (e.g., 'Male', 'Female', 'n/a'). 
  birthdate 	DATE 	The date of birth of the customer, formatted as YYYY-MM-DD (e.g., 1971-10-06). 
  Create_date 	DATE 	The data and time when the customer record was created in the system.


  2. **gold.dim_products **

Purpose: Provides information about the products and their attributes 

Columns:
Column name 	Data Type 	Description 
Product_key 	INT 	Surrogate key uniquely identifying each product record in the product dimension table. 
Product_id 	INT 	A unique identifier assigned to the product for internal tracking and referencing. 
Product_number 	NVARCHAR(50) 	A structured alphanumeric code representing the product, often used for categorization or inventory. 
Product_name 	NVARCHAR(50) 	Descriptive name of the product, including key details such as type, color, and size. 
Category_id 	NVARCHAR(50) 	A unique identifier for the product's category, linking to its high-level classification. 
category 	NVARCHAR(50) 	The broader classification of the product (e.g., Bikes, Components) to group related items. 
subcategory 	NVARCHAR(50) 	A more detailed classification of the product withing the category, such as product type. 
Maintenance_required 	NVARCHAR(50) 	Indicates whether the product requires maintenance (e.g., 'Yes', or 'No'). 
cost 	INT 	The cost or base price of the product, measured in monetary units. 
Product_line 	NVARCHAR(50) 	The specific product line or series to which the product belongs (e.g., Road, Mountain). 
Start_date 	DATE 	The date when the product became available for sale or use. 


3. **gold.fact_sales** 

Purpose: Stores transactional sales data for analytical purposes. 

Columns:
Column Name 	Data Type 	Description 
Order_number 	NVARCHAR(50) 	A unique alphanumeric identifier for each sales order (e.g., 'SO54496'). 
Product_key 	INT 	Surrogate key linking the order to the product dimension table. 
Customer_key 	INT 	Surrogate key linking the order to the customer dimension table. 
Order_date 	DATE 	The order when the order was placed. 
Shipping_date 	DATE 	The date when the order was shipped to the customer. 
Due_date 	DATE 	The date when the order was due. 
Sales_amount 	INT 	The total monetary value of the sale for the line item, in whole curreny units (e.g., 25). 
quantity 	INT 	The number of units of the product ordered for the line item (e.g., 1). 
price 	INT 	The price unit if the product for the line item, in whole currency units (e.g., 25). 
