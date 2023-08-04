# Notes

## Day 1

### Drum Kit
Today I started the JavaScript 30 day challenge. 
First off is the Drum Kit challenge which has proven really fun. 
I cloned the repo from github containing all the starter code for the challenges and created my own separate repo to push my own work to. I'm just copying and pasting the relevant code accross and removing the temptation of looking at the final code supplied in git repo supplied. 
I'm using the videos online by Wes Bos, the author of this curriculum thing. This first video I'm just coding along but the next challenge I'm planning on trying to figure out more on my own without following the video and then refering to the content if/when I need it. 
Finished the project with ease, following Wes Bos's first video. So it was less a case of being able to code the drum kit and more a case of whether I could follow instructions and emulate his code. 

## Day 2

###  CSS and JS Clock.
It was a fun one, didn't take too long and the video structure this time had a bit more do it yourself. Though he showed how to do the second hand on the clock, the hour and minute hands were up encourgaed to be done on your own. Which defintely helped it sink in. 
We used const to great a variable out of the div that created the clock arms. Then in the function we made variables of the seconds, minutes, hours and made variables of those figures that converted them to degrees. Then we used the degrees variable to transform the style of the css of each hand to rotate the hand as the seconds/minutes/hours changed. 
Then using the set interval function for every second, we also called this fcuntion every second where it updates. 

## Day 3

### CSS Variables
I'ce used variables in CSS before but not really understood the foundations or the scope of them. They're quite simple really, but this exercise helped to gain a much better understanding of them. 

So for this exercise I started with the html page template which had 2 range input sliders and a colour pallet control option. 
I added a root variable in css with a few variables for spacing, blur and filter. 
From there I selected all the input controls in a const variable and created a function to handle the users updates to the controls. 

I also made a variable to add the "px" suffix to the end of the values. 
Then made a set property function that changes the root variable in css to the value of the controls the user is changing. 
Also made 2 event listeners that use the function above when there's a change to the controls and they listen for mousemove as well. 
And that's pretty much it. Fun and simple exercise that was. 

### JavaScript Arrays

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

# Day 4 + 5

### Flexbox + JavaScript Image Gallery

This one was fun. Building in transitions that when the click event happened it transformed the panel. 
I can see one day that you build up your personal portfolio full of menus, transitions etc that you can use to just quickly implement a website or function from. So you just copy and paste your previous creations and make them work on the new project you're working on. 


# Day 6

### Ajax Type Ahead with fetch() 
This was a fun one making a search box that would show all results that matched each letter as you typed it. Used RegExp for the first time. Will need to reiterate over this project a few times for it to sink in. 

# Day 7

### Array cardio
trying to do as much as I can before he explains and I'm getting closer each time.
.some(), .every(), .find() and [...SPREADS]

# Day 8

### HTML Canvas
Really fun challenge of making this canvas. Lots of nuanced things to think of so I pretty much just followed along with the video as it was far more cokmplicated than I anticipated. 

# Day 9 + 10

### Dev Tools
Fun little exercise going over all the different console.doSomething functions. 
```
console.log("Hello");: Outputs a simple log message.
console.log("Hello", ", I am a shit string!");: Outputs an interpolated log message with string concatenation.
console.log('%c I am some great text', 'font-size:50px; background:red; text-shadow: 10px 10px 0 blue');: Outputs a styled message using CSS styles.
console.warn("OH NOOOO");: Outputs a warning message with a yellow warning icon.
console.error("Shit");: Outputs an error message with a red error icon.
console.info("Hello");: Outputs an informational message with a blue "i" icon.
console.assert(p.classList.contains('ouch'), 'That is wrong');: Asserts that the condition is true. If it's false, it will output the error message provided.
console.clear();: Clears the console.
console.dir(p);: Outputs the properties of a DOM element in a collapsed tree format.
console.groupCollapsed('${dog.name}');: Groups console logs together in a collapsed group.
console.groupEnd('${dog.name}');: Ends the group of console logs.
console.count('Wes');: Counts the number of times "Wes" appears in the console.
console.time('fetching data');: Starts a timer with a given name.
console.timeEnd('fetching data');: Ends the timer with the given name and outputs the time taken.
console.table(dogs);: Outputs the array of objects in a tabular format.
```

### Hold Shift

This one was cool because I asked chat GPT and it provided the EXACT same code the Wes was about to go through. Which is crazy! So cool. 

# Day 11

### Custom Video Player

Created the variables by grabbing the premade divs etc wesbos made.
Assigned a function to each variable/button. 
Got the play button working and got it toggling the icons for play and pause. 
Got the volume slider and speed slider working, as well as progress bar. 
Got help from the video getting the progress bar to be grabbable so the user could choose where to playback the video. 
Skip buttons were quite easily configured.
CHatGPT helped with the grunt work and in a few areas where I got stuck. 

### Coded Keys

Created "Secret code" variable. 
Stored the keystokes in an array with event listener. 
Made sure the array doesnt grow larger than the keyword bt removing the elements from the beginning of the array using splice. 
Made loop looknig through array for secret code. 
If winner was found a function was run to change the webpage. 


