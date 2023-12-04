#Databases 
 - De manier om structuur te brengen in data
	- Includes creating tables and establishing relationships between those tables according to rules designed both to protect the data and to make the database more flexible by eliminating redundancy and inconsistent dependancy
- 2 grootste soorten databanken
	- Relationele Database Management Systems (RDMS)
		- Oracle
		- MySQL
		- PostgreSQL
		- MSSQL
		- SQLite
	- NoSQL's (Not Only SQL)
		- MongoDB
		- CouchDP (VRT gebruikt deze voor het weer)
		- Firebas DB
- Voordelen
	- NoSQL's
		- Speed + large
	- RDMS
		- relaties tss tabellen
		- Kunnen schema's maken met tabellen en kolommen (vergelijking met spreadsheet)
	- Rij in database = record
- Cockroach DB
	- Databases scalen horizontally instead of vertically
- Devops
	- Profiel die alles kan (zowel programmeren als network engineer)
- Never make Orphan records (useless records, not able to be used)
![[Pasted image 20231004100739.png]]
- Normaalvormen
	- 1NF
		- Atomair
	- 2NF
		- Ontdubbel
	- 3NF
		- Zoek Relaties
- Table Names: Always in English!
- Column names: singular
- Relations singular_id
![[Pasted image 20231004110212.png]]
- id is auto-assigned => als record verwijderd wordt is die value voor altijd weg (1,2,3,4 => (delete 2) => 1,3,4)
![[Pasted image 20231004110816.png]]
- SQL = Structured Query Language
	- Programming language for storing and processing information in a relational database
[[Normalisatie opdracht 1 Dierenarts]]
[[Normalisatie opdracht 2 vliegtuig]]
[[Normalisatie opdracht 3 Schoonmaakbedrijf]]

- Many-2-Many
	- a type of database relationship in which a single record in one table can be related to multiple records in another table AND VICE VERSA
	- (example) a student can take multiple courses and a course can have multiple students
	- using a third table (pivot/join/intermediate table) 
	![[Pasted image 20231006141559.png]]
	- NAAM VAN PIVOT TABEL ALTIJD ALPHABETISCH!!
		- Anders kan Laravel geen relaties leggen
	- Werkt in 2 richtingen!
[[Normalisatie opdracht 4 Dierenarts Continued]]
[[Normalisatie opdracht 5 Tech-orders]]
[[Normalisatie opdracht 6 Galerij]]
