order types


Processing Constraints 
are a security framework where you can define rules in Oracle Order Management that validate back-end operations such as Create, Update, Delete and Cancel.
There are three types of processing constraints - user, extensible and system. You cannot modify system processing constraints.


Pricing engine
Basic Pricing is part of Oracle Order Management and Advanced Pricing is part of the Order Management family. The pricing engine is integrated with Order Management processes and flows. The pricing engine consists of a search engine and a calculation engine. 
When you enter an item on the sales orders line, the pricing engine is called and it calculates the price on the order line after reading it from the price list associated with the customer/order type. The price list may contain some modifiers and qualifiers that may be applied to the base price and the pricing engine calculates these before placing a final value in the Unit Selling Price field in the order line.
A modifier such as a discount, surcharge or special charge may be applied to the base price and may alter the value of the item. You can apply a modifier at the list (order) level or the line level.
A qualifier helps you define who is eligible for a price list or modifier. A qualifier can be a customer name, a customer class, an order type, or an order amount that can span orders. Usually you set up a qualifier and associate it to a modifier or price list.
From the header or line, you can use Actions > View Adjustments to see the details of modifiers that were applied automatically by the pricing engine or to apply manual discounts.


### Order to Cash Lifecycle with Standard Items
- enter header information and line information on sales order
- processing constraints and defaulting rules
- the pricing engine
- view the workflow process for the order
- check availability and book the order
- pick release the order
- ship confirm the order
- use autoinvoice to create an invoice



Using the sales order screen, we can also enter a sales return in Oracle Order
Management. A return should be negative in quantity so that it will be
considered as returns.



Defining Sales Order






### Sales Orders Workbench 
- Find Orders
- Order Organizer
- Sales Orders
- Quick Order Organizer 
- Quick Sales Orders


The Sales Order window allows you to enter orders in any of the Operating Units
accessible to you.

You must enter a customer to be able to book an order. This is the Sold To customer
for the order.
Customers are visible across all organizations and customer addresses are
organization specific.




