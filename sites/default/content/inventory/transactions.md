# Transactions

### Main transactions
- Receiving: you should define receiving options first
- Issuing
- Subinventory Transfer
- Inter-Organization Transfer  
  require defining shipping network, and the item should be assigned for both the organizations  
	- Direct: require no receiving
	- Intransit: require receiving

you view the recipt from recipts form
	 then from receiving form you query the recipt and when you save it transacte to the inventory


Receipt Routing
- Standard
- Inspection
- Direct


To request a material transfer between organizations requires an internal requisition



move orders
Move orders are the requests for transferring and issuing goods from an inventory
organization. When we issue goods using the move order, we need to select the
Transaction Type as Move Order Issue.
move orders requisitions
	- workflow-based approval process

Approval is required only for requisition move orders. Other move orders created by shipping or replenishment processes are approved automatically.


transaction 
	source types
	action
	reasons
	types

?? transaction managers 4
transaction workers
processing intervals



item transaction defaults

__________________________

picking rules
you can create picking rules for
- sales orders
- manufacturing
- work in process

sort criteria
- Lot 
- Revision
- ???Subinventory
- Locator

Assignment
___________________________


account aliases

accounting periods

material shortage alerts and notifications


???? movement statistics



### move order steps:
- create 
- approve
- allocate
- transact




### Setup
- Setting transaction profile options
- Launching transaction managers
- Setting control options (locator, lot, serial, revision) and restrictions(subinvetories, locators)
- Define item transaction defaults
- Define UOM conversions
- Define transaction (source types, actions, types, reasons)
- Define account aliases  
	You must create an inventory account alias for each GL account if you wish to use an alias for that GL account in inventory transactions. Oracle Inventory does not honor GL account aliases.
- Define shipping networks
- Define shipping methods
- Define the parameters for gathering movement statistics
- Define economic zones
- Define intercompany relations