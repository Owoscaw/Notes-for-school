## Creation:

Tables can be created using the CREATE keyword, followed by a set of brackets, in which all columns (and which data types are accepted) are defined. There are many data types in SQL:
> Integer
> Char
> VarChar
> Boolean
> Currency
> Time

Linked tables can be defined by defining a column with the FOREIGN KEY keyword, followed by the name of the foriegn key, then the REFERENCE keyword and the table it is from. Data types of key definintions have to be the same in both tables:
```SQL
CREATE TABLE tblExample (
	PRIMARY KEY exampleID
	FORIEGN KEY otherExampleID REFERENCES tblOtherExample
	columnExample DATA TYPE
)
```



## Alteration:

The ALTER TABLE keyword can be used to add, delete, or modify columns in a pre-existing table, for example:

Adding a column:

ALTER TABLE tblExample
ADD ColumnExample EXAMPLE DATA TYPE


Deleting a column:

ALTER TABLE tblExample
DROP ColumnExample

Modifying a column:

ALTER TABLE tblExample
MODIFY COLUMN ColumnExample EXAMPLE DATA TYPE

## Updating:

The INSERT INTO command can be used to add a new record to a table, for example:

INSERT INTO Product (ProductID, Description, Price)
VALUES ("A345", "Pink Rabbit", 7.50)

Values need to be listed in the order in which they are defined in the INSERT INTO line. 

The UPDATE statement is used to update an existing record within a table. This command has to have a WHERE clause, to specify which record or records need to be changed:

UPDATE tblExample
SET exampleColumn = "example", anotherExampleColumn = "another example"
WHERE criteriaColumn = "criteria

The DELETE command is used to delete a record from a table, again the WHERE clause has to be included so that every record is not deleted:

DELETE FROM tblExample
WHERE exampleColumn = "example"




## Client-server database:

A client-server database can provide simultanous access to a database for multiple clients. A Database Management System (DMBS) is a pirce of software responsible for processing client requests. For example, when queerying a bank database, a client program will forward a request to a server program that manages the request.

Record locking prevents simultanious access to objects in a database in order to rpevent updates being lost of inconsistanceis in the data arising. For example, multiple people could be trying to save to a record at the same time, one could override the other and prevent an ongoing change. With record locking, only one change can be active at a time. One person has to wait for another to finish updating or altering a record.

Serialisation is an alternative technique used to ensure that transactions in a database do not overlap in time. This can be implimented via timestamp ordering. Every object in the database has a read timestamp and a write timestamp. Both are updated whenever an object is read or written to. When a user tries to save an update, the update can be denied if the read timestamp has changed since the user read the object - this is because another used must be editting the same object.

Another serialisation technique to ensure no transactions are lost is commitment ordering. This is where transactions are ordered in terms of their dependencies on one another as well as the time at which they were initiated.

Some advantages of a client-server database are:
> Database consistency is maintained - only one copy
> Resources of a powerful computer are made availible to many clients
> Access and secuirty rights are managed centrally
> Backup and recovery are managed centrally

