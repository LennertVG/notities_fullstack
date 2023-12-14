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

Databinding: content/attributes {{var}}
Eventbinding: (click)
Attribute binding: value (using NgModel)
Components/routing
`<router-outlet>` gaat in de root
3 componenten nodig
```gitBash
ng g c home
ng g c about
ng g c contact
```


Routes voor navigatie
```TypeScript
import { Routes } from '@angular/router';
import { HomeComponent } from './home/home.component';
import { AboutComponent } from './about/about.component';
import { ContactComponent } from './contact/contact.component';

export const routes: Routes = [
    {
        path: '',
        redirectTo: 'home',
        pathMatch: 'full',
    },
    {
        path: 'home',
        component: HomeComponent
    },
    {
        path: 'about',
        component: AboutComponent
    },
    {
        path: 'contact',
        component: ContactComponent
    }
];
```

Data storage in db.json file
- make db folder in src
- make db.json
- create your db
- example
``` json
{
    "todo": [
        {"id":1, "title": "Soupmaker", "owner": "V", "done": false},
        {"id":2, "title": "Douglas Skincare", "owner": "Z", "done": false},
        {"id":3, "title": "Soupmaker", "owner": "A", "done":false},
        {"id":4, "title": "Drone", "owner": "M", "done":false}
    ]
}
```
- to show in terminal:
	- cat => volledig database
	- Head => begin database
	- tail => einde database
	- nano => editor
- To watch
`json-server --watch db.json` in gitBash

ngOnInit => start component bij initializen van component (testscript)
```TypeScript
  ngOnInit() {
    console.log('yay mijn init werkt')
  }
```
Voor data te fetchen op initialiseren van component (in home.components.ts in het voorbeeld van Massimo)
```Typescript  
export class HomeComponent {
	url:string = 'http://localhost:3000/todo';
	todos:any[]=[];
	
  fetchMyData() {
    fetch(this.url)
    .then(response => response.json())
    .then(json => this.todos = json)
  }
  ngOnInit() {
	this.fetchMyData();
	}
}
```
Daarna kun je in de home.component.html de inhoud van todos ophalen met {{todos}}

Voor het itereren van de array kunnen we dan de volgende code gebruiken in home.component.html
``` 
@for(todo of todos; track todo.id){
	<li>{{todo.title}} - {{todo.owner}}</li>
	}
```
Result: ![[Pasted image 20231208143500.png]]
- de "track todo.id" is een verplichting
	- De track is een soort index, de for-loop gaat de lijst doorgaan

{{ }} => String Interpolation: weergeven van een tekst vanuit een component uit onze Angular

Minimale functionaliteit die moet kunnen toegevoegd worden aan een tabel!
CRUD
- Create
- Read
- Update
- Delete
BREAD
- Browse
- Read
- Edit
- Add
- Delete

HTTP-requests
- POST
- PUT
- PATCH
- GET
- DELETE
put vs patch => Patch past kleine dingen aan, put vervangt de waarden van het hele object!

API Endpoints => Terminologie aan het einde van de API-url  (vb.  /Posts ; /Todos ; /id)

Angular Directives => bijv @if en @for ; zal iets itereren of individuele values targeten

Pagination is het gedeeltelijk inladen van een dataset
- Denk aan een aantal paginas waarbij je 50 posts ziet en een knop onderaan hebt om het volgende deel van de data in te laden (bijv door nummertjes vanonder)

If you use insomnia you can use the "generate client code"-button to get the code
![[Pasted image 20231211101114.png]]

LocalStorage gaat gebruikt worden voor tokens te maken => Ingelogd blijven bijvoorbeeld

If you want to use pipe operators => add the common module

UPDATE en DELETE hebben id nodig in URL in HTTP-requests

POST en GET hebben er geen nodig in de URL

PUT vernietigt alles in de array en vervangt wat meegegeven wordt (shotgun)
PATCH vervangt enkel de waarden meegegeven (sniper)

Interfaces are a TypeScript for defining the shape of an Object
BESTAAN ENKEL BIJ COMPILING
```Typescript
interface MyUsers {
id: number;
name: string;
password: string;
}
```
Deze custom type geeft aan dat een user een object moet zijn met een id wat een nummer is, een naam die een string is, en een passwoord dat een string is
=> dit wordt gebruikt voor typechecking

via de angular CLI is de syntax voor een interface
`ng generate interface interfaceNaam.interface`
=> Met de angular interfaces moet je ze importeren in je TypeScript file
voorbeeld:
```Typescript
import {Env} from '.../env.interface'
```
```Typescript
export interface Env {
	production: boolean;
	api: string;
	version?: string;
}
```
``` Typescript
config: Env = {
	production: false,
	api: 'http://localhost:3000/'
	version: '1.0.0'
}
```
=> Het vraagteken bij version geeft aan dat die optional is, er is geen probleem als de version niet meegegeven is

alternative message prompt: toasts
[Demonstration](https://ngx-toastr.vercel.app/)
[installation](https://www.npmjs.com/package/ngx-toastr)

Je kan bepaalde services en methods beschikbaar maken in meerdere componenten
=> Maak folder "shared" (mag ook andere naam maar liever dit)
=> gebruik in de "shared" folder `ng g s users` 
=> Maak je shared method
vb: 
```Typescript
	constructor ( ) { }

	url: string='http://localhost:3000'
	getUsers() {
		return fetch(this.url)
		.then(res => res.json())
	}
}
```
![[Pasted image 20231213094433.png]]
(zie ook code Massimo)
=> dan ga je naar je component.ts van het element waar je die service wilt gebruiken
=> 
```typescript
//bij imports voeg je dan de module toe
import {usersService} from '../shared/users.service';
import {MyUsers} frrom '../my-users.interface';

//in de typescript van het component kun je die methods enzo dan aanspreken
users: MyUsers [] = []
apiurl = this.usersService.url
ngOnInit(){
	this.usersService.getUsers().then(data => {
		this.users = data
	})
}
```
dit doe je gewoonlijk voor elke databasetabel  als je met grotere apps bezig bent

[[Login service]]
[[Echte RestAPI]]
