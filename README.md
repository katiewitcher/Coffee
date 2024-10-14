# Coffee
MIST 4610: Group Project 1 Information
 
Team name and members:
Include information about the name of the team, the names of all team members as well as links to their corresponding GitHub repos that have the project on them.
Giovanna Palma - 
Katie Witcher - @katiewitcher https://github.com/katiewitcher/Coffee
Jack Macken- https://github.com/jackmacken/4610Project
Andrew Baich -
Brooke Istishin - 
 
# Scenario description:
Our project models a small, local coffee shop chain in Georgia, operating multiple locations under unique names, but all managed centrally with a unified menu. The owner oversees all locations using a central data center to streamline operations.
Key entities in the database include Customer, Order, Employee, Coffee Shop, OrderItem, MenuItem, RecipeItem, Ingredients, Supplier, and Category. These entities and their relationships allow the database to efficiently track customer visits, the details of their orders, payment methods, and the employee handling each transaction at a specific location. Additionally, the database stores information on the menu items ordered, their ingredients, and the corresponding recipes. It also manages stock levels and tracks suppliers for each ingredient, ensuring a seamless supply chain.
 
# Data Model:
Customers can make many orders, an order can only be made by one customer.
An order can only be taken by one employee and an employee can take many orders.
Many Employees work at a coffee shop but employees are only employed at one coffee shop.
An employee can only have one boss but a boss can be in charge of many employees.
Orders can have many menu items and menu items can appear in multiple orders – therefore creating a third entity between the two, ‘Order Item” which contains every time a menu item appears in an order.
Menu Items can have many ingredients and ingredients (like coffee) can be in many menu items, therefore the entity between them, “RecipeItem” details the ingredient amount in each product.
Ingredients have one supplier but suppliers can supply many ingredients.
Menu Items fall into one category, like “Breakfast”, and categories can have many menu items
  ![image](https://github.com/user-attachments/assets/d45b6a4e-3ba1-49a1-80f3-036237eeb288)



# Data Dictionary:
<img width="468" alt="image" src="https://github.com/user-attachments/assets/40f72c6c-890b-47a8-924e-e290f165783d">
<img width="468" alt="image" src="https://github.com/user-attachments/assets/c7a28666-8024-471a-b94a-38e19fa23bc0">
<img width="468" alt="image" src="https://github.com/user-attachments/assets/11d7c1c3-b604-4452-b227-00fb19ed9ade">
<img width="487" alt="image" src="https://github.com/user-attachments/assets/2cf23f36-e130-416a-a85c-cda279feb94d">
<img width="468" alt="image" src="https://github.com/user-attachments/assets/7edd0220-fab8-498e-9540-2ec312f5ec89">
<img width="468" alt="image" src="https://github.com/user-attachments/assets/25dbb014-50b7-4cc6-b691-ddb403f90220">
<img width="468" alt="image" src="https://github.com/user-attachments/assets/9df74cf8-1db0-42c6-82b6-251f20c55110">
<img width="468" alt="image" src="https://github.com/user-attachments/assets/9b3c92af-3378-4b51-b88c-37a2e40fd951">
<img width="468" alt="image" src="https://github.com/user-attachments/assets/4d6b70f4-b172-4320-ba9d-b85a2978e144">
<img width="468" alt="image" src="https://github.com/user-attachments/assets/04126216-4097-4a41-a36f-70abe0aaf2ce">

 
# TEN QUERIES:
 <img width="466" alt="image" src="https://github.com/user-attachments/assets/6b5d2034-aaf4-4111-9310-c09bf99dde96">


1. Query 1 finds the most frequently ordered menu items by counting the occurrences of each menu item in the ‘OrderItem’ table. The results are also ordered by the number of occurrences of each menu item in descending order. 
 ![image](https://github.com/user-attachments/assets/e9f278f9-7fee-4470-93f0-8ef773893902)

Query 1 allows managers to track what menu items are the most popular and see which ones are not selling well.  This is important for optimizing inventory levels to make sure the right amount of items are stocked. It can also help management make important decisions when designing or updating the menu to ensure customer satisfaction and further sales. Additionally, it will help management focus marketing and promotion efforts on popular items. Listing the results in descending order helps with efficiency when retrieving information about which menu items to promote and stock the most of.    


2. Query 2 retrieves the employees who have processed more than 3 orders. It then organizes the number of orders each employee has processed in descending order. 
 ![image](https://github.com/user-attachments/assets/709c0a88-b525-49b8-a53e-e6abed58d014)

Query 2 allows managers to see employee performance on handling orders. This is important for understanding employee efficiency, time management, and overall employee performance. Managers can use this information for future schedules in order to optimize employee productivity and work distribution. This information can also help with goal and target setting for employees to motivate them. 


3. Query 3 counts the frequency of each payment type, either credit, cash, or debit. It also orders the results by descending frequency. 
 ![image](https://github.com/user-attachments/assets/4568c0ae-5257-476d-a615-885771a1cb3b)

Query 3 allows managers to understand customer preferences and which payment options to promote or expand. For instance, if the manager wanted to decide if the establishment should be accepted. Different payment methods can also come with varying fees (credit fees on transactions, etc.) which can help managers understand the most cost-effective methods to use. This can lead to managers potentially negotiating better rates or finding cost-saving opportunities. 

  
4. Query 4 reports the total amount of all cash orders. 
 ![image](https://github.com/user-attachments/assets/ac298998-b714-46ee-824c-c3d0618b00e7)

Query 4 allows managers to have an immediate snapshot of the business’s daily revenue to help understand the company’s financial health. Having information about the business’s cash flow helps to ensure the business is functioning at optimal liquidity to cover expenses. It also helps managers to evaluate if sales goals are being met and identify if the business has a steady cash flow. 

 
5. Query 5 retrieves all ingredients where the quantity in stock is less than 30 at the location. 
 ![image](https://github.com/user-attachments/assets/115a5a66-bd0e-482e-8d99-831fc13314d5)

Query 5 allows managers to maintain efficient inventory management by monitoring low stock levels. This will allow for optimal inventory levels and ensure that there is enough stock of ingredients for the items without over-ordering. Managers will be able to better meet customer demand and avoid loss of business. Knowing the low stock quantity will also aid cost control, helping managers reorder ingredients at the most optimal time and plan ahead while minimizing waste. 

   
6. Query 6 selects the average total sales from each category of menu items. 
 ![image](https://github.com/user-attachments/assets/e74de975-4c37-4fc0-8d64-24a43a214d28)

Query 6 allows managers to understand total sales by category, helping them grasp which product categories are contributing most to revenue. By comparing these sales figures with associated costs, the coffee shop could find out which categories (e.g., coffee, pastries, etc.) offer the highest profitability. This may allow for a variety of things - like optimizing pricing, managing inventory more efficiently, and focusing promotional efforts on the best categories.

   
7. Query 7 shows how many employees each boss is responsible for managing. 
 ![image](https://github.com/user-attachments/assets/024fb9ee-a622-4746-a675-f812f00b3160)

Query 7 can help the coffee shop when evaluating effective management and workload distribution. By tracking the number of employees reporting to each boss, they can balance team sizes, prevent overburdening managers, and identify areas where additional leadership may be needed. 


8. Query 8 reports each supplier name that supplies more ingredients than the average amount of ingredients that each supplier supplies.
 ![image](https://github.com/user-attachments/assets/0e155f29-6bcb-46f7-859a-28198e0cd4db)

Query 8 allows managers to track how much stock comes from each supplier with shows the reliability and performance of suppliers. This can help to hold suppliers accountable to their delivery schedules and order quantity requests. It also allows for managers to maintain optimal inventory levels by having a better understanding of how many recipes and menu items are reliant on which suppliers. If the business is too reliant on one supplier for its ingredients and that supplier has issues such as delays or supply shortages there could be increased risk. It is important for managers to diversify their supply chain to mitigate operational disruption. 


9. Query 9 reports menu items that have not been ordered yet. (Items that appear in no Orders by checking OrderItems). 
 ![image](https://github.com/user-attachments/assets/033a9078-c856-42d6-aff6-f0ec185a2fd8)

Query 9 allows managers to track how many items are still available for purchase. This can help to quickly identify what items need to be restocked, allowing for better efficiency and inventory management efforts. It can also help managers to identify which menu items may be less popular, aiding menu design. 
 

10. Query 10 reports the id of employees that have processed Criag’s order. 
 ![image](https://github.com/user-attachments/assets/54cad467-c9a6-44c8-b204-6c6e179234da)

Query 10 allows managers to access information that would be helpful in the event that Craig (or another customer) reported a complaint or posted a bad review and management wanted to know which employees might be responsible for the negative customer experience. This can help managers hold employees accountable, complete employee evaluations, and improve customer service overall. 


 
# Database information:
Name of database: cs_gcp90285

Additional information: Each Each query listed above is marked in the database using stored procedures which can be called using the following format: CALL TP_Q1();


![image](https://github.com/user-attachments/assets/f99b4105-e40a-47a6-a5e9-26a3b68b434d)
