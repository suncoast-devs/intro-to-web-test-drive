# If/Else

- Slides: [https://slides.com/lizthrilla/if-else](https://slides.com/lizthrilla/if-else)
- In Class Example: [https://glitch.com/~class-example-0425](https://glitch.com/~class-example-0425)

## Review

- Types

  - `const count = 5` // Number
  - `const dayOfWeek = "Tuesday"` // String
  - ```javascript
    const updateButtonEvent = () => {
      console.log("button clicked");
    }; // function
    ```

- Functions can be used not only to hold logic, but also can be use to calculate and return a new value

```javascript
const getRandomNumber = () => {
  return Math.ceil(Math.random() * 6);
};

const rollDice = () => {
  const randomNumber = getRandomNumber();
  document.querySelector(".result").textContent = randomNumber;
};

document.querySelector(".d6").addEventListener("click", rollDice);
```

## Booleans

- true/false
  - const needCoffee = true
  - const hungry = false
- allows our programs to make decisions

- comparing:

```javascript
const numberOfRedCrayons = 10;

const numberOfBlueCrayons = 7;

numberOfRedCrayons > numberOfBlueCrayons; // true

numberOfRedCrayons >= numberOfBlueCrayons; // true

numberOfRedCrayons < numberOfBlueCrayons; // false

numberOfRedCrayons <= numberOfBlueCrayons; // false
```

- equality:

```javascript
const scoreString = "10";

const currentScore = 10;

const target = 15;

currentScore == target; // false

currentScore === target; // false

currentScore == scoreString; // true

currentScore === scoreString; //false
```

## If/Else Statements

### "if" statements allow our programs to make basic decisions based on a yes or no value

```javascript
const animal = selectAnimal();
let habitat = "the city";

if (animal === "fox") {
  habitat = "the farm";
}
```

### Else Statements

- adds complexity to our if statements and allows us to declare what will happen if the "if" is false

```javascript
const animal = selectAnimal();
let habitat = "the city";

if (animal === "fox") {
  habitat = "the farm";
} else {
  habitat = "woods";
}
```

### Else If Statements

- like an "or" option.
- If the "if" is false but you want to add more logic.

```javascript
const animal = selectAnimal();
let habitat = "the city";

if (animal === "fox") {
  habitat = "the farm";
} else if (animal === "moose") {
  habitat = "tundra";
} else {
  habitat = "woods";
}
```

#### If, else if and else can stack

```javascript
const animal = selectAnimal();
let habitat = "the city";

if (animal === "fox") {
  habitat = "the farm";
} else if (animal === "moose") {
  habitat = "tundra";
} else if (animal === "otter") {
  habitat = "river";
} else if (animal === "sea tutle") {
  habitat = "sea";
} else {
  habitat = "woods";
}
```

## Boolean Logic

- && = both options must be true for the statement to be true
- || = only one option needs to be true for the statement to be true
- ! = means it must be the opposit or "not" the statement

```javascript
const niceOutside = sunny && notTooHot; // True & True = true

const shouldIwatchAMovie = GoodMovie || Raining; // True & False = False

const isNight = !isDay; // night is not day
```

## Putting it all together

- boolean logic
- if statement
- else if statement
- else statement

```javascript
const ringsToDestroy = getNumberOfRingsToDestroy();

const ringBearer = getCurrentRingBearer();

if (ringsToDestroy > 0 && ringBearer === "Frodo") {
  keepWalking();
} else if (ringsToDestroy === 0) {
  relaxInTheShire();
} else if (ringBearer !== "Frodo") {
  findTheRing();
}
```

## Truthy/falsy

- In JavaScript, a truthy value is a value that is considered true when encountered in a Boolean context. All values are truthy unless they are defined as falsy (i.e., except for false, 0, -0, 0n, "", null, undefined, and NaN).

- truthy:

    - non-zero number
    - any string
    - anything that is not falsy

- falsy:
    - false
    - 0
    - undefined
    - null
    - NaN
    - ''
    - ""

- [More info on MDN](https://developer.mozilla.org/en-US/docs/Glossary/Truthy)

## Additional resources

- [w3schools](https://www.w3schools.com/js/js_intro.asp)
- [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/A_re-introduction_to_JavaScript)
- [Girl Develop It - Intro to Javascript](https://www.girldevelopit.com/materials/intro-js)
