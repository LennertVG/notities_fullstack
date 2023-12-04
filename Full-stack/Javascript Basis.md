#basicJava #modules 
[[Completed]]
Gebruik Bootstrap 5 starter templates (googlen)
SCRIPT ALTIJD ONDERAAN DE PAGINA ZETTEN!!!
VERGEET NIET, ALLES IN JS IS HOOFDLETTERGEVOELIG

CONST vs VAR vs LET
- let => maakt reassignment mogelijk
	- let mijnvar = 'invullen'
	  OF
	- let mijnvar;
	- mijnvar = 'invullen'
function langeFunctie () {
	let naam;
	let voornaam;
	let result;
	let details;
	let naam ='massimo' ;
	let naam ='lennert';
	const now = new Date() ; 
	(=> bijvoorbeeld voor examen => KAN NIET MEER VERANDERD WORDEN)
	console.log(naam) => lennert
}
![[Pasted image 20231108151415.png]]
![[Pasted image 20231108151432.png]]
- var bestaat NIET MEER => heel oude JavaScript

Integers
- Alles wat je van HTML binnenhaalt is altijd een string ookal staat er number => als je niet de parseInt/parseFloat doet => geeft het de inhouden van de waarden naast elkaar weer: 10+10=1010 ipv 20
	- parseInt voor volle getallen 
	  => bijvoorbeeld voor aantal tickets
	- parseFloat voor kommagetallen

**(alvorens die let commando's declareren bovenaan)**
![[Pasted image 20231108091107.png]]
![[Pasted image 20231108091115.png]]
![[Pasted image 20231108091130.png]]
![[Pasted image 20231108091145.png]]

CLI= command-line-interface
![[Pasted image 20231108091438.png]]
![[Pasted image 20231108092150.png]]
![[Pasted image 20231108092426.png]]
![[Pasted image 20231108092924.png]]
(from here on it's my own notes again)

- ECMASCRIPT
	- EUROPEAN COMPUTER MANUFACTUROR ASSOCIATION
- [Babel](http://babeljs.io) => Converteert moderne JavaScript naar versie die op alle browsers kan draaien
	- is ook ingebouwd in angular => Build vertaalt onze moderne taal naar ECMAScript5
- DUS wij leren nu ECMAScript5/VanillaJS (Vanilla JavaScript)
	- GEEN external libraries & frameworks
![[Pasted image 20231108101557.png]]

Belangrijk DRY-principle
- Don't Repeat Yourself
	- bij hernoemen => moet alles aanpassen
	- kans op fouten is hoger
	- => nieuwe functie!
- Dates
```
const now= new Date();
console.log(now);
```
- use console.log(now.getMonth()); to get only the month
	- !!!!IMPORTANT!!!! DATE/MONTH in JS => January=0, December=11
	- days: sunday=0, monday=1, etc...
![[Pasted image 20231108114220.png]]

een `\` is een escape karakter, het karakter recht erna gaat genegeerd worden (bijv `'vikings'`) => zo kunnen we speciale karakters laten zien in onze strings (zoals 'de symbolen hierrond')

- Sessie's/sessions
	- tijdelijke data die in de RAM van de computer worden bewaard

[State of Javascript](https://stateofjs.com)
=> The annual developer survey of the JavaScript ecosystem

Alles tussen { } is een block

[[Arrays and objects]]

[[GROEPSWERK 1 FRONT-END]]

[[RestAPI]]

[[localStorage]]
