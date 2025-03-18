# Groceries - Group 8 MIST 4610 Group Project 1

## Group Name:
21482 Group 8

## Group Members:

1. Ryan Buckley [@rwb11687](https://www.github.com/rwb11687)
2. Suba Senthil [@subasen25](https://github.com/subasen25)
3. Ayush Desai [@Ayush-des](https://github.com/Ayush-des)
4. Mithun Fernandez [@MFernandez2005](https://www.github.com/MFernandez2005)
5. Alex Waller [@alexwaller05](https://www.github.com/alexwaller05)

## Task Description:

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

![image](https://github.com/user-attachments/assets/1f544455-c4dc-4b97-af17-fac3b5d9c83f)

4. Query 4 lists the product names and prices for products that have a higher buy price than the average buy price in their specific department. It also orders them from highest price to lowest price.
   
![image](https://github.com/user-attachments/assets/e9918084-175a-4904-8db2-ea7b4094a7d6)

Query 4 allows the store to see which items are priced above the average price for that department so that they can reevaluate if products are priced too highly or not. Using these product names, they can investigate consumer purchase behavior for these departments and evaluate each product's profitability based on the average quantity purchased for the products returned by this query.

5. Query 5 lists the payment methods for transactions that did not have a coupon associated with them.

![image](https://github.com/user-attachments/assets/386d5084-c0b0-4fe6-98d3-c9fea0f388e4)

Query 5 allows the store to evaluate which forms of payment are most frequently used in transactions without a coupon. If credit or debit cards are a popular payment type, this can indicate that customers are more fond of digital payment methods, and digital coupons should be promoted more frequently. However, if most of these transactions are made using cash, one can reasonably make the conclusion that advertising traditional coupons may be more effective, solely because these customers prefer traditional payment methods as opposed to digital payment methods.

## Database Information:

Name of the database: ns_Sp25_21482_Group8

Additional clarifying information: Within the database, each query is marked as a stored procedure that can be called using the following format: CALL TP_Q1(); and so on.
