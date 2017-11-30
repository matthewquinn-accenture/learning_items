# JavaScript Testing Environment Setup

The following is **one** of many ways to set up a JavaScript testing environment. In this example, we will use _Mocha_ and _Chai_ to test, _Babel_ for es6 syntax, _VS_ _Code_ for the text editor, and _npm_ as our package manager.

The following process will be done from the command line.

1. Create a base directory for our project.

    ```mkdir my_directory_name```

2. Create a `src` and `test` sub-directory inside of our base directory. The `src` sub-directory will hold our application code. The `test` sub-directory will hold the tests for our application code.

    ```mkdir my_directory_name/src```

    ```mkdir my_directory_name/test```

3. Create a `.babelrc` file inside of the base directory that contains the presets which allow us to utilize es6.

    ```touch my_directory_name/.babelrc```

4. Create an `index.js` and `test.js` file inside of the respective sub-directory. The `index.js` file is where application code is written. The `test.js` is where the test code is written.

    ```touch my_directory_name/src/index.js```

    ```touch my_directory_name/test/test.js```

5. Enter the base directory

    ```cd my_directory_name```

6. Initialize your package manager so that you can install the necessary packages needed for es6 syntax and testing. **NOTE** You will be promted with a series of environmental confirmations. Just hit `enter` until complete.

    ```npm init```

7. Install the testing libraries.

    ```npm install mocha chai``` 

8. Install the babel packages.

    ```npm install babel-cli babel-core babel-polyfill babel-preset-es2015 babel-register```

9. Install yarn

   ```yarn install```

10. Open the .babelrc file

    ```code .babelrc```

11. Type in the presets to configure es6 syntax

    ```{

        "presets": ["es2015"]

                }```

12. In the `test.js` file in the `test/` directory import the Mocha and Chai testing libraries

    ```import Mocha from 'mocha'```

    ```import { chai } from 'chai'```


