# learn-node-js

### Importing Node JS Code Modules.
```node
app.js

const fs = require('fs')
fs.writeFileSync('notes.txt', 'This file was created by Node.js!!')
fs.appendFileSync('notes.txt', ' My Name is Tanvir')
```

### Importing Your own file
```node

----------------------------------
app.js

const name = 'Tanvir'
console.log(name)
----------------------------------
utils.js
console.log('utils.js')
const firstName = 'Mohammad'
module.exports = firstName

app.js
const firstName = require('./utils.js')

const lastName = 'Tanvir'
console.log(firstName + ' ' + lastName)
----------------------------------
utils.js
console.log('utils.js')

const add = function(a, b) {
    return a + b
}

module.exports = add

app.js
const add = require('./utils.js')

const sum = add(2, 4)
console.log(sum)
----------------------------------
notes.js
console.log('notes.js')

const getNotes = function() {
    return "Your Notes..."
}

module.exports = getNotes

app.js
const getNotes = require('./notes.js')

const notes = getNotes()
console.log(notes)

-------------------------------------
```
### Importing npm Modules

```node
npm install
npm i validator@13.12.0


```

