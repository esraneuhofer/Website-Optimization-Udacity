# Website_Optimization

######Project Overview

Project #8
"You will optimize a provided website with a number of optimization- and performance-related issues so that it achieves a target PageSpeed score and runs at 60 frames per second."

## Task 1 PageSpeed Score
####index.html achieves a PageSpeed score of at least 90 for Mobile and Desktop.

######Minified css/html and js files
######Minified the images
######inlined CSS(although I prefer to keep it in an external file)
######Added "async" to js files since the where not critical
######Added media="print" to print.css file

## Task 2 Getting Rid of Jank
####1.Optimizations made to views/js/main.js make views/pizza.html render with a consistent frame-rate at 60fps when scrolling.
####2.Time to resize pizzas is less than 5 ms using the pizza size slider on the views/pizza.html page. Resize time is shown in the
browser developer tools.

######I did not inline the css file since I find the loss of preformance excaptable and rather keep a clean ordered filestructure. 
######Minified css/html and js files
######Minified the images
######The changes in the main.js file where rather little but enough to get the required fram-rates.I change the for Loop in updatePositions() and changePizzaSizes().
######In updatePosition() ijust placed "var mathSin= Math.sin(document.body.scrollTop / 1250)" outside of the looop. 
######In changePizzaSizes() "document.querySelectorAll(".randomPizzaContainer")[i].offsetWidth" gave a consistend number for each change. Therefor I took both varibales var dx and var newwidth out of the loop with a fixed number in this case 10.



**1.** Clone this repo:

```
$ git clone https://github.com/esraneuhofer/Website_Optimization.git
````

**2.** Serve the application:

```
$ run index.html in your browser
```

###Resources

#####"http://www.willpeavy.com/minifier/"
#####"optimizilla.com/"
#####"https://developers.google.com/speed/pagespeed/insights/?hl=de"
