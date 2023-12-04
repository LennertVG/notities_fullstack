#introductie 
pwd = path to directory
cd = change directory
ls = list
mkdir (name) = make directory (mapje)
rmdir (name) = remove directory (mapje)
git init = initialize git
code. => opent visualstudiocode in de folder waar we zitten
![[Pasted image 20231017111325.png]]
cd .. => Return folder

In VSC: Install gitGraph

U(ntracked)= new
M(odified)= bestaand/gewijzigd
D(eleted)= iets verwijderd (komt ook bij renaming)

Na wijzigingen: Ga naar Source Control => + (state changes)
A(dded) = toegevoegd aan uw gitHub repository

Type a message and commit to take the snapshot

To find older versions => Git Graph
Right click and press checkout a version to use that specific iteration of the file

git clone "github link" => download another person's github repository

Pull can draw in the latest version!

Removing git: rm -rf .git => BE CAREFUL, THIS BREAKS EVERYTHING IN SOME CASES

touch .gitignore => Alles wat je hierin typt wordt genegeerd door git
- maak een file: .gitignore
- Maak een file die je wilt dat genegeerd wordt (bijvoorbeeld credentials, .env-files, etc...)
- zet in de .gitignore de .filename van de file die je wilt dat genegeerd wordt

git Stash
- saves current changes without committing them

Forking = duplicate a project, edit it, send your copy to the creator for review to see if they use it

Auth GitHub

Forking
 ![[Pasted image 20231113145110.png]]
- IS EEN EIGEN VERSIE VAN IEMAND ANDERS ZIJN REPOSITORY
	- Maakt een branch![[Pasted image 20231113145234.png]]
	- links onder VS-Code ![[Pasted image 20231113145635.png]]
		- Hier kunnen takken gemaakt worden![[Pasted image 20231113145706.png]]
	- Na nieuwe tak gemaakt te hebben maak je nieuwe files
		- zorg ervoor dat de namen anders zijn, als nieuwe naam => Merge conflict
		- OF zorg ervoor dat de pulls gedaan zijn VOORDAT je zelf terug edit => niet tegelijk bewerken en eerst externe changes in orde maken voor je begint met editten
	- Commit changes and push
	- Create pull-request