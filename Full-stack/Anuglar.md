#JavaFrameworks 
Overal gaat in classes gewerkt worden
Bijna alles gaat via onze command line interface (CLI) gebeuren
maakt een SPA (single page application)
Anuglar werkt volledig in classes (zie ook OOP)
ng is afkorting voor angular commands in de CLI
installation:
- https://angular.io/cli

![[Pasted image 20231206100816.png]]
DI zijn Dependency injections

to start an angular project in git bash
`ng new "naam van uw project"]`
VIA CLI EEN COMPONENT MAKEN
to test, use `ng serve --open` => Doe dit in een apparte terminal of gitBash instance want hier komen errors en info
Dan kunnen we die onder de localhost vinden
[LocalHost](http://localhost:4200/)

`ng generate component myComponent` of `ng g c myComponent`
=> hebben eigen CSS, HTML, TS (class @decorator -> selector:app-myComponent)
=> app.component.html -> `<app-mycomponent></app-mycomponent>`

in de app-folder komen alle elementen
in de assets-folder komen alle static items gelijk afbeeldingen enzo

`ng add @ng-bootstrap/ng-bootstrap` (add bootstrap with angular) 

`#template variables`

`[(NG Model)]` => een banana in a box, een combinatie van attribute en event binding