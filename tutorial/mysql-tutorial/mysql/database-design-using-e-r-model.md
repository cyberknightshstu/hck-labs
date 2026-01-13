# Database Design Using E-R Model

* [ ] Overview of the Design Process
* [ ] The Entity-Relationship Model
* [ ] Complex Attributes
* [ ] Mapping Cardinalities
* [ ] Primary Key
* [ ] Removing Redundant Attributes in Entity Sets
* [ ] Reducing ER Diagrams to Relational Schemas
* [ ] Extended E-R Features
* [ ] Entity-Relationship Design Issues
* [ ] Alternative Notations for Modeling Data
* [ ] Other Aspects of Database Design
* [ ] Extended E-R Features
* [ ] Entity-Relationship Design Issues
* [ ] Alternative Notations for Modeling Data
* [ ] Other Aspects of Database Design



### Design Phases

* Initial phase -- characterize fully the data needs of the prospective database users.
* Second phase -- choosing a data model
  * Applying the concepts of the chosen data model
  * Translating these requirements into a conceptual schema of the database.
  * A fully developed conceptual schema indicates the functional requirements of the enterprise.
    * Describe the kinds of operations (or transactions) that will be performed on the data.
* Final Phase -- Moving from an abstract data model to the implementation of the database
  * Logical Design – Deciding on the database schema.
    * Database design requires that we find a “good” collection of relation schemas.
    * Business decision – What attributes should we record in the database?
    * Computer Science decision – What relation schemas should we have and how should the attributes be distributed among the various relation schemas?
  * Physical Design – Deciding on the physical layout of the database



### Design Alternatives

* In designing a database schema, we must ensure that we avoid two major pitfalls:
  * Redundancy: a bad design may result in repeat information.\
    Redundant representation of information may lead to data inconsistency among the various copies of information
  * Incompleteness: a bad design may make certain aspects of the enterprise difficult or impossible to model.
* Avoiding bad designs is not enough. There may be a large number of good designs from which we must choose.



### &#x20;Design Approaches

* Entity Relationship Model (covered in this chapter)
  * Models an enterprise as a collection of entities and relationships
    * Entity: a “thing” or “object” in the enterprise that is distinguishable from other objects
      * Described by a set of attributes
    * Relationship: an association among several entities
  * Represented diagrammatically by an entity-relationship diagram:
* Normalization Theory (Chapter 7)
  * Formalize what designs are bad, and test for them



## Outline of the ER Model

### ER model -- Database Modeling

* The ER data mode was developed to facilitate database design by allowing specification of an enterprise schema that represents the overall logical structure of a database.
* The ER data model employs three basic concepts:
  * entity sets,
  * relationship sets,
  * attributes.
* The ER model also has an associated diagrammatic representation, the ER diagram, which can express the overall logical structure of a database graphically.



### &#x20;Entity Sets

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

### Entity Sets -- instructor and student

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

### Representing Entity sets in ER Diagram

* Entity sets can be represented graphically as follows:
  * Rectangles represent entity sets.
  * Attributes listed inside entity rectangle
  * Underline indicates primary key attributes

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>





### Relationship Sets

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

* Example: we define the relationship set advisor to denote the associations between students and the instructors who act as their advisors.
* Pictorially, we draw a line between related entities.

<figure><img src="../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

### &#x20;Representing Relationship Sets via ER Diagrams

* Diamonds represent relationship sets.

<figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

* An attribute can also be associated with a relationship set.
* For instance, the advisor relationship set between entity sets instructor and student may have the attribute date which tracks when the student started being associated with the advisor

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

### Relationship Sets with Attributes

<figure><img src="../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

### Roles

* Entity sets of a relationship need not be distinct&#x20;
  * Each occurrence of an entity set plays a “role” in the relationship&#x20;
* The labels “course\_id” and “prereq\_id” are called roles.



