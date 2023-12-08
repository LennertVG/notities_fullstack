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
