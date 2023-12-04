#modules#introductie 
[[INHOUD EXAMEN LEREN PROGRAMMEREN]]
- Research-opdracht
	- Maze-solving algorithm
		- Summary by ChatGPT
			- [[Maze-solving]]

- Dark Web (Enkel via TOR browser) (**!Geen directe link met FullStack!**)
	- Foto ijsberg
	- Inhoud
		- Goed: Journalistiek in onderdrukte landen, etc...
		- Slecht: Huurmoordenaars, Wapenhandel, video's van onthoofdingen, etc...
	- Deep web
		- Logins, databases, etc...
	- Surface Web: Alles wat normaal toegankelijk is
	- Links eindigen in .onion

[**Video: Leer programmeren met een boterham met choco**](https://www.youtube.com/watch?v=JmCsuyuVvjQ&pp=ygUsbGVlciBwcm9ncmFtbWVyZW4gbWV0IGVlbiBib3RlcmhhbSBtZXQgY2hvY28%3D)
=> Computationeel denken (zie definities)

[[Klas-Groepswerk 1 Carbonara]]

[[Olifanten door de alpen]] =>Splitsen in Deelproblemen

[[Voorbeeld semantische code]]

[[Klas-groepswerk Raket naar Mars]]

wat is Programmeren en wat hoort er bij?
- Set van instructies
- Algoritmen
- Deelproblemen opstellen
- Concepten leren
	- Variabelen
	- arrays
	- iteraties
	- loops
	- http-codes
	- etc...
- UI UX opstellen
- ................
- Code/syntax (komt pas later)
NA ALLE TIJD IS OPLOSSEN VAN PROBLEMEN IDENTIEK, MAAR SYNTAX IS VERANDERD
- hulp van AI, programmas, etc...

[[Versioning]]

[[Block-programming]] (zie begrippen)

- Problemen splitsen in deelproblemen
**[Trello](http://trello.com/)** => een site voor collaborative splitsing in deelproblemen met optie tot "to do, working on it, done, etc..."
![[Pasted image 20230927092512.png]]

- Objects (zie begrippen)
	- Classes kunnen geinstantieerd worden naar een object
		- Class: table
			- 4 poten
			- tafelblad
	- Object WR
		- Wit
		- Rond
	- Ander object RV
		- Rood
		- Vierkant
	- Bij objecten moeten alle zaken die elke tafel gemeenschappelijk heeft (class) niet meer gespecifieerd worden
		- Dus als er een aanpassing aan wat een tafel is komt, dan moet dit ENKEL bij de class aangepast => alle objecten aangepast naar verandering class

- Native vs Hybrid apps (iOS, Android, etc....)
	- Native werkt enkel op één platform
		- Runt direct op de OS
	- Hybrid werkt op alle platformen
		- Runt een virtual layer om alles te verwerken
	- Vroeger was native beter omdat hybrid trager was, tegenwoordig is dit verschil miniem (bij hedendaagse smartphones)
	- Tools zoals Electron, Cordova, etc... converteren de code automatisch met Javascript, HTML, CSS => HYBRID
		- Discord, Dropbox, Obsidian, Teams, etc...

- Variabelen (zie begrippen) vs Constanten (voorbeeld kast)
	- Variabelen kun je dingen inzetten en terug uithalen en een nieuwe waarde erin plaatsen
		- vb
	- Constanten kun je maar één keer een waarde aan toekennen en dat blijft die waarde
		- vb Kerstmis
	- Er kan maar 1 item in een variabele zitten, maar dat item kan extreem groot zijn
	- Array is de verzameling van variabelen
		- (vb.) let myArrayInt = [1,2,3]
			- nummers
		- (vb.) let myArrayString = ["one", "two", "three"]
			- tekst
		- Je kan deze enkel met een loop aflezen
			- Je kan zo alle "lades" afgaan
			- Deze loop kun je ook gebruiken om te kijken waar een bepaalde waarde is "zoeken tot juiste lade gevonden is"
		![[Pasted image 20230927100727.png]]
![[Pasted image 20230927101458.png]] (vanilla javascript)
![[Pasted image 20230927101552.png]]
- Naamgeving moet INTUITIEF zijn, we mogen GEEN spaties gebruiken in naamgeving van variabelen !spaties betekenen het begin van een nieuw concept => Niet meer die zelfde variabele!
	- variables: choose naming wisely: always start with alphanumeric, never with numbers
	- prefer camelCase!
		- technisch niet fout om anders te werken maar is minder duidelijk volgens conventie
  ![[Pasted image 20230927102054.png]]
  
- Controlestructuren
	- 
- oneindige herhaling: "while(true) {...}
- While-condities
	- Will execute code as long as the condition is true
	- let i=0 & let loopresult => ALWAYS DECLARE VARIABLES, OTHERWISE THEY DO NOT EXIST!
	![[Pasted image 20230927105616.png]](vanilla javascript)
	- => 29 loops (want i<30)
	- zolang i<30 => Loop
	- anders: doe iets anders
- if-condities
	- GEEN LOOP MAAR CONDITIE
	- ALS de conditie waar is, run de code éénmaal![[Pasted image 20230927110211.png]](vanilla javascript)
- Else-conditie
	- Vervolg op if-conditie => ALS conditie NIET waar is, run andere code![[Pasted image 20230927110438.png]](vanilla javascript)

- Operatoren (KUNNEN VERSCHILLEN TUSSEN TALEN)
	- toekenningsoperator (=)
		- Waarden toekennen aan variabelen of objecteigenschappen
	- Rekenkundige operatoren
		- getallen aanpassen (+,-,/,*)
	- Relationele operatoren
		- <, >, <=, >= (kleiner dan, groter dan, kleiner of gelijk aan, groter of gelijk aan)
		- == (gelijk aan)
		- ! (negation, bijvoorbeeld != betekent is NIET gelijk aan)
	- Logische operatoren
		- and(&&), or(||).

[[Splitsen in Deelproblemen (Computational Thinking)]]

[[Codecombat]]

[[Wordpress]]

[[GIT]]
shift+ctrl+L to modify all of a certain tag