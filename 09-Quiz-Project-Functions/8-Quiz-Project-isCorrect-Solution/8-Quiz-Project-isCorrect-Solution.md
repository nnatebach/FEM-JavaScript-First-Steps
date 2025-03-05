# 8. Quiz Project isCorrect Solution

Link: [https://frontendmasters.com/courses/javascript-first-steps/quiz-project-iscorrect-solution/](https://frontendmasters.com/courses/javascript-first-steps/quiz-project-iscorrect-solution/)

1. Requirement
    
    ```jsx
    // TODO 5: Declare an isCorrect function that compares a guess to the right answer
    // isCorrect(guess) should return true if the guess matches the fact's answer
    ```
    
2. Work
    
    This is the “fact” object we created before
    
    ```jsx
    const fact = {
        statement: "Arrays are like objects",
        answer: true,
        explanation: "Arrays are a kind of object with special properties"
    }
    ```
    
    The “isCorrect(guess)” function will return “true” if the guess matches the fact’s answer
    
    ```jsx
    function isCorrect(guess) {
    	return guess === fact.answer
    }
    ```
    
3. Test
    
    ![image.png](./image/image.png)