# What is map() ?
- In JavaScript, the map() method is used to iterate over an array and apply a function to each element of the array, returning a new array with the results of calling the provided function on every element. It does not mutate the original array.
```js
const map = (array,   instructions) => {
  const output = [];
  for(let i = 0; i < array.legth; i++){
    output.push(instructions(array[i]));
  }
  return output;
}

const multiplyBy2 = input => input2;
const result = map[1, 2, 3], multiplyBy2);
```

- - - - -

# What is reduce()?

- Reduce is a fundamental higher-order function in functional programming, and particularly in JavaScript. It is used to iterate over an array and accumulate a single result by applying a combining function to each element of the array.

```js
  const reduce = (array, howToCombine, buildingUp) => {
  for(let i = 0; i < array.length; i++){
    buildingUp = howToCombine(buildinUp, array[i]);
  }
  return buildinUp;
}

const add = (a, b) => a + b;

const summed = reduce([1, 2, 3], add, 0);
```

![image](https://github.com/saidali-ibn-zafar/Hard-Parts-of-Functional-JS-Fundamentals/assets/120341849/8f4c22d8-9d0d-4021-9a8a-dce8609a9480)
