#  Calculator

Today I'm going to start the odin project calculator project. 
So it took a couple hours over 2 days but I made the calculator. I used a bit of chatgpt and followed a tutorial when I was stuck. Though to be honest I struggled to know what to do initially so I did use the tutorial video as a crutch to get started and once I started following it, it was hard to stop. 

I used query selectors to grab all the necessary elements from the HTML document. First, I used the querySelector method to select the element with the ID clear and assigned it to the clear variable. Similarly, I selected the element with the ID equals and assigned it to the equal variable. I also grabbed the element with the class decimal and assigned it to the decimal variable, which corresponds to the decimal button on the calculator.

Next, I used the querySelectorAll method to select all elements with the class number and assigned them to the numbers variable. These are the number buttons on the calculator. Similarly, I selected all elements with the class operator and assigned them to the operators variable, which represent the operator buttons.

To display the previous and current values on the calculator screen, I selected the elements with the classes previous and current and assigned them to the previousScreen and currentScreen variables respectively.

Once I had all the necessary elements, I added event listeners to the number buttons using a forEach loop. For each number button, when clicked, I called the handleNumber function and passed the clicked button's text content as an argument. I also updated the text content of the current screen to display the current value.

Similarly, I added event listeners to the operator buttons. When an operator button is clicked, I called the handleOperator function, passing the clicked button's text content as an argument. I also updated the text content of the previous screen to display the previous value and the operator.

I also added an event listener to the clear button. When clicked, I reset the previous value, current value, and operator variables to empty strings. I updated the text content of the previous and current screens to display the empty values.

Similarly, I added an event listener to the equal button. When clicked, I checked if both the current value and previous value are not empty. If they are not empty, I called the calculate function to perform the calculation. I updated the previous screen's text content to an empty string and checked the length of the previous value. If the length is less than or equal to 5, I updated the current screen's text content to display the full previous value. Otherwise, I truncated the previous value to 5 characters followed by an ellipsis (...).

Lastly, I added an event listener to the decimal button. When clicked, I called the addDecimal function to add a decimal point to the current value if it doesn't already contain one.

Overall, this code sets up event listeners for the calculator buttons and handles the logic for updating the screens and performing calculations based on user input.