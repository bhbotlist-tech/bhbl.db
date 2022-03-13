# bhbl.db
<a href="https://bhbotlist.xyz/dc" target="_blank"><img src="https://logos-world.net/wp-content/uploads/2020/12/Discord-Logo.png?size=512" alt="Join our discord" width="256"></a><br>
**Support:** [https://bhbotlist.xyz/dc](https://bhbotlist.xyz/dc) <br>
**NPM:** [npmjs.com/package/bhbl.db](https://www.npmjs.com/package/bhbl.db)<br>

```js
const Database = require("bhbl.db");
const db = new Database("./db.json");

db.set('serverStatus', { status: 'Online' })
/*
"serverStatus": {
  "status": "Online"
}
*/
db.add("money_bhbl", 500)
/* 
  "money_bhbl": 500
*/
db.push("serverSettings", { whitelist: "on", playerCount: "24" })
/*
"serverSettings": [
    {
      "whitelist": "on",
      "playerCount": "24"
    }
  ]
*/
db.has("money_bhbl") // true
db.has("money_ibhbl") // false

db.get("money_bhbl")
// => 500

db.sub("money_bhbl", 100)
// => 400

db.fetch("serverStatus")
// => { status: "Online" }

db.get("serverStatus")
// => { status: "Online" }

db.delete("serverStatus")
// => {}

db.all()
/*
{
  money_bhbl: 500,
  serverSettings: [ { whitelist: 'on', playerCount: '24' } ]
}
*/

db.clear()
// {}
```
## Installation
*If you have trouble with the installation, please feel free to visit our [discord](https://bhbotlist.xyz/dc) address.*
- `npm i bhbl.db`
