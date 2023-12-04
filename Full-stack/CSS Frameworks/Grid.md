#CSSFrameworks 
(zie ook module CSS: Flexboxes and Grids)
- bevindt zich in  bootstrap altijd in een container
```
<div class="container">
	<div class="row">
		<div class="col">
		</div>
	</div>
</div>
```
=> het lijkt op een tabel om een grid te maken 
(allemaal div's maar classes zijn container, row en col)
kolommen hebben BP's (breakpoints)
=> als we een bepaalde resolutie hebben breekt de kolom en nest die zich in een volgorde

ALTIJD 12 KOLOMMEN
Tussenin een "GUTTER" spatie ertussen
![[Pasted image 20231027130302.png]]
```
<div class="container">
	<div class="row">
		<div class="col-md-3"></div>
		<div class="col-md-6"></div>
		<div class="col-md-3"></div>		
	</div>
	<div class="row">
		<div class="col-md-6"></div>
		<div class="col-md-6"></div>
	</div>
	<div>
		<div class="col-md-12"></div>
	</div>
</div>
```
We gebruiken col-md om het moment te veranderen wanneer de grid breekt
![[Pasted image 20231027132851.png]]
