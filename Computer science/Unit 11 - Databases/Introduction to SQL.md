SQL (Structured Query Language) is a declaritive language used for querying and updating tables in a relational database. It can also be used to create tables. SQL statements can be created in many other programming lanuages that can be used to manipulate a database.

The SELECT statement is used to extract fields from one or more tables. The syntax of the statement is as follows:
```SQL
SELECT --list of fields to be displayed
FROM --list the table or tables the data will come from
WHERE --list of search criteria
ORDER BY --lists the fields that the data is to be sorted on (ASC or DESC)
```
The results of this query will return a table, with colums specified by SELECT from the database specified by FROM that meet the conditions specified by WHERE in the order specified by ORDER BY.  

### WHERE:
LIKE can be used in the WHERE clause to return fields that match a certain string criteria. For example WHERE {attribute} LIKE "XXX" will return any fields with "XXX" in the {attribute} column. The character * can be used as a "wildcard" that will specify any value. For example XXX* will specify any field where the first three characters are XXX. BETWEEN and IN can be used to select a range of numerical values to return. IN can be used to compare the target to a range of strings.

All equality operators, including AND, OR, and NOT can be used in the WHERE clause to combine logical statements.

---------------------------------------

Semicolons are a standard way in many SQL database interfaces to specify the end of a query.

The JOIN keyword can be used in the SELECT query to pull data from two linked tables. An example of two tables linked by a 1:M (one to many) relationship:

tblTeam(teamID, teamName, manager)
tblPlayer(playerID, surname, firstname, teamID)

To return all players from a team:

SELECT tblPlayer.surname, tblPlayer.firstname, tblTeam.teamName
FROM tblTeam, tblPlayer
JOIN tblPlayer
ON tblTeam.teamID = tblPlayer.teamID
WHERE team.teamName = "TEAM NAME"

JOIN and ON refer to the intersection of two tables.