#modules #Databases
[[INHOUD EXAMEN DATABASES]]

Wat is data?
- Gegevens die een bepaalde structuur hebben zodat wij hier kennis kunnen uit putten
[[Database-normalisatie]]

- id => primary key integer =>**pk int** (index zoals in een boek)
	- Wanneer id in andere tabel gebruikt => **int** 
- text => **varchar ... (value)** (eg. varchar 255; varchar 110) => Minder karakters => Minder storage usage (MAS000000000.... => Aantal nummers gelijk aan value van varchar - aantal karakters)
- Datums en tijden => ALTIJD **datetime**
- getallen
	- float
	- decimal
![[Pasted image 20231009112613.png]]![[Pasted image 20231009112628.png]]
 [DrawSQL: Manier om orde te brengen alvorens databases te maken](https://drawsql.app/diagrams)
ERD=Entity Relationship Diagram

1) Normaliseer (Excel)
2) Draw (DrawSQL) => **KAN GEIMPORTEERD WORDEN IN MYSQL**
3) Make (MySQL)
4) Dummy Data
5) Test

[[MAMP starting up server]]

[[SQL (sequential query language)]]

[[Stored Procedures]]

[[Foreign Keys (FK)]]

[[Tableplus]]

