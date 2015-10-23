
This is a portfolio webpage. The main page can be accessed via index.html.  All supporting subfolders are located within the same directory (css, img, js, as well as the html files found in the hyperlinks).  The pizza project is located in it's own subfolder (views) and the html file for that page is labeled pizza.html. The corresponding files for pizza.html can be located in the same director (css, images, js).  What follows is a list of updates made to improve performance of index.html and pizza.html.'

UPDATES:
In main.js, 'updated querySelectorAll()' to 'getElementByClass()' to reduce the amount of time necessary to traverse the DOM.
In updatePositions(), moved 'var phase' outside of the painting loop to stop the forced layout.
Changed all instances of 'queryselector()' to 'getElementsById()'.'
In 'changePizzaSlices()', Created local varialbes (container, dx, newwidth) to pull those variables out of the for loop so they the DOM doesn't need to be accessed through each iteration.
Moved 'var pizzasDiv' out of the for loop so it doesn't need to access the DOM with each iteration.
Created 'var screenHeight' to be used in 'var numPizzas'.  This dynamically calculates the number of pizzas needed based on display size.  In 'numPizzas', division by 135 was used to keep the number pizzas within a reasonable range for performance.
In 'addEventListener("DOMContentLoaded"...")', moved the the declaration of var elem outside of the for loop so it doesn't need to be created with every iteration.

In style.css, added vendor prefixes.  To .mover, added blackface-visibility: hidden and moved the moving pizzas (.mover) to their own layer via transform: translateZ(0).
