#introductie 
API's
- LAMP stack (Linux Apache MySQL PHP)
- Mean stack (Mango Express Angular Node JS)

Browsers kunnen enkel HTML, CSS en JS weergeven => Parsers nodig om backend talen (PHP, etc...) te vertalen naar Front-end talen (HTML, CSS, JS)

LocalWP
- GEBRUIK NOOIT ALS USERNAME ADMIN!!!!
- Passphrase>password => Easy to remember, difficult to brute-force, 

Site werkt op 12 kolommen grid
- Responsiveness
	- Als site/app kleiner wordt (tussen site, gsm, tablet, of bij kleiner maken tablad) dan breekt de grid en zet dat elementen onder elkaar
![[Pasted image 20231002111249.png]]
![[Pasted image 20231002111313.png]]
- breekt de content in kolommen wanneer we responsive gaan!
	- Onder elkaar zetten bij bepaalde scherm-breedtes
- Som van aantal kolommen moet ALTIJD 12 zijn
	- col-md-2, col-md-4, col-md-4, col-md-2 => 12 in totaal!
	- md-tags zijn generic, wij kunnen aanpassen wanneer de tekst breekt

- Bootstrap cdn
	- (Way to include more easily)
- CSS
	- Massimo stylet via inspector => Snel zien wat effect is van Stylesheet
		- VERGEET NIET TE KOPIËREN EN PLAKKEN => NIET PERMANENT

[Wordpress Local run](https://localwp.com/)  [Wordpress](https://wordpress.com/nl/)
- Settings => Reading => Set Homepage => Static => Pagina die je als home wilt
	- Als je dit niet doet laat de home-pagina nieuwste posts zien
- Plugins
	- Elementor 
		- is een block-editor (sites made easy)
	- Wordfence
		- Security PAS ACTIVEREN ALS SITE KLAAR IS
	- WooCommerce
		- Tools voor online storefronts
- Customizer
	- Customize your theme
		- best is hello-theme

Mails sturen via SMTP
- [Test email Spammynes](http://mail-tester.com)
	- Check of mail goed aankomt of in spam terecht komt
