#basicJava 
- slaat data op (max 10MB)
	- slaat dingen op per domain
		- JavaScript object is niet op te slaan
- doet set en retrieve van name and value pair
```
localStorage.setItem("lastname","Smith");
localStorage.getItem("lastname");
```
- name en value moeten zich houden aan strict set of rules
	- key: url/domain
	- name: always string
![[Pasted image 20231115091502.png]]
```
    document.getElementById('buttonmovie').addEventListener('click', setStorage);

    function setStorage() {
        console.log('yay');
        localStorage.setItem('yay','this is a stored value _ no expiration date');
    }
```

![[Pasted image 20231115092539.png]] 
(in console)
- om op te halen
` document.getElementbyId('movie').value = localStorage.getItem('yay')`

!verschil JSON en JavaScript objects
![[Pasted image 20231115093639.png]]
```
myObj = {
name: 'massimo',
age: 47,
city: 'Zonhoven',
};

const myJSON = '{
"name": "massimo",
"age": 47,
"city": "Zonhoven"
}';
```

omzetten van JSON naar Javascript
`localStorage.setItem('data',JSON.stringify(myObj));

omzetten van string naar Object
```
const result = JSON.parse(localStorage.getItem(data));
document.getElementById('movie').value=result.city;
```
Om meerdere zaken te storen in een array (zoals favourite movies)
=> gebruik het push-commando (zo vervang je niets)

Nullish coalescence  => If movies is not set as localStorage: make empty array
`favieStorage = JSON.parse(localStorage.getItem('movies') || []`
basically same as this
![[Pasted image 20231115115415.png]]

 [[opdracht movies namiddag]]
 