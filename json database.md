

Json is the data for a javascript database.

 ![Build a JSON database in 5 mins with JavaScript](https://www.youtube.com/watch?v=tP1kwGwh0U8)

<https://github.com/jamezmca/json-db>


The json data
db.json
``` json
{"james":"hello"}
```


dbFunctions.js
``` js
const fs = require('fs')

function readDb(dbName = 'db.json') {
    // read JSON object from file
    const data = fs.readFileSync(dbName, 'utf8')
    return JSON.parse(data)
}

function writeDb(obj, dbName = 'db.json') {
    if (!obj) return console.log('Please provide data to save')
    try {
        fs.writeFileSync(dbName, JSON.stringify(obj)) //overwrites current data
        return console.log('SAVE SUCESS')
    } catch (err) {
        return console.log('FAILED TO WRITE')
    }
}



module.exports = { readDb, writeDb }
```

writeExample.js
``` js
const { writeDb } = require("./dbFunctions")

const dataObj = {
    james: 'hello'
}

writeDb(dataObj)
```

readExample.js
``` js
const { readDb } = require("./dbFunctions");

console.log(readDb())
```

---


# Master JSON in an easy way

![Master JSON in an easy way](https://www.youtube.com/watch?v=KMLOWkGAxVc)

