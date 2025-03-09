# 9. Boolean Q&A

Link: [https://frontendmasters.com/courses/javascript-first-steps/boolean-q-a/](https://frontendmasters.com/courses/javascript-first-steps/boolean-q-a/)

- Given the “fact” object from previous lesson
    
    ```jsx
    const fact = {
        statement: "Arrays are like objects",
        answer: true,
        explanation: "Arrays are a kind of object with special properties"
    }
    ```
    
- Given the function “isCorrect” from previous lesson
    
    ```jsx
    function isCorrect(guess) {
        return guess === fact.answer
    }
    ```
    
- Question: declare **isCorrect(guess)** function that compares a guess string to your fact's answer string.
    
    Reason for this question is that later on when we pull out the things that they are clicked on and its value, in HTML we are dealing with string all the times.
    
    For example, the value of the button is the string “true”
    
    ![image.png](9%20Boolean%20Q&A%2017f3ca73cd2080958ee0d475746f1143/image.png)
    
    Problem: A string will never equal a boolean
    
    ```jsx
    "true" === true // false
    "true" == true // false
    ```
    
    Solution: Convert anything in JS to a string with [toString()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/toString)
    
    ```jsx
    function isCorrect(guessString) {
    	return guessString === fact.answer.toString()
    }
    ```
    
    Demo:
    
    ```jsx
    isCorrect("true") // true
    isCorrect("false") // false
    ```