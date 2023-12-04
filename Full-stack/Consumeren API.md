#basicJava 
[RapidAPI](https://rapidapi.com/)
- use JavaScript - Fetch
- => In script tag function maken
	- altijd met dit 'fetch().then().then().catch();'
		- fetch => Die gaat de URL fetchen (http get request) => fetch(URL)
		- then => txt JSON (string) komt binnen (result van fetch) 
		  => JSON converteren naar JavaScript object => then(res => res.json())
		- then => hierin komt JavaScript object terecht (MEEST BELANGRIJKE)
		  => then(console.log(data))
		- catch => fouten opvangen
(is scoped => Werkt binnen block)
In ECMAscript 6
```
function functionName () {
	fetch('url').then(res => res.json()).then(console.log(data)).catch();
} 
console.log(obj.name)
```
oude versie (ter illustratie van block)
```
fetch('url').then(
	function (res) {
		return res.json();
	}
).then(
	function (data) {
		console.log(data);
	}
).catch();
```
`res => res.json()` = `function(res){return res.json()}`
- links heeft de fat arrow function
	- ECMAScript6functie:
		- function myName (parameter) {
			console.log (parameter);
		}
	- verandert dan naar
		- myName = (parameter) => console.log(parameter)
	- Als het op één lijn staat moet er zelfs geen open en sluit bloknotatie gebruiken (zijn wel aanwezig dus het is wel een block), als je meerdere lijnen gebruikt heb je wel { } nodig
	- ZEER belangrijk voor Angular.dev!
`console.log(data)` = `function(data){console.log(data)}`
(data kan je zelf benoemen als parameter)
=> anonymous function: functie zonder naam = callback function

Voorbeeld (zou niet werken want niet mijn key)
```
fetch('https://www.omdbapi.com/?i=tt3896198&apikey=d67c387a&s=barbie').then(result => result.json()
).then(data => console.log(data)
).catch();
   obj = {name:'Massimo'};
   console.log(obj.name)
```
=> output: Array van films

gebruiken van data
```
fetch('https://www.omdbapi.com/?i=tt3896198&apikey=d67c387a&s=barbie').then(result => result.json()
).then(data => console.log(data['search'][1].Title)

).catch();
   obj = {name:'Massimo'};
   console.log(obj.name)
```
=> Output= title of second move (Barbie as Princess and the Pauper)
(search is deel van de array => Key) (zie hoe je de zoekterm in de console log tag van "het treintje" zit)

zelfde principe als OMDbAPI movie restapi
```
obj={search:[
	{obj1:'value1'},
	{obj2:'value2'}
]};
console.log(obj['Search'][1].obj2)
```

```
fetch('https://www.omdbapi.com/?i=tt3896198&apikey=d67c387a&s=barbie').then(result => result.json()
).then(data =>{
	document.getElementById('result').innerHTML=data['Search'][2].Title;
	}
).catch();
   obj = {name:'Massimo'};
   console.log(obj.name)
```
=> Hier gaat de data weergegeven worden op de site voor de tweede value uit de array (Barbie in the Nutcracker)

```
fetch('https://www.omdbapi.com/?i=tt3896198&apikey=d67c387a&s=barbie').then(result => result.json()
).then(data => {
	let i=0;
	while(i< data.Search.length) {
		 
}
).catch();
   obj = {name:'Massimo'};
   console.log(obj.name)
```

good to know
- [JSONviewer](http://jsonviewer.stack.hu)
	- paste your JSON text and it converts the JSON-text to a structured view
- [Jsonplaceholder](http://jsonplaceholder.typicode.com)
	- testen van JSON met fake data

`document.getElementById('myButton').addEventListener('click', getTodo)`
=> hiermee staat de event trigger in het script ipv in de html
(als ik klik op het element 'myButton' dan voert de Todo-functie uit)

- data is hier nu beschikbaar
function getData(data){
	console.log(data);
}

- deze is verbonden met de API
function getTodo(){
	fetch(url).then(res=>res.json()).then(data=>console.log(data)
		function(data){
			getData(data)
		}).catch(error => console.log(error))
	}

gebruik makende van backticks\`...\` kan je een volledige string maken zonder de nood aan concatenation

[[Opdracht ToDo API]]
