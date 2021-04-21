# node_security_tests
Security tests in Node.js

#### Basic framework: 
- Node.js (JavaScript) and pentest-tool-lite npm package.

#### Configuration: 
- Clone this repository.
- You must have Node.js installed in your local machine. 
- After that, install the dependencies running this command in the root: 
```sh
 npm install
```
#### Project structure:
- There is a script configured for security test on package.json.
- It was created a .gitignore file to not push "node_modules" folder.
- It was added CircleCI file to run tests in pipeline (CI/CD/Continuous Testing).

#### About test script:

**pentest**
![N|pentest](https://github.com/marcoshioka/node_security_tests/blob/main/pentest.png)

It's a script using npm package "pentest-tool-lite", to finds common vulnerabilities. That includes: file availability, caching, content sniffing and minification.

To execute this script, run the command (a log file "log-pentest.txt" is generated in the end of execution):
```sh
npm run vulnerabilities
```

### CircleCI: 
It was included a configuration to execute these security tests in CircleCI (CI/CD/Continuous Testing). The config is in "circle.yml" file, in the project root. With this config the project execute in Circle CI, including the log file in the end of execution.

### Version information:
- 1.0.0: first version

### Author:
- Marcos Ribeiro Hioka
- contact: marcosribeirohioka@gmail.com