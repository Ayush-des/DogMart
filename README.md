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
<img width="670" alt="Transactions Table" src="https://github.com/user-attachments/assets/f6cbd7ad-9971-4067-9813-043564366ea5" />
<img width="670" alt="Coupons Table" src="https://github.com/user-attachments/assets/446b9b39-ea44-4da0-9876-bc19d5e42079" />
<img width="520" alt="Customers Table" src="https://github.com/user-attachments/assets/d75a8f29-1878-4965-9b7d-18e4fdf46a1e" />

## Queries

![Screenshot 2025-03-18 at 5 07 47 PM](https://github.com/user-attachments/assets/3cd3d57c-e672-4f49-b1b9-ae74b5c35cdb)

**Query 1** <br>
Query 1 lists all product names along with their total quantity sold, ordering the results in descending order based on total sales.

<img width="1477" alt="Screenshot 2025-03-18 at 4 57 49 PM" src="https://github.com/user-attachments/assets/90dacdbc-aa79-4491-b628-1695cb6a54e0" />


Query 1 helps managers identify their best-selling products, which can help them with inventory planning, restocking decisions, and marketing strategies. By listing the results in descending order, managers can quickly determine which products are in the highest demand and which ones may require more attention because of low sales.

**Query 2**<br>
Query 2 identifies stores where inventory levels for particular product categories fall below the average inventory level for those categories across all stores.

<img width="1477" alt="Screenshot 2025-03-18 at 4 58 32 PM" src="https://github.com/user-attachments/assets/58aba29d-aaf1-40fd-a8cd-389037cdb8b1" />


Query 2 helps managers identify stores that may need to be restocked. Having enough inventory in all stores helps improve sales opportunities, enhances customer satisfaction, and prevents some products from being completely out of stock that would lead to lost sales.

**Query 3**<br>
Query 3 retrieves a list of all product names along with the total quantity of each product currently in stock and then sorted in descending order by their stock quantity.

<img width="1480" alt="Screenshot 2025-03-18 at 8 18 12 PM" src="https://github.com/user-attachments/assets/204fd714-c62a-4d46-a9a1-485d2782e4aa" />


Query 3 helps managers keep track of inventory levels and whether the stock is too high, too low, or optimal. Having optimal levels of stock prevents overstock and stockouts, which can either increase costs unnecessarily or lose sales. This information helps managers make informed decisions about reordering, promotions, and managing inventory.

**Query 4**<br>
Query 4 lists the products that are priced higher than the average for their department and orders them from highest to lowest price

<img width="1477" alt="Screenshot 2025-03-18 at 4 59 31 PM" src="https://github.com/user-attachments/assets/36fa45eb-1da5-4325-aa8e-02b25368f457" />


Query 4 helps store managers determine which of the higher-priced products would require a higher profit margin. Understanding which products are above their department average helps with pricing strategy, mark-up adjustments, and competitive pricing.

**Query 5**<br>
Query 5 counts the number of times each payment method is used for transactions that did not have a coupon associated with them.

<img width="1480" alt="Screenshot 2025-03-18 at 7 24 11 PM" src="https://github.com/user-attachments/assets/a2d07a19-5c5b-407c-bc7e-3d3efc75efce" />


Query 5 allows for the store manager to see if a customer pays with a card (credit or debit) more often makes them not use a coupon and therefore, if they should use more digital advertisements because people aren’t using cash.

**Query 6**<br>
Query 6 lists customers who exclusively used credit cards as their payment method during March 2025, along with their complete transaction details.

<img width="1477" alt="Screenshot 2025-03-18 at 5 01 15 PM" src="https://github.com/user-attachments/assets/59fddc1b-46b1-4a2d-8503-c4263ac50f38" />


Query 6 helps managers know which customers always pay with credit cards. This lets managers create special deals with credit card companies, decide if launching a store credit card would be worthwhile, and figure out which types of customers prefer using credit. Store managers can use this knowledge to plan what payment systems to invest in and develop better customer rewards programs.

**Query 7**<br>
Query 7 identifies which stores have inventory shortages so that these stores can be easily contacted to restock their inventory.

<img width="1480" alt="Screenshot 2025-03-18 at 8 19 40 PM" src="https://github.com/user-attachments/assets/90aa8c95-2e92-42dd-a49d-648ed451686a" />


Query 7 lists stores with their ID, address, phone number, and total inventory quantity. These stores have less total inventory than the average across all stores. The list is ordered from lowest to highest inventory, so stores with the most critical shortages appear first, making it easy for managers to prioritize which locations to contact for restocking.

**Query 8**<br>
Query 8 lists all of the most popular products by calculating the total quantity sold for each item and then sorting them by most sold to least sold.

<img width="1480" alt="Screenshot 2025-03-18 at 8 20 48 PM" src="https://github.com/user-attachments/assets/7da15ec3-df39-4556-89cc-a593c23f9163" />


Query 8 helps store managers make critical inventory decisions by highlighting which products to keep well-stocked, determining optimal shelf placement for high-selling items, and identifying potential candidates for promotional bundles or special displays. Understanding top-selling products also guides purchasing decisions and helps prevent costly stockouts of items customers expect to find.

**Query 9**<br>
Query 9 lists the customers who have spent more than the average amount across all transactions. The results are ordered by total spending in descending order.

<img width="1480" alt="Screenshot 2025-03-18 at 8 21 24 PM" src="https://github.com/user-attachments/assets/aff67c91-56da-45ac-8043-decfc0c858b8" />


Query 9 allows managers to understand these premium customers better so they can implement targeted loyalty programs and personalized marketing strategies. Managers can use this information to prioritize customer service resources, develop exclusive offers for top spenders, and analyze common characteristics among high-value customers to identify potential new premium customers. Understanding spending patterns also helps in forecasting revenue and planning inventory for products that appeal to these valuable customers.

**Query 10**<br>
Query 10 lists the products that have never been sold, along with their current stock levels.

<img width="1480" alt="Screenshot 2025-03-18 at 8 21 49 PM" src="https://github.com/user-attachments/assets/1b8cc4fe-063b-46a1-809a-12ae25f95edd" />


Query 10 helps managers identify products that have never been sold and their current stock levels. This information is crucial for inventory management, as it highlights products that may need promotions or discounts to clear stock. By addressing these unsold products, managers can optimize inventory turnover and reduce storage costs. The query provides a clear list of products that require attention, making it easier to prioritize actions such as marketing campaigns or clearance sales.

## Database Information:

Name of the database: ns_Sp25_21482_Group8

Additional clarifying information: Within the database, each query is marked as a stored procedure that can be called using the following format: CALL TP_Q1(); and so on.
