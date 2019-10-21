
# ES7 JavaScript/Node/Mongoose/MongoDB-Mysql snippets


This extension provides you JavaScript and Node/MongoDb/Mongoose-Mysql snippets in ES7 with Babel plugin features for VS Code.

## Search command

### Please Reload plugin after installation in VScode 

You can search through snippets with `nodejssnippetsearch` command which can be run with `CMD + Shift + P` or Please enter the characters like cc or below listed Basic methods prefixes .
 <!-- just use `CMD + Shift + R` keybinding. -->

Here is direct link to marketplace [ES7 JavaScript/Node/Mongoose/MongoDB-Mysql snippets](https://marketplace.visualstudio.com/items?itemName=abrahamwilliam007.es7-javascript-class-snippets)

## Supported languages (file extensions)

- JavaScript (.js)
- JavaScript React (.jsx)

## Snippets info

Every space inside `{ }` and `( )` means that this is pushed into next line :)
`$` represent each step after `tab`

## Basic Methods

|  Prefix | Method                                              |
| ------: | --------------------------------------------------- |
|  `cc→` | `Creates javascript class'`                   |
|  `set→` | `Creates a set from the implementation of bucket-Please install npm install buckets-js `                                   |
|  `linkedlist→` | `Creates a LinkedList from the implementation of bucket-Please install npm install buckets-js`       |
|  `dic→` | `Creates a Dictionary from the implementation of bucket-Please install npm install buckets-js`                   |
|  `mdic→` | `Creates a MultiDictionary from the implementation of bucket-Please install npm install buckets-js ` |
|  `bst→` | `Creates a BSTree from the implementation of bucket-Please install npm install buckets-js `                         |
|  `stack→` | `Creates a Stack from the implementation of bucket-Please install npm install buckets-js`       |
|  `queue→` | `Creates a Queue from the implementation of bucket-Please install npm install buckets-js` |
|  `bag→` | `Creates a bag from the implementation of bucket-Please install npm install buckets-js `       |
|  `heap→` | `Creates a Heap-(min/max) from the implementation of bucket-Please install npm install buckets-js `                    |
|  `pq→` | `Creates a PriorityQueue from the implementation of bucket-Please install npm install buckets-js `                      |
|  `mysqldb→` | `Creates a Mysql Database sample implementation `                  |
|  `mongodb→` | `Creates a MongoDb Database sample implementation `                |
|  `mongoose→` | `Creates a Moongose Database sample implementation  `                |
| `mongoose-model→` | `Creates a Moongose Model sample implementation `                                   |
|  `func→` | `Creates a function  `              |
|  `arfunc→` | `Creates an arrow function `              |




### `cc`

```javascript
class Hero {
   constructor(name, level) {
       this.name = name;
       this.level = level;
   }
}
```

### `Heap`

```javascript
var bucket=buckets.Heap(compareFunction);
bucket.add(1);

//Min heap
function compare(a, b) {
 if (a is less than b by some ordering criterion) {
    return -1;
 } if (a is greater than b by the ordering criterion) {
    return 1;
 }
 // a must be equal to b
 return 0;
}

//max heap
function reverseCompare(a, b) {
 if (a is less than b by some ordering criterion) {
    return 1;
 } if (a is greater than b by the ordering criterion) {
    return -1;
 }
 // a must be equal to b
 return 0;
}

```



### `linkedlist`
```javascript
buckets.LinkedList()
Creates an empty Linked List.

var petsAreEqualByName = function(pet1, pet2) {
   return pet1.name === pet2.name;
  }
  ```

### `function`
```javascript
function functionName(){

    return;
}
  ```

### ` arrow function`
```javascript
() =>{

}
```


### `mocha`
```javascript
var assert = require('assert');
describe('Array', function() {
  describe('#indexOf()', function() {
    it('should return -1 when the value is not present', function() {
      assert.equal([1, 2, 3].indexOf(4), -1);
    });
  });
});  
```


### `mysqldb`
```javascript
var mysql = require('mysql');

var con = mysql.createConnection({
  host: "localhost",
  user: "myusername",
  password: "mypassword"
});

con.connect(function(err) {
  if (err) throw err;
  console.log("Connected!");
});
```



### `mongodb`
```javascript
var MongoClient = require('mongodb').MongoClient;
var url = 'mongodb://localhost/EmployeeDB';

MongoClient.connect(url, function(err, db) {

    var cursor = db.collection('Employee').find();

    cursor.each(function(err, doc) {

        console.log(doc);

    });
}); 
```



### `mongoose`
```javascript
  //Import the mongoose module
var mongoose = require('mongoose');

//Set up default mongoose connection
var mongoDB = 'mongodb://127.0.0.1/my_database';
mongoose.connect(mongoDB, { useNewUrlParser: true });

//Get the default connection
var db = mongoose.connection;

//Bind connection to error event (to get notification of connection errors)
db.on('error', console.error.bind(console, 'MongoDB connection error:'));
```


### `mongoose-model`
```javascript
 // Define schema
var Schema = mongoose.Schema;

var SomeModelSchema = new Schema({
  a_string: String,
  a_date: Date
});

// Compile model from schema
var SomeModel = mongoose.model('SomeModel', SomeModelSchema );
```
