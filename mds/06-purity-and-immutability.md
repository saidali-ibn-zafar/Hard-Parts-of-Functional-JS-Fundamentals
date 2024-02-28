# What is `pure function`?

- `Pure functions` are functions in programming that give the same output for the same set of inputs, regardless of how many times it's called.

```js
function add(a, b) {
    return a + b;
}

```

### This add function takes two numbers as input (a and b) and returns their sum. It meets the criteria of a pure function because:

- It always returns the same output for the same input. For example, add(2, 3) will always return 5.
- It doesn't have any side effects. It doesn't modify any variables outside its scope or perform any other actions besides computing the sum of its inputs.
- So, add is a pure function.

- - - - - 

# What is `Immutability`?

-  Immutable basically means something that cannot be changed.

```js
// Mutable approach (not immutable)
let mutableArray = [1, 2, 3];
mutableArray.push(4); // Modifies the original array
console.log(mutableArray); // Output: [1, 2, 3, 4]

// Immutable approach
let immutableArray = [1, 2, 3];
let newArray = [...immutableArray, 4]; // Create a new array with additional element
console.log(immutableArray); // Output: [1, 2, 3] (original array remains unchanged)
console.log(newArray); // Output: [1, 2, 3, 4]

```
