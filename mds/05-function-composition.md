# What is Function Composition

- Function composition is a fundamental concept in functional programming where individual functions are combined together to create a new function. Instead of nesting function calls, function composition allows you to chain functions together, passing the output of one function as the input to another.

  ## Look here 
```js
const multiplyBy2 = x => x*2
const add3 = x => x+3
const divideBy5 = x => x/5
const initialResult = multiplyBy2(11)
const nextStep = add3(initialResult)
const finalStep = divideBy5(nextStep)
console.log("finalStep", finalStep)
```

## Look here
```js
const multiplyBy2 = x => x*2
const add3 = x => x+3
const divideBy5 = x => x/5
const result = divideBy5(add3(multiplyBy2(11)))
```

## Reduce as the most versatile function in programming
```js
const multiplyBy2 = x => x*2
const add3 = x => x+3
const divideBy5 = x => x/5
const reduce = (array, howToCombine, buildingUp) => {
 for (let i = 0; i < array.length; i++){
 buildingUp = howToCombine(buildingUp, array[i])
 }
 return buildingUp
}
const runFunctionOnInput = (input,fn) => {
 return fn(input)
}
const output = reduce([multiplyBy2, add3, divideBy5], runFunctionOnInput, 11)
```

# TO BE CONTINUED ...
