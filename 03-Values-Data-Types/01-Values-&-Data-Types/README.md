# 1. Values & Data Types

Link: [https://frontendmasters.com/courses/javascript-first-steps/values-data-types/](https://frontendmasters.com/courses/javascript-first-steps/values-data-types/)

JavaScript has TWO kinds of data

- Primitive types
    - string
    - number
    - boolean
        - true
        - false
    - undefined
    - null
    - A couple **others** we don’t need yet ([BigInt](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/BigInt), [Symbol](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Symbol))
- Objects (E.g.: document & friends)

[Undefined](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined) vs [Null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null)

- Technical explanation
    
    ### **Difference Between `undefined` and `null` in JavaScript**
    
    Both `undefined` and `null` represent the absence of a value, but they are used in different scenarios.
    
    ---
    
    ### **1. `undefined`**
    
    **Definition:** A variable that has been declared but **has not been assigned a value** will be `undefined` by default. It also represents missing properties in objects or missing function arguments.
    
    ### **Examples:**
    
    ```jsx
    let x; // No value assigned
    console.log(x); // undefined
    
    function greet(name) {
        console.log("Hello, " + name);
    }
    greet(); // Hello, undefined (because no argument was passed)
    
    let obj = {};
    console.log(obj.age); // undefined (property 'age' does not exist)
    ```
    
    ### **Key Characteristics of `undefined`**
    
    - A **variable that is declared but not initialized** is `undefined`.
    - Accessing **non-existent object properties** returns `undefined`.
    - If a **function does not return anything**, it returns `undefined` by default.
    - It is the **default value of function parameters** when arguments are missing.
    
    ---
    
    ### **2. `null`**
    
    **Definition:** `null` is an **intentional absence of a value**. It is explicitly assigned to indicate that a variable **should have no value**.
    
    ### **Examples:**
    
    ```jsx
    let y = null;
    console.log(y); // null
    
    let user = { name: "Alice", age: 25 };
    user.age = null; // Intentionally removing the value
    console.log(user.age); // null
    ```
    
    ### **Key Characteristics of `null`:**
    
    - It is a **deliberate assignment** that signifies “no value” or “empty.”
    - It is **not the default value** of a variable.
    - Often used when you want to **reset or clear** a variable's value.
    
    ---
    
    ### **3. Differences Between `undefined` and `null`**
    
    | Feature | `undefined` | `null` |
    | --- | --- | --- |
    | **Type** | `undefined` | `object` (a known JavaScript bug) |
    | **Default Value?** | Yes, for uninitialized variables | No, must be manually assigned |
    | **Purpose** | Absence of value, variable not assigned | Intentional absence of value |
    | **Used By** | JavaScript (automatically) | Developers (manually assigned) |
    | **Example** | `let x; console.log(x); // undefined` | `let x = null; console.log(x); // null` |
    
    ---
    
    ### **4. Type Checking**
    
    ```jsx
    console.log(typeof undefined); // "undefined"
    console.log(typeof null); // "object" (this is a known JavaScript bug)
    ```
    
    ---
    
    ### **5. Comparisons**
    
    ### **Loose Equality (`==`)**
    
    ```jsx
    console.log(undefined == null); // true
    ```
    
    - `null` and `undefined` are considered **loosely equal** (`==`) because they both represent missing values.
    
    ### **Strict Equality (`===`)**
    
    ```jsx
    console.log(undefined === null); // false
    ```
    
    - `undefined` and `null` are **not strictly equal** (`===`) because they are of different types.
    
    ---
    
    ### **6. When to Use `undefined` vs `null`**
    
    | Scenario | Use `undefined` | Use `null` |
    | --- | --- | --- |
    | Uninitialized variable | ✅ | ❌ |
    | Missing function parameter | ✅ | ❌ |
    | Non-existent object property | ✅ | ❌ |
    | Reset or clear a value | ❌ | ✅ |
    | Indicating "no data available" | ❌ | ✅ |
    
    ---
    
    ### **Summary**
    
    - Use `undefined` when a value is **not assigned or missing**.
    - Use `null` when you want to **explicitly indicate** that a value is **empty or reset**.

- Practical explanation
    
    ### **1. `undefined`**
    
    Your mom gave you an empty lunchbox, but she **forgot to put any food in it**. Now, when you open it at school, there's **nothing inside**! You were expecting something, but it's just empty. **That's `undefined`!**
    
    💡 **Example:**
    
    ```jsx
    let lunchbox;  // Mom forgot to pack anything
    console.log(lunchbox); // undefined
    ```
    
    ---
    
    ### **2. `null`**
    
    This time, your mom **did put food in your lunchbox** in the morning, but then you **ate everything** at lunch. Now, your lunchbox is **completely empty on purpose**. **That's `null`!**
    
    💡 **Example:**
    
    ```jsx
    let lunchbox = "sandwich"; // Lunchbox had food
    lunchbox = null; // Now it's empty after eating
    console.log(lunchbox); // null
    ```
    
    ---
    
    ### **🚀 Quick Summary**
    
    | Situation | Is the Lunchbox Empty? | Why? |
    | --- | --- | --- |
    | `undefined` | Yes 😢 | Mom forgot to pack food! |
    | `null` | Yes 😊 | You ate everything! |
    
    Now, if JavaScript were a kid, it would say:
    
    - `"undefined? Oh no, I didn’t even get my lunch today!"` 😭
    - `"null? I had lunch, but now I finished it!"` 😋