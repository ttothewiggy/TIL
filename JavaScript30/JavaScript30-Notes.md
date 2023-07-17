# Notes

## Day 1

Today I started the JavaScript 30 day challenge. 
First off is the Drum Kit challenge which has proven really fun. 
I cloned the repo from github containing all the starter code for the challenges and created my own separate repo to push my own work to. I'm just copying and pasting the relevant code accross and removing the temptation of looking at the final code supplied in git repo supplied. 
I'm using the videos online by Wes Bos, the author of this curriculum thing. This first video I'm just coding along but the next challenge I'm planning on trying to figure out more on my own without following the video and then refering to the content if/when I need it. 
Finished the project with ease, following Wes Bos's first video. So it was less a case of being able to code the drum kit and more a case of whether I could follow instructions and emulate his code. 

## Day 2

Day 2 we have the CSS and JS Clock.
It was a fun one, didn't take too long and the video structure this time had a bit more do it yourself. Though he showed how to do the second hand on the clock, the hour and minute hands were up encourgaed to be done on your own. Which defintely helped it sink in. 
We used const to great a variable out of the div that created the clock arms. Then in the function we made variables of the seconds, minutes, hours and made variables of those figures that converted them to degrees. Then we used the degrees variable to transform the style of the css of each hand to rotate the hand as the seconds/minutes/hours changed. 
Then using the set interval function for every second, we also called this fcuntion every second where it updates. 

## Day 3

CSS Variables
I'ce used variables in CSS before but not really understood the foundations or the scope of them. They're quite simple really, but this exercise helped to gain a much better understanding of them. 

So for this exercise I started with the html page template which had 2 range input sliders and a colour pallet control option. 
I added a root variable in css with a few variables for spacing, blur and filter. 
From there I selected all the input controls in a const variable and created a function to handle the users updates to the controls. 

I also made a variable to add the "px" suffix to the end of the values. 
Then made a set property function that changes the root variable in css to the value of the controls the user is changing. 
Also made 2 event listeners that use the function above when there's a change to the controls and they listen for mousemove as well. 
And that's pretty much it. Fun and simple exercise that was. 

JavaScript Arrays

Javascript fundamentals, Array Methods. 
Filter, map, sort, reduce etc. 

Map = Always returns same amount of items you've given it. Returns them transformed but without affecting the original array. 

.filter: Creates a new array containing only the elements that pass a specified condition based on a provided filtering function.

.map: Creates a new array by applying a transformation function to each element of the original array, resulting in a new array of the same length.

.sort: Sorts the elements of an array in place, either using the default lexicographic (alphabetical) order or a custom sorting function.

.reduce: Applies a reduction function to each element of an array, accumulating a single value by iteratively combining the elements from left to right.

```
console.table(variable) 
```
Is a great way to display array data in a table in the console. 

# Day 4

Flexbox + JavaScript Image Gallery

This one was fun. Building in transitions that when the click event happened it transformed the panel. 
I can see one day that you build up your personal portfolio full of menus, transitions etc that you can use to just quickly implement a website or function from. So you just copy and paste your previous creations and make them work on the new project you're working on. 


# Day 5

