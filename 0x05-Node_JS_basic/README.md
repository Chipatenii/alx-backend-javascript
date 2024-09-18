```
# 0x05. NodeJS Basics

## Description
This project focuses on the fundamentals of **NodeJS**, **ExpressJS**, and **ES6**. By the end of this project, you will be able to run JavaScript code using NodeJS, handle HTTP requests using NodeJS and ExpressJS, and develop faster using tools like **Nodemon** and **Babel-node**.

## Learning Objectives
By completing this project, you will learn to:
- Run JavaScript using NodeJS.
- Use NodeJS modules effectively.
- Read files with specific NodeJS modules.
- Access command-line arguments and environment variables using the **process** module.
- Create a small HTTP server with NodeJS.
- Build a small HTTP server using **ExpressJS**.
- Implement advanced routes using ExpressJS.
- Use ES6 features with NodeJS using **Babel-node**.
- Leverage **Nodemon** for faster development.

## Requirements
- Allowed editors: `vi`, `vim`, `emacs`, **Visual Studio Code**.
- All files will be interpreted/compiled on **Ubuntu 18.04 LTS** using **NodeJS version 12.x.x**.
- All JavaScript files must use the `.js` extension.
- End all files with a new line.
- Your code will be tested with **Jest** using the command: `npm run test`.
- Ensure your code passes all **lint** rules by running: `npm run full-test`.
- Export functions or classes using the `module.exports = myFunction` format.

## Tools and Libraries
- **NodeJS**: JavaScript runtime environment for server-side programming.
- **ExpressJS**: Web framework for NodeJS to create HTTP servers and advanced routing.
- **Mocha**: Testing framework.
- **Nodemon**: Development tool to automatically restart the server after changes.
- **Babel-node**: Tool to use ES6+ features in NodeJS.

## Installation
To get started with the project, ensure you have NodeJS and npm installed, then run the following command:
```bash
$ npm install
```
## Usage
1. Run the server:
   ```bash
   $ node server.js
   ```
2. For development, use **Nodemon** to automatically reload:
   
   $ nodemon server.js
   

## File Structure
- **database.csv**: A sample CSV file containing user data.
- **package.json**: Contains project dependencies and scripts.
- **babel.config.js**: Babel configuration file.
- **.eslintrc.js**: ESLint configuration file.

### Sample CSV Data
The `database.csv` file contains the following fields: `firstname`, `lastname`, `age`, and `field`. Some example rows:
```
Johann, Kerbrou, 30, CS
Guillaume, Salou, 30, SWE
Arielle, Salou, 20, CS
```

## Testing
To run the tests:
```bash
$ npm run test
```

Ensure your code passes all tests and lint rules before submission by running:
```bash
$ npm run full-test
```

## Resources
- [Node JS Getting Started](https://nodejs.org/en/docs/guides/getting-started-guide/)
- [Process API Documentation](https://nodejs.org/dist/latest-v12.x/docs/api/process.html)
- [Child Process Documentation](https://nodejs.org/dist/latest-v12.x/docs/api/child_process.html)
- [Express Getting Started](https://expressjs.com/en/starter/installing.html)
- [Mocha Documentation](https://mochajs.org/)
- [Nodemon Documentation](https://nodemon.io/)

## Author
- GitHub: [chipatenii](https://github.com/chipatenii)
```
