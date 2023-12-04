[github link start json server](https://github.com/typicode/json-server)
![[Pasted image 20231129100114.png]]
[API  - http://localhost:3000](http://localhost:3000)
=> lokaal enkel beschikbaar, uiteindelijk gaan we dit pushen
=> hier kunnen we onze end points ook zien (die gaan nodig zijn voor data te gebruiken)
=> shut down by pressing ctrl+c

insomnia
- new collection
- try get-request (use link of api, in this case the localhost)![[Pasted image 20231129100943.png]]
301-redirect => neemt de page-rank mee naar de nieuwe pagina als je van domeinnaam verandert bijvoorbeeld
- post-request = add content to api
	- select which endpoint (in this case: posts)
	- add JSON body in the post-request  which you want to be added
	- send
	- double check the 201 code and check if data is posted succesfully (get-request)
	- in JS.
```

```
![[Pasted image 20231129102139.png]]
- delete-request
	- select which data id you want to delete (add id to end of link: in this case 2)
	- click send
	- check for 200 OK message![[Pasted image 20231129102512.png]]
- put-requests
	- maakt object opnieuw aan om de data te overriden
	-  select which data id you want to delete (add id to end of link: in this case 2)
	- enter data you want to update or add
	- send
	- wait for 200 OK message
	- double check data (get request)![[Pasted image 20231129102821.png]]![[Pasted image 20231129102914.png]]

zie ook code Massimo!