# Coffee
Team 7 Mist 4610 Group Project 1
Team Name:Team 7

Team Members:

Giovanna Palma - 
Katie Witcher -
Jack Macken - 
Andrew Baich -
Brooke Istishin -


Problem Description:

Our project models a small, local coffee shop chain in Georgia, operating multiple locations under unique names, but all managed centrally with a unified menu. The owner oversees all locations using a central data center to streamline operations.
Key entities in the database include Customer, Order, Employee, Coffee Shop, Payment, OrderItem, MenuItem, RecipeItem, Ingredients, Supplier, and Category. These entities and their relationships allow the database to efficiently track customer visits, the details of their orders, payment methods, and the employee handling each transaction at a specific location. Additionally, the database stores information on the menu items ordered, their ingredients, and the corresponding recipes. It also manages stock levels and tracks suppliers for each ingredient, ensuring a seamless supply chain.

Data Model:

Customers can make many orders, an order can only be made by one customer.
An order can only be taken by one employee and an employee can take many orders.
Many Employees work at a coffee shop but employees are only employed at one coffee shop.
An employee can only have one boss but a boss can be in charge of many employees.
Orders can have many menu items and menu items can appear in multiple orders – therefore creating a third entity between the two, ‘Order Item” which contains every time a menu item appears in an order.
Menu Items can have many ingredients and ingredients (like coffee) can be in many menu items, therefore the entity between them, “RecipeItem” details the ingredient amount in each product.
Ingredients have one supplier but suppliers can supply many ingredients.
Menu Items fall into one category, like “Breakfast”, and categories can have many menu items


<img width="962" alt="Screenshot 2024-10-13 at 6 25 51 PM" src="https://github.com/user-attachments/assets/7458f408-a2b0-44cb-bd5d-e0f50b30d22c">



