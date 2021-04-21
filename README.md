# node_security_tests
Security tests in Node.js

#### Basic framework: 
- Node.js (JavaScript), is-website-vulnerable and pentest-tool-lite npm packages.

#### Configuration: 
- Clone this repository.
- You must have Node.js installed in your local machine. 
- After that, install the dependencies running this command in the root: 
```sh
 npm install
```
#### Project structure:
- There are scripts configured for each security test on package.json.
- It was created a .gitignore file to not push "node_modules" folder.
- It was added CircleCI file to run tests in pipeline (CI/CD/Continuous Testing).



#### About each test script:

**vulnerabilities**
![N|is-website-vulnerable](https://github.com/marcoshioka/node_security_tests/blob/main/vulnerabilities.png)

It's a script using npm package "is-website-vulnerable" to finds publicly known security vulnerabilities in a website's frontend JavaScript libraries. 

To execute this script, run the command (a log file "log-vulnerabilities.txt" is generated in the end of execution):
```sh
npm run vulnerabilities
```

**pentest**
![N|pentest](https://github.com/marcoshioka/node_security_tests/blob/main/pentest.png)

It's a script using npm package "pentest-tool-lite", to finds common vulnerabilities. That includes: file availability, caching, content sniffing and minification.

To execute this script, run the command (a log file "log-pentest.txt" is generated in the end of execution):
```sh
npm run vulnerabilities
```

### CircleCI: 
It was included a configuration to execute these security tests in CircleCI (CI/CD/Continuous Testing). The config is in "circle.yml" file, in the project root. With this config the project execute in Circle CI each job/script in parallel, including the log file in the end of execution.

### Version information:
- 1.0.0: first version

### Author:
- Marcos Ribeiro Hioka
- contact: marcosribeirohioka@gmail.com