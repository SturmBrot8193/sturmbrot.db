# sturmbrot.db
**Support**: [Discord Server](https://discord.com/invite/Chu4sxNfaB)<br>
**Package**: [NPM Package](https://www.npmjs.com/package/sturmbrot.db)<br><br>
<a href="https://discord.com/invite/Chu4sxNfaB" target="_blank"><img src="https://img.devsforum.net/tr/img/h1Z2X3.png" alt="Join discord" width="256"></a><br>

## Installation
- `npm install sturmbrot.db` 
## Triggers
- `db.set('value', { value: '1' }`
- `db.add("value", 1)`
- `db.sub("value", 1)`
- `db.push("value", {value: "1"} )`
- `db.get("value")`
- `db.delete("value")`
- `db.all()`
- `db.clear()`<br><br>
 ## Examples
```js
const Database = require("sturmbrot.db");
const db = new Database("./database.json");

db.set('status', { status: 'Online' })
/*
JSON Output:
{
  "status": {
    "status": "Online"
  }
}
*/
db.set('status', { status: 'Offline'})
/*
JSON Output:
{
  "status": {
    "status": "Offline"
  }
}
*/

db.set('money', {userid: '0'})
/*
JSON Output:
{
  "money": {
    "userid": "0"
  }
}
*/

db.add('money', {userid: '5'})
/*
JSON Output:
{
  "money": {
    "userid": "5"
  }
}
*/

db.sub('money', {userid: '5'})
/*
JSON Output:
{
  "money": {
    "userid": "0"
  }
}
*/

db.has("money", {userid: '0'}) // Output: true
db.has("money", {userid: '5'}) // Output: false

console.log(db.all()) // Get the json file

db.delete("money", {userid}) // Deleting the Users money

db.clear() // Clears the database
```
