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
