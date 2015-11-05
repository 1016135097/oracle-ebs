# Items
### Items Status
is a set of attributes that you could toggle, which is:

- BOM Allowed
- Build in WIP
- Customer Orders Enabled
- Internal Orders Enabled
- Invoice Enabled
- Process Execution Enabled
- Purchasable
- Recipe Enabled
- Stockable
- Transactable


item attributes control level

types
catalouges
categories
container types

items relationships

organization assignment
You can enable an item in all child organizations under your master organization or choose child organizations where you use the item. Oracle Inventory propagates the item to all organizations in which you want to enable it. You can enter or change organization-controlled item attributes. For example, you can choose reorder point planning in one organization and min-max planning in another organization for the same item.


You cannot define an item at the organization level. Oracle Inventory automatically switches to the Master Item window when you define a new item.

You cannot copy items across item master organizations.

pending statuses


templates
You can predefine templates with relatively few attributes enabled because you can apply more than one template to define one item.
Oracle Inventory updates only the attributes that are enabled for the template.
The order in which templates are applied is extremely important.

the predefined templates that Inventory provides:
- ATO Model
- ATO Option Class
- ATO Item
- Finished Good
- Kit
- Outside Processing Item
- PTO Model
- PTO Option Class
- Phantom Item
- Planning Item
- Purchased
- Reference Item
- Subassembly
- Supply Item
- Freight
- Product Family



revision control


You can define relationships between items.  This allows you to search for items through these relationships.  Except in Oracle Purchasing, these relationships are for inquiry and reporting purposes only.