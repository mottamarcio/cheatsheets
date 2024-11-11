## JAVASCRIPT

**Basic Syntax:**

  * **Variables:**

    ```javascript
    let age = 30; // Mutable variable
    const name = "John Doe"; // Immutable variable
    ```

  * **Data Types:**

      * `number`: Number (e.g., 10, 3.14)
      * `string`: String (e.g., "Hello", 'JavaScript')
      * `boolean`: Boolean (true or false)
      * `object`: Object (e.g., { name: "John", age: 30 })
      * `array`: Array (e.g., [1, 2, 3])
      * `null`: Intentional absence of a value
      * `undefined`: Uninitialized variable
      * `symbol`: Unique identifier

  * **Operators:**

      * Arithmetic: `+`, `-`, `*`, `/`, `%`, `**`
      * Comparison: `==`, `===`, `!=`, `!==`, `>`, `<`, `>=`, `<=`
      * Logical: `&&`, `||`, `!`
      * Assignment: `=`, `+=`, `-=`, `*=`, `/=`, etc.
      * Ternary: `condition ? expr1 : expr2`

  * **Control Flow:**

      * `if-else` statement
      * `for` loop
      * `while` loop
      * `switch` statement
      * `try...catch` statement

**Intermediate Concepts:**

  * **Functions:**

    ```javascript
    function add(x, y) {
      return x + y;
    }

    const add = (x, y) => x + y; // Arrow function
    ```

  * **Arrays:**

    ```javascript
    const numbers = [1, 2, 3];
    numbers.push(4); // Add element to the end
    numbers.map(x => x * 2); // Transform elements
    numbers.filter(x => x > 2); // Filter elements
    ```

  * **Objects:**

    ```javascript
    const user = { name: "John", age: 30 };
    user.age = 31; // Modify property
    Object.keys(user); // Get keys
    Object.values(user); // Get values
    ```

  * **Template Literals:**

    ```javascript
    const name = "John";
    console.log(`Hello, ${name}!`);
    ```

  * **Destructuring:**

    ```javascript
    const user = { name: "John", age: 30 };
    const { name, age } = user;
    ```

  * **Classes:**

    ```javascript
    class Dog {
      constructor(name) {
        this.name = name;
      }

      bark() {
        console.log("Woof!");
      }
    }
    ```

  * **Modules:**

    ```javascript
    // myModule.js
    export function add(x, y) {
      return x + y;
    }

    // main.js
    import { add } from './myModule.js';
    ```

**Advanced Concepts:**

  * **Promises:**

    ```javascript
    const promise = new Promise((resolve, reject) => {
      // Asynchronous operation
      if (success) {
        resolve(result);
      } else {
        reject(error);
      }
    });

    promise.then(result => {
      // Handle success
    }).catch(error => {
      // Handle error
    });
    ```

  * **Async/Await:**

    ```javascript
    async function fetchData() {
      try {
        const response = await fetch('https://api.example.com/data');
        const data = await response.json();
        return data;
      } catch (error) {
        console.error(error);
      }
    }
    ```

  * **Generators:**

    ```javascript
    function* myGenerator() {
      yield 1;
      yield 2;
      yield 3;
    }
    ```

  * **Proxy:**

    ```javascript
    const handler = {
      get(target, prop) {
        return prop in target ? target[prop] : "Not found";
      }
    };

    const proxy = new Proxy({}, handler);
    ```

  * **Regular Expressions:**

    ```javascript
    const pattern = /hello/i;
    pattern.test("Hello, world!"); // true
    ```

**Tips and Tricks:**

  * Use strict mode (`"use strict";`).
  * Use linters like ESLint for code quality.
  * Use a debugger to troubleshoot your code.
  * Keep your code clean and readable.
  * Learn about design patterns.

**Resources:**

  * **MDN Web Docs:** [https://developer.mozilla.org/en-US/docs/Web/JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
  * **JavaScript.info:** [https://javascript.info/](https://www.google.com/url?sa=E&source=gmail&q=https://javascript.info/)
  * **You Don't Know JS:** [https://github.com/getify/You-Dont-Know-JS](https://www.google.com/url?sa=E&source=gmail&q=https://github.com/getify/You-Dont-Know-JS)
  * **ES6 Features:** [http://es6-features.org/](https://www.google.com/url?sa=E&source=gmail&q=http://es6-features.org/)
