# Intro to CSS

This is the basic intro to CSS. This lecture is what will review HTML and introduce students to the basics of CSS.

## Learning Objectives

- What is CSS?
- What is an CSS file?
- How does CSS improve the development experience?
- What are some common CSS elements we like?

## Recommended Previous Knowledge

- Students should be able to open a file in a text editor.
- Students should have app-app installed

## Slides

- [https://slides.com/lizthrilla/test-drive-class1/](https://slides.com/lizthrilla/test-drive-css)

## Full Code Samples

- list of tags here: https://suncoast.io/handbook/curriculum/fundamentals/static-sites/lectures/elements-we-like

## Lecture notes

- Go over HTML notes
  - Semantic vs non-semantic
- Review the good and bad of inline styling
- What is CSS?
  - cascading style sheets
  - allows us to make a website look how we want it to
  - a way to apply styules to your website both globally and singularly
  - a set of rules
- CSS Rules
  - a set of properties which have values set to update how HTML content is displayed
  - selectors reference the HTML tags to apply styles specifically to them
- example:
  - ```css
    h1 {
      color: blue;
      background-color: yellow;
      border: 1px solid black;
    }

    p {
      color: red;
    }```
- Property and Value:
  - Property is the first part
    - ie background-color, height, font-weight, etc
  - value is what comes afer the colon
    -ie - blue, yellow, 1px solid black
  - there are over 300 different css properties to chose from. HAVE FUN WITH IT!
- Class selectors
  - Classes are selectors we use to apply more specific rule sets 
  - If you don't want to apply it to every `<p>` tag but to a select few you would add `class=yourClassName`
    - Classes are represented in CSS with a period in front: `.yourClassName`
- ID Selectors
  - IDs are even more specific selectors
  - If you want to apply to only one specific item in the document you would add `id="yourIdName"`
    - IDs are represented in CSS with a `#` in front: `#yourIdName`


## Possible Assignments

- Adding CSS to our website

## Additional Resources

- [SDG handbook on CSS](https://handbook.suncoast.io/lessons/css-intro)
- [list of properties here](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Properties_Reference)
- [Introduction to CSS](https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS)
- [Getting Started with CSS Rules](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/CSS_basics#Anatomy_of_a_CSS_ruleset)
- [All the CSS properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference#Keyword_index)
- [Evolution of the Web](http://www.evolutionoftheweb.com)
- [http://www.csszengarden.com/](http://www.csszengarden.com/)


## Tools

- [Color Hunt - Trendy Color Palettes](https://colorhunt.co/)
- [CSS Gradient - Apply background color gradients with this took](https://cssgradient.io/)
- [Page Ruler Redux - Chrome Extension](https://chrome.google.com/webstore/detail/page-ruler-redux/giejhjebcalaheckengmchjekofhhmal?hl=en)
- [ColorZilla - color picker Chrome Extension](https://chrome.google.com/webstore/detail/colorzilla/bhlhnicpbhignbdhedgjhgdocnmhomnp?hl=en)
- [Built in CSS Colors](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value)
- [Some nice Google Font Pairings](http://femmebot.github.io/google-type/)
- [Google Fonts](https://fonts.google.com/)

## Next Lectures

- Responsive CSS and Flexbox
