<h1 align="center">JavaScript Interview Questions</h1>

## 🎯 JavaScript Fundamentals

## Q01. What are the data types present in JavaScript?

JavaScript has 8 data types. Seven of them are primitive data types, and one is a non-primitive data type.

The seven primitive data types are String, Number, BigInt, Boolean, Undefined, Null, and Symbol.

The non-primitive data type is Object. Arrays and Functions are also considered objects in JavaScript.

For example, String is used for text, Number is used for numeric values, Boolean stores true or false, and Object can store multiple related values.

## Q02. What is the difference between null and undefined?

undefined and null both represent the absence of a value, but they have different meanings.

undefined usually means that a variable has been declared but no value has been assigned to it yet.

On the other hand, null is an intentional empty value. It means that the developer has explicitly set the value to null to show that there is currently no value.

For example, if we write let user;, the value of user is undefined. If we write let user = null;, the value is null.

One more important point is that typeof null returns "object". This is an old behavior in JavaScript, and null itself is not actually an object.

## Q03. How does JavaScript handle type coercion?

JavaScript handles type coercion by converting a value from one data type to another when it is needed.

There are two types of coercion. The first one is implicit coercion, where JavaScript automatically converts the type. For example, when we write "10" + 5, JavaScript converts the number 5 into a string, so the result is "105".

The second one is explicit coercion, where we convert the type ourselves. For example, Number("10") converts the string "10" into the number 10.

The == operator can also perform type coercion during comparison, while the === operator does not perform type coercion. It checks both the value and the type.

## Q04. Explain the concept of hoisting in JavaScript.

Hoisting is a JavaScript behavior where variable and function declarations are processed before the code is executed.

For example, a variable declared with var can be accessed before its declaration, and it returns undefined because the var declaration is hoisted and initialized with undefined.

let and const are also hoisted, but they stay in the Temporal Dead Zone until the code reaches their declaration. If we access them before that point, JavaScript throws a ReferenceError.

Function declarations are also hoisted, so we can call a function before its declaration in the code.

## Q05. What is the scope in JavaScript?

Scope defines where a variable can be accessed in JavaScript.

JavaScript mainly has global scope, function scope, and block scope. A variable in the global scope can be accessed from different parts of the code. A variable declared inside a function is normally available only inside that function. Variables declared with `let` and `const` are block-scoped, so they can only be accessed inside the block where they are declared.

If JavaScript cannot find a variable in the current scope, it looks for it in the outer scope. This process is called the scope chain.

## Q06: What is the difference between == and === ?

## Q07. Describe closure in JavaScript. Can you give an example?

## Q08. What is the 'this keyword' and how does its context change?

## Q09. What are arrow functions and how do they differ from regular functions?

## Q10. What are template literals in JavaScript?

## 🎯 JavaScript Functions and Higher-Order Functions

## Q11. What is a higher-order function in JavaScript?

## Q12. Can functions be assigned as values to variables in JavaScript?

## Q13. How do functional programming concepts apply in JavaScript?

## Q14. What are IIFEs (Immediately Invoked Function Expressions)?

## Q15. How do you create private variables in JavaScript?
