# Example of using map
Use the Array.prototype.map to transform the names to all uppercase
> Expected result: ["MATHIAS", "KASPER"]
```js
const array = ["Mathias", "Kasper"];

const toUpperCased = array.map(name => {
  return name.toUpperCase()
})
```
Notice that the original "array" variable is unchanged, and that the .map method returns a new array.

## Exercise 1
Given the strings array use the Array.prototype.map to convert the strings to numbers.
> Expected result: [1, 2, 3, 4, 5]

```js
const strings = ["1", "2", "3", "4", "5"];
// TODO: 
const numbers = 
```

<details><summary>Solution</summary>
<p>
Using the unary operator:

```js
  const numbers = strings.map(x => +x);
```
</p>
</details>


## Exercise 2
Given the numbers array from previous exercise, use the Array.prototype.map method to square the numbers.
> Expected result = [1, 4, 9, 16, 25]

```js
// TODO: 
const squared = 
```

<details><summary>Solution</summary>
<p>

```js
const squared = numbers.map(x => x*x)
```
</p>
</details>


## Exercise 3:
Given the people array, use the Array.prototype.map method, to go through these people, 
calculate their BMI, and add the result as an attribute to the object

> BMI formula: weight / (height * height) 
>
> Weight given in kg's and height in meters.
>
> Expected result: [ {name: "Mathias", height: 1.80, weight: 95, bmi: 29.3}, {name: "Kasper", height: 1.78, weight: 85, bmi: 26.8} ]


```js
const people = [
  {name: "Mathias", height: 1.80, weight: 95},
  {name: "Kasper", height: 1.78, weight: 85}
]
// TODO:
const withBmi = 
```



<details><summary>Solution</summary>
<p> 

### With default object handling:

```js
const withBmi = people.map(person => {
  const bmi = person.weight / (person.height * person.height)
  const roundedBmi = Math.round(bmi * 10) / 10
  person.bmi = roundedBmi;
  return toReturn
})
```

### With the spread operator:
This is usefull in frameworks like React, when state is immutable

```js
const withBmi = people.map(person => {
  const bmi = person.weight / (person.height * person.height)
  const roundedBmi = Math.round(bmi * 10) / 10
  return {
    bmi: roundedBmi,
    ...person
  }
})
```
</p>
</details>


