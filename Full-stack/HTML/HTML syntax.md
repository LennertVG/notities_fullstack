#HTML 
```
<html>
<head>
        <Title> title </title>
</head>
<body>
		<h1 id="title"> sub1 </h1>
		<h2> sub2 </h2>
		<h3> sub3 </h3>
		<!-- Commenting in html is done with these symbols -->
<div id="intro">
	<p>
	In a paragraph one can write anything, but never use the enter key; you are of course allowed to use space and other keys, but don't use enter... this is not an A4 ISO document... but an HTML file is a flexible document that needs to adjust to the screen sizes a canvas.
	</p>
</div>
<div id="CallToAction">
	<p>
	this is a big difference
	</p>
</div>
</body>
</html>
```

- In code
<html>
<head>
        <Title> title </title>
</head>
<body>
		<h1> sub1 </h1>
		<h2> sub2 </h2>
		<h3> sub3 </h3>
		<!-- Commenting in html is done with these symbols -->
<div id="intro">
	<p>
	In a paragraph one can write anything, but never use the enter key; you are of course allowed to use space and other keys, but don't use enter... this is not an A4 ISO document... but an HTML file is a flexible document that needs to adjust to the screen sizes a canvas.
	</p>
</div>
<div id="CallToAction">
	<p>
	this is a big difference
	</p>
</div>
</body>
</html>

- To see a full paragraph instead of just the part that fits on screen in VisualStudioCode, ALT+Z

- Inline tags are HTML elements that do not start a new line and can be used to format text within a paragraph or other block element. Some common inline tags include:
- `<b>`: Bold text
- `<i>`: Italic text
- `<u>`: Underlined text
- `<em>`: Emphasized text
- `<a>`: Hyperlink
- `<img>`: Image

The antagonist of inline tags is block tags. Block tags start a new line and are used to create different sections of a web page, such as headings, paragraphs, and lists. Some common block tags include:

- `<h1>`: Heading level 1
- `<p>`: Paragraph
- `<div>`: Division
- `<ul>`: Unordered list
- `<ol>`: Ordered list

```
	<p> this is a line </p>
	<p> this is a different line <p/>
	<p> this is yet another one </p>
```
- Als je geen paragrafen gebruikt komt het recht achter elkaar => GEEN ENTERS ERVOOR
- Gebruik ook geen `<br>` => Véél minder finetuning met classes!
- difference between a p-tag and a div-tag
	- p is used to style and format text
	- div is used as a more universal container (secties)
		- vaak ga je p-tags in div-tags zetten
- h1 vs h2
	- h1 often used for page titles
	- h2 used for p-titles
	- h3 for sub-p titles
- Tabellen
```
<table>
	<tr>
		<th>test1</th>
		<th>test2</th>
	</tr>
	<tr> 
		<td> data1 </td>
		<td> data2 </td>
	</tr>
	<tr>
		<td> data1 </td>
		<td> data2 </td>
	</tr>
	<tr>
		<td> data1 </td>
		<td> data2 </td> 
	</tr>
	<tr> 
		<td> data1 </td>
		<td> data2 </td>
	</tr>
</table>
```
- TR = Table Row
- TH = Table Head (niet verplicht)
- TD = Table Data/ Table Delimiter
<table>
	<tr>
		<th>test1</th>
		<th>test2</th>
	</tr>
	<tr> 
		<td> data1 </td>
		<td> data2 </td>
	</tr>
	<tr>
		<td> data1 </td>
		<td> data2 </td>
	</tr>
	<tr>
		<td> data1 </td>
		<td> data2 </td> 
	</tr>
	<tr> 
		<td> data1 </td>
		<td> data2 </td>
	</tr>
</table>
	- aanpassen van breedte, etc... => Zie CSS

- Lists
	- Order
		- uses  `<ol> </ol>`
		- Gives 1. 2. 3. 
	- Unorder
		- uses `<ul> </ul>`
		- gives dots
	- `<li> </li>` is used put items into list
<ul>
	<li> item 1 </li>
	<li> item 2 </li>
	<li> item 3 </li>
</ul>
```
<ul>
	<li> item 1 </li>
	<li> item 2 </li>
	<li> item 3 </li>
</ul>
```
<ol>
	<li> item 1 </li>
	<li> item 2 </li>
	<li> item 3 </li>
</ol>
```
<ol>
	<li> item 1 </li>
	<li> item 2 </li>
	<li> item 3 </li>
</ol>
```
- Anchor Text Linkage
<a href ="https://www.google.com">Google</a>
`<a href ="https://www.google.com">Google</a>`
- if used to link to external pages always use the target attribute and set it to `_blank`
	- DIT WORDT GEBRUIKT OM ERVOOR TE ZORGEN DAT DE PAGINA OPENT IN NIEUW TABLAD
	- `<a href ="https://www.google.com" target="_blank">Google</a>`
- if we are linking internally and more specifically to the SAME page we can use the href attribute `#idname` => Wordt vaak voor one-pagers gebruikt
<a href="#title">go to the top where the title lives</a>
`<a href="#title">go to the top where the title lives</a>`
- er kan maar zijn met een specifieke id => Unique
	- kan gebruikt worden in CSS, Links (href), JavaScript
- a-tags zijn ook inline-tags, DUS gaan niet in verschillende lijnen gezet worden
- If used to go to other page
<a href="otherpage.html">Go to the other page</a>
`<a href="otherpage.html">Go to the other page</a>`

- Functional href tags
	- open default mailclient
<a href="mailto:5w1l1@example.com">send an email</a>
`<a href="mailto:5w1l1@example.com">send an email</a>`
	- Call someone
<a href="tel:080020080">call proximus</a>
`<a href="tel:080022800">call proximus</a>`

![[Pasted image 20231016131618.png]]
![[Pasted image 20231016131627.png]]![[Pasted image 20231016134646.png]]
- Use "colspan" to make one square span multiple columns
- use "rowspan" to make one square span multiple rows

LOCAL
<img src="C:\Users\redle\Pictures\Syntra-logo-removebg-preview.png" width=200px>
`<img src="C:\Users\redle\Pictures\Syntra-logo-removebg-preview.png">`

ONLINE
<img src="https://art.pixilart.com/4692e4b4aecad6f.png" width= 200px>
`<img src="https://art.pixilart.com/4692e4b4aecad6f.png">`

alt-tag voor alternative view => text bijvoorbeeld die beschrijft wat er staat, of voor search engines

Forms
<form action="action_page.php">
	<label for="fname">First Name:</label><br>
	<input type="text" id="fname" name="fname" value=""><br>
	<label for="lname">Last Name:</label><br>
	<input type="text" id="lname" name="lname" value=""><br><br>
	
	<label for="password">password:</label><br>
	<input type="password" id="password" name="password" value=""><br><br>
	
	<label for="age">Age:</label><br>
	<input type="number" id="age" name="age" value=""><br><br>
	
	<label for="age">Age:</label><br>
	<input type="number" id="age" name="age" value=""><br><br>
	
	<input type="checkbox" name="wish" value="wish1" checked>wish1
	<input type="checkbox" name="wish" value="wish1" checked disabled>wish1
	<input type="checkbox" name="wish" value="wish1">wish1
	
	<input type="radio" name="eatin" value="eat in">eatin1
	<input type="radio" name="eatin" value="delivery">eatin2
	
	<input type="submit" value="Submit"><br>

	<textarea name="textarea" id="" cols="30" rows="10"></textarea>
</form>
```
<form action="action_page.php">
	<label for="fname">First Name:</label><br>
	<input type="text" id="fname" name="fname" value=""><br>
	<label for="lname">Last Name:</label><br>
	<input type="text" id="lname" name="lname" value=""><br><br>
	
	<label for="password">password:</label><br>
	<input type="password" id="password" name="password" value=""><br><br>
	
	<label for="age">Age:</label><br>
	<input type="number" id="age" name="age" value=""><br><br>
	
	<label for="age">Age:</label><br>
	<input type="number" id="age" name="age" value=""><br><br>
	
	<input type="checkbox" name="wish" value="wish1" checked>wish1
	<input type="checkbox" name="wish" value="wish1" checked disabled>wish1
	<input type="checkbox" name="wish" value="wish1">wish1
	
	<input type="radio" name="eatin" value="eat in">eatin1
	<input type="radio" name="eatin" value="delivery">eatin2
	
	<input type="submit" value="Submit"><br>

	<textarea name="textarea" id="" cols="30" rows="10"></textarea>
</form>
```
input types (GEEN EINDTAGS </...>)
- text
- password
- number
- submit
- checkbox (meerdere opties mogelijk)
- radio (maar één optie mogelijk)
- File => Kun je een bestand in uploaden
Textarea
- mogelijkheid grote textvakken te maken
	- BELANGRIJK: HEEFT WEL EINDTAG

VOOR SUBMITS
- in JavaScript => Gebruik Button
- Python => Gebruik Submit

Javascript
- `<button onclick="alert('ok dankjewel je wordt verwacht')"> Submit</button>`

Running static site
- Netlify
	- Sign up with GitHub
	- Home MOET index.html noemen!

- IFrame
	- runt html van andere site alsof die op deze site geintegreerd was

- `<span>tekst</span>`
	- is een inline tag => wordt altijd op één lijn weergegeven