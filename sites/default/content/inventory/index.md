# Inventory Management
[Menu](inventory/menu)

### Topics
- [Units of measure](inventory/uom)
- [Items](inventory/items)
- [Lot & Serial control](inventory/lot_serial)
- [Transactions](inventory/transactions)
- [Material Status](inventory/material_status)
- [On-hand](inventory/onhand)
- [Replenishment](inventory/replenishment)
- [Inventory Accuracy](inventory/accuracy)

### Setup
- Assign the inventory responsibility to your user
- Adjust the profile options to the MO hierarchy on the responsibility level
	- HR: business group
	- GL: Ledger name
	- MO: operating unit
- Defining Key Flexfields
```Setup | Flexfields | Key | Segments```
	- System Items
	- Item Categories
	- Item Catalogue
	- Stock Locators
	- Account Aliases
	- Sales Order
- Defining Location
- Defining Calender
	- The inventory organization calendar is mandatory for any inventory if we are 
	performing activities related to planning and forecasting. The calendar is also 
	used for calculating the number of working days and holidays for manufacturing 
	inventory organization.
- Defining inventory organization
- Defining and assigning master org to the inventory organization
- Defining Sub-Inventories & Locators
- Defining items/templates & categories/category sets & assigning items
	item status
	
- Defining transaction types
- Defining receiving parameter
- Defining unit of measures
- Other steps
	- Run [replicate seed data](inventory/replicate_seed_data) report after assigning the profile options


### Notes
- The organization's costing method cannot be changed once cost enabled items have been assigned to the organization.
- Organization's item master organization cannot be modified once the organization has other item child organizations.