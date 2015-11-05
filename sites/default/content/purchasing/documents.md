# Documents

###	 Document Types
- **Requisitions** - Purchase and Internal
- **Requests for Quotations** - Bid, Catalog and Standard
- **Quotations** - Bid, Catalog and Standard
- **Purchase Agreements** - Blanket and Contract
- **Purchase Orders** - Standard and Planned
- **Releases** - Blanket and Planned

**You cannot enter new document types**; you can enter new document subtypes only for RFQs and quotations.

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



### Position approval hierarchies
```Human Resources > Work Structures > Position > Hierarchy ```

- must set up both jobs and positions
- easy to maintain and allow you to define approval routing structures that remain stable regardless of how frequently individual employees move within your organization or terminate their employment
- all positions you want to include in your hierarchies must be included in the Business Group you set in the Financial Options window.
- A single position can be added to one or more hierarchies, but a position cannot appear in a
single hierarchy more than once
- You may be build a single hierarchy for use by all document types, a separate hierarchy for each document type or multiple hierarchies per document type
- Some implementations create a main hierarchy for a document type along with possibly several alternate hierarchies. The main hierarchy is defined on the Document Type window as the default, with the alternate hierarchies available for overriding the defaulting hierarchy





### Reports
### Setup Options
### Additional implementation considerations



