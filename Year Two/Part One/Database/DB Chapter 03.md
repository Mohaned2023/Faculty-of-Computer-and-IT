### **ER Model Concepts: Entities and Attributes**
- ! **Entity:** *is a basic concept for the ER model. Entities are specific things or objects in the mini-world that are represented in the database.* ^bb5f33
- ! **Attributes:** *are properties used to describe an entity.* ^a84eec
- ? A specific entity will have a value for each of its attributes.
- ? Each attribute has a value set (or data type) associated with it.

### **Types of Attributes:**
- ! **Simple:** *Each entity has a single atomic value for the attribute. `SSN or Sex`* ^e64640
- ! **Composite:** *The attribute may be composed of several components. `Address(Street, City, State, ZipCode, Country)`* ^373439
- ! **Multi-valued:** *An entity may have multiple values for that attribute. `Color of a CAR or PreviousDegrees of a STUDENT.`* ^53273a
- ? In general, composite and multi-valued attributes may be nested arbitrarily to any number of levels, although this is rare.

### **Entity Types and Key Attributes:**
- ? Entities with the same basic attributes are grouped or typed into an entity type.
- ? An attribute of an entity type for which each entity must have a unique value is called a key attribute of the entity type.
- ? A key attribute may be composite.
- ? An entity type may have more than one key.
- ? Each key is underlined. (Note: this is different from the relational schema where only one “primary key is underlined).

### **Entity Set:**
- ? Each entity type (entity set or nentity collection) will have a collection of entities stored in the database.
- ? Same name (CAR) used to refer to both the entity type and the entity set.
- ? However, entity type and entity set may be given different names.
- ? Entity set is the current state of the entities of that type that are stored in the database.

### **Value Sets (Domains) of Attributes:**
- ? Each simple attribute is associated with a value set.
- ! **Value Set:** *specifies the set of values associated with an attribute.* ^a97ac7

### **Attributes and Value Sets:**
- ? Value sets are similar to data types in most programming languages.
- ? Mathematically, an attribute A for an entity type E whose value set is V is defined as a function.
- @ We refer to the value of attribute A for entity e as A(e).

### **Displaying an Entity type:**
- ? In ER diagrams, an entity type is displayed in a rectangular box.
- ? Attributes are displayed in ovals.

### **Relationships and Relationship Types:**
- ! **Relationship:** *relates two or more distinct entities with a specific meaning.* ^db059d
- ? Relationships of the same type are grouped or typed into a relationship type.
- ! **Degree of a relationship type:** *is the number of participating entity types.* ^ac2f72

### **Relationship type vs. relationship set:**
- ! **Relationship Type:** *Is the schema description of a relationship.* ^b469d5
	- ? Identifies the relationship name and the participating entity types.
	- ? Also identifies certain relationship constraints.
- ! **Relationship Set:** *The current set of relationship instances represented in the database.* ^6d530a
	- ? The current state of a relationship type.
- ? Previous figures displayed the relationship sets.
- ? Each instance in the set relates individual participating entities.
- ! In ER diagrams, we represent the relationship type as follows:
	- ! **Diamond-shaped box:** *is used to display a relationship type.* ^d06940
	- ? Connected to the participating entity types via straight lines.
	- ! Note that the relationship type is not shown with an arrow. The name should be typically be readable from left to right and top to bottom.

### **Constraints on Relationships:**
- ? (Also known as ratio constraints).
- ? Cardinality Ratio (specifies maximum participation):
	- @ One-to-one (1:1).
	- @ One-to-many (1:N) or Many-to-one (N:1).
	- @ Many-to-many (M:N).
- ? Existence Dependency Constraint (specifies minimum participation) (also called participation constraint):
	- @ zero (optional participation, not existence-dependent).
	- @ one or more (mandatory participation, existence-dependent).

### **Recursive Relationship Type:**
- ? A relationship type between the same participating entity type in distinct roles
- ? Also called a self-referencing relationship type.

### **Displaying a recursive relationship:**
- @ In a recursive relationship type:
	- ? Both participations are same entity type in different roles.
- ? In ER diagram, need to display role names to distinguish participations.

### **Weak Entity Types:**
- ! **Weak Entity:** *An entity that does not have a key attribute and that is identification-dependent on another entity type.* ^530cff
- ? A weak entity must participate in an identifying relationship type with an owner or identifying entity type.
- @ Entities are identified by the combination of:
	- ? A partial key of the weak entity type.
	- ? The particular entity they are related to in the identifying relationship  type.

### **Relationships of Higher Degree:**
- @ Relationship types of degree 2 are called binary.
- ? Relationship types of degree 3 are called ternary and of degree n are called n-ary.
- ? In general, an n-ary relationship is not equivalent to n binary relationships.
- ? Constraints are harder to specify for higher-degree relationships (n > 2) than for binary relationships.

### **Definitions:**
1. Entity: [[#^bb5f33|Here]].
2. Attributes: [[#^a84eec|Here]].
3. Simple: [[#^e64640|Here]].
4. Composite: [[#^373439|Here]].
5. Multi-valued: [[#^53273a|Here]].
6. Value Set: [[#^a97ac7|Here]].
7. Relationship: [[#^db059d|Here]].
8. Degree of a relationship type: [[#^ac2f72|Here]].
9. Relationship Type: [[#^b469d5|Here]].
10. Relationship Set: [[#^6d530a|Here]].
11. Diamond-shaped box: [[#^d06940|Here]].
12. Weak Entity: [[#^530cff|Here]].
