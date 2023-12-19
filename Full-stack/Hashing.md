#JavaFrameworks 
Salt + password = Hash
Hashing vs Encrypting
- Hashing
	- One-way => kan niet unhashed worden
	- "Salt" added => Verandert wachtwoord zodat het praktisch onmogelijk is dat het wachtwoord al eens voorkomt in de "rainbow table"
- Encryption
	- two-way => Kan decrypted worden
	- makkelijker gehackt

WW kunnen technisch gehasht worden zonder salt, but it's less secure