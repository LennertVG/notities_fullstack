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

installing bcrypt
`npm install bcrypt`
= >adding bcrypt as type instead of module, because there is no more moule usage
`npm i --save-dev @types/bcrypt`
in de userservice de import
```typescript
import * as bcrypt from 'bcrypt';
```
dit geeft de mogelijkheid tot het commando 
```typescript
const salt= bcrypt.genSaltSync(10);
```
en 
```typescript
const hashedPassword = bcrypt.hashSync(password, salt)
```
deze samen gaan salt genereren en het passwoord encrypten met (in dit geval 10 karakters van) salt