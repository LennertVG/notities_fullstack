#AdvancedFront
4 pillars of Object Oriented Programming
![[Pasted image 20231122110438.png]]
![[Pasted image 20231122114846.png]]

a library is a collection of classes

Een class is het ontwerp, ook wel het supertype, een object is een instantiering
- vb: car=class ; myCar = object ;
![[Pasted image 20231122114512.png]]

![[Pasted image 20231122112154.png]]
de racecar en truck erven eigenschappen over van de superclass ´car´ (inheritance)

the *new* keyword allows you to instantiate a class
![[Pasted image 20231122112925.png]]

alle objecten onder class Car hebben toegang tot de methods van de class ![[Pasted image 20231122113515.png]]
Utils kunnen gebruikt worden om bijvoorbeeld data te exporteren uit een object
![[Pasted image 20231122113711.png]]

Methods kunnen elkaar overriden
![[Pasted image 20231122115642.png]]

[demonstratie classes vb game](https://www.freecodecamp.org/news/object-oriented-javascript-for-beginners/)

classes zijn "syntactic sugar" => Eigenlijk zijn er geen classes MAAR het wordt mogelijk gemaakt door ES6 (lang leven de moderne tech)
methods en properties kunnen public of private zijn
- all methods and properties zijn public by default!
	- Public: you can access these methods and properties from outside it's own body

Als uw variabele begint met een underscore is het een private property (dus # of _ )

```
function myReturn (number) {
	let vat = number * 1.21;
	return vat
}

let totalAmount = myReturn(134);
console.log(totalAmount)
```
=> Bedrag inclusief btw
De return kan gebruikt worden om eender waar de btw te berekenen => je kan dit blijven gebruiken
RETURN is mandatory, otherwise we would not get a value from this function

in ES6:
```
const myReturn = (number) =>{
	let vat= number * 1.21
	return vat;
}
let totalAmount = myReturn (134)
console.log(totalAmount)
```

Another method: ES6-function on one line => No need for curly braces, also has auto-return
```
const myReturn = (number) => number * 1.21;
```
Vrij gelijkaardig aan de api fetcher
```
fetch(apiUrl).then(res => res.json).then(data => console.log(data)).catch()
```
er zit een return function in de 'res => res.json'
conclusie! enkel de return command nodig als je multi-line gaat!

(OM TE TESTEN KUN JE ALTIJD IN GitBash of VS-Terminal "node {filename.js}" uitvoeren)

Arrays!
old-fashioned
```
function checkForFruit(array) {
	for (let i=0; i<array.length;i++) {
		if (array[i].category === fruit){
		return true;}
	}
	return false;
}
```
Using the built-in array method "includes"
=> map does callback on every item in the array and returns a new array with the result
	(a callback is a function that is passed into another function)
	in this case: "item => item.category" => returns all categories (only categories)
(if no item matches condition: undefined)
```
function checkForFruitIncludes(array) {
	let categories = array.map(item => item.category);
	return categories.includes("fruit");
}
```

Find-method
find does a callback on every item in the array and returns the first item that meets the condition
(if no item matches: undefined)
```
function checkForFruitFind (array){
	return array.find(item => item.category == "fruit")
}
```

Some-method(opposite of every)
does callback on every item and gives true if any item matches the condition
if no item matches condition: false
```
function checkForFruitFind (array){
	return array.some(item => item.category == "fruit")
}
```

Every-method
gives true if ALL items match the condition
if no item matches condition: false
```
function checkForFruitFind (array){
	return array.every(item => item.category == "fruit")
}
```

Filter-method
Returns an array with all items which match the condition
if no item matches: empty array
```
function checkForFruitFind (array){
	return array.filter(item => item.category === "fruit")
}
```


forEach-method
does a callback on every item in the array
if no item matches condition: undefinded
```
function checkForFruitForEach (array) {
	let result = false
	array.forEach(item=>{
		if (item.category === "fruit") {
			result = true;
		}
	});
	return result;
}
```
```
function checkForFruitForEach (array) {
	let result = false
	array.forEach(item=>{
		document.getElementbyID('result').innerHTML += item.category;
	});
	return result;
}
```
other cases
![[Pasted image 20231128110535.png]]
![[Pasted image 20231128110554.png]]

array-sorting
```
const arr = [5, 3, 1, 4, 2]
arr.sort ((a,b) => a - b);
console.log (arr) // output: 1, 2, 3, 4, 5
```
![[Pasted image 20231128110836.png]]
ternary operator is een IF ELSE - ? :
	if it's true, do first thing, else, the other thing![[Pasted image 20231128110934.png]]
![[Pasted image 20231128111539.png]]
output: 1, 3, 4, 5, 7, 8, 9, 12, 16
als je niet de "return a-b;" doet, dan sorteert die de array in met alle eentjes vanvoor en dan de tweetjes vanvoor, etc....
output: 1, 12, 16, 3, 4, 5, 7, 8, 9

![[Pasted image 20231128112414.png]]

![[Pasted image 20231128112425.png]]
bij destructuring maakt die ene nieuwe variabele aan vanuit een array
![[Pasted image 20231128113036.png]]
door de "myArray3" achter de let "[fruitD1, fruitD2, fruitD3]" te zetten inverteer je de functie en maak je dus objecten vanuit een array ipv objecten in een array te duwen
de "traditional way" is hoe het anders zou gedaan worden (ES5 vs ES6)
![[Pasted image 20231128113849.png]]
de "..." is een spread-operator => de ...rest (rest kan vervangen worden door eender wat) => Dit gaat alles wat nog verder in het object zit bewaren => In het voorbeeld hieronder houdt dit in "quantity, category, origin (en de country en state daarin)"
=> "..." betekent basically "de rest"
MOET ALTIJD OP HET EINDE STAAN
![[Pasted image 20231128114036.png]]

![[Pasted image 20231128114821.png]]
old school:
`const combinedArray2 = array1.concat(array2);`

try-catch method
Tests the block in try, if it fails => execute command in catch block
you can add finally, this block will ALWAYS execute after the try and catch methods
(kan ook gebruikt worden om loading icons te displayen)
```
try {
  nonExistentFunction();
} catch (error) {
  console.error(error);
  // Expected output: ReferenceError: nonExistentFunction is not defined
  // (Note: the exact output may be browser-dependent)
}
```

[site to download loading icon](https://loading.io/)

async vs sync code => synchronous code is handled line per line, for async code is run simultaneously

