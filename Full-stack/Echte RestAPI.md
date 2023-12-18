#JavaFrameworks 
SQL database maken => Back to MAMP en PHP-myAdmin
![[Pasted image 20231213101621.png]]
=> Use tablePlus to interact with the db
als er een applicatie met veel packages en node-modules enzo gemaakt wordt => Use npm init

CORS: als je van een applicatie op een domein requests doet op een ander domein moet je een CORS-policy hebben
- ofwel: "iedereen welkom" => alle requests zijn toegestaan naar de API
- anders: CORS-policy => Enkel angular app mag requests doen

We gaan de API af te schermen met een token
- `node app_bearer.js` => Als je dan geen token hebt: "401 error: Unauthorized"
- In Insomnia zie je een menu "authorization" => Zet deze op "Bearer" en dan kun je een token aangeven
![[Pasted image 20231215092920.png]]
- uiteindelijk genereer je een token per user => Mogelijkheid die te revoken!
