# Arrays and Loops

- Slides: [https://slides.com/lizthrilla/arrays-and-loops#/](https://slides.com/lizthrilla/arrays-and-loops#/)
- In Class Example: [https://glitch.com/~class-example-0425](https://glitch.com/~class-example-0425)

## Add html elements to using JavaScript

```javascript
   const mySection = document.createElement("section");
   mySection.textContent = 'Hello, World'
   document.querySelector(".container").appendChild(mySection)
```

## Loops

- Loops allow us to do the same task repeatedly a controlled amount of times.
- use cases: 
    - I want to count from 1 to 100 and print out all the even numbers

    - While my hand of playing cards totals less than 21, draw a card

    - disable all the buttons on the page

    - until I run out of meatballs, keep making meatball subs


### For Loops

#### Definition: 
```javascript
for (COUNTER; TILL WHEN; CHANGE COUNTER){

}

// print out the numbers 0-9
for( let i = 0; i <= 9; i++) {
    console.log(i)
}
```

#### Example:

```javascript
// Count the numbers 1-100, 
// if the number is /5 then put in the DOM

for(let i = 1; i <= 100; i++){
    if (i % 5 == 0){
        const newSpan = document.createElement("span");
        newSpan.textContent = i
        document.querySelector(".list").appendChild(newSpan)
    }
}
```

### While Loops

#### Definition:

```javascript
while (some_truthy_expression){
    // do something
}
```

#### Example:

```javascript
let isNightTime = lookOutsideForSun()

while (isNightTime){
    // do something
    sleep(oneHour)
    isNightTime = lookOutsideForSun()
}
```

## Arrays

- a new type (like strings, numbers, functions and booleans)
- Arrays are a data structure that allows us to store things in a list-like manner 

### example:

```javascript
const lions = ["Simba", "Nala", "Scar", "Mufasa"]

console.log(lions[2]) // what will this print out?
```
- `[2]` identifies the index of an element within the array.  
- index means it's placement in the array (is it first? second? third? etc)
- arrays begin on 0 instead of 1 so `lions[2]` will return `Scar` because Simnba is `[0]` and Nala is `[1]`

### Using Arrays

- you can add, update and delete items from an array
- To add something to the end of an array you will "push" it with `Array.push(newItem)` 
- To add an item to a specific index via assignment `Array[2] = newItem`
- To delete an item you need to use `Array.splice(index, numberOfItems)` 
    - index is the index of the item you wish to remove
    - numberOfItems is a how many items you want to remove.  If just one, it'll be 1, if more then it'll be a higher number.

#### Example

```javascript
const myFavoriteThings = []

// add
myFavoriteThings.push('Raindrops on roses')

myFavoriteThings.push('whiskers on kittens')

// add and update
myFavoriteThings[5] = 'Bright copper kettles'

// delete

myFavoriteThings.splice(5,1);

```

## Putting it together

```javascript
const disneyVillains = ["Jafar", "Scar","Hades", "The Shadow Man"]

for (let i= 0; i < disneyVillains.length; i++){
    const listItem = document.createElement('li')
    listItem.textContent = disneyVillains[i];
    document.querySelector('.villains').appendChild(listItem)  
}
```

## Bonus: arrays, loops and if statements together!

```javascript
const disneyVillains = ["Jafar", "Scar","Hades", "The Shadow Man"]

for (let i= 0; i < disneyVillains.length; i++){
    const currentVillain = disneyVillains[i];
    const listItem = document.createElement('li')
   
    if (currentVillain === "Hades"){
         listItem.classList.add("under-appreciated-villain") 
    }
    listItem.textContent = currentVillain;
    document.querySelector('.villains').appendChild(listItem)  
}
```

## Additional resources

- [MDN Docs Array.push()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/push)
- [MDN Docs on other array methods -- check the left side navigation!](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)
- [MDN Docs on strings methods -- you can play with strings like you do arrays](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)
- [In class example](https://glitch.com/~sdg-0502)
- ["Starter" for the in class example](https://glitch.com/~quarantine-fun-jar-starter)*
    * a starter is a project you can use as a base to then personalize.  This one provides the html and `TODOs` to help you create your own fun jar project.  If you click view source and then "edit to remix" it will create a copy for you within glitch.