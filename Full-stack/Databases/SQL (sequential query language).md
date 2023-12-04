#Databases 
- Querries
- ALWAYS WRITTEN IN CAPS (conventie, niet verplicht)
- Manier voor programmas om inhoud van een database op te halen
- Statements (SELECT name, price FROM products ORDER BY price DESC)
	- SELECT => **SELECT * FROM products;**
		- * is "wildcard"/alles
		- vervang * door kolomnamen om enkel die zaken op te vragen
	- Meest populaire select-querries
		- WHERE => een selectie waar een bepaalde situatie aan voldoet 
		   ... WHERE company = 'prometheus';
			- = ; < ; > => gelijk aan, kleiner dan, groter dan 
			  ... WHERE price > 10
		- IS NULL => enkel zaken waar een value mist 
		  ...WHERE company IS NULL
		-  ORDER BY  => sorteren op waarde
			- default sorteermethode: ASC = ascending => minst recent
				- Laagste ID
			- tegengesteld: DESC = descending => meest recent (also meest gebruikt)
				- Hoogste ID
		- WHERE NOT => Waar een waarde niet gelijk is aan iets 
		  ... WHERE NOT company='unilever'
			- Alternatieven
				- NOT IN
				- <>
				- !=
				- Subqueries (gebruiken we nog niet)
		- LIKE => Basic for all seach functions 
		  .... WHERE company LIKE = '%unilever%'
			- %... betekent EENDER WAT ER VOOR KOMT  
			  ...% betekent EENDER WAT ER ACHTER KOMT
			- als je zoekt naar %unilever% => Dan is 'ile' genoeg om unilever te vinden (zoekt alles waar unilever in voor komt) ![[Pasted image 20231010120145.png]]
			-  -`'%$search$%'` (remove spaces maar Obsidian had da niet graag) wordt gebruikt in zoekfuncties
		- AVG => average, het gemiddelde van een bepaalde hoeveelheid waarden
		  SELECT AVG(price) FROM products => Onbruikbaar
			- PHP kan niet omweg met () => Deze dataset is onbruikbaar
				=> Kan NIET weergegeven worden in tabel/resultaat
		- AS hernoemt bijvoorbeeld AVG(price) naar een andere naam average => alias, dit kan wel verwerkt worden
		  Aliases are used to mitigate special chars in mysql formulas
		SELECT AVG(price) AS average FROM products => bruikbaar
			=> Kan WEL weergegeven worden in tabel/resultaat
		-  COUNT
			- telt hoeveel rijen er zijn (in dit geval van unilever) en slaat het op in waarde 'totalunilever'
			SELECT COUNT( * ) AS totalunilever FROM products WHERE company = 'unilever'7
		- MAX en MIN
			- laat de hoogste en laagste waarde zien van een kolom
			SELECT MAX(price) AS expensive, MIN(price) AS cheapest FROM products
		- DISTINCT
			- toon waarden van een tabel maar geef maar één keer elke unieke waarde => Geen herhaling in tabel (bijvoorbeeld om alle bedrijven die klant zijn te zien in één tabel zonder herhalingen)
			  SELECT DISTINCT company FROM products
		- (mathematical operators +, -, * , /)
			- SELECT price, price + (price * vat/100) AS pricevat FROM products; 
		- SQL-Syntax: CURRENT_DATE
			- SELECT * FROM products WHERE releasedate < CURRENT_DATE
	- Waarden invoegen
		- INSERT INTO 'categories' ('id', 'name') VALUES (NULL, 'vervoer') ;
		- de NULL-waarden zijn nodig voor de auto-incrementie!
	- We kunnen één query verdelen op meerdere rijen, een query wordt pas afgesloten met een ; (puntkomma)
	- Wees voorzichtig met Reserved Keywords (select, between, etc...)
		- ideaal gezien niet als tabelnaam
		- als toch tabelnaam: zet tussen backticks
![[Pasted image 20231011092200.png]]
- joining tables
	- => dit is nodig om ervoor te zorgen dat info die als id in een tabel staat opgehaald kan worden!
	- SELECT * FROM products 
	  JOIN categories ON categories.id = products.category_id
	  JOIN companies ON companies.id = products.company_id
	  WHERE products.id = 1
	  (die 'products.' is niet noodzakelijk)![[Pasted image 20231011093551.png]]
	- => uit de productstabel gaat die de id's nemen en de waarden daarvan uit de categories en companies tabel ![[Pasted image 20231011093701.png]]
	- OP DIT PUNT BOTST UW CODE MET DE MEERDERE ID-KOLOMMEN IN NodeJS, PHP, etc....
		- de code weet niet of die "toveren voor beginners", "boek", of "prometheus" moet laten zien!
	- Oplossing hiervoor
		- * aanpassen => Aliassen en kiezen wat weergegeven moet worden => verschillende kolommen met name? => AS productName, categoryName, companyName
		- SELECT
		  products.id,
		  products.name AS productname,
		  products.price,
		  products.stock,
		  products.vat,
		  categories.name AS categoryName,
		  companies.name AS companyName
		  FROM products
		  JOIN categories ON categories.id = products.category_id
		  JOIN companies ON companies.id = products.company_id
		  WHERE products.id = 1![[Pasted image 20231011094524.png]]![[Pasted image 20231011094554.png]]
	- [Visual JOIN](https://joins.spathon.com/)
	- Dit was een "inner JOIN" => kan enkel werken als er voor de linker tabel ook waardes zijn in de rechter tabel
		- *INNER JOIN* => Je ziet enkel waarden als die voor beide tabellen ingevuld is![[Pasted image 20231011095216.png]]
		- ENKEL ALS IK ALLE GEBRUIKERS WIL ONGEACHT OF ZIJ EEN SPORT BEOEFENEN MAAK IK GEBRUIK VAN EEN *LEFT JOIN*![[Pasted image 20231011095228.png]]
		- MET EEN *RIGHT JOIN* ZIE JE ALLE GEBRUIKERS ONGEACHT OF ER IEMAND INGESCHREVEN IS![[Pasted image 20231011095325.png]]
		- OUTER JOIN KAN OOK TECHNISCH MAAR KOMT MINDER VOOR![[Pasted image 20231011100618.png]]
		- ![[Pasted image 20231011101230.png]]