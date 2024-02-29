# What is `closure`?

- Closures in JavaScript are functions that have access to the parent scope, even after the parent function has closed. 

```js
const functionCreator = () => {
  let counter = 2;
  const add3 = (num) => {
    const result = num + 3;
    return result;
  }
  return add3;
}

const generateFunc = functionCreator();

const result = generatedFunc(2); // 5
```

- `const generateFunc = functionCreator();` - as you could see in this case generatedFunc is `add3` function, because functionCreator points into adds3,
- if we remove () from functionCreator then generatedFunc would be functionCreator function.

   
