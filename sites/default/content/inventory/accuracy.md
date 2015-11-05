https://en.wikipedia.org/wiki/Physical_inventory
https://en.wikipedia.org/wiki/Cycle_count
https://en.wikipedia.org/wiki/ABC_analysis
http://www.supplychainconsortium.com/Report/GetReport.asp?ID=57
http://www.bastiansolutions.com/blog/index.php/2012/08/15/why-cycle-counting-beats-physical-inventories/
http://www.inventoryops.com/guide_inv_acc.htm

https://www.youtube.com/playlist?list=PLjPRCUDAqllygn5NC4Z-bDB7nzMw22JXx


Attention: You cannot compile an ABC analysis for a subinventory that is defined as a non-quantity tracked subinventory. You can, however, use non-asset (expense) subinventories for which you track quantities.


- ABC Analysis
	- Define and run an ABC compilation
	- Define ABC classes
	- Define ABC group, assign items to ABC classes within a group
	- Update item assignments
	- Purge ABC information
- Physical Inventory
- Cycle Counting



Automatic Scheduling
Oracle Inventory uses the number of items in each cycle count class, the count
frequency of each class, and the workday calendar of your organization to determine
how many and which items you need to count during the scheduling frequency


the Cycle Count
Listing report. This report lists all counts that you need to perform within a given date
range.

Inventory performs a cycle count adjustment by creating a material transaction for
the quantity and sign (plus or minus) of the adjustment. The transaction debits or
credits the adjustment account depending on the direction of the transaction.


When determining if approvals are required, the system first checks the item attributes.
If no tolerances are defined, the system checks the item class definition. If there are no
tolerances defined on the item class definition, the system checks the cycle count header
for tolerance values.

The hit/miss tolerance is used to
evaluate the accuracy of your cycle counting procedures rather that the actually
accuracy of inventory.

Inventory uses these tolerances to generate the Cycle Count Hit/Miss Analysis report.


Important: Oracle Inventory does not stop inventory processing during
a physical inventory. Therefore, you must procedurally coordinate the
snapshot of your physical inventory with your actual counting, and
ensure that no transaction activity occurs in a particular location until
after you have performed your adjustments.


Example of a Physical Inventory Count
For example, suppose that at the start of your physical inventory the system on-hand
quantity for item WIDGET in a particular bin is 30. Oracle Inventory saves this
information with the physical inventory snapshot. During the warehouse count, you
count a total of 25 units of item WIDGET in the same bin. Before you approve your
counts and perform your adjustments, you resume normal transaction operations, and
consequently, item WIDGET reaches a system on-hand quantity of 45. At this point, you
perform your physical inventory adjustments. Oracle Inventory computes the
adjustment as the difference between the tag count and the snapshot quantity, NOT the
current system quantity of the item that has now reached 45. So in this case, the
adjustment is 25 - 30 = -5 units. When the adjustment is posted, the new system on-hand
quantity becomes 40 units.

It is recommended to clear the Pending Transactions and Transactions Open
Interface, before taking a snapshot of inventory quantities.


If you enable dynamic tag entry for your physical inventory, you can enter counts for
any item and stock-keeping unit combination without a pre-generated tag number.



Void Tags
It is important for auditing purposes to track the status of each physical inventory tag.
Therefore, if you do not use one or more of the tags Oracle Inventory generates, you
should void them in the Physical Inventory Tag Counts window. A voided tag is not
reported as a missing tag in the Physical Inventory Missing Tag Listing.
If you generated a certain number of blank tags at the beginning of your physical
inventory, and ended up not using all of them, you would void the unused tags. When
you run the Physical Inventory Missing Tag Listing for the whole range of tags you
initially generated, the unused ones are accounted for and appear as missing tags.
If you void a default tag, (i.e. a tag that identifies a stock-keeping unit for which there is
system on-hand quantity), Oracle Inventory adjusts the quantity in that location to zero.
This indicates that you did not use the tag in question, presumably because the
stock-keeping unit corresponding to the tag did not exist.