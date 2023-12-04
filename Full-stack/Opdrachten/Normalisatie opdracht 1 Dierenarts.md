#Opdrachten #Databases 
![[Pasted image 20231004112709.png]]
(doorstreept: many-2-many)
- we krijgen dataset
	- dierenarts
- Maak een maat-applicatie om dierenpraktijk te managen
	- momenteel in excel
- Wat is er aan de hand
	- Atomair?
		- Nee, meerdere waarden per cel (voor- en achternaam)
	- Ontdubbeld?
		- Nee, er zijn meerdere keren dezelfde waarden (veel honden of meermaals zelfde eigenaar)
	- Relaties?
		- Het soort dier heeft niets met de eigenaar te maken
- Belangrijk, voorkoom redundancy en orphan records! => breng tot derde vorm van normalisatie
