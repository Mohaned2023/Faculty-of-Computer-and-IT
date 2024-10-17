### **Informal Design Guidelines for Relational Databases:**
- ! **Relational database design:** *The grouping of attributes to form <u>good</u> relation schemas.* ^eea350
- ? Two levels of relation schemas:
	- ! The logical <u>user view</u> level.
	- ! The storage <u>base relation</u> level.
- ? Design is concerned mainly with base relations.

### **Redundant Information in Tuples and Update Anomalies:**
- ! Information is stored redundantly:
	- ? Wastes storage.
	- ? Causes problems with update anomalies.
		- @ Insertion anomalies.
		- @ Deletion anomalies.
		- @ Modification anomalies.

### **Functional Dependencies:**
- ! **Functional dependencies (FDs):** *are used to specify formal measures of the "goodness" of relational designs.* ^eb976e
- ? And keys are used to define <u>normal forms</u> for relations.
- ? Are <u>constraints</u> that are derived from the meaning  and interrelationships  of the data attributes.

### **Defining FDs from instances:**
- ? An FD is a property of the attributes in the schema R.
- ? Given the instance (population) of a relation, all we can conclude is that an FD <u>may exist</u> between certain attributes.
- ? that certain FDs do not exist because there are tuples that show a violation of those dependencies.

### **Normalization of Relations:**
- ! **Normalization:** *The process of decomposing unsatisfactory <u>bad</u> relations by breaking up their attributes into smaller relations.*
- ! **Normal form:** *Condition using keys and FDs of a relation to certify whether a relation schema is in a particular normal form.*
- ? 2NF, 3NF, BCNF : based on keys and FDs of a relation schema.
- ? 4NF : based on keys, multi-valued dependencies (MVDs).
- ? 5NF : based on keys, join dependencies (JDs).
- ! **Denormalization:** *The process of storing the join of higher normal form relations as a base relation.* ^771473

### **Definitions of Keys and Attributes Participating in Keys:**
- ! If a relation schema has more than one key, each is called a <u>candidate key</u>.
- ! A <u>Prime attribute</u> must be a member of some candidate key.
- ! A Nonprime attribute is not a prime attribute—that is, it is not a member of any candidate key.

### **First Normal Form:**
- ? Disallows:
	- ! composite attributes.
	- ! multivalued attributes.
	- ! nested relations; attributes whose values for an individual tuple are non-atomic.
- ? Considered to be part of the definition of a relation.
- ? Most RDBMSs allow only those relations to be defined that are in First Normal Form.

### **Second Normal Form:**
- ? Uses the concepts of FDs, primary key
- ? Definitions:
	- ! **Prime attribute:** *An attribute that is member of the primary key K.* ^712da0
	- ! **Full functional dependency:** *a FD  Y -> Z where removal of any attribute from Y means the FD does not hold any more.* ^62ebfc
- ? A relation schema R is in <u>second normal form (2NF)</u> if every non-prime attribute A in R is fully functionally dependent on the primary key.
- ? R can be decomposed into 2NF relations via the process of 2NF normalization or <u>second normalization</u>.

### **Third Normal Form:**
- ? Definition:
	- ! **Transitive functional dependency:** *a FD  X -> Z that can be derived from two FDs   X -> Y and Y -> Z.* ^002b2d
- ? A relation schema R is in <u>third normal form (3NF)</u> if it is in 2NF and no non-prime attribute A in R is transitively dependent on the primary key.
- ? R can be decomposed into 3NF relations via the process of 3NF normalization.

### **Definitions:**
1. Relational database design: [[#^eea350|Here]].
2. **Bottom Line:** *Design a schema that can be explained easily relation by relation.*
3. Functional dependencies (FDs): [[#^eb976e|Here]].
4. Denormalization: [[#^771473|Here]].
5. Prime attribute: [[#^712da0|Here]].
6. Full functional dependency: [[#^62ebfc|Here]].
7. Transitive functional dependency: [[#^002b2d|Here]].