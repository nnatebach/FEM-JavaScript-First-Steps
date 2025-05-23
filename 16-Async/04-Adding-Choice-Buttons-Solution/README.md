# 4. Adding Choice Buttons Solution

URL: [https://frontendmasters.com/courses/javascript-first-steps/adding-choice-buttons-solution/](https://frontendmasters.com/courses/javascript-first-steps/adding-choice-buttons-solution/)

- The array of choices is called by different parameter names
    - In the function **renderButtons**, it is called by the name *choicesArray*
        
        ```jsx
        // Function to add the multiple-choice buttons to the page
        function renderButtons(choicesArray, correctAnswer) {
        
          // Event handler function to compare the clicked button's value to correctAnswer
          // and add "correct"/"incorrect" classes to the buttons as appropriate
          function buttonHandler(e) {
            if (e.target.value === correctAnswer) {
              e.target.classList.add("correct");
            } else {
              e.target.classList.add("incorrect");
              document.querySelector(`button[value="${correctAnswer}"]`).classList.add("correct");
            }
          }
        
          const options = document.getElementById("options"); // Container for the multiple-choice buttons
        
          // TODO 4
          // For each of the choices in choicesArray,
          // Create a button element whose name, value, and textContent properties are the value of that choice,
          // attach a "click" event listener with the buttonHandler function,
          // and append the button as a child of the options element
          
        
        }
        ```
        
    - In the **renderQuiz** function, it is called by the name *choices*
        
        ```jsx
        // Function to add the quiz content to the page
        function renderQuiz(imgUrl, correctAnswer, choices) {
          const image = document.createElement("img");
          image.setAttribute("src", imgUrl);
          const frame = document.getElementById("image-frame");
        
          image.addEventListener("load", () => {
            // Wait until the image has finished loading before trying to add elements to the page
            frame.replaceChildren(image);
            renderButtons(choices, correctAnswer);
          })
        
        }
        ```
        
    
    They are just parameter names which can be almost anything, but they should be meaningful names.
    
- TODO 4
    
    ```jsx
    // TODO 4
    // For each of the choices in choicesArray,
    for (let choice of choicesArray) {
    	// Create a button element whose name, value, and textContent properties are the value of that choice,
    	const button = document.createElement("button")
    	button.textContent = choice
    	button.value = choice
    	button.name = choice
    	// attach a "click" event listener with the *buttonHandler* function,
    	button.addEventListener("click", buttonHandler)
    	// and append the button as a child of the options element
    	options.appendChild(button)
    }
    ```
    
    Notes:
    
    - The *value* in `button.value = choice`  is important
        
        *value* is often used in *event handlers* like when we do `e.target.value` 
        
        Example: **buttonHandler** function
        
        ```jsx
        if (e.target.value === correctAnswer) {
          e.target.classList.add("correct");
        } else {
          e.target.classList.add("incorrect");
          document.querySelector(`button[value="${correctAnswer}"]`).classList.add("correct");
        }
        ```
        
    - Setting the *name* `button.name = choice`, which is best practice
    - attach a "click" event listener with the *buttonHandler* function
        
        ```jsx
        button.addEventListener("click", buttonHandler)
        ```
        
        We want the function *buttonHandler* to be passed in as the *callback* for *addEventListener* method. We’re not calling the function and return its value so there is no need for the parentheses “()”.
        
    - append the button as a child of the options element
        
        “options” is a “container” for the multiple-choice buttons 
        
        ```jsx
        const options = document.getElementById("options"); // Container for the multiple-choice buttons
        ```
        
        append the button as a child - [**appendChild()](https://developer.mozilla.org/en-US/docs/Web/API/Node/appendChild)** method of the [`Node`](https://developer.mozilla.org/en-US/docs/Web/API/Node) interface adds a node *to the end* of the list of children of a specified parent node
        
        ```jsx
        options.appendChild(button)
        ```
        
        appendChild() in HTML element is similar to push() in array, they both add something, the differences are in scope and usage.
        
    - You can't access stuff like *options* here for multiple reasons.
        - One, it's inside of a function, so that means it's local to the function scope.
        - Two, we said we can't really pull out the values in this, which is because it is a module.