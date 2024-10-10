# codeConcepts

## Javascript
### helperMethods
- `document.write('HelloWorld')`
- `alert('Hello World')`
- `console.log('hello world')`

### variable
- basic building block, which can store, access and modify the values
- const
    - `const lastName = 'Kundala'`
    - can't reassign or redeclared,
    - needs to be initialized while declaration.
- let
    - `let name = 'Aawni'`
    - can be reassigned and redeclare.
- var
    - `var value = 'Abc'`

### Number
- +, -, *, /, %
+=, -=, *=, /=, ++, --, %

### TypeConversion
- Implicit
    - Happens automatically when we perform operations with mixed types.
- Explicit
    - manually, using built-in Functions
    - String Conversion
    - Number Conversion
    - Boolean Conversion

### DataType
- Primitive
    - String
    - Number
    - Boolean
    - Undefined
    - Null
    - Symbol
    - BigInt
- Non-Primitive
    - Object
    - Array
    - Function
    - Date

### Operators
- ArthematicOperator__+, -, *, /, %, **
- comparisionOperator__==, ===, !==, !===, >, <, >=, <=
- LogicalOperator__&&, ||, !
- AssignmentOperator__=, +=, -=, *=, /=, %=
- BitwiseOperator__&, |, ^, ~, <<, >>, >>>

### Array, Property & Methods
- Array, used to store multiple values in a single variable.
- Creating
    - `let abc = ['A', 'B', 'C']`
- Accessing
    - `let a = abc[0]`;
    - `let b = abc[1]`;

- Common Methods
    - push()
        -  Adds a new element to the end of an array.
    - pop()
        - Removes the last element from an array.
    - shift()
        - Removes the first element from an array.
    - unshift()
        - Adds a new element to the beginning of an array.
    - length
        - Returns the number of elements in an array.
    - slice()
        - Returns a section of an array.
    - splice()
        - Adds or removes elements at a specified index.

- Array iteration Methods
    - forEach()
        - takes a callback Function
        - executes the function once for each element.
        - `abc.forEach((ele)=>{console.log(ele)})`
    - map()
        - creates new array, the result of the function performed on every ele.
        - ```Javascript
            let nums = [1,2,3,4];
            let double = nums.map(function(ele){return ele2})
            ```
    - filter()
        - creates new array with the elements which satisfy the condition provided.
        - ```Javascript
            let age = [12,23,14,45,26];
            let adult = age.filter((ele)=>{return age >= 18})
            ```
    - reduce()
        - 
    - some()
        - Tests whether at least one element in the array satisfies the condition implemented by the function.
        - ```javascript
            let nums = [1,2,3,4]
            let hasEven = nums.some((ele)=>{return ele % 2 === 0})
            ```
    - every()
        - tests if all ele in an array satisfies the condition provided by the function
        - ```javascript
            let num = [2,4,5,6,7,8]
            let even = num.every((ele)=>{return num%2 === 0})
            ```
    - find()
        - returns the value of the 1st ele which satisfies the condition provided by the function.
        - ```javascript
            let ages = [3,10, 18, 20]
            let adult = ages.find((ele)=>{return ele >= 18})
            ```
    - findIndex()
        - returns the index of firstEle which satisfies the condition.
    - sort()
        - sort the ele of an array in accessending order
        - ```javascript
            let a = ['s','h','b','a','z']
            a.sort()
            ```

### String Property & Methods
- which allows us to manipulate and interact with string data effectively.
- Properties
    - length, returns the length of the string
    - `let text = 'HelloWorld'; console.log(text.length)`
- Methods
    - **charAt(index)**
        - returns the character present at the specified index.
        - `console.log(text.chatAt(2))`     // l
    - **charCodeAt(index)**
        - returns the 'unicode' of the character at specified index
        - `console.log(text.charCodeAt(0))` // 72
    - **concat(string2, string3, ..., stringN)**
        - joins 2 or more strings
        - `console.log(text1.concat(' ', text2))`
    - **includes(searchString)**
        - checks for a "string" present in another string.
        - `console.log(text.includes(World))`
    - **indexOf(searchValue, fromIndex)**
        - returns the index, of the first occurrence of the specified value
        - `console.log(text.indexOf('World'))`  // 7
    - **slice(start, end)**
        - extracts a part of the string, Returns it as a new String.
        - `console.log(text.slice(0,5))`  // Hello
    - **toLowerCase()**
        - converts the string to toLowerCase
        - `console.log(text.toLowerCase())`  // helloworld
    - **toUpperCase()**
        - converts the string to toUpperCase
        - `console.log(text.toUpperCase())`  // HELLOWORLD
    - **trim()**
        - removes whitespace from both ends of the string
        - `text.trim()`
    - **replace(searchValue, newValue)**
        - replaces a specified value, with another value
        - `console.log(text.replace('World', 'Javascript'))`    // HelloJavascript

### Functions
- functions are the fundamental building blocks which allows us to encapsulate the code for reuse and modularity.
- Definitions
    - Declaration
    - ```javascript
        function greet(name){
            return `Hello ${name}`  // doesn't print anything, doesn't allow to execute any code further.
        }
        ```
    - Expression
    - where the function is defined and stored in a variable.
    - ```javascript
        const greet = function(name) {
        return `Hello, ${name}!`;
        };
        console.log(greet("Bob")); // Output: Hello, Bob!
        ```
    - Arrow Function
    - ```javascript
        const greet = (name)=>{return `Hello ${name}`}
        console.log(greet('Charlie'))
        ```

- Function Types
    - Regular function
    - Async function
        - handles asyncOperations using 'async' and 'await'
        - ```javascript
            async function fetchData() {
            let response = await fetch('https://api.example.com/data');
            let data = await response.json();
            console.log(data);
            }
            fetchData();
            ```
    - Generator Function
        - useful for handling the sequence of data and implementating iterators
        - ```javascript
            function* generateSequence(start, end){
                for(let i=start; i<=end; i==>){ yield i; }
            }
            ```
    - Self Invoking Functions
        - functions which executes immediately after they are defined.
        - ```javascript
        (()=>{console.log('This function runs immediately..!')})
        ```
    - Function Constructor
        - creates new function object
        - ```javascript
            const add = new Function('a', 'b', 'return a + b');
            console.log(add(2, 3)); // Output: 5
            ```

- Function Parameters
    - Default Parameters
        - allows to set default values to the parameters
        - ```javascript
            function greet(name = "Guest") {
            return `Hello, ${name}!`;
            }
            console.log(greet()); // Output: Hello, Guest!
            ```
    - Rest Parameters
        - allows to pass an indefinite number of arguments as an array
        - ```javascript
            function sum(...numbers) {
            return numbers.reduce((acc, num) => acc + num, 0);
            }
            console.log(sum(1, 2, 3)); // Output: 6
            ```
    - Destructuring Parameters
        - allows to unpack the values from arrays or properties from objects.
        - ```javascript
            function display({ name, age }) {
            console.log(`Name: ${name}, Age: ${age}`);
            }
            const person = { name: "Alice", age: 25 };
            display(person); // Output: Name: Alice, Age: 25
            ```

- Declare & Invoke
- Parameters & Arguments
- Return
- Expressions

### Objects

### Conditional Statements
- Switch
- while
- do-while
- for

### Misc
#### Template Literals
#### Value vs Reference
#### Null and Undefined
#### Truthy & Falsy
#### Ternary Operator
#### GlobalScope
#### Local Scope
#### callBack Functions
#### HigherOrder Functions
#### Array iterators
#### forEach
#### map
#### filter
#### find
#### reduce
#### Math Object
#### Date Object


## JS_DOM
### window and document
### GetElementById
### GetElementsByTagName
### GetElementByClassName
### QuerySelector & QuerySelectorAll
### Navigate the DOM
- Childern
- parentElement
- nextSibiling
- previousSibiling
- nextElementSibling
### textContent NodeValue
### getAttribute(), setAttribute()
### classList & className
### createElement_createTextNode
- appendChild
- insertBefore
- replaceChild
- prepend innerText
- remove removeChild
### innerHTML & textContent
### Events
- click Events
- FunctionRefrence
- Mouse Events
- key Events
- Event Object
- currentTarget Vs Target
- Event Propagation, Bubbling, Capturing

### Forms
### Local Storage
### Local Storage with multiple values
### setTimeout
### setInterval
### Events_'DOMContentLoaded'
### Events_'Load'
### Events_'Scroll'
### Events_'ReSize'



## NodeJS
