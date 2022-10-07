The process through which the best possible design of a database is created is called normalisation. Tables should be organised such that data is not repeated in the same, or different, tables. The structure should allow for complex queries. There are three stages to normalisation:
> First normal form, 1NF
> Second normal form, 2NF
> Third normal form, 3NF

## First normal form:
A table is in first normal form if there are no repeating attributes or groups of attributes. All attroibutes must be atomic, as in it contains a single unit of information. Cannot consist of two data items. Often data can be resolved into 1NF by introducing a third table in the middle, see the end of [[Entities and relationship modelling |this page]].

## Second normal form:
A table is in second normal form if it is in first normal form and contains no partial dependencies. This only occurs when the primary key is a composite key, as in one foriegn key relies on the other and vice versa. The combination of these foriegn keys form the primary key of the table.

## Third normal form:
A table is in third normal form if it is in second normal form (and therefore 1NF) and contains no non-key dependencies. This can be defined by saying "All attributes are dependent on the key, the whole key, and nothing but the key" - couldn't make this shit up if I tried. All attributes that are independant of the primary key should be extracted to their own table and said table's foreign key should be used to make the composite key.

---------------------------------------

Normalisation is important because it allows databases to be easier to maintain and change. There is no unecessary duplication of data, and integrity is maintained - if one attribute gets changed that relies on many others, the update only needs to happen in one table. Smaller tables with fewer fields means faster searches and smaller storage requirements.

If one record is deleted off of on table that is linked to many, data integrity dictates that all other records linked to the deleted one are not allowed and are also deleted. The same holds for any updates to a record.