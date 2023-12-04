#basicJava 
Array
- Arrays Objecten
myArray = [1,2,3];
myObject = {'num':1,'num':2,'num3':3};
=> Zijn beiden hetzelfde maar bij objects vraag je de property bij name (zoals console.log(myobject.num1);)
Arrays beginnen met tellen vanaf de 0ste positie

iteration of array with the for method
for (let i=0;myArray.length< i;i++) {
	console.log(myArray[i])
}

iteration of array with the while method
let j=0
while (myArray.length > i) {
	console.log(myArray[i]);
	i++
}

iteration of object with for method (key is de naam waaronder de values staan)
for(key in myObject) {
	console.log(key);
	console.log(myObject[key]);
}

add an element to an array
myArray.push(10)

Add an element to my object
myObject.num4 = 4;
(array.key = value)

(use case cevapi)
```
let order={};

order.sandwich= 4;
order.sauce= 2;
order.schotel= 3;

console.log(order);

let totalprice=0;
for (key in order) {
	totalprice = totalprice + order[key]
}

console.log(totalprice);
```
