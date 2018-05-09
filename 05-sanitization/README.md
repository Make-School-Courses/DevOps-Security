
# Class 5: Sanitizing Input

At any point where input is used in code you must clean
it up to prevent input from become an exploit. 

## What is sanitization? 

Cleaning up input so that can not be executed as code. 
Any plain text that is part of the the content for page 
that is code will treated as code! 

To prevent malicious scripts from running in your pages
all input needs to be sanitized. This process converts 
all special characters to HTML entities. 

## HTML entities 

https://developer.mozilla.org/en-US/docs/Glossary/Entity

## CSS Escapes 

https://developer.mozilla.org/en-US/docs/Web/API/CSS/escape

## URL Encoding

https://developer.mozilla.org/en-US/docs/Glossary/percent-encoding

## Client side vs Server side

Some code run on the server. These are things like getting and 
putting things into the database. Other code runs in the browser
or client computer. This is code that handles user interaction 
and manages content from the browser. 

Depending on where you are using user input you will want to 
sanitize from one side or the other and probably both. 

## Bundling JS with Browserify

When working with Node and Express you are managing dependancies 
on the server side. These files are not accessible in the browser. 

You can use Browserify to bundle JavaScript files into a single 
file that can be used by the client browser. This allows you to 
leverage NPM libraries in the Client. 

- http://browserify.org

### Serving static files

Express only serves files that from routes. To serve static files
you will need to designate a static folder. 

```JS
// Serve static resources from the public folder
app.use(express.static('public'));
```

## Sanitizing Clientside 

Write your own sanitization script

- https://stackoverflow.com/questions/2794137/sanitizing-user-input-before-adding-it-to-the-dom-in-javascript

```JS
function encodeHTML(s) {
    return s.replace(/&/g, '&amp;').replace(/</g, '&lt;').replace(/"/g, '&quot;');
}
```

Or, use a library: 

- https://wesbos.com/sanitize-html-es6-template-strings/
- https://github.com/cure53/DOMPurify

## Sanitizing server side

You could use DOMPurify or write your own sanitization script
but, if you're working with Express JS you have access to 
middleware. 

- https://www.npmjs.com/package/express-sanitizer

## Challenges


- Write a sanitization script for the client
  - Choose one: 
    - Write a string parser that replaces <, >, and & with HTML entities. 
    - Use Browserify to install DOMPurify. 
      - Follow the instructions to install Browserify
      - Define a Public static folder in Express
      - Install DOMPurify
        - You will have to run all of your client JS from a module!

- Add a sanitizer to Express. 
  - Feel free to use any approach, realize that in this case 
  it's probably best to use middleware as this is the best workflow 
  with express. 
    - Try this middleware: 
      - https://www.npmjs.com/package/express-sanitizer


