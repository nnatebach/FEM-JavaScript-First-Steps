# 4. indexOf

Link: [https://frontendmasters.com/courses/javascript-first-steps/indexof/](https://frontendmasters.com/courses/javascript-first-steps/indexof/)

1. indexOf
    
    ```jsx
    "ALOHA".indexOf("L") // 1
    "ALOHA".indexOf("A") // 0
    "ALOHA".indexOf("Q") // -1
    ```
    
    At what index does this substring begin?
    
    ```jsx
    "ALOHA".indexOf("HA") // 3
    "ALOHA".indexOf("LOL") // -1
    ```
    
2. includes
    
    ```jsx
    "ALOHA".includes("HA") // true
    "ALOHA".includes("LOL") // false
    ```
    
3. startsWith
    
    ```jsx
    "ALOHA".startsWith("AL") // true
    "ALOHA".startsWith("HA") // false
    ```
    
4. Connecting strings
    
    ```jsx
    "ALOHA" + "!" // 'ALOHA!'
    ```
    
5. toLowerCase
    
    ```jsx
    "ALOHA".toLowerCase() // 'aloha'
    ```