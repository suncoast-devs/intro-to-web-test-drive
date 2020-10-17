# Intro to CSS Layouts

In this lecture, the students will grow their knowledge of css by adding media queries and building a responsive website.

## Learning Objectives

- understand CSS can be used to tailor your site for smaller or larger screens
- understand how to apply media queries and responsive css to a site
- create a mobile first design
- create a responsive design
- use media queries to build a responsive, mobile first design

## Recommended Previous Knowledge

- HTML
- Basic styling CSS

## Slides

https://slides.com/lizthrilla/test-drive-mobile-first


## Lecture notes

- Mobile First Design
    - creates a focused user experience
    - mobile friendly webpages
    - better desktop webpages
- [UI vs UX](https://careerfoundry.com/en/blog/ux-design/the-difference-between-ux-and-ui-design-a-laymans-guide/)
    - The main difference to bear in mind is this: UX design is all about the overall feel of the experience, while UI design is all about how the product's interfaces look and function. A UX designer considers the user's entire journey to solve a particular problem; what steps do they take? 
- discuss differences between a [mock](https://handbook.suncoast.io/lessons/css-responsive/workflow#example) for a mobile UI and a desktop UI.
- Media queries
    - 
    ```css        
        /* on small screens */
        h1 {
            border: 1px solid green;
        }
        
        /* on big screens*/
        @media (min-width:600px) {
            h1 {
                border: 1px solid pink;
            }
        }
    ```
    
    - 
    ```css
        	
        main{
            display: flex;
            justify-content: center;
            flex-direction: column;
        }
        
        /* on big screens use the CSS here*/ 
        @media (min-width:800px) {
            main {
            justify-content: space-around;
            flex-direction: row;
            }
        }
    ```


## Possible Assignments

- add media queries to our website

## Additional Resources

- [Intro to Responsive Web](https://handbook.suncoast.io/lessons/css-responsive)
- [Media Queries Details](https://handbook.suncoast.io/lessons/css-responsive/media-query-details)

## Next Lectures

- Media Queries
- Intro to JavaScript
