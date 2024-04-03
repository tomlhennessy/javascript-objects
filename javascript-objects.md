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

# Reference vs Primitive Types

* Primitive Types:
    - Boolean, null, undefined, number, string
    - immutable: cannot be directly changed

* Reference Type:
    - Object (arrays are objects too)
    - Mutable: values can be directly changed


# Rest and Spread

* Overview:
    - Functions in JavaScript can take fewer or more arguments than specified
    - Rest parameter syntax captures multiple arguments into an array
    - Spread operator syntax spreads elements of arrays or objects

* Accepting Arguments
    - Functions can take fewer arguments (default to undefined) or more arguments (extras ignored)

* Rest Parameter Syntax
    - Uses '...' before the name of the array parameter
    - Captures incoming arguments into an array
    - Only last parameter can be a rest parameter
    Example:
    - __'function logArguments(...allArguments) {...}'__
    - Captures all incoming arguments into an array

* Utilising Rest Parameters:
    - Useful for functions with an unknown number of arguments
    - Example: summing all incoming numbers

* Spread in Objects:
    - Spreads key-value pairs from one object to another
    - Also used to merge multiple objects
    Example (Spreading Arguments):
    - Spread array elements into function arguments

* Conclusion:
    - Rest parameter collects multiple elements into an array
    - Spread operator expands elements of arrays or objects


# Destructuring

* Overview:
    - Destructuring allows easy access to elements in arrays or objects
    - You can destructure arrays to reference specific elements or objects to reference specific values
    - It's useful for simplifying code and parameter handling in functions

* Destructuring Arrays:
    - Syntax __'let [var1, var2] = array;'__
    - Variables on left correspond to elements in array
    Example
    - __'let [firstEl, secondEl] = numArray;'__

* Swapping Variables:
    - Destructuring enables swapping variable values easily
    - Example: __'[num1, num2] = [num2, num1];'__

* Destructuring Objects:
    - Syntax: __'let { key1, key2 } = obj;'__
    - Variables match object keys
    - Can alias variables if key names differ
    - Useful for nested objects

* Destructuring in Functions:
    - Parameters can be destructured into variables
    - Useful for handling objects passed to functions
    - Simplifies accessing specific values
    Example (Destructuring Parameters):
    - __'function ownerName({ owner }) {...}'__
    - Assigns value of 'owner' key to 'owner' parameter

* Complex Example:
    - Aliased object destructuring used for handling same key names
    - Parameters can be nested objects for more complex data

* Conclusion:
    - Destructuring simplifies accessing and handling elements in arrays and objects
    - Useful for cleaner code and easier parameter handling in functions
