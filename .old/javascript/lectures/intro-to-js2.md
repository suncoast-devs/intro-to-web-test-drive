# Javascript Part Deux

Mark's video: https://www.youtube.com/watch?v=Z-Q_c2wg2w8&t=2651s&list=PLWwthP6_aKmdxLKyXwDh0XXEgsWarTEpI&index=7

## Variables

Variables in programming languages allow us to store information and give that information a name so we can recall it later.

- [let](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let) & [const](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const)
- [array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)
  (approx 00:35:20)

  - ordered list of collection of data
  - index starts at `0`
  - values are separated by commas
  - different types of values can be mixed in an array
  - use `push` to add a value to an array
  - use `pop` to remove the last index of an array
  - use `shift` to remove the first index of an array
  - use `unshift` to insert a value at the beginning of an array

  ```javascript
  let instructors = ["Jason", "Toni", "Gavin", "Mark"];
  instructors.push("Joebob");
  instructors[("Jason", "Toni", "Gavin", "Mark", "Joebob")];

  instructors.pop();
  instructors[("Jason", "Toni", "Gavin", "Mark")];

  instructors.shift();
  instructors[("Toni", "Gavin", "Mark")];
  ```

## "types"

- numbers

  - basic math

- strings

  - use either single or double quote: `'string of characters'` or `"string of characters"`
  - concat: strings and numbers can be concatenated together in JS
    ```javascript
    let name = "Gavin"
    let favoriteNumber = 42
    let sentence = name + ' favorite number is ' + favoriteNumber
    sentence
    -> "Gavin favorite number is 42"
    ```
  - use escape character - backslash `\\` to use a single quote inside of singe quotes `''` or use double quotes

    ```javascript
    let sentence = name + '\'s favorite number is ' + favoriteNumber
    newSentence
    -> "Gavin's favoriteNumber is 42"
    ```

    or

    ```javascript
    let sentence = name + "'s favorite number is " + favoriteNumber
    newSentence
    -> "Gavin's favoriteNumber is 42"
    ```

- interpolation

  - use of backquote ` `` `: What is inside of `${}` within backquote gets evaluated

    ```javascript
    let newSentence = `${name} favoriteNumber is ${favoriteNumber}`
    newSentence
    -> "Gavin favoriteNumber is 42"
    ```

    ```javascript
    let newSentence = `${name} favoriteNumber is ${favoriteNumber * 2} or ${favoriteNumber * 3}`
    newSentence
    -> "Gavin favoriteNumber is 84 or 14"
    ```
```

## functions

(approx 1:00:00)

- data + behavior(actions taken on data) = programming
- functions are just variables whose value is the code to execute when you call that function
- named

  ```javascript
  function greet(nameOfPerson) {
    console.log('Hello ${nameOfPerson}')
  }

  greet()
  -> Hello undefined

  greet('Gavin')
  -> Hello Gavin

  name = 'Gavin'
  greet(name)
  -> Hello Gavin

  name = 'Gavin'
  greet(name + !!!!)
  -> Hello Gavin!!!!

  function greet(nameOfPerson, greeting) {
    console.log(`${greeting}, ${nameOfPerson}`)
  }
  greetFunction('Gavin', 'Howdy')
  -> Howdy, Gavin
  ```

  Another way to write function using `arrow function` (newer way in ES6)

  ```javascript
  let greetFunction = (nameOfPerson, greeting) => {
    console.log(`${greeting}, ${nameOfPerson}`)
  }

  greetFunction('Gavin', 'Howdy')
  -> Howdy, Gavin
  ```

- anonymous
  - functions that are dynamically declared at runtime. They're called anonymous functions because they aren't given a name in the same way as normal functions