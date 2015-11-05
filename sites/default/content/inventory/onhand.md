# Onhand & Avalibility

Oracle Inventory enables you to view on-hand quantities, reservations, and supply and
demand information.

Features
- View material quantities and locations
- Request a report of item quantities across multiple organizations
- View item supply and demand

Material Workbench
The Material Workbench enables you to view material in receiving, on-hand quantities,
and intransit material. You can also view material across organizations. In addition, you
can create and save queries, create move orders, and request cycle counts, as well as
change material statuses.

On-hand quantity is the physical quantity that resides in your subinventory.  For example, the Bulk subinventory has 15 items that reside in it.  Therefore, the on-hand quantity for the Bulk subinventory is 15.

A reservation is a link between a supply source and a demand source.
Item reservations prevent the allocation of material you previously set aside for a sales order, account, account alias, inventory allotment, user-defined source, process batch components or, Oracle Complex Maintenance and Repair Overhaul work order components.

You can also create reservations for different types of supplies such as on-hand inventory, purchase orders, internal requisitions, discrete jobs, shop floor jobs, and process manufacturing batches. In addition, you can create reservations for advanced shipment notices (ASNs) and material in receiving for Oracle Warehouse Management enabled organizations.


### Notes
- Availability to Inventory is not the same as availability to Planning- Planning looks at inbound supply in addition to on hand quantity and deducts other demand. Inventory only looks at what is on hand and subtracts what is committed to other uses (i.e reserved or about to be moved or issued out the door)

- Availability to Inventory depends on what you want to use the material for.  For example, if you have material that is in a non-reserved subinventory, that quantity will not be available to reserve but it may be available to transact (for miscellaneous issues etc).


### Reservation Versus Allocation



### Material Workbench
The Material Workbench enables you to view material in receiving, on-hand quantities, and inbound material. You can also view material across organizations. In addition, you can create and save queries, create move orders, and request cycle counts, as well as change material statuses.
You can view item quantity across organizations. You can view only material in organizations to which you have access.


Viewing Available Items
You can use the Material Workbench to view item availability.  The system can calculate item availability for a given item at the subinventory, locator, lot, serial, or revision level. You can view items that are available to reserve as well as available to transact.  


Material Workbench Transactions
You can use the material workbench to perform the following transactions:
Status Update: Enables you to change material status information. 
Cost Group Transfer: Enables you to transfer the item to another cost group. 
Grade Update: Enables you to update a lot grade.
You can use the material workbench to perform the following requests:
Mass Move:  Moves the selected items to a new subinventory. 
Mass Issue: Enables you to mass issue an item.
Cycle Counting: Enables you to initiate a cycle count for the selected subinventory.


Available to Promise
Available to Promise (ATP) represents the quantity available for sale at any given period.
The basic formula for ATP is ATP quantity = on-hand quantity + supply - demand – shortage
Oracle Inventory enables you to define different rules that govern what is considered supply and demand.

Available to promise process looks at existing supply and demand to determine availability. For example, you have 100 units on hand on Monday, and 100 units of purchase orders coming on Tuesday and new orders that you plan to release to execution for 100 units on Wednesday. Consequently, the available to promise on Monday is 100, Tuesday is 200, and Wednesday is 300. 

Capable to promise
The capable to promise computations will try and create new supplies to compute availability. If there is a demand for 200 units on Monday, then the system determines whether to move the availability date to  Tuesday when the Purchase orders and on-hand make it 200 units or see if there is enough capacity and upstream materials (components) to make, procure, or transfer 100 additional units to make the availability for Monday.

Uses of ATP in Inventory
You can view the earliest available data for a specific quantity of an item or a group of items and the available quantity of an item for a specific date.
You can view the supply, demand, and ATP item quantities for the periods that fall between the current date and the end of the ATP horizon.

### ATP Rules Setup
- Define computation options
- Specify supply time fence
- Specify end of ATP horizon
- Specify demand time fence
- Specify demand sources
- Specify supply sources



ATP Computation Options
When you define ATP rules, you must specify computation options. Computation options govern how to calculate the ATP quantity in each period. You can use computation options individually or in combination.
Backward Consumption of Shortage
You can calculate ATP information by using the surplus quantity of an item from prior ATP periods to cover a period shortage. If the period ATP is negative, you can go backward through the supply periods, one at a time, and subtract the shortage from the available quantity. You can keep going backward until the shortage disappears or you run out of periods.
Forward Consumption of Shortage
You can calculate ATP information by using a surplus quantity of an item from future ATP periods to cover an earlier period shortage. If the period ATP is negative, then you can go forward through the supply periods, one at a time, and subtract the shortage from the available quantity. You can keep going forward until the shortage disappears or you run out of periods.