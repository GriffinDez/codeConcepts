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
- Function Return
    - `return` statement is used to stop the execution of a function and return a value to the function.
    - return 'expression';    // if 'expression' is omitted, function returns `undefined`
    - returning functions
        - where functions can return other functions, which is useful for creating the higherOrder functions.
        - ```javascript
            function multiply(num1){
                return function(num2){
                    return num1*num2
                }
            }
            const double = multiply(2);
            console.log(double(5))
            ```
    - Asynchronous function
        - return statement used to return a promise
        - ```javascript
            async function fetchData() {
            let response = await fetch('https://api.example.com/data');
            let data = await response.json();
            return data;
            }
            fetchData().then(data => console.log(data));
            ```
- Expressions
    - expression is a way to define a function within an expression, rather than as a standalone project.
    - Anonymous function expression
        - ```javascript
            const greet = function(name){
            return `Hello ${name}..!`;
            }
            ```
    - Named function expression
        - ```javascript
            const factorial = function fact(n) {
            if (n <= 1) return 1;
            return n * fact(n - 1);
            };
            console.log(factorial(5)); // Output: 120
        ```

### Objects
- An object is a collection of properties, where each property is defined as a key-value pair. The key is a string (also called a property name), and the value can be any data type, including another object or a function.

- Creating Objects
    - Object Literals
        ```javascript
            const person = {
                firstName:'Abc',
                lastName:'xyz',
                age:30,
            }
        ```

    - using `new Object()`
    - using constructor function
        ```javascript
            function Person(firstName, lastName, age){
                this.firstName = firstName;
                this.lastName = lastName;
                this.age = age;
            }
            const person1 = new Person('Abc', 'xyz', 20);
        ```
- Accessing Object Properties
    - using dot/Bracket Notation
    - `console.log(person.firstName)`   // Dot Notation
    - `console.log(person['firstName'])`  //Bracket Notation
- Modifying

### Conditional Statements
- Switch
- while
- do-while
- for

### Misc
#### Template Literals
ES6 feature, ``(backticks) encloses the string.
- to create complex strings
- improves code readiblity.

#### Value vs Reference
value(Primitive dataTypes), like Numbers, String, Boolean, null, undefined, Symbol, BigInt... where the **copy** of the value is created.
- the change does not affects the original variable.
**NOTE**: Values, are stored directly in the variable.
```javascript
let a = 5;
let b = a; // b is a copy of a
b = 10;

console.log(a); // Outputs: 5
console.log(b); // Outputs: 10
```
================

RefrenceType___like Objects,Arrays,Functions. 
- where the ref to the same object is created in the memory.
- this affects the original array
**NOTE**: stores the refrence of the actual data. Multiple variables can refrence the same object.
```javascript
let obj1 = { name: "Alice" };
let obj2 = obj1; // obj2 is a reference to obj1
obj2.name = "Bob";

console.log(obj1.name); // Outputs: Bob
console.log(obj2.name); // Outputs: Bob
```
#### Null and Undefined
- Undefined, where the variable has been declared but not initialized.
    - typeOf undefined    // undefined
    - if a variable has not been initialized or if a function did not returns a value.

- null, represents the intentional absence of any object value.
    - typeOf null    // Object
    - explicitly indicates the variable to be empty.

#### Truthy & Falsy
Falsy___false, 0, -0, 0n, ""/''/``, null, undefined, NaN
Truthy___true, NonZeroNumbers, NonEmptyStrings, Objects, Functions.

#### Ternary Operator
- concise way to perform conditional operations.
- ifcondition ? returnIfTrue : returnIfFalse
- Readability__consider using if_else statements
- avoid Nesting, 

#### GlobalScope
- Global Scope is the outermost scope which is accessible from anywhere in the code. both from inside and outside the function.

- Declaration
    Variables declared outside any function/block are in global scope.
    `var globalVar = "I'm global"`;
- Accessiblity
    - can be accessed from any part of the code,
    ```javascript
    function showGloVar(){ console.log(globalVar) }
    showGloVar()
    ```
- Potential issues
    - Name collisions, since global variablesa are accessible anywhere, the risk of unintentionally modifying the same variable.
    - Memory Usuage, global variables remain in memory for lifetime of the application, which leads to the higher memory usuage.
- Best Practices
    - Minimize the use of global variables to avoid the conflicts of memory issues.
    use localScope whenever possible to limit the variable's accessiblity and lifespan.

#### Local Scope
- refers to the scope confined within a function.
- variables declared within a function are only accessible within that function and cannot be accessed from outside it.
- Declaration
    - variables declared inside the function using var, let, const in global scope.
    - ```javascript
        function myFunction() {
        var localVar = "I'm local!";
        console.log(localVar); // Outputs: I'm local!
        }
        console.log(localVar); // Error: localVar is not defined
        ```
- Accessibility
    - local variables can only be accessed within the function where they are declared.
- Purpose
    - Encapsulation
        - with the local scopes, we can keep the variables confined to the function they are used in.
        - encapsulation, prevents the interference with other variables within a function of a program.
    - Avoiding name conflict
        - as we can have the variables with same names to be existed in different function with having a clash.
    - Memory management
        - as it is created when the function is called and destroyed when it the function exists.

#### Function Vs Block Scope
    - Before ES_6, it was globalScope and FunctionScope.
    - With ES_6, this introduced Block Scope => let & const, which allows the variable to be scoped within the blocks. i.e, `{}`
        - Here, blockScoped is only accessible within the `if` or `for` block.
        - trying to access the blockscoped outside the block, it throws the RefrenceError.
#### callBack Functions
- callback function, a function which is being passed as an argument to the another function, and is executed after the operation has been completed.
- used to handle asynchronous functions, as such this ensures the code is being executed only after the another piece of code has finished its execution.

Purpose of callback
- Handling of Asynchronous Operations
    - js is single threaded, means this performs only one operation at a time.
    - callback allows us to handle operations like fetching data from a server without blocking the main thread. ex:_ readingFiles, interacting with Databases etc..
- creatin reusuable and Modular code
    - callbacks allows functions to be more flexible and reusuable. which enables us to pass different functions such as to make the code more modular.
    - ```javascript
        function fetchData(callback){
            setTimeout(()=>{
                let data = 'Data from Server';
                callback(data)
            }, 2000)
        }
        function displayData(data){
            console.log(data);
        }
        fetch(displayData)
        ```
- `fetchData` is a function that simulates fetching data from a server. It takes a callback function as an argument.
- `setTimeout` is used to mimic a delay (asynchronous operation). After 2 seconds, it calls the `callback` function with the fetched data.
- `displayData` is a callback function that logs the data to the console.
- `fetchData(displayData)` passes `displayData` as a callback to fetchData.

>Handling Errors
- by `error-first` callback pattern, where the first argument of the callback function is an error Object, 2nd is the result.
- > SameExample with Error Handling
    - ```javascript
        function fetchData(callback) {
          setTimeout(() => {
            let error = null;
            let data = "Data from server";

            if (!data) {
              error = "No data found";
            }

            callback(error, data);
          }, 2000);
        }

        function handleResponse(error, data) {
          if (error) {
            console.error("Error:", error);
          } else {
            console.log("Data:", data);
          }
        }

        fetchData(handleResponse); // After 2 seconds, logs         "Data: Data from server"
        ```
> Using callback with Higher Order Functions
- HigherOderFunction, which take other functions as arguments or return the functions as the result.
- callback with HOF used to add the functionalty to oexecute the specific tasks.
- ```javascript
    function createMultiplier(factor) {
    return function (number) {
    return number * factor;
        };
    }
    const double = createMultiplier(2);
    const triple = createMultiplier(3);

    console.log(double(5)); // 10
    console.log(triple(5)); // 15
    ```
- Callbacks are used to handle asynchronous operations, creating the reusuable code which ensures the code is being executed in the correct order.

#### HigherOrder Functions
- js feature which takes other functions as an argument or returns the functions as their result.
- > What is the Higher Order function
    - which takes 1 or more function as arguments
    - Return the function as its result.
- > Why HigherOrder functions.
    - Reusablity
        - HigherOrderFunction, promote code reuse by abstracting common patterns and operations.
    - Functional Programming
        - which makes the code more declarative and concise.
    - Asynchronous Operations
        - used to handle Async Operations like promises and event listeners.
- > Examples of Higher Order Functions
    - ArrayMethods, `map(), filter(), reduce()` are some of the methods of HOF.
        - used to test each element of an array based on certain condition.
        - takes function as an argument.
        - results in the transformed array of data
    - Event Handlers
        - used to handle and verify userInput, userAction and browserAction
        - because they take faunction as args, and executes it when a certain event occurs.
        - ```javascript
            document.getElementById("myButton").addEventListener("click", function() {
            alert("Button was clicked!");
            });
            ```
        - When you use `addEventListener`, you pass it a function (callback) to execute when the event happens.
        - The function passed to `addEventListener` is a callback function.
        - This makes `addEventListener` a higher-order function since it's accepting another function as an argument.
        - Such that, each time the button is clicked, the `addEventListener` HOF executes the callback function, demonstrating the higher-order nature.
    - Customized HOF
        - ```javascript
            function applyDiscount(discount) {
            return function (price) {
            return price - price * discount;
                };
            }

            const tenPercentOff = applyDiscount(0.10);
            console.log(tenPercentOff(100)); // 90
            console.log(tenPercentOff(50));  // 45
            ```
        - applyDiscount is a higher-order function.
        - It takes a discount rate and returns a new function that applies the discount to a given price.
    - Generally used to handle callbackFunctions
        - ```javascript
            function fetchData(callback) {
            setTimeout(() => {
            let data = "Data from server";
            callback(data);
                }, 1000);
            }

            function handleData(data) {
            console.log(data);
            }
            fetchData(handleData);
            ```
        - Here, fetchData is a higher-order function that takes a callback and executes it after fetching data asynchronously.

#### Math Object
- Properties
    - Math.PI
- Methods
    - `Math.abs(x)`, returns the absolute of a number
    - `Math.ceil(x)`, Returns the smallest integer greater than or equal a number.
    - `Math.floor(x)`, returns the largest integer less than or equal to a number.
    - `Math.round(x)`, returns the value of a number rounded to the nearest integer.
    - `Math.max(x,y,z,...)`, Returns the largest of zero or more numbers.
    - `Math.min(x,y,z,...)`, Returns the smallest of zero or more numbers.
    - `Math.random()`, Returns the pseudo-number b/w 0-1
    - `Math.sqrt(x)`, Returns the positive square root of a number
    - `Math.pow(base, exponent)`, Returns the base to the exponent of the power
    - `Math.log(x)`, Returns natural logarithm (base E)

- > NOTE
    - we have to use the Math object directly, without creating an instance
    - `Math` obj covers a vast area of Mathematical Ops, i.e. trigno to logarithms...
    

#### Date Object
- current Date & time
    - `const now = new Date(); c.log(now)`, outputs current date & time
- Specific Date & time
    - `const specificDate = new Date('2024-10-17T22:23:00');  c.log(specificDate)`
- Date Components
    - `const dateComponents = new Date(2024, 9, 17, 22, 23, 0, 0);  c.log(dateComponents)`

- > Date Methods
- Get Methods
    - `getDate()`: Returns the day of the month (1-31).
    - `getMonth()`: Returns the month (0-11).
    - `getFullYear()`: Returns the year (4 digits).
    - `getHours()`: Returns the hours (0-23).
    - `getMinutes()`: Returns the minutes (0-59).
    - `getSeconds()`: Returns the seconds (0-59).
    - `getMilliseconds()`: Returns the milliseconds (0-999).
    - `getTime()`: Returns the time value in milliseconds since January 1, 1970.
- > Set Methods
    - `setDate(day)`: Sets the day of the month.
    - `setMonth(month)`: Sets the month (0-11).
    - `setFullYear(year)`: Sets the full year.
    - `setHours(hours)`: Sets the hours (0-23).
    - `setMinutes(minutes)`: Sets the minutes (0-59).
    - `setSeconds(seconds)`: Sets the seconds (0-59).
    - `setMilliseconds(milliseconds)`: Sets the milliseconds (0-999).
    - `setTime(milliseconds)`: Sets the time in milliseconds since January 1, 1970.
- > Formating Dates
    - `toString()` and `toISOString()`
        - toString(): Returns a string representation of the date.
        - toISOString(): Returns the date in ISO 8601 format.
    - `toDateString()` and `toTimeString()`:
        - toDateString(): Returns the date portion of the date.
        - toTimeString(): Returns the time portion of the date.
- > Manipulating Dates
    ```javascript
        const date = new Date();
        date.setDate(date.getDate() + 5); // Adds 5 days
        console.log(date);
        
        date.setHours(date.getHours() - 2); // Subtracts 2 hours
        console.log(date);
    ```
- > Timezone & locale 
    ```javascript
        const date = new Date();
        console.log(date.toLocaleDateString('en-US')); // Outputs date in 'MM/DD/YYYY' format for the US locale
        console.log(date.toLocaleTimeString('en-US')); // Outputs time in 'HH:MM:SS AM/PM' format for the US locale
    ```
- > NOTE
    - Learn different ways to initiate Date Objects
    - Get and Set Methods, used crucial for extracting and manipulating date Components
    - Formatting, Practice more methods
    - understand how Date object handles timezone and offsets.



## JS_DOM
### window and document
### selectors
- `getElementById`, Selects a single element by its ID.
- `getElementsByTagName`, Selects all elements with a specified tag name. Returns a live HTMLCollection.
- `getElementByClassName`, Selects all elements with a specified class. Returns a live HTMLCollection.
- `querySelector`, Selects the first element that matches a CSS selector.
- `querySelectorAll`, Selects all elements that match a CSS selector. Returns a static NodeList.

- useCase & Examples
    - Changing text Content
        - `const ele = document.getElementById('myId'); ele.textContent = 'NewTextContent'`
    - Modifying CSS
        - `const ele = document.querySelector('.myClass'); ele.style.backgroundColor = 'blue'`
    - Adding/Removing classes
        - ```javascript
            const element = document.querySelector('.myClass');
            element.classList.add('newClass');
            element.classList.remove('oldClass');
        ```
    - iterating over NodeList
        - ```javascript
            const elements = document.querySelectorAll('.myClass');
            elements.forEach(element => {
              element.style.color = 'red';
            });
        ```
- > Performance
    - ** Always ensure the elements exist before accessing them.
    - `getElementById`: Fastest as it directly accesses elements.
    - `querySelector` and `querySelectorAll`: More flexible but slightly slower due to CSS parsing. wide support, cross browser compatiblity
    - `getElementsByClassName` and `getElementsByTagName`: Return live collections which update dynamically; this can impact performance with large sets.

- combining all the methods for more complex selections
    - by using Id
        - `const parentElement = document.getElementById('parentId');`

### Traversing the DOM
- Traversing through DOM, allows us to access, modify and manage the relationship b/w the elements.
- Purpose
    - Access & manipulate elements
    - Respond to user input & Events
    - alter the layout and content in realTime.
- > upwardTraversal (Accessing Parents)
    - parentNode, Access the parent element of a node.
    - closest(), gets the closest ancestor which matches the given CSS Selector.

- > DownwardsTraversal (Accessing Children)
    - `childNodes`, Returns the nodeList of all childNodes, **including Text Node.**
    - `children`, returns the HTML collection of all the child elements, **excluding text nodes**

- > SidewaysTraversal (Accessing Sibling)
    - `nextSibling`, Access the next sibling node.
    - `previousSibling`, Access the previous sibling node.
    - ```Javascript
        // Example DOM structure
        /*
        <div id="parent">
          <div id="child1">Child 1</div>
          <div id="child2">Child 2</div>
        </div>
        */

        let parent = document.getElementById('parent');
        let child1 = parent.children[0]; // Accessing the first child element
        console.log('First Child:', child1.textContent);

        let child2 = child1.nextSibling; // Accessing the next sibling node
        while (child2 && child2.nodeType != 1) { 
            child2 = child2.nextSibling; // Skip text nodes
        }
        console.log('Next Sibling:', child2.textContent);
    ```
- > Always check for ExistenceOfTheElement
    - ```javascript
        let element = document.getElementById('elementID');
        if (element) {
          // Safe to manipulate element
        }
    ```
### textContent NodeValue
- Defn 
    - textContent
        - textContent is a property that represents the text content of a node and its descendants. It includes all text inside the element, including text within child elements.
        - Used to get or set the text content of an element,
        - useful for manipulating the text within an element without affecting any nested HTML structure
        - ```javascript
            // Selecting an element
            let element = document.getElementById('myElement');

            // Getting text content
            console.log(element.textContent);

            // Setting text content
            element.textContent = 'New Text Content';
        ```
    
    - NodeValue
        - property that represents the value of a node. For text nodes, it’s the text content. For other node types like attributes and comments, it returns the value of the node.
        - Used to get or set the value of a node.
        - useful for text nodes, comments, and attribute nodes.
        - ```javascript
            // Creating a text node
            let textNode = document.createTextNode('Hello World');

            // Getting node value
            console.log(textNode.nodeValue);

            // Setting node value
            textNode.nodeValue = 'New Text Content';

            // Working with attribute nodes
            let attr = document.createAttribute('class');
            attr.nodeValue = 'new-class';
        ```
- Differences
    - Scope
        - textContent: Affects the entire text content of an element, including its children.
        - nodeValue: Typically used with text, comment, and attribute nodes directly.
    - usuageContext
        - textContent: Commonly used for elements to read or write their text content.
        - nodeValue: Used in more specific contexts, like manipulating individual text or attribute nodes.

- > NOTE
    - performance, `textContent` replaces all text inside an element, which can be more efficient than modifying individual child nodes.
    - both supports Cross Browser Compatiblity
    - Security, `textContent` is safer for setting text content since it does not parse HTML, avoiding potential cross-site scripting (XSS) attacks.

### getAttribute()
- Defn 
    - getAttribute() is a method in JavaScript used to retrieve the value of a specified attribute from an HTML element. 
    - returns the value as a string,
- Purpose
    - access the value of an attribute of a DOM (Document Object Model) element
    - generally used when working with dynamic attributes, which might change durning the lifecycle of a web page.
    - `var attributeValue = ele.getAttribute(attributeNameWhoseValueNeedsToBeFetched);`

- Example
    - ```
        > html
            <a id="myLink" href="https://www.example.com" title="Example Site">Visit Example</a>

        > javascript
            var link = document.getElementById("myLink");
            var hrefValue = link.getAttribute("href");
            console.log(hrefValue); // Outputs: "https://www.example.com"
    ```
- Example with Custom attribute
    - ```
        > html
            <div id="myDiv" data-custom-attr="someValue">Hello World</div>
        > Javascript
            var div = document.getElementById("myDiv");
            var customAttrValue = div.getAttribute("data-custom-attr");
            console.log(customAttrValue); // Outputs: "someValue"
    ```

### setAttribute()
- Defn 
    - method adds a new attribute or changes the value of an existing attribute on the specified element.
    - Used to dynamically set or update the value of an attribute.
    - ```javascript
        // Assuming an element like <div id="myDiv"></div>
        let element = document.getElementById('myDiv');

        // Set the "class" attribute
        element.setAttribute('class', 'newClass');
        console.log(element.className); // Outputs: newClass

        // Set a custom data attribute
        element.setAttribute('data-value', '456');
        console.log(element.getAttribute('data-value')); // Outputs: 456
    ```
- creates new attributes if it does not exists.
- sets the attribute's value,
- custom Data Attribute, need to be prefixed with `data-` used to store data.

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

## ES_version
### ES_6(ECMAScript 2015)
### ES_7(ECMAScript 2016)
- Exponentiation Operator(**)
    - `let result = 2**3` // 8
- Array.prototype.includes
    - `let arr = [1,2,3]; console.log(arr.includes(2))`
### ES_8(ECMAScript 2017)
- Async/Await
    ```javascript
    async function fetchData() {
    let response = await fetch('url');
    let data = await response.json();
    return data;
    }
    ```
- Object.values, Object.entries
    ```javascript
    let obj = { a: 1, b: 2 };
    console.log(Object.values(obj)); // [1, 2]
    console.log(Object.entries(obj)); // [['a', 1], ['b', 2]]
    ```

### ES_9(ECMAScript 2018)
- Rest/Spread
- Asynchronous Iteration
- promise.prototype.finally

### ES_10(ECMAScript 2019)
- Array.prototype.flat, Array.prototype.flatMap
- Object.fromEntries
- String.prototype.trimStart, String.prototype.trimEnd

### ES_11(ECMAScript 2020)
- Optional Chaining(?.)
- Nullish Coalescing Operator(??)
- Dynamic Import

### ES_12(ECMAScript 2021)
- Logical Assignment Operator
- Numeric Separators
- String.prototype.ReplaceAll

### ES_13(ECMAScript 2022)
- Top-Level Await
- class Fields
- Private Method and Fields

### ES_14(ECMAScript 2023)
- Array.prototype.toSorted
- Array.prototype.toReserved
- Array.prototype.toSpliced

### ES_15(ECMAScript 2024)
- RegExp Match Indices
- Array.prototype.with

## NodeJS
