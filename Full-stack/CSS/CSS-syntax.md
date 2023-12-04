#CSS 
selectors
- Kiest het element waaraan de style toegekend wordt
- 3 soorten
	- tag selector
		- bijv. p, div, h1, etc...
	- class selector (most commonly used)
		- starts with a "." 
		- bijv.: .smart
		- toekennen door in een tag `class="naam"` toe te voegen (bijv: 
		  `<a class="navlink" href="index.html">)
		- GEBRUIK ZO VEEL MOGELIJK CLASSES=> IF NOT, TD's OP ANDERE DELEN VAN SITE GAAN OOK KAPOT
		- Classes kan je combineren met een spatie
		  "Cross White" bijvoorbeeld heeft de Cross-class en de White-class
		  - Er kan ook geselecteerd worden als "td.class" om zo enkel td's te targeten met de aangegeven class
	- id selector (pseudo class)
		- start with a "#"
		- bijv.: `#one`
- Pseudoselectors
	- :hover
		- verandert stijl wanneer de muis over een element staat
			- a.navlink:hover
	- :focus
		- verandert een kader wanneer je muis erin staat om te typen
			- input#lastname:focus
- kunnen gecombineerd worden: bijv a.navlink
	- a van de a-class, en .navlink van de class
- geheel aan selector + eigenschap + waarde = rule
=> h1 {color: white}
- indien je meerdere selectors wilt: gebruik "," om te onderscheiden
=> h1,p,h2 {color: white}
groottes kunnen in verschillende maten
- Px, %, em, rem...
- Inheritance
	- Geneste elementen gaan de eigenschappen van de hogere orde aanhouden unless specified otherwise


Eigenschappen
- Border
	- omlijning
	- verschillende stijlen
		- solid, dotted, dashed, etc...
	- border-radius
		- rondt de randen af
- background
	- kleur van de achtergrond
- color
	- tekstkleur
	- hexcode, rgb-code, kleurnaam
- text-align
	- left, right, center, fill
- text-decoration
	- dingen zoals onderlijnen
![[Pasted image 20231023110616.png]]
- Padding
	- afstand van tekst tot de border
- Margin
	- afstand van border tot margin
- vertical-align
	- top, bottom, etc...
	- brengt alles naar een specifieke plaats in de tabel
- Gradiënten
	- linear-gradient
		- bv: background: linear-gradient(to right, rgb(126, 4, 4), rgba(255, 213, 0, 0.744))
	- radial-gradient
		- bv: background: radial-gradient(circle, rgb(126, 4, 4), rgba(255, 213, 0, 0.744))
	- Probleem: image repeats itself
- Fonts
	- font-size
	- font-family (lettertype)
	- font-weight
		- dun of dikke drukking (tussen 100 en 900)
	- Importing google fonts
		- either using <link>(in head of HTML) or @import (at top of CSS stylesheet)
			- prefer @import!
- box-shadow
	- can be used to create shadows around an image or box
	- box-shadow: 0 0 10px 10px white;

[[CSS opdracht 1 kruiswoord]]
[[CSS oefening 2 backgrounds]]