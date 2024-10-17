### **Informal Definitions:**
- ! Informally, a relation looks like a table of values.
- ! **Relation:** *typically contains a <u>set of rows</u>.* ^2141f1
- ? The data elements in each row represent certain facts that correspond to a real-world entity or relationship.
	- ! In the formal model, rows are called <u>tuples</u>.
- ? Each column has a column header that gives an indication of the meaning of the data items in that column.
	- ! In the formal model, the column header is called an <u>attribute name</u> (or just <u>attribute</u>).
- ? Key of a Relation:
	- ! Each row has a value of a data item (or set of items) that uniquely identifies that row in the table (Called the <u>key</u>).
	- ! Sometimes row-ids or sequential numbers are assigned as keys to identify the rows in a table (Called <u>artificial key</u> or <u>surrogate key</u>).

### **Formal Definitions - Domain:**
- ! A domain has a logical definition.
- ! A domain also has a data-type or a format defined for it.
- ! The attribute name designates the role played by a domain in a relation.

### **Relational Integrity Constraints:**
- ! **Constraints:** *are <u>conditions</u> that must hold on <u>all</u> valid relation states.* ^ec1ca9
- ? There are three main types of (explicit schema-based) constraints that can be expressed in the relational model:
	- ! Key constraints.
	- ! Entity integrity constraints.
	- ! Referential integrity constraints.
- ? Another schema-based constraint is the domain constraint: 
	- ! Every value in a tuple must be from the domain of its attribute (or it could be null, if allowed for that attribute).

### **Key Constraints:**
- ! If a relation has several <u>candidate keys</u>, one is chosen arbitrarily to be the <u>primary key</u>.
	- ? The primary key attributes are <u>underlined</u>.
- ! The primary key value is used to uniquely identify each tuple in a relation:
	- ? Provides the <u>tuple identity</u>.
- ! Also used to <u>reference</u> the tuple from another tuple

### **Displaying a relational database schema and its constraints:**
- ? Each relation schema can be displayed as a row of attribute names.
- ? The name of the relation is written above the attribute names.
- ? The primary key attribute (or attributes) will be underlined.
- ? A foreign key (referential integrity) constraints is displayed as a directed arc (arrow) from the foreign key attributes to the referenced table.

### **Definitions:**
1. Relation: [[#^2141f1|Here]].
2. Constraints: [[#^ec1ca9|Here]].