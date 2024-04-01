# The Object Type

* Objects:
    - Diverse data structures, store data with key-value pairs
    - Keys are strings, values can be any data type
    - Accessed through bracket or dot notation

* Setting Keys and Values:
    - Use bracket notation to create key-value pairs
    - Access values using keys. Undefined if key doesn't exist
    - Check existence with "key in object"

* Using Variables as Keys:
    - Variables with string values can be keys
    - Values in objects can change with variable keys

* Different Notations:
    - Bracket vs Dot notation: pros and cons
    - Dot notation is cleaner but less flexible

* Operator Precedence:
    - Objects follow operator presedence rules
    - Associativity determines order of operations

* Recap
    - Objects: key-value pairs, flexible data storage
    - Accessing, setting values with different notations
    - Checking key existence with patterns like object[key] === undefined

# Iterating Through Objects

* Iterating Through Objects:
    - Objects store unordered key-value pairs
    - No indices to access values; need to iterate differently

* For...in loop:
    - Syntax: __'for (let variable in object) { statement; }'__
    - Example: Iterate through keys with __'for (let currentKey in obj)'__

* Accessing Values:
    - Bracket notation: __'obj[key]'__ for values
    - Cannot use dot notation for iteration

* Methods vs Functions:
    - Methods are functions belonging to objects
    - Defined with key-value pairs
    - Example: __'dog.bark = function() { ... };'__

* Useful Object Methods:
    - __'Object.keys(obj)'__ returns keys as an array
    - __'Object.values(obj)'__ returns values as an array
    - __'Object.entries(obj)'__ returns [key, value] pairs as an array

* Recap
    - Iterating with 'for...in' loop
    - Defining and invoking methods on objects
    - Using 'Object.keys()', 'Object.values()', and 'Object.entries()' for iteration


## Iterate Through Obj
Takes an object as input and iterates through each key-value pair  in the object, printing them to the console in the format "key - value".

```javascript
// define a function that takes an object as input
function printObject(obj) {
    // iterate through each key in the object
    for (let key in obj) {
        // get the value associated with the current key
        let value = obj[key];
        // print the key-value pair to the current key
        console.log(key + ' - ' + value);
    }
}
```

## Cat Builder
Creates and returns a new cat object with specified properties based on the arguments passed to the function

```javascript
function catBuilder(name, color, toys) {
    // create new object named "cat" with properties assigned from the parameters
    let cat = {
        name: name,
        color: color,
        toys: toys
    };

    return cat;
}
```
