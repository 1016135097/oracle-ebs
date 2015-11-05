# Suppliers

Suppliers are companies and individuals from whom you purchase goods and services. When you enter a supplier that does business from multiple locations, you enter header information only once, and you enter supplier sites for each location. Most supplier information defaults to supplier sites.   
However, you can override the values that default if necessary. After you define suppliers, you can use them when you import/enter invoices and create purchasing documents.


- supplier definition consists of supplier header and sites
- supplier could have unlimited sites
- Supplier information defaults to sites, but you can override these defaults and assign each site different criteria based upon its business terms and its performance in meeting your business needs.
- You have the ability to identify terms and conditions, purchasing details, and payment information for each supplier site.
- You can decide to which site or sites the invoices and purchase orders are sent. In addition, you can designate a site to receive only requests for quotes, until you have certified this supplier as a purchasing site.
- You can put a supplier on hold or set a date to inactivate the supplier.
- You can buy from several different sites while sending the payments to only one site.
- For each supplier site, you can enter contact information (name, address, telephone) specific to that site. Contact information is for your reference only.

### Purchasing Use of Supplier Information
- A recommended supplier is optionally entered on a requisition.
- A supplier is needed to send a request for quote.
- That same supplier is used when entering a quotation.
- Purchase orders need supplier information.
- You receive goods or services from a supplier.
- You return goods to a supplier.
- You must pay the supplier for the goods or services purchased.


### Performance Reporting
Your suppliers performance may impact your company’s ability to conduct business. To identify the suppliers who meet, or fail to meet, your company requirements, you can use the report options available in Oracle Purchasing and Oracle Business Intelligence. This enables you to analyze a supplier’s performance when making future procurement decisions.

### Flow of Default Values
Changes to default values affect only new records, not existing records.  
...................... 

### Define Supplier
```Supply Base > Suppliers``` or ```Buyer Work Center > Suppliers```

**Important info at the supplier header:**

- Organization Name (unique) (updatable)
- Country of Origin: for government reporting purposes
- Taxpayer ID: If the supplier is a corporation or partnership, use the federal identification number. If the supplier is an individual, use a social security number. Optionally enter the value-added tax (VAT) registration number in the Tax Registration Number field if you are entering a VAT supplier.

**Other Information**

*there is a great deal of information that can be collected about a supplier but we only need some of that to use the supplier in Oracle Purchasing transactions.*

- Quick Update
- **Company Profile**
	- Organization
	- Tax Details
	- Address Book
	- Contact Directory
	- Business Classification
	- Product & Service *- Identify which products and services this supplier provides. Not used by Oracle Purchasing.*
	- Banking Details
	- Surveys
- **Terms and Control**
	- Accounting
	- Tax and Reporting
	- Purchasing
	- Receiving
	- Payment Details
	- Relationship
	- Invoice Management

Supplier info - Page 221 - 244


### Define Supplier sites
### Manage Suppliers

### Maintaining supplier and supplier site information
If you want the changes to affect existing sites, then you must make the changes directly to the site. If you want the changes to affect new sites only, then you can make the changes to the supplier header. If you want the changes to affect both existing and new sites, then make the changes to both the supplier header and any existing supplier sites.

### Avoiding duplicate suppliers
Before setting up a new supplier, verify it doesn't already exist.  
System requires unique supplier names.  
If duplicate entries are found, consider using the Supplier Merge functionality to correct and consolidate records. 

### Merging suppliers
```Supply Base > Supplier Merge```
.......

### Merging suppliers reports

### Identify key reports

### Understand setup options

### Understand additional implementation considerations



### Define how supplier sites can be used with the following options:
- Pay - You can import/enter invoices for and make payments to the site.
- Primary Pay - Default pay site for invoice entry and import.
- Purchasing - You can create purchase orders for the site.
- RFQ Only - You can create request for quotations in Purchasing for the site. You cannot create purchase orders for an RFQ Only site.
- Procurement Card - You can purchase goods or services using a procurement card.
- Primary Pay - If a supplier has multiple pay sites, one can be designated as the primary. The primary pay site defaults in the Invoices window, helping to speed the invoice entry process. Also, Payables Open Interface Import uses this site when it imports an external invoice with no specified site.