# JAVASCRIPT QUESTIONS : Variables, Data Types, Functions & Scope

## Q1. What is the difference between var, let, and const in JavaScript?

var, let, and const are all used to declare variables in JavaScript. The main difference is their scope and mutability. var is function-scoped and allows both redeclaration and reassignment, which can lead to bugs. let is block-scoped, allows reassignment but not redeclaration. const is also block-scoped, but it cannot be reassigned after initialization. For objects and arrays declared with const, their properties or elements can still be modified. In modern JavaScript, it's recommended to use const by default and let only when reassignment is needed. var is generally avoided in modern code

## Q2. Explain the concept of hoisting in JavaScript.

Hoisting is JavaScript's behavior of moving declarations to the top of their scope before execution. Variables declared with var are hoisted and initialized with undefined, so accessing them before declaration returns undefined. Variables declared with let and const are also hoisted, but they remain in the Temporal Dead Zone until their declaration is reached, so accessing them earlier throws a ReferenceError. Function declarations are fully hoisted and can be called before they are defined, while function expressions are not.

```
Example 1: var

console.log(name); // undefined
var name = "Nur";
console.log(name); // Nur

Example 2: let

console.log(age); // ReferenceError: Cannot access 'age' before initialization
let age = 24;

Example 3: const

console.log(PI); // ReferenceError
const PI = 3.1416;

Example 4: Function Declaration

sayHello(); // Hello

function sayHello() {
    console.log("Hello");
}

Example 5: Function Expression

sayHello(); // ReferenceError

const sayHello = function () {
    console.log("Hello");
};
```

## Q3. What is the Temporal Dead Zone (TDZ)?

The Temporal Dead Zone (TDZ) is the period between entering a scope and the point where a let or const variable is declared.
During this time, the variable exists but cannot be accessed.

```
{
    // TDZ starts

    console.log(name); // ReferenceError

    let name = "Nur";

    // TDZ ends
}
```

## Q4. Is there any difference between let and const regarding hoisting?

Actually there is no difference between them regarding hoisting. Both let and const are hoisted, but unlike var, they remain in the Temporal Dead Zone until their declaration is reached. The difference is not in hoisting—it's that const must be initialized when declared and cannot be reassigned, while let can be declared first and assigned later.

## Q5. What are primitive data types in JavaScript?

In JavaScript, data types are divided into two categories: primitive and non-primitive.Primitive data type is the most basic type of data in JavaScript. It stores a single value directly and is immutable, meaning the value itself cannot be changed.
When we copy a primitive value, JavaScript creates a new independent copy.

Primitive values are:

Stored by value, not by reference.
Immutable (the value itself cannot be modified).
Compared by their actual value.

```
let a = 10;
let b = a;

b = 20;

console.log(a); // 10
console.log(b); // 20

Changing b does not affect a because primitive values are copied.
```

JavaScript has 7 primitive data types:

- String – Represents text.
- Number – Represents integers and floating-point numbers.
- Boolean – Represents true or false.
- Undefined – A variable that has been declared but not assigned a value.
- Null – Represents the intentional absence of a value.
- Symbol – Represents a unique and immutable identifier.
- BigInt – Represents integers larger than the safe limit of the Number type.

## Q6. What are the non-primitive data types in JavaScript?

Non-primitive data types are also called reference types because they store a reference to a memory location instead of the actual value. The main non-primitive types in JavaScript are objects, arrays, and functions. Built-in types like Date, Map, Set, and RegExp are also objects, so they are non-primitive. Unlike primitive values, non-primitive values are mutable, and when copied, both variables refer to the same object in memory.

## Q7. Is an array an object?

Yes. In JavaScript, an array is a special type of object.

## Q8. Is a function an object?

Yes. Functions are special objects in JavaScript because they can be assigned to variables, passed as arguments, returned from other functions, and even have their own properties.

## Q9. What is the difference between == and === in JavaScript?

Both == and === are comparison operators in JavaScript, but they compare values differently.
The == operator is called loose equality. It compares values after performing type conversion if the data types are different. The === operator is called strict equality. It compares both the value and the data type without any type conversion. For example, 5 == '5' returns true because the string is converted to a number, but 5 === '5' returns false because their data types are different. In modern JavaScript, === is generally preferred because it avoids unexpected behavior caused by automatic type conversion.

## Q10. What is type coercion?

Type coercion is JavaScript's automatic conversion of one data type to another during an operation.

## Q11. What are Closures? Explain how closures work in JavaScript with an example.

A closure is a function that remembers the variables from its outer function, even after the outer function has finished executing. This allows the inner function to access and use those variables later. For example, if an outer function creates a count variable and returns an inner function, the inner function can continue updating count every time it's called. Closures are commonly used to maintain state and create private variables.

```
function outer() {
    let count = 0;

    function inner() {
        count++;
        console.log(count);
    }

    return inner;
}

const counter = outer();

counter(); // 1
counter(); // 2
counter(); // 3
```

## Q12. Why do closures work?

Closures work because JavaScript uses lexical scoping. A function remembers the scope in which it was defined, not where it is called.

## Q13. What is lexical scope?

Lexical scope means that a function can access its own variables, variables from its parent (outer) function and global variables.

```
const language = "JavaScript";

function outer() {
    const name = "Nur";

    function inner() {
        console.log(name);      // From outer scope
        console.log(language);  // From global scope
    }

    inner();
}
```

## Q14. What is the difference between null and undefined?

Both null and undefined represent the absence of a value, but they are used in different situations.undefined means a variable has been declared but hasn't been assigned a value yet. null, on the other hand, is a value that the programmer intentionally assigns to represent the absence of a value. For example, a newly declared variable is undefined, while setting a variable to null means you intentionally want it to have no value.

## Q15. What are arrow functions and how do they differ from regular functions?

Arrow functions are a shorter syntax for writing functions in JavaScript, introduced in ES6. They make code more concise and are commonly used for callbacks and array methods. The main difference is that regular functions have their own this, while arrow functions inherit this from the surrounding scope. Also, arrow functions cannot be used as constructors with the new keyword

## Q16. What is the Scope Chain in JavaScript?

The scope chain is the mechanism JavaScript uses to find variables. When a variable is accessed, JavaScript first looks in the current scope. If it's not found, it searches the parent scope, then the global scope. If the variable doesn't exist in any scope, JavaScript throws a ReferenceError. This allows inner functions to access variables from their outer functions.

## Q17. Explain the concept of the temporal dead zone.

The Temporal Dead Zone, or TDZ, is the period between entering a scope and declaring a let or const variable. During this time, the variable cannot be accessed, even though it has been hoisted. Trying to access it before its declaration results in a ReferenceError. The TDZ helps prevent bugs caused by using variables before they are initialized.

## Q18. What is a Pure Function? Give an example.

A pure function is a function that always returns the same output for the same input and doesn't modify or depend on any external data. For example, an add(a, b) function is pure because it always returns the same result for the same inputs. Pure functions are easier to test, debug, and maintain.

## Q19. What is the difference between function declaration and function expression?

A function declaration defines a named function using the function keyword and is fully hoisted, so it can be called before its declaration. A function expression stores a function inside a variable. It is not fully hoisted, so it must be declared before it is called. The main difference between them is their hoisting behavior.

## Q20. What are default parameters in JavaScript?

Default parameters allow us to assign default values to function parameters. If an argument is not provided, or if undefined is passed, JavaScript uses the default value instead. This makes functions more flexible and helps avoid undefined values.

## Q21. What is the typeof operator and what are its possible return values?

The typeof operator is used to determine the data type of a value or variable. It returns the type as a string, such as 'string', 'number', 'boolean', or 'object'. One important exception is that typeof null returns 'object', which is a historical bug in JavaScript. Also, arrays return 'object', while functions return 'function'.

## Q22. What is an immediately invoked function expression (IIFE)?

An Immediately Invoked Function Expression, or IIFE, is a function that executes immediately after it is defined. It is created by wrapping the function in parentheses and then adding another pair of parentheses to invoke it. IIFEs are commonly used to create a private scope and prevent variables from polluting the global scope.


Q16. What is destructuring in JavaScript? Explain with array and object examples.
Q17. What are the spread and rest operators and how are they used?
Q18. Explain the difference between map(), filter(), and reduce().
Q19. What is the difference between for...in and for...of loops?
Q20. What are template literals and tagged templates?
Q21. What is the event loop in JavaScript?
Q22. Explain how Promises work in JavaScript.
Q23. What is async/await and how does it improve upon Promises?
Q24. What is the difference between call(), apply(), and bind()?
Q25. What is prototypal inheritance in JavaScript?
Q26. Explain the concept of this keyword in different contexts.
Q27. What are JavaScript modules (import/export)?
Q28. What is the difference between shallow copy and deep copy of objects?
Q29. What are WeakMap and WeakSet and when would you use them?
Q30. Explain the concept of memoization with an example. 
