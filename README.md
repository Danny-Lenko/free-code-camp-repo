# Standard README.md File

![Design preview for the Space tourism website coding challenge](./assets/preview.jpg)

## Welcome! 👋
## Table of contents

- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow
- CSS utility classes

## Basic JS

### Return Early Pattern for functions

```js
// Setup
function abTest(a, b) {
  // Only change code below this line
  if (a < 0 || b < 0) {
     return
  }
  // Only change code above this line
  return Math.round(Math.pow(Math.sqrt(a) + Math.sqrt(b), 2));
}
abTest(2,2);
```

### Replace loops using recursion
```js
function sum(arr, n) {
   // Only change code below this line
   if (n <= 0) {
      return 0;
   } else {
      return sum(arr, n - 1) + arr[n - 1];
   }
   // Only change code above this line
}

console.log(sum([2, 3, 4, 5], 3));
```
### Countdown resursion
```js
// Only change code below this line
function countdown(n){
   if (n <= 0) {
      return [];
   } else {
      let numArr = countdown(n - 1);
      numArr.unshift(n);
      return numArr;
   }
}
console.log(countdown(10));
// Only change code above this line
```
### Use recursion to create range of numbers
```js
function rangeOfNumbers(startNum, endNum) {
   if (endNum < startNum) {
      return [];
   } else {
      const numArr = rangeOfNumbers(startNum, endNum - 1);
      numArr.push(endNum);
      return numArr;
   }
};
```

## ES 6

### Prevent object mutation
```js
  function freezeObj() {
     const MATH_CONSTANTS = {
        PI: 3.14
     };
     // Only change code below this line
     Object.freeze(MATH_CONSTANTS);

     // Only change code above this line
     try {
        MATH_CONSTANTS.PI = 99;
     } catch(ex) {
        console.log(ex);
     }
     return MATH_CONSTANTS.PI;
  }
  const PI = freezeObj();
```

### Set Default Parameters for Your Functions
```js
  const increment = (number, value = 1) => number + value;
```

### Use the Rest Parameter with Function Parameters
```js
  const sum = (...args) => args.reduce((a, b) => a + b, 0);
  console.log(sum(3, 4, 1))
```

### Use Destructuring Assignment to Extract Values from Objects
```js
const HIGH_TEMPERATURES = {
  yesterday: 75,
  today: 77,
  tomorrow: 80
};
// Only change code below this line
// const today = HIGH_TEMPERATURES.today;
// const tomorrow = HIGH_TEMPERATURES.tomorrow;
const { today, tomorrow } = HIGH_TEMPERATURES;
// Only change code above this line
```

### Use Destructuring Assignment to Assign Variables from Objects
```js
   const HIGH_TEMPERATURES = {
      yesterday: 75,
      today: 77,
      tomorrow: 80
   };
   // Only change code below this line
   // const highToday = HIGH_TEMPERATURES.today;
   // const highTomorrow = HIGH_TEMPERATURES.tomorrow;
   const {today: highToday, tomorrow: highTomorrow} = HIGH_TEMPERATURES;
   // Only change code above this line
```

### Use Destructuring Assignment to Assign Variables from Nested Objects
```js
const LOCAL_FORECAST = {
  yesterday: { low: 61, high: 75 },
  today: { low: 64, high: 77 },
  tomorrow: { low: 68, high: 80 }
};
// Only change code below this line
// const lowToday = LOCAL_FORECAST.today.low;
// const highToday = LOCAL_FORECAST.today.high;
const { today: { low: lowToday, high: highToday }} = LOCAL_FORECAST;
// Only change code above this line
```

### Use Destructuring Assignment to Assign Variables from Arrays
```js
let a = 8, b = 6;
// Only change code below this line
[a, b] = [b, a];
```

### Use Destructuring Assignment with the Rest Parameter to Reassign Array Elements
```js
   const source = [1,2,3,4,5,6,7,8,9,10];
      function removeFirstTwo(list) {
         // Only change code below this line
         const [a, b, ...arr] = list;
         // Only change code above this line
         return arr;
      }
   const arr = removeFirstTwo(source);
```








### Continued development

* CSS grid;

*Use this section to outline areas that you want to continue focusing on in future projects. These could be concepts you're still not completely comfortable with or techniques you found useful that you want to refine and perfect.

### Useful resources

- [Array.prototype.reduce()](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce) - Helped me understand the reduce() method;

- [Git + GitHub](https://www.youtube.com/watch?v=RGOj5yH7evk) - the basic git commands (Youtube).
- [The Markdown Guide](https://www.markdownguide.org/) - for more help with writing markdown (Article).

## Author

- Github - [DannyLenk](https://github.com/DannyLenk)
- Frontend Mentor - [@DannyLenk](https://www.frontendmentor.io/profile/DannyLenk)
- Facebook - [Valerii Danylenko](https://www.facebook.com/valerii.danylenko)
- LinkedIn - [Valerii Danylenko](https://www.linkedin.com/in/valerii-danylenko-74379212b)
- insta - [valeriidanylenko](https://www.instagram.com/valeriidanylenko/?hl=ru)

## Acknowledgments

Thank you, Kevin Powell. Hats off to you and your clear English.
