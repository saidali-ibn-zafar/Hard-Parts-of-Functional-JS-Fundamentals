# What is `function decoration`?

- 
Function decoration, also known as function wrapping or function composition, is a programming technique where one or more functions are wrapped around another function to extend or modify its behavior without changing its core implementation.

```js
// Original function
function greet(name) {
    return `Hello, ${name}!`;
}

// Decorator function to add additional behavior
function withUpperCase(originalFunction) {
    return function(name) {
        return originalFunction(name.toUpperCase());
    };
}

// Decorate the original function
const decoratedGreet = withUpperCase(greet);

// Call the decorated function
console.log(decoratedGreet('John')); // Output: "Hello, JOHN!"
```


- - - - - 

# What is `partial application`?

- Partial application is a functional programming technique where a function is applied to some of its arguments, producing a new function that takes the remaining arguments. In other words, it allows you to create a new function by fixing a certain number of parameters of an existing function.

Example 1:

```js
// Original function with multiple parameters
function add(a, b, c) {
    return a + b + c;
}

// Partially apply the add function
const add5 = add.bind(null, 5); // Fixing the first parameter to 5

// Now add5 is a new function with the first parameter fixed to 5
console.log(add5(10, 15)); // Output: 5 + 10 + 15 = 30

```

Example 2:

```js
const multiply = (a, b) => a * b
function prefillFunction (fn, prefilledValue){
 const inner = (liveInput) => {
 const output = fn(liveInput, prefilledValue)
 return output
 }
 return inner
}
const multiplyBy2 = prefillFunction(multiply, 2)
const result = multiplyBy2(5)
```

