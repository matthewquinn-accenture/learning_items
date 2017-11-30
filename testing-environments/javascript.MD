# JavaScript Testing Environment Setup

The following is **one** of many ways to set up a JavaScript testing environment. This example uses _VS_ _Code_ for the text editor, _Mocha_ and _Chai_ libraries for testing, _npm_ and _yarn_ for package managers, and _babel_ for es6 syntax.

**This tutorial assumes the following**
a. Unit test experience
b. Command line experience
b. The latest version of `npm` is installed
c. The latest version of `yarn` is installed

## Steps

**Each step will be completed from the commmand line**

1. Create a base directory for the project:

    `mkdir my_directory_name`

2. Enter the base directory:

    `cd my_directory_name`

3. Create a `src` and `test` sub-directory. The `src/` sub-directory will hold the application code. The `test/` sub-directory will hold the unit tests:

    `mkdir src`

    `mkdir test`

4. Create and open a `.babelrc` file:

    `code .babelrc`

5. In the `.babelrc` file, type the presets to configure es6 syntax:

    ```
       {
        "presets": ["es2015"]
                }
    ```

6. Go back to the command line.

7. Inside of the `src/` directory, create an `index.js` file. This file will contain the application code:

    `touch src/index.js`

8. Inside of the `test/` directory, create a `test.js` file. This file will contain the unit tests:

    `touch test/test.js`

9. Initialize npm to manage project dependencies and settings:

 **NOTE** You will be promted with a series of environmental confirmations. Just hit `enter` until complete:

    `npm init`

10. Install the testing libraries:

    `npm install mocha chai`

11. Install the babel packages so `es6` can be used:

    `npm install babel-cli babel-core babel-polyfill babel-preset-es2015 babel-register`

12. Configure yarn:

   `yarn install`

13. Open the `package.json` file:

   `code package.json`

14. In `package.json`, change:

    ```
        "scripts": {
    		"test": "echo \"Error: no test specified\" && exit 1"
 	 },
    ```

    to:

    ```
        "scripts": {
                "test": "mocha --require babel-polyfill --compilers js:babel-register"
         },
    ```

14. Save and return to the command line.

15. Open the `test.js` file:

    `code test/test.js`

13. In the `test.js` file, import the Mocha and chai libraries for unit testing:

    ```
        import Mocha from 'mocha'`

        import { chai } from 'chai'
    ```

14. In the same file, write the canary test:

    ```
    describe("Canary test", () => {
        it("should return true", () => {
            expect(true).to.equal(true);
        })
    ```
