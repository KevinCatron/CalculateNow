# CalculateNow
An online calculator that can calculate basic functions.

# Technology Used

* HTML
* CSS
* JavaScript

# Into The Code

The way CalculateNow is coded is a little different than most online calculators. I believe it;s a more easy and simple way to understand and write. The meat of the calculate function is here:
````
for (var i = 0; i < buttons.length; i++) {
        if (buttons[i].innerHTML === '=') {
            buttons[i].addEventListener("click", calculate(i));
        } else {
            buttons[i].addEventListener("click", addValue(i));
        }
    }
````

As you can see we use JavaScript to loop through all the buttons(keys) Once the loop runs into the "=" character it will calculate once clicked, when the loop doesn't land on the "=" sign. It will add the value of whatever is ran.

`````
    function addValue(i) {
//This will display the correct operator for the assigned text. 
        return function() {
            if (buttons[i].innerHTML === '/') {
                result.innerHTML += '/';
            } else if (buttons[i].innerHTML === 'x') {
                result.innerHTML += '*';
            } else {
                result.innerHTML += buttons[i].innerHTML;
            }
        };
    }
`````

This block of code above us is the addValue function which we obtained in the first chunk of code. This function sets the operators equal to the charactors on the calculator. Once everything is selected the equation is ran with:

`````
result.innerHTML += buttons[i].innerHTML;
`````

# Make Me Pretty

I wanted to go for a simple clean and a hint of interaction in the design process. When the buttons are clicked just a simle offset of the buttons is visable making the user feel as they have actually pressed a button. I have seen alot of calculators online that use the two input/result screen method which I don't really like since almsot no calculators use that in real life. 

# Problems? We All Got Problems?

I'm not sure why but when I set the code so the inner.HTML = `````&divide;````` It does not work to equal "/". I have not found a solution to that other than just setting the inner.HTML "/" = "/"


