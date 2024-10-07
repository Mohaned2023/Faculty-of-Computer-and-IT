
### **Data Models:**
- ? **Data Model:** *A set of concepts to describe the structure of a database, the operations for manipulating these structures, and certain constraints that the database should obey.* ^46eb2a
- Data Model Structure and Constraints:
	- ? Constructs are used to define the database structure. ^590b49
	- Constructs typically include elements.
- ? **Data Model Operations:** *These operations are used for specifying database retrievals and updates by referring to the constructs of the data model.* ^5affe3
	- @ Operations on the data model may include basic model operations.

### **Categories of Data Models:**
- ! **Conceptual (high-level, semantic) data models:** *Provide concepts that are close to the way many users perceive data.* ^6efb8b
- ! **Physical (low-level, internal) data models:** *Provide concepts that describe details of how data is stored in the computer.* ^0e8375
- ! **Implementation (representational) data models:** *Provide concepts that fall between Conceptual and the Physical.* ^2e1344
- ! **Self-Describing Data Models:** *Combine the description of data with the data values.* ^21cca2

### **Schemas versus Instances:**
- ? **Database Schema:** *The description of a database.* ^90cacf
- ! **Schema Diagram:** *An illustrative display of (most aspects of) a database schema.* ^e5091a
- ! **Schema Construct:** *A component of the schema or an object within the schema.* ^76db15
- ! **Database State:** *The actual data stored in a database at a particular moment in time.* ^4ea756
	- ? Also called database instance (or occurrence or snapshot).
	- ? The term instance  is also applied to individual database components.

### **Database Schema vs Database State:**
- @ **Database State:** *Refers to the content of a database at a moment in time.* 
- ! **Initial Database State:** *Refers to the database state when it is initially loaded into the system.* ^943382
- ! **Valid State:** *A state that satisfies the structure and constraints of the database.* ^b30de2
- ! **Distinction**

> [!TIP]
> - The database <u>schema</u> changes very <u>infrequently</u>.
> - The database <u>state</u> changes every time the <u>database is updated</u>.

> [!IMPORTANT]
> - <u>Schema</u> is also called <u>intension</u>.
> - <u>State</u> is also called <u>extension</u>.

### **Three-Schema Architecture:**
- ! **Internal schema:** *at the internal level to describe physical storage structures and access paths (e.g indexes).* ^782250
- ! **Conceptual schema:** *at the conceptual level to describe the structure and constraints for the whole database for a community of users.* ^8cd9e3
- ! **External schemas:** *at the external level to describe the various user views.* ^e761ff

### **Definitions:**
1. Data Model: [[#^46eb2a|Here]].
2. Constructs: [[#^590b49|Here]].
3. Data Model Operations: [[#^5affe3|Here]].
4. Conceptual (high-level, semantic) data models: [[#^6efb8b||Here]].
5. Physical (low-level, internal) data models: [[#^0e8375|Here]].
6. Implementation (representational) data models: [[#^2e1344|Here]].
7. Self-Describing Data Models: [[#^21cca2|Here]].
8. Database Schema: [[#^90cacf|Here]].
9. Schema Diagram: [[#^e5091a|Here]].
10. Schema Construct: [[#^76db15|Here]].
11. Database State: [[#^4ea756|Here]].
12. Initial Database State: [[#^943382|Here]].
13. Valid State: [[#^b30de2|Here]].
14. Internal schema: [[#^782250|Here]].
15. Conceptual schema: [[#^8cd9e3|Here]].
16. External schemas: [[#^e761ff|Here]].