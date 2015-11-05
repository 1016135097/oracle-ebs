# Unit Of Measure
### UOM Classes
Unit of measure classes represent groups of units of measure with similar characteristics.  
each class has a base unit.

**Examples of Unit of Measure Classes**  

Unit Base | Unit of Measure |Other Units Measure
----------|-----------------|-------------------
Quantity  | each            | dozen, box
Weight    | gram            | pound, kilogram
Time      | second          | minute, hour
Volume    | cubic           | inches cubic feat, cubic centimeters


### Conversions
Unit of measure conversions are numerical factors that enable you to perform
transactions in units other than the primary unit of the item being transacted, and has three types.

- Standard: converting from a UOM to the base unit in the same class
- Intra class: converting from a UOM to the base unit in the same class for a certain item
- Inter class: converting from the base unit of a class to the base unit of another class for a certain item

### Specifying Which Conversion to Use
When you define an item you decide which type of unit of measure conversion to use

- Itemspecific: Only uses unit of measure conversions unique to this item. If none exist,
you can only transact this item in its primary unit of measure.
- Standard: Uses standard unit of measure conversions for this item if an item-specific
conversion is not available.
- Both: Uses both item-specific and standard unit of measure conversions. If both exist
for the same unit of measure and item combination, the item-specific conversion is
used.

Defaulting>>>>>>>>> defining item>>>>>>>

### Lot-Specific Unit of Measure Conversions
Lot specific conversions enable you to perform a specific inter-class conversion for a
given lot that provides more granular control over the transactional quantities for a lot.  
For example, the standard inter-class conversion for a lot controlled item is 1 gallon
equals 15 pounds; however, when you receive a particular lot of the item, 1 gallon
equals 16 pounds. You can create a lot specific unit of measure for this instance.  
You can also view the history of changes made to the lot unit of measure conversion,
and the corresponding quantity changes.  
**Note**: Lot-specific conversions are available only for items that are set
up for dual unit of measure control.

### Primary Unit of Measure
When you define an item you establish a primary unit of measure.  
The system tracks on-hand quantity and calculates transactions based on the primary unit of measure.  
### Secondary Unit of Measure  
You can optionally establish a secondary unit of measure (dual unit of measure control) for an item.   
Secondary unit of measure can be used for cases where you need to track in two units of measure and there is no constant conversion between the two unit of measures (UOMs).  
For example, chickens can be tracked in pounds and eaches.   
If an item is under dual unit of measure control the system tracks on-hand quantity based on both the primary and secondary units of measure. For example, you can track an item in both eaches and liters.


### Setup steps
- defining UOM classes
- defining UOMs
- defining Conversions

### Notes
- The primary unit of measure is the stocking unit of measure for an item in a particular
organization, and is selected for the item during item setup.
- You must define a conversion between a non-base unit of measure and the base unit of
measure before you can assign the non-base unit of measure to an item.
- Transactions are performed in the unit of measure you specify. The conversion happens
automatically and item quantities are updated in the primary unit of measure of the
item.
- Inventory transactions and on hand balance supports decimal precision to 5 digits after the decimal point. Oracle Work in Process supports decimal precision to 6 digits. Other Oracle
Applications support different decimal precision. As a result of the
decimal precision mismatch, transactions another Oracle Application
passes may be rounded when processed by Inventory. If the transaction
quantity is rounded to zero, Inventory does not process the transaction.
**It is therefore suggested that the base unit of measure for an item is set
up such that transaction quantities in the base unit of measure not
require greater than 5 digits of decimal precision.**
- Units of measure are not organization-specific.
- You can delete existing units of measure that are not base units of measure if no
standard or item specific conversions are defined.
- To make a unit of measure inactive, enter the date on which the unit of measure becomes inactive.