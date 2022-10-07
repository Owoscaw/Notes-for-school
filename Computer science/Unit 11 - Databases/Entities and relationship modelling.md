An entity is a category of an object. This object can be a person, an event, or anything of interest that needs it's related data recorded. An entity in a school database, for example, would be a student. Data about this student entity could be things such as grades, behaviour points, timetable, ect.

Notation:
>EntityName(entityData1, entityData2, entityData3, ...)

Each entity must be uniquely identifiable using an itentifier. In a relational database, the identifier is known as a primary key, and is underlined in entity notation. Sometimes two or more attributes are needed to uniquely identify a record, this is called a composite primary key. 

Entities can be linked together in one of three ways:
> One-to-one, one entity is only related to one other entity. They are exclusive to each other.
> One-to-many, one entity is related to more than one other entity. Many entities are exclusive to one entity, however this entity is not exclusive to any one of the many.
> Many-to-many, many entities are related to many other entities. Many entities may be related to many other entitiy, there is no exclusivity.

Entity Relationship Diagrams (ERDs) are a graphics way of representing relationships between entities. They consist of an entity, followed by a verb, then another entity. Symbols connecting both entities identify their relationship. A straight line represents a One-to or a to-one, a "crows foot" represents a Many-to or to-many. Intermediary entities can help resolve many-to-many relationships, which are bad because they are unweildy to work with, for example customer one-to-many subscription many-to-one product avoids a many-to-many relationship with customer and product.

The abstract idea of entity relationship is represented in a database by a table. Tables are often reffered to as "relations". A database can contain one or more relations, each relation has a row that contains a single record. The columns in a relation each contains on field (attribute) belonging to the records.

Relation | column 1 | column 2
----------------|----------------|-----------
row 1 | field 1 | field 2
row 2 | field 1 | field 2

Relationships can be created between entities by using the primary key from one in the other:
> Entity1(entity1PrimaryKey, data, ....)
> Entity2(entity2PrimaryKey, *entity1PrimaryKey*, data, ...)

The primary key from entity1 is included in entity2's description, noted in italics. Within entity2, entity1's primary key is known as a foriegn key. A forgien key should only be included in the descripton on the "many" side of the relationship.

Customer Database | customer ID | customer Address | customer name
------------------|-------------------|-------------|--------------
customer 1|1|Easton|Aleks
customer 2|2|Burtle|Oscar
customer 3|3|Cheddar|Fin

Product Database | product ID | product name | product location | *customer ID*
----------------|------------|-------------|------------|------------
product 1|A|crisps|tesco|*2*
product 2|B|sandwich|sainsburys|*3*

The relationship between primary and foriegn key dictates the type of relationship between entities. In the above example, customer ID is the foriegn key in the product database.

Refferential integrity dictates that if two entities are related, one will not exist without the other. For example, a teacher will never have no students and a student will never have no teachers.

In a many-to-many relationship, each table cannot be directly linked. This is because there would need to be many foreign key fields in both tables, which becomes messy and not good. Many-to-many relationships can be resolved with an intermediate table. For example, to avoid a many-to-many relaitonship between teacher and student, an intermediary table, class, can be introduced. This "middle" table will have to have two foriegn keys, one for each relationship. This makes the intermediary table have a many-to-one relationship with both tables that it resolved. Sometimes called the "link" table.