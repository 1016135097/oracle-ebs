# Material Status
*TODO: review the docs*

Material statuses control the transactions that could be happen on items
In addition, you can determine whether products with a particular status can be reserved, included in available to promise calculations, or netted in production planning.   
You assign material statuses at four levels: subinventory, locator, lot, and serial.  


### Material Status Examples
This example describes four typical material statuses

- **Active**: This is a typical default for your warehouse. It allows all transaction types.
- **Hold**: You might use this status for material that needs to be inspected or whose quality is suspect.
- **Immature**: This status is useful for material that needs to age in the warehouse before being picked or shipped for a sales order. You may want to allow internal orders to move the material around your distribution chain, but picking and shipping this material for orders to customers should be prevented.
- **Almost Mature**: This material has a very short aging process, or is nearly mature. By assigning material this particular status, you enable that material to be picked and staged, but prevent the material from being shipped. As soon as material is completely matured, it can be assigned a  status of Active and shipped immediately.


### Setup
- **Transaction types status control**
	- When you set up transaction types, you determine whether some transactions can be restricted by material status. The transactions for which you enable status control appear in the Material Status Definition window. If you do not enable status control for a transaction type, then the transaction type is always allowed. 

- **Define material statuses**
	- You can assign the planning attributes Allow Reservations, Include in ATP, and Nettable to the material statuses that you create. When you transact an item, the system checks all of the material statuses. If the system finds a status that disallows the transaction, whether at the serial, lot, locator, or subinventory level, then the transaction fails.
	- When you define a material status, you can select the Lot or Serial check boxes so the system can assign a default material status to a serial or lot controlled item at receipt. The receiving operator can accept the default status that the system suggests, or he or she can assign another status.

- **Define material status control of an item**
	- You determine the default material status during item definition, it found under "Material status control" in the inventory tab
	- Assigning a default material status to an item under lot or serial control is optional

- **Assign material status control to subinventories and locators**
	- The field of material status in forms called "Status" in the subinventory form, and "Default Locator Status" if locator control is enabled.
	- Subinventories are assigned a material status in the Subinventories window. You also assign a default locator status for all locators within the subinventory. This default locator status is used in two situations:
		- When locator control is set to prespecified (all locators in the subinventory must be defined before they can be used), the default status is used to default the locator status. However, this status can be changed for each locator as it is defined. 
		- When locator control is set to dynamic (locators need not be defined in advance, but will be created on the fly as users define new locators), the default locator status will be used for these newly defined locators.

### Reports
- **Material Status Definition Report** provides an overview of each material status and how it is used
- **Material Status History Report** Provides you the full status history of who changed the material status and what reason was given

### Profile Option
- **INV: Material Status Support** This profile option determines whether material status is enforced. if your installation never uses material status, and you set this profile option to No, then system performance improves slightly

### Implementation Considerations
- Do you need to use material statuses in your organization?
- Which transaction types should always be allowed?
- Which transaction types should you restrict?
- What material statuses do you need to define?
- At what levels do you need to assign your material statuses?
- Can you update a status once it has been assigned?
- Does restricting receipt transactions apply to statuses?

### Notes
- You can disable material statuses you no longer use. If a material material status is assigned to any lot, serial, subinventory, or locator, then you cannot disable it.
- You can use the Material Workbench query to update material status for a set of entities, query all entities with a particular material status, and then update the material status of those entities.
