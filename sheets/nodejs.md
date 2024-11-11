## NODEJS

**I. Basics**

  * **What is Node.js?** A JavaScript runtime environment that executes JavaScript code outside a web browser.
  * **Key Features:**
      * **Asynchronous and Event-Driven:** Non-blocking I/O operations.
      * **Fast:** Built on Chrome's V8 JavaScript engine.
      * **Single-Threaded but Highly Scalable:** Uses a single thread for event looping.
      * **npm:** The largest ecosystem of open-source libraries.

**II. Getting Started**

  * **Installation:** Download and install Node.js from the official website ([https://nodejs.org/](https://www.google.com/url?sa=E&source=gmail&q=https://nodejs.org/)).
  * **REPL (Read-Eval-Print Loop):**
      * Start the Node.js REPL by typing `node` in your terminal.
      * Execute JavaScript code interactively.
  * **Running a Script:**
      * Create a file (e.g., `app.js`) with your JavaScript code.
      * Run the script using `node app.js`.

**III. Modules**

  * **Built-in Modules:** Node.js provides core modules like `fs` (file system), `http` (web server), `path` (file paths), etc.
      * Example:
        ```javascript
        const fs = require('fs');
        fs.readFile('file.txt', 'utf8', (err, data) => {
          if (err) throw err;
          console.log(data);
        });
        ```
  * **Creating Modules:**
      * Define functions or objects in a file.
      * Export them using `module.exports`.
      * Import them into other files using `require()`.
      * Example:
        ```javascript
        // myModule.js
        function greet(name) {
          console.log(`Hello, ${name}!`);
        }
        module.exports = { greet };

        // app.js
        const myModule = require('./myModule');
        myModule.greet('World');
        ```

**IV. npm (Node Package Manager)**

  * **What is npm?** A package manager for JavaScript, included with Node.js.
  * **Essential Commands:**
      * `npm init`: Initialize a new project and create a `package.json` file.
      * `npm install <package_name>`: Install a package.
          * `-g`: Install globally.
          * `--save-dev`: Install as a development dependency.
      * `npm uninstall <package_name>`: Uninstall a package.
      * `npm update <package_name>`: Update a package.
      * `npm start`: Run the script specified in the `start` property of `package.json`.
      * `npm test`: Run the script specified in the `test` property of `package.json`.
      * `npm publish`: Publish a package to the npm registry.

**V. npx (Node Package Executor)**

  * **What is npx?** Executes packages without installing them globally.
  * **Common Use Cases:**
      * Running one-off commands: `npx create-react-app my-app`
      * Executing different versions of a package: `npx webpack@<version>`
      * Running scripts from a local `node_modules` directory.

**VI. Advanced Concepts**

  * **Events:**
      * Node.js uses an event loop to handle asynchronous operations.
      * Use the `events` module to emit and listen for events.
  * **Streams:**
      * Handle large amounts of data efficiently.
      * Types: Readable, Writable, Duplex, Transform.
  * **Child Processes:**
      * Execute external commands.
      * Use `child_process.spawn()` or `child_process.exec()`.
  * **Clusters:**
      * Utilize multiple CPU cores for improved performance.
  * **Worker Threads:**
      * Enable parallel execution of JavaScript code within a single process.

**VII. TypeScript with Node.js**

  * **Installation:** `npm install typescript tsx tsup`
  * **Configuration:** Create a `tsconfig.json` file to configure the TypeScript compiler.
  * **Compilation:** Use `tsc` to compile TypeScript code into JavaScript.
  * **Bundling:** Use a bundler like `tsup` to bundle your code for production.

**VIII. Useful npm Packages**

  * **Express.js:** Web framework for building APIs and web applications.
  * **Socket.IO:** Enables real-time, bidirectional communication.
  * **Mongoose:** ODM (Object Data Modeling) library for MongoDB.
  * **Jest:** Testing framework.
  * **PM2:** Production process manager for Node.js applications.

**IX. Debugging**

  * **Console Logging:** Use `console.log`, `console.error`, etc.
  * **Node.js Debugger:** Use the `node debug` command or IDE debugging tools.
