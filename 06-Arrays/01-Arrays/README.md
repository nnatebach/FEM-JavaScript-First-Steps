# 1. Arrays

Link: [https://frontendmasters.com/courses/javascript-first-steps/arrays/](https://frontendmasters.com/courses/javascript-first-steps/arrays/)

```jsx
let synonyms = ["plethora", "array", "cornucopia"];
```

1. Like strings, arrays have a length
    
    ```jsx
    synonyms.length // 
    ```
    
2. Each value has an index
    
    ```jsx
    synonyms[1]
    synonyms.indexOf("cornucopia")
    ```
    
3. Also like strings, we can check if an array contains a certain value
    
    ```jsx
    synonyms.includes("plethora")
    synonyms.includes("variety")
    ```
    
4. Unlike strings, we can modify arrays
    
    ```jsx
    synonyms[1] = "variety";
    let lastItem = synonyms.pop();
    synonyms.push("multitude");
    ```
    
    - `synonyms[1] = "variety";`
        
        ![image.png](1%20Arrays%2017f3ca73cd2080c0a594fa1abd3451c4/image.png)
        
    - `let lastItem = synonyms.pop();`
        
        ![image.png](1%20Arrays%2017f3ca73cd2080c0a594fa1abd3451c4/image%201.png)
        
        What happened to the “synonyms” array after “pop()”?
        
        ![image.png](1%20Arrays%2017f3ca73cd2080c0a594fa1abd3451c4/image%202.png)
        
    - `synonyms.push("multitude");`
        
        ![image.png](1%20Arrays%2017f3ca73cd2080c0a594fa1abd3451c4/image%203.png)