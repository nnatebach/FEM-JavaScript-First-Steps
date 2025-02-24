# 7. Statements vs Expressions

Link: [https://frontendmasters.com/courses/javascript-first-steps/statements-vs-expressions/](https://frontendmasters.com/courses/javascript-first-steps/statements-vs-expressions/)

1. An *expression* “asks” JS for a value
    
    “Hey, what is this value?”
    
    ```jsx
    myAssignedVariable // "What is the current value of myAssignedVariable?"
    6 + 4 // "What is 6 + 4?"
    document.getElementById("board") // "What is this element with a certain ID?"
    ```
    
2. A *statement* “tells” JS to do something
    
    ```jsx
    let ten = 6 + 4; // "Assign the evaluated value of 6 + 4 to the variable 'ten'"
    myDeclaredVariable = "new value"; // Assigning a variable to a new value
    let board = document.getElementById("board");
    ```
    
    Declaring a variable is a statement: For example `let ten`
    
    The “semi-colon” at the end of each statement is a “punctuation” to say that you’re done telling JS what to do for now.
    

1. The distinction between Statement and Expression
    
    ```jsx
    function add(x, y) {
        return x + y;
    }
    let biggest;
    if (5 > 4) {
        biggest = 5;
    } else {
        biggest = 4;
    }
    for (let character of "string") {
        console.log(character);
    }
    ```
    
    - *Expressions* are equivalent to *values*
    - *Statements* are like *actions* we want JS to take to do stuff
    
    In a JS program, within the chunks of code, sometimes we are going to need
    
    - A *statement*, which is a *command* for JS to do something
    - An *expression*, a long way to ask JS for a particular *value*
    - *Statements* and *expressions* are **not** **always interchangeable**