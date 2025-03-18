# DawgMart - Group 8 MIST 4610 Group Project 1

## Group Name:
21482 Group 8

## Group Members:

1. Ryan Buckley [@rwb11687](https://www.github.com/rwb11687)
2. Suba Senthil [@subasen25](https://github.com/subasen25)
3. Ayush Desai [@Ayush-des](https://github.com/Ayush-des)
4. Mithun Fernandez [@MFernandez2005](https://www.github.com/MFernandez2005)
5. Alex Waller [@alexwaller05](https://www.github.com/alexwaller05)

## Task Description:

The goal is to design and implement a relational database that effectively models the operations of a retail store management system. At the core of this system is the Store entity, representing each physical retail location. Each store oversees multiple Departments, employs Employees, manages Inventory, and serves Customers who make purchases.

The database must accurately track Products sold, their Suppliers, and stock levels across different locations. It also records Transactions, capturing essential details such as purchased items, quantities, payment methods, and applied Coupons. By structuring this data effectively, we aim to generate sample datasets, populate the entities with relevant information, and execute insightful queries to support business decisions related to sales performance, inventory management, and customer purchasing trends.

## Data Model:

Explanation of data model:

Our model is based on the structure of a retail store management system. The Department entity represents different departments within the store (such as Electronics, Clothing, Groceries, etc.). Each department has many employees, which is represented by the one-to-many relationship between the Department and Employee entities. Employees are also assigned to specific Store locations, which is shown by a one-to-many relationship between Store and Employee.

The Products entity stores item details, including name, category, and price. Products are supplied by Suppliers, forming a one-to-many relationship since one supplier can provide multiple products. Products also belong to Departments and are tracked in Inventory, which records stock levels across different Stores, establishing one-to-many relationships between Products and Inventory and Store and Inventory.

Customer purchases are managed through several entities. The Customers entity holds customer details, while Transactions capture purchase information such as date, total amount, and payment method. Each Customer can make multiple Transactions. Because a transaction can involve multiple products, and each product can appear in multiple transactions, the OrderDetails entity serves as an associative table linking Transactions and Products, storing details such as quantity and price per item, which can be helpful when creating receipts for customers.

The system also handles promotions through the Coupons entity, which stores discount information and expiration dates. Coupons can be applied to transactions, represented by a one-to-many relationship between Coupons and Transactions.

Lastly, the Store entity represents physical store locations with their address and contact information. Stores maintain inventory levels, which is represented by the one-to-many relationship between Store and Inventory entities.

<img width="960" alt="Screenshot 2025-03-11 at 2 42 51 PM" src="https://github.com/user-attachments/assets/0821a039-43ac-40d0-aca9-d1555added4f" />


## Data Dictionary
<img width="535" alt="Suppliers Table" src="https://github.com/user-attachments/assets/d2781671-c9ae-4a49-adca-de6cb8118c95" />
<img width="532" alt="Products Table" src="https://github.com/user-attachments/assets/53e482a9-66a2-4464-8fb2-94721d7cd730" />
<img width="524" alt="Department Table" src="https://github.com/user-attachments/assets/bdf39f95-3438-438e-bb8c-b5236eda2ebe" />
<img width="529" alt="Employee Table" src="https://github.com/user-attachments/assets/571be308-b039-4eb3-8f36-1725b9510ff8" />
<img width="521" alt="Store Table" src="https://github.com/user-attachments/assets/90558612-4ee5-4d13-b342-c9909c648991" />
<img width="525" alt="Inventory Table" src="https://github.com/user-attachments/assets/064f4f0e-94fe-4749-b225-c785fb0bc5e3" />
<img width="525" alt="OrderDetails Table" src="https://github.com/user-attachments/assets/49563b4a-179f-4227-a754-b377e0708a4b" />
<img width="528" alt="Transactions Table" src="https://github.com/user-attachments/assets/4b726b54-ba4c-465b-afeb-7bc853063dc5" />
<img width="518" alt="Coupons Table" src="https://github.com/user-attachments/assets/08f2f1ca-b2d1-4044-9714-c43fcbcee41e" />
<img width="520" alt="Customers Table" src="https://github.com/user-attachments/assets/d75a8f29-1878-4965-9b7d-18e4fdf46a1e" />

## Queries

![Screenshot 2025-03-18 at 5 07 47 PM](https://github.com/user-attachments/assets/3cd3d57c-e672-4f49-b1b9-ae74b5c35cdb)


1. Query 1 lists all product names along with their total quantity sold, ordering the results in descending order based on total sales.

Query 1 helps managers identify their best-selling products, which can help them with inventory planning, restocking decisions, and marketing strategies. By listing the results in descending order, managers can quickly determine which products are in the highest demand and which ones may require more attention because of low sales.

2. Query 2 identifies stores where inventory levels for particular product categories fall below the average inventory level for those categories across all stores.

4. Query 4 lists the product names and prices for products that have a higher buy price than the average buy price in their specific department. It also orders them from highest price to lowest price.
   
<img width="1477" alt="Screenshot 2025-03-18 at 4 59 31 PM" src="https://github.com/user-attachments/assets/60fb29a2-33cd-4426-828f-6aacd6d73954" />


Query 4 allows the store to see which items are priced above the average price for that department so that they can reevaluate if products are priced too highly or not. Using these product names, they can investigate consumer purchase behavior for these departments and evaluate each product's profitability based on the average quantity purchased for the products returned by this query.

5. Query 5 counts the number of times each payment method is used in a transaction that does not have a coupon associated with it.

<img width="1480" alt="Screenshot 2025-03-18 at 7 24 11 PM" src="https://github.com/user-attachments/assets/4ceb7988-0834-4cec-87b2-adf15318707f" />


Query 5 allows the store to evaluate which forms of payment are most frequently used in transactions without a coupon. If credit or debit cards are a popular payment type, this can indicate that customers are more fond of digital payment methods, and digital coupons should be promoted more frequently. However, if most of these transactions are made using cash, one can reasonably make the conclusion that advertising traditional coupons may be more effective, solely because these customers prefer traditional payment methods as opposed to digital payment methods.

9. Query 9 lists the customers who have spent more than the average amount across all transactions. The results are ordered by total spending in descending order.

<img width="1477" alt="Screenshot 2025-03-18 at 5 02 38 PM" src="https://github.com/user-attachments/assets/103c8513-6373-4408-83ae-5639f1ebe22f" />


Query 9 allows managers to understand these premium customers better so they can implement targeted loyalty programs and personalized marketing strategies. Managers can use this information to prioritize customer service resources, develop exclusive offers for top spenders, and analyze common characteristics among high-value customers to identify potential new premium customers. Understanding spending patterns also helps in forecasting revenue and planning inventory for products that appeal to these valuable customers.


10. Query 10 lists the products that have never been sold, along with their current stock levels.

<img width="1477" alt="Screenshot 2025-03-18 at 5 04 10 PM" src="https://github.com/user-attachments/assets/ff460f44-678e-4988-aeb0-84d5e6310768" />

Query 10 helps managers identify products that have never been sold and their current stock levels. This information is crucial for inventory management, as it highlights products that may need promotions or discounts to clear stock. By addressing these unsold products, managers can optimize inventory turnover and reduce storage costs. The query provides a clear list of products that require attention, making it easier to prioritize actions such as marketing campaigns or clearance sales.


## Database Information:

Name of the database: ns_Sp25_21482_Group8

Additional clarifying information: Within the database, each query is marked as a stored procedure that can be called using the following format: CALL TP_Q1(); and so on.
