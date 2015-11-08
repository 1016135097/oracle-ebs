# Documents

###	 Document Types
- **Requisitions** - Purchase and Internal
- **Requests for Quotations** - Bid, Catalog and Standard
- **Quotations** - Bid, Catalog and Standard
- **Purchase Agreements** - Blanket and Contract
- **Purchase Orders** - Standard and Planned
- **Releases** - Blanket and Planned

**You cannot enter new document types**; you can enter new document subtypes only for RFQs and quotations.

### Document Type Settings
```Purchasing Responsibility > Setup > Purchasing > Document Types```   
Click Update on the document type you want to edit  
[All Settings](/purchasing/doctypeset)  
![Document Type Settings](/images/doctypesit.png)

### Security Levels
Anyone with menu access to the document entry window can create a document. These individuals then become the document owners.  
**Security level options include**:  

- **Private** - Only the document owner and subsequent approvers can access the document.
- **Purchasing** - Only the document owner, subsequent approvers, and individuals defined as buyers can access the document.
- **Hierarchy** - Only the document owner, subsequent approvers, and individuals above the document owner in the security hierarchy can access the document.
- **Public** - All system users can access the document.


### Access Levels  
Document owners always have full access to their documents.  
**Access level options include:**

- **View Only** - Accessing employees can only view the document. Only the document owner may modify or control the document.
- **Modify** - Accessing employees can view, modify, freeze and close the document.
- **Full** - Accessing employees can view, modify, freeze, close, cancel and finally close the document.

### Document Approvals and routing process

When Oracle Human Resources is used in conjunction with Oracle Purchasing, they share
employee information and job and position information. Consider your requirements from
both perspectives before deciding on a configuration of security, approval and routing features.
For each job or position, you will be able to establish approval authorization rules that define
whether the person holding the job or position can approve the document. 

- Jobs are general, positions are specific.   
- One job can have multiple positions associated with it.   
- Many employees may hold the same job or position.   
- If Oracle Human Resources is installed, an employee can hold more than one position, but only one position is  used to assign rules.   
- If only Oracle Purchasing is installed, an employee can hold only one position. 


### Employee / Supervisor Relationship

if Human Resources is installed assign supervisor from:   
```Human Resources > Work Structure > Position > Description ```   
![Assigning Supervisor](/images/supervisor.png)

- define your approval routing structures as you enter employees using the Enter Person window. In this case, Oracle Purchasing does not require that you set up positions, allowing you to assign approval groups to either jobs or positions. 
- Employee/supervisor relationships must be maintained each time there is a change to the relationship. 
- Each employee can have only one supervisor.


**Employee/Supervisor Approval Path:**

If you are using the employee/supervisor relationship to determine approval paths, the system will locate the approver as follows:

- User Name of person submitting document for approval
- Employee Name attached to the User Name
- Supervisor Name attached to the Employee Record

Assuming the person submitting the document for approval is unable to approve the document, workflow will route the document to the Notifications In-Box of the User Name for the Supervisor.

**Global Supervisor/Approver**   
For organizations using Employee/Supervisor approval routing, you can route the document to approvers in other business groups.  

- Set the profile HR: Cross Business Groups to Yes at the site Level.

### Position approval hierarchies
```Human Resources > Work Structures > Position > Hierarchy ```

- must set up both jobs and positions
- easy to maintain and allow you to define approval routing structures that remain stable regardless of how frequently individual employees move within your organization or terminate their employment
- all positions you want to include in your hierarchies must be included in the Business Group you set in the Financial Options window.
- A single position can be added to one or more hierarchies, but a position cannot appear in a
single hierarchy more than once
- You may be build a single hierarchy for use by all document types, a separate hierarchy for each document type or multiple hierarchies per document type
- Some implementations create a main hierarchy for a document type along with possibly several alternate hierarchies. The main hierarchy is defined on the Document Type window as the default, with the alternate hierarchies available for overriding the defaulting hierarchy

**Position Approval Hierarchies Approval Path:**   

If you are using a position approval hierarchy to determine approval paths, the system will locate the approver as follows:

- User Name of person submitting document for approval
- Employee Name attached to the User Name
- Position Name attached to the Employee Name
- Position Name of parent in hierarchy for this Position Name
- Employee Name of parent Position Name
- User Name attached to the parent Employee Name

Assuming the person submitting the document for approval is unable to approve the document, workflow will route the document to the Notifications In-Box of the User Name for the parent Position Name or to the first position that has the sufficient approval authority to approve the document (Forward Method of Direct versus Hierarchy).


### Strengths and Weaknesses of Approvals Paths 

### Approval Workflow
You can accept the default workflow or if you customized a workflow of your own and want to associate it with a specific document type, you can choose that workflow instead.


### Approvals Group
By default, all accounts are excluded from an approval group and therefore documents governed by this approval group cannot be approved. You avoid this situation by ensuring that there is at least one Account Range Include rule on every Approval Group.

### Approvals Assignment


### Running Fill Employee Hierarchy Request

### Setup as Worker and Buyer to be able to open purchasing windows


### Reports

- **Employee Listing**  
	Lists employee number, employee name, supervisor, location and expense account for all active employees. Additionally lists the same information for all inactive employees along with the inactive date.
- **Employee Organization Movements Report**  
	Lists new hires, terminations, transfers in and transfer out of a selected organization, or organization hierarchy. This report can be submitted from various HRMS responsibilities or can be added to a purchasing responsibility.
- **Position Hierarchy Report**  
	Displays the relationship between the positions in a hierarchy. The report also lists the current holders of each position in the hierarchy. This report can be submitted from various HRMS responsibilities or can be added to a Purchasing responsibility.

### Setup

- which document types
- which approval routing
- settings (document type settings, financial options "business group, use approval hierarchy")
- setup hierarchy, or supervisor relationship
- setup approvals group, and approvals assignment

### Additional implementation considerations
**What if there is more than one holder in a job or position?**  
Multiple holders in the same job or position can only occur if Oracle Human Resources is installed. If only Oracle Purchasing is installed, you can assign only one employee to each job or position. If multiple holders exist when using position approval hierarchies, Oracle Workflow will route the document to the holder based on alphabetical order. You can see who the system will route the document to by clicking the Forward radio button, overriding the defaulted name if needed.

**What if there are changes to the position approval hierarchy?**  
Personnel changes are updated in the position approval hierarchy by running the Fill Employee Hierarchy process which reviews the employee record to determine the current position assignment. You will probably want to schedule this process to run on a frequent basis to ensure smooth processing of all approval requests. Structural changes to the position approval hierarchy require the hierarchy to be rebuilt from the point where the change occurs to the bottom of that branch. Documents are routed according to the hierarchy in effect at the time they are submitted for approval.

**What if Human Resources was already implemented with jobs set up, but no positions?**  
Unless the decision to set up jobs only and no positions can be revisited, you will have to route all documents by the employee/supervisor relationship and maintain this data on the employee records.

**What if the approver is unavailable for an extended period?**  
Oracle Purchasing has the ability to automatically forward documents when users do not respond to notifications. This tool should be used when possible to prevent documents from holding up business productivity. Oracle Workflow manages this functionality, typically set up to send a first and second reminder after pre-determined time periods before forwarding the notification to the next approver.

**What if the document has a status of Pre-Approved?**  
The status of Pre-Approved is the outcome of a person forwarding a document for approval even though the forwarding person has the necessary authority to approve it. The document may have been forwarded by mistake or for business reasons. Once the person it was forwarded to approves the document, the status will be changed to Approved and subsequent actions such as receiving and invoicing can be completed. 

**What if there is no account range on an approval group assigned to a job or position?**  
By default, all accounts are excluded from an approval group and therefore documents governed by this approval group cannot be approved. You avoid this situation by ensuring that there is at least one Account Range Include rule on every Approval Group.

**What if Workflow can’t find a supervisor to approve the document?**  
If this occurs, the person submitting the request for approval must forward the document to a different person in the list of values for Forward To. If this isn’t done, the document will be returned to an Incomplete status and a notification will be sent stating No Approver Found - Please Select a Forward To Employee. If using employee/supervisor relationship to determine approval paths, the list of values will include all active employees. If using position approval hierarchies to determine approval paths, the list of values will include all employees in the hierarchy selected.

**What if a job or position has different authority levels for different document types?**  
You may have jobs or positions that can approve one document up to a specified dollar amount, while they can approve another document at a lower dollar amount. If this occurs, simply set up multiple approval groups with the rules properly defined for the differences and ensure that the right approval group is assigned to the correct document type.

**What if documents flow employee/supervisor, but approval rules are needed?**  
Approval Groups can be used whether approval paths are determined by employee/supervisor relationships or by position approval hierarchies.