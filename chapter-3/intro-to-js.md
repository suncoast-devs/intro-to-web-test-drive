# Introduction to JS

Slides: https://slides.com/lizthrilla/intro-to-js

Mark's video: https://www.youtube.com/watch?v=Z-Q_c2wg2w8&t=2651s&list=PLWwthP6_aKmdxLKyXwDh0XXEgsWarTEpI&index=7

## [What is JS](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/What_is_JavaScript)

- Designed by [Brendan Eich](https://en.wikipedia.org/wiki/Brendan_Eich)

> JavaScript is a scripting or programming language that allows you to implement complex things on web pages — every time a web page does more than just sit there and display static information for you to look at — displaying timely content updates, interactive maps, animated 2D/3D graphics, scrolling video jukeboxes, etc. — you can bet that JavaScript is probably involved. It is the third layer of the layer cake of standard web technologies, two of which (HTML and CSS) we have covered ([MDN](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/What_is_JavaScript))

## How does this compare to what we know

- There are 3 ways to run JS
  - Browser based JS: Loaded into a browser (Primarily what we are referring to)
  - Backend JS: JS that runs on Backend such as Node
  - JS that runs on the computer such as code that is powering app-app

## How to run JS in Browser

- HTML script tag

```html
<script>
  // JavaScript code would be here
</script>
```

- Link to separate JavaScript file

```html
  <script src="main.js">
```

## Basic JS topics

- Google Chrome Tool -- `inspect`
  - console tab: You can type live JS code into a browser and the browser executes the code
  - source tab: Shows you the JavaScript files loaded into the current page

## Console

The JavaScript console is where we can output messages to ourselves (the developer) that are helpful in many ways:

- Outputs values (the result of some computation)
- Outputs messages that let us know when some action has happened in our application
- Outputs errors that are important to us as a developer but not useful to the user

- `console.log`

  ```javascript
  console.log('Hello World')
  ```

## What is the DOM (Document Object Model)

(approx 00:45:00)

- DOM: Browser's representation of your webpage in memory
- document - variable that is given by web page browser's JavaScript environment
- selectors

  - We can use the selectors we learned about with CSS to help us find/target elements on the page
  - querying selectors
  - `querySelector` > `querySelector` selects the very first `h1` element from document and returns it

        ```javascript
        document.querySelector('hi')
        -> <h1>Hello World</h1>
        ```

        ```javascript
        let header = document.querySelector('h1')
        header
        -> <h1>Hello World</h1>
        ```

  - `querySelectorAll` > given that there are 3 `h1` elements in the example document, to select all the `h1` elements from document

        ```javascript
        let allOurFirstDOM = document.querySelectorAll('h1')
        allOurFirstDOM
        -> NodeList(3) [h1,h1,h1]
        ```

  - [`NodeList`](https://developer.mozilla.org/en-US/docs/Web/API/NodeList) is an array like list that browser gives us to represent collection of nodes.

- Why do we normally put our `<script>` tag at the end of our HTML?

  - scripts run right away so only the DOM that has been evaluated so far is available to us
  - So how do we ensure that the DOM is loaded when our JavaScript runs?
  - Use `DOMContentLoaded` event (see below in `Events`)

- Updating (approx 00:53:00)

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

## Events

(approx 1:10:40)

- JS and DOM are event based world where we are waiting for events to happen and we react to them
- [what is an event](https://developer.mozilla.org/en-US/docs/web/events)
- In JS we can pass around functions to other functions
- listening for events
- attaching code to events

```javascript
const main = () => {
  document.querySelector('h1').textContent += '?'
}

// when DOMContentLoaded happens, call main
document.addEventListener('DOMContentLoaded', main)
```

## DEMO: a simple "how many times have your clicked this button"

(approx 1:35:00)

## Additional resources

[w3schools](https://www.w3schools.com/js/js_intro.asp)
[MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/A_re-introduction_to_JavaScript)
[Girl Develop It - Intro to Javascript](https://www.girldevelopit.com/materials/intro-js)
