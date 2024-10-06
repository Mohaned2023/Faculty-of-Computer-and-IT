### **Types of Databases and Database Applications:**

- @ **Traditional Applications:**
	- Numeric and Textual Databases
- @ **More Recent Applications:**
	- Multimedia Databases
	- Geographic Information Systems (GIS)
	- Biological and Genome Databases
	- Data Warehouses
	- Mobile databases
	- Real-time and Active Databases

### **Impact of Databases:**

- ? Businesses. `Banking`
- ? Service Industries. `Small businesses`
- ? Education. `Resources for content and Delivery`
- ? More recently. `Social Networks`
- ? Personalized Applications. `smart mobile devices`
### **Basic Definitions:**

- **Database:** *A collection of related data.* ^fe9cbc
- **Data:** *Known facts that can be recorded and have an implicit meaning.* ^043eed
- **Mini-world:** *Some part of the real world about which data is stored in a database. `student grades and transcripts at a university.`* ^630aed
- **Database Management System (DBMS):** *A software package/ system to facilitate the creation and maintenance of a computerized database.* ^412f77

### **Typical DBMS Functionality:**

- ? **Meta-data:** *Database definition or descriptive information.* ^20a3b5
	- @ Stored by the DBMS in the form of a database catalog or dictionary.
- ? Construct or Load the initial database contents on a secondary storage medium.
- ? Manipulating the database:
	- @ Retrieval.
	- @ Modification.
	- @ Accessing the database through Web applications.
- ? Sharing.
- ? Protection includes.
- ? Maintain the database system.

### **Application Activities Against a Database:**

- @ Applications interact with a database by generating:
	- ? **Queries:** *that access different parts of data and formulate the result of a request.* ^153476
	- ? **Transactions:** *that may read some data and “update” certain values or generate new data and store that in the database.* ^b3faf7
- @ Applications must not allow unauthorized users to access data.
- @ Applications must keep up with changing <u>user requirements</u> against the database.

### **Main Characteristics of the Database Approach:**

- @ Self-describing nature of a database system.
- @ Insulation between programs and data:
	- ? **program-data independence:** *Allows changing data structures and storage organization without having to change the DBMS access programs.* ^e07616
- @ Data Abstraction:
	- ? **Data model:** *is used to hide storage details and present the users with a conceptual view  of the database.* ^a3b50b
- @ Support of multiple views of the data.
- @ Sharing of data and multi-user transaction processing:
	- ? **OLTP (Online Transaction Processing):** *is a major part of database applications. This allows hundreds of concurrent transactions to execute per second.* ^bf236f

### **Advantages of Using the Database Approach:**

- ? Controlling redundancy in data storage and in development and maintenance efforts.
- ? Restricting unauthorized access to data.
- ? Providing persistent storage for program Objects.
- ? Providing Storage Structures (e.g. indexes) for efficient Query Processing.
- ? Providing optimization of queries for efficient processing.
- ? Providing backup and recovery services.
- ? Providing multiple interfaces to different classes of users.
- ? Representing complex relationships among data.
- ? Enforcing integrity constraints on the database.
- ? Drawing inferences and actions from the stored data using deductive and active rules and triggers.
- @ Potential for enforcing standards.
- @ Reduced application development time.
- @ Flexibility to change data structures.
- @ Availability of current information.
- @ Economies of scale.

### **When not to use a DBMS:**

1. ! Main inhibitors (costs) of using a DBMS.
2. ! When a DBMS may be unnecessary.
3. ! When a DBMS may be infeasible.
4. ! When no DBMS may suffice.
### **Definitions:**
1. Database: [[#^fe9cbc|Here]].
2. Data: [[#^043eed|Here]].
3. Mini-world: [[#^630aed|Here]].
4. Database Management System (DBMS): [[#^412f77|Here]].
5. Meta-data: [[#^20a3b5|Here]].
6. Queries: [[#^153476|Here]].
7. Transactions: [[#^b3faf7|Here]].
8. Program-data independence: [[#^e07616|Here]].
9. Data model: [[#^a3b50b|Here]].
10. OLTP (Online Transaction Processing): [[#^bf236f|Here]].
