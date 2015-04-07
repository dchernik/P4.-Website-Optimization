## Website Performance Optimization portfolio project

### Part 1. Optimizing PageSpeed results.

Majority of optimization procedures for index.html was done using Grunt and
tasks described in Gruntfile.js. But first:
	- all CSS rules were in-lined and precise dimensions were added to images;
	- @font-face rules were added for web fonts;
	- async property was added to Google analytics script;
	- media type 'print' was added to print.css style sheet reference.

Then, using Grunt:
	- two images of appropriate sizes were created out of views/img/pizzeria.jpg,
	one for index.html, and one for views/pizza.html;
	- reference to pizzeria image in index.html was modified to point to the correct file;
	- all images were minified;
	- were created minified versions of all HTML, CSS and JavaScript files
	- links inside HTML documents were changed to point to minified assets (style sheets,
	site pages, scripts), except for Google analytics;
	- "un-uglified" assets were also included;
	- tests were ran to ensure above 90 PagesPeed scores for both mobile and Desktop
	strategies.


### Part 2. Optimizing pizza.html.

In views/js/main.js:
	-	got rid of all functions inside resizePizzas, and used switch to figure out new size
	of pizza;
	- reduced number of moving pizzas to 20;
	- took the calculation of bodyScroll outside of the loop;
	- each time updatePositions runs it creates phases array with 5 distinct values based on
	bodyScroll value, instead of calculating phase inside the for loop.
	- comments were added.


