#Databases 
Foreign keys duiden relaties aan tussen twee tabellen in een database
- Constraints
	- Consistency
	- Errors
		- no orphan records!
- Default
- Cascade
	- If you delete one, you delete everything from a line
- RESTRICT/NO ACTION
	- If you try to delete, it won't do it if there are still values in the foreign key

Set Null
- Sets foreign key to NULL when foreign key is deleted
SET DEFAULT
- Sets the foreign key to a default value (often 1 which refers to missing value)

FOUTMELDINGEN
- FK Constraint Fails
	- Als je iets wilt toevoegen waar geen resultaat is voor de gelinkte tabel

##### FK's creëren (zie ook video Massimo)
(in PHPmyAdmin)
- Go to 'structure'
- Press 'relations'
- hover on 'more' for the corresponding id
- press 'index'
- press 'correct'
(you'll notice the corresponding id gets a silver key)
- Go to table designer
- In the left-hand bar of the designer, press "make relation"
- select the referred key
- select the foreign key
- set the right type of relation
	- if this doesn't happen, go to the table, look at structure and put it in relation view


