# npm packages

NPM is the most popular package manager today and if 
you have worked with Node JS you have probably used 
NPM. 

## Introduction

NPM manages packages libraries of code that add 
functionality to JavaScript projects. 

## Write and Publish a package to NPM

- Make an NPM account
- Set up a GitHub project
  - Think of a name
    - Search NPM for the name
  - Create a new GitHub project with these settings: 
    -
  - Clone the project locally
- Login `npm login`
  - Set your author name: `npm set init.author.name Joe Smith`
  - Set your email: `npm set init.author.email "joesmith@gmail.com"`
  - Set your author URL: `npm set init.author.url "http://www.joesmith.com"`
- Navigate in the terminal to your GitHub project
- Init a new NPM project `npm init`
  - Use these settings
    - Version `0.1.0`
    - test `mocha --reporter spec`
- Add a new file to the project 'index.js'
- Add your code
- Write a Read Me
- Commit and Push to GitHub
- Publish to NPM `npm publish`

## Tests

## Continuous Integration

## Coverage

## Badges 

## Resources 

- https://codeburst.io/how-to-create-and-publish-your-first-node-js-module-444e7585b738
- https://docs.npmjs.com/getting-started/creating-node-modules
- https://docs.npmjs.com/getting-started/publishing-npm-packages
- https://lexi-lambda.github.io/blog/2016/08/24/understanding-the-npm-dependency-model/