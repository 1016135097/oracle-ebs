Item Orderability 
	restrict the item list based on customer and other related criteria
You can set up rules based on either Item or Item Category. If you set up a rule for an
item, which belongs to a category that has a rule already defined, you will not be
allowed to set up a rule and the following error message displays: "Active rules already exist at Item Category Level"

Order Management > Setup> Rules > Item Orderability

Item Orderability rules are defined at Operating Unit Level. The Item Category and Items LOV are always
displayed based on the Master Organization or the Item Validation Organization
attached to the operating unit. However, the Ordered Items LOV will not display all
items; the list is populated depending on the Item Orderability Rules you have set up. If
you have not set up the Item Orderability Rules, it means that the Item Orderability
functionality is disabled or the functionality cannot be used. Additionally,
RMA/Returns do not validate or honor the Item Orderability rules. Returns do not need
to validate item orderability rules, as you can return goods that you ordered earlier but
are not currently allowed to order.

### OM: Use Materialized View for Items LoV
