### **Subclasses and Superclasses:**
- ? An entity type may have additional meaningful subgroupings of its entities.
- ! EER diagrams extend ER diagrams to represent these additional subgroupings, called subclasses or subtypes.
- @ Note: An entity that is member of a subclass represents the same real-world entity as some member of the superclass:
	- ? The subclass member is the same entity in a distinct specific role.
	- ! An entity cannot exist in the database merely by being a member of a subclass; it must also be a member of the superclass.
	- ? A member of the superclass can be optionally included as a member of any number of its subclasses
- ! It is not necessary that every entity in a superclass be a member of some subclass.

### **Attribute Inheritance in Superclass/Subclass Relationships:**
- ? An entity that is member of a subclass inherits:
	- ! All attributes of the entity as a member of the superclass.
	- ! All relationships of the entity as a member of the superclass.
### **Specialization:**
- ! **Specialization:** *is the process of defining a set of subclasses of a superclass.* ^32a8d8
- ? The set of subclasses is based upon some distinguishing characteristics of the entities in the superclass.

### **Generalization:**
- ! **Generalization:** *is the reverse of the specialization process.* ^ce7ff3
- ? Several classes with common features are generalized into a superclass;
	- ! original classes become its subclasses.

### **Generalization and Specialization:**
- @ Data Modeling with Specialization and Generalization:
	- ! A superclass or subclass represents a collection (or set or grouping) of entities.
	- ! It also represents a particular type of entity.
	- ! Shown in rectangles in EER diagrams (as are entity types).
	- ! We can call all entity types (and their corresponding collections) **<u>classes</u>**, whether they are entity types, superclasses, or subclasses.

### **Types of Specialization:**
1. ! **Predicate-defined ( or condition-defined):** *based on some predicate. ^e55287
2. ! **Attribute-defined:** *shows the name of the attribute next to the line drawn from the superclass toward the subclasses.* ^0b3288
3. ! **User-defined:** *membership is defined by the user on an entity by entity basis.* ^962de8

### **Constraints on Specialization and Generalization:**
- ? If we can determine exactly those entities that will become members of each subclass by a condition, the subclasses are called predicate-defined (or condition-defined) subclasses.
	- ! **Condition Constraint:** *is a constraint that determines subclass members.* ^14fa78
- ? If all subclasses in a specialization have membership condition on same attribute of the superclass, specialization is called an attribute-defined specialization.
	- ! **Specialization Attribute:** *is called the defining attribute of the specialization.* ^d8416c
- ? If no condition determines membership, the subclass is called user-defined.
	- ! Membership in a subclass is determined by the database users by applying an operation to add an entity to the subclass.
	- ! Membership in the subclass is specified individually for each entity in the superclass by the user.
- ? Two basic constraints can apply to a specialization/generalization:
	- ? Disjointness Constraint:
		- ! Specifies that the subclasses of the specialization must be disjoint.
		- ! If not disjoint, specialization is overlapping.
	- ? Completeness (Exhaustiveness) Constraint:
		- ! Total specifies that every entity in the superclass must be a member of some subclass in the specialization/generalization.
		- ! Partial allows an entity not to belong to any of the subclasses.
- ? Hence, we have four types of specialization/generalization:
	- ! Disjoint, total
	- ! Disjoint, partial
	- ! Overlapping, total
	- ! Overlapping, partial
> [!NOTE]
> Generalization usually is total because the superclass is derived from the subclasses.

### **Specialization/Generalization Hierarchies, Lattices & Shared Subclasses:**
- ? A subclass may itself have further subclasses specified on it.
- ? Hierarchy has a constraint that every subclass has only one superclass (called single inheritance); this is basically a tree structure.
- ? In a lattice, a subclass can be subclass of more than one superclass (called multiple inheritance).
- ? In a lattice or hierarchy, a subclass inherits attributes not only of its direct superclass, but also of all its predecessor superclasses.
- ? A subclass with more than one superclass is called a shared subclass (multiple inheritance).
- @ Can have:
	- ! nspecialization hierarchies or lattices.
	- ! ngeneralization hierarchies or lattices.
	- ! ndepending on how they were derived.
- ? We just use specialization (to stand for the end result of either specialization or generalization).
- ? In specialization, start with an entity type and then define subclasses of the entity type by successive specialization (top down conceptual).
- ? In generalization, start with many entity types and generalize those that have common properties (bottom up conceptual).
- ? In practice, a combination of both processes is usually employed.

### **Categories (UNION TYPES):**
- @ A shared subclass is a subclass in:
	- ! more than one distinct superclass/subclass relationships.
	- ! each relationships has a single superclass.
	- ! shared subclass leads to multiple inheritance.
- ? In some cases, we need to model a single superclass/subclass relationship with more than one superclass.
- ! Superclasses can represent different entity types.
- ! Such a subclass is called a category or UNION TYPE.
- ? Difference from shared subclass, which is a:
	- ! subset of the intersection of its superclasses.
	- ! shared subclass member must exist in all of its superclasses.

### **Alternative diagrammatic notations:**
- ? ER/EER diagrams are a specific notation for displaying the concepts of the model diagrammatically.
- @ DB design tools use many alternative notations for the same or similar concepts.
- @ One popular alternative notation uses UML class diagrams.

### **Knowledge Representation:**
- @ Deals with modeling and representing a certain domain of knowledge.
- ? Typically done by using some formal model of representation and by creating an Ontology.
- ? An ontology for a specific domain of interest describes a set of concepts and interrelationships among those concepts.
- ? An Ontology serves as a “schema” which enables interpretation of the knowledge in a “knowledge-base”.
- @ COMMON FEATURES between KR and Data Models:
	- ! Both use similar set of abstractions – classification, aggregation, generalization, and identification.
	- ! Both provide concepts, relationships, constraints, operations and languages to represent knowledge and model data.
- @ DIFFERENCES:
	- ! KR has broader scope.
	- ! KR schemes typically include rules and reasoning mechanisms for inferencing.
	- ! Most KR techniques involve data and metadata.
	- ! KR is used in conjunction with artificial intelligence systems to do decision support applications.

### **Ontologies:**
- @ Use conceptual modeling and other tools to develop “a specification of a conceptualization”:
	- ! Specification refers to the language and vocabulary (data model concepts) used.
	- ! Conceptualization refers to the description (schema) of the concepts of a particular field of knowledge and the relationships among these concepts.
- ? Many medical, scientific, and engineering ontologies are being developed as a means of standardizing concepts and terminology
### **Definitions:**
1. Specialization: [[#^32a8d8|Here]].
2. Generalization: [[#^ce7ff3|Here]].
3. Predicate-defined: [[#^e55287|Here]].
4. Attribute-defined: [[#^0b3288|Here]].
5. User-defined: [[#^962de8|Here]].
6. Condition Constraint: [[#^14fa78|Here]].
7. Specialization Attribute: [[#^d8416c|Here]].