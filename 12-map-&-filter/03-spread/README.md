# 3. Spread

Link: [https://frontendmasters.com/courses/javascript-first-steps/spread/](https://frontendmasters.com/courses/javascript-first-steps/spread/)

[Spread (...)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax): 

- A trick for iterating over *arrays* in order to **put** all the **items from one array inside another array**.
- Modifies the array **in place**. The original array is changed.
    
    ![It lets us take all the items in an array and **spread** 'em around.](./image/image.png)
    
    It lets us take all the items in an array and **spread** 'em around.
    
- Examples
    - We can use it to put all the items from one array inside another array
        
        ```jsx
        const oldBurns = ["square", "wack"];
        const newBurns = ["basic", "dusty", "sus"];
        const burnBook = [...oldBurns, ...newBurns]; // (5) ['square', 'wack', 'basic', 'dusty', 'sus']
        ```
        
        equivalent to
        
        ```jsx
        const burnBook = oldBurns.concat(newBurns); // (5) ['square', 'wack', 'basic', 'dusty', 'sus']
        ```
        
    - We can also use it to **pass** all the **items** from an **array** as *arguments* to a **function** or method
        
        ```jsx
        const skills = ["HTML", "CSS", "JS"];
        const newSkills = ["React", "TypeScript", "Node"]
        skills.push(...newSkills); // 6
        console.log(...skills); // HTML CSS JS React TypeScript Node
        ```
        
        equivalent to
        
        ```jsx
        skills.push(newSkills[0], newSkills[1], newSkills[2]) // 6
        console.log(...skills); // HTML CSS JS React TypeScript Node
        ```
        
- Question:
    
    Given the array
    
    ```jsx
    const skills = ["HTML", "CSS", "JS"];
    ```
    
    What is the difference between `console.log(...skills);`  and `console.log(skills);` 
    
    - `console.log(skills);`
        
        Prints the entire array as single object
        
        ```jsx
        [ 'HTML', 'CSS', 'JavaScript' ]
        ```
        
    - `console.log(...skills);`
        
        It is equivalent to
        
        ```jsx
        console.log('HTML', 'CSS', 'JavaScript');
        ```
        
        **"Spreads" the array** and logs each item as separate arguments
        
        ```jsx
        HTML CSS JavaScript
        ```