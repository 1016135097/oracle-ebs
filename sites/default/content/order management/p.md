Pick release
With pick release you move the items from the
warehouse to the staging area. Along with physically moving the items, you perform a move
order transaction to record the stock movement in Inventory.
You can Pick Release using a one, two, or three-step process.
The one-step process consists of selecting the Auto Allocate box on the Inventory tab and the
Auto Pick Confirm box on the Inventory tab when you run Pick Release, which means that the
Pick Recommendation is automatically created and Pick Confirmed without any manual
intervention.
The two-step process consists of selecting Auto Allocate (not Auto Pick Confirm), which
creates a move order that is automatically detailed. It enables you to view the Pick
Recommendation and provides the opportunity to change quantity, location, and subinventory.
You can report a missing quantity at the Pick Confirmation step in the Transact Move Orders
window. Once you have made your changes, you can transact the move order to Pick Confirm
the inventory.


The three-step process consists of selecting neither the Auto Allocate or Auto Pick Confirm
check boxes. This creates a move order whose details you can enter manually or automatically
in the Transact Move Orders window. After the details are entered, you can transact the move
order to pick confirm the transaction.
You can pick release the order using the Shipping > Release Sales Orders window to pick
release online or using a concurrent program or SRS – Pick Selection List Generation – SRS.
You need to specify the Release Rule Name to be able to proceed with the pick release when
using the concurrent program or SRS.



Ship Confirm
When you need to confirm that your items have been shipped out of inventory to the customer
as a delivery, use the Ship Confirm window. Perform Run Ship Confirm to indicate that the
items are loaded onto the carrier from the staging location. When you run Ship Confirm, the
system decrements Oracle Inventory and updates the sales order line status. This information is
then transferred through AutoInvoice to Oracle Accounts Receivables for invoicing. Finally,
accounting information can be sent to the general ledger from Oracle Inventory and Oracle
Accounts Receivables.


AutoInvoice
Use the AutoInvoice concurrent program to create invoices for the processed orders. You
cannot use AutoInvoice to create invoices for the following items:
Where the item attributes Invoice Enabled or Invoiceable Item is set to No; included item or
internal order. If you do use AutoInvoice, the Invoice Interface workflow activity is completed
with a status of Not Eligible.
If the order or lines are on hold, the order details will not be interfaced to Receivables. The
Invoice Interface workflow activity will complete with a status of On Hold. You can either
release the hold manually, or progress the workflow Actions > Progress Order in the Lines tab.
Alternatively you could wait till the hold is re-evaluated after a time period of 12 hours, in
which case if it is eligible for invoicing, the Workflow Background Process activity progresses
the lines to invoice interface.







__________________________

Each user can access, process, and report on data only for
the operating units assigned to the MO: Operating Unit or MO: Security Profile profile option.
The MO: Operating Unit profile option only provides access to one operating unit. The MO:
Security Profile provides access to multiple operating units from a single responsibility.


Responsibility determines access to operating unit or units: If MOAC is not enabled, you can
implement security at the operating unit level through the MO: Operating Unit profile option
called, which is set at the site, responsibility or user level. If MOAC is enabled, you can
implement security at the operating unit level using the MO: Default Operating Unit and MO:
Security Profile profile options.

All tables in Purchasing, Payables, Order Management, and Receivables, except vendors and
customers tables, contain an ORG_ID column. When you open a window in these applications,
you are actually looking at a view of the underlying table. The window will show only those
records where the value in the ORG_ID (operating unit) column corresponds to the value of the
profile option for the responsibility you are logged in with.





Setup windows that have the Operating Unit field: Approvals, Transaction Types, Payment
Types, System Parameters, Shipping Tolerances.
Transaction windows that have the Operating Unit field: Sales Orders, Quick Sales Orders,
Order Import Corrections, Pricing and Availability, Processing Messages, Order Organizer,
Retrobilling Organizer, Audit History, Create Hold Sources, Release Hold Sources, Sales
Agreements, Scheduling Organizer, Order Information Portal (HTML pages).


Agreements, Scheduling Organizer, Order Information Portal (HTML pages).
The Operating Unit field is a required field in the above windows. When the window opens,
the Operating Unit field gets its value from the profile option MO: Default Operating Unit,
however it displays as an LOV, so that you can select a different operating unit other than the
default if needed. The Operating Unit field is always displayed in the windows that are not
folder enabled (Transaction Type, System Parameters). The operating unit field is a hidden
field on all folder enabled windows and you can select to display this field in windows like
Sales Order, Quick Sales Orders.