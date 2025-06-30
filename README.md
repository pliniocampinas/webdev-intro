# webdev-intro
A Web development introduction repository

## Web Development Introduction

### Abstractions, protocols and key words.

Web apps work based on a client-server architecture. In such a model the communication is one sided, the client starts the communication with a request and receives a response from the server. Those two words are key to web development, being the base abstraction of the HyperText Transfer Protocol, HTTP for short.


HTTP is used to establish the communication between the client and the server through the internet. As its name says, the requests and responses are encoded as text or hypertext.
Hypertext contains links to other requests.

On the web the client is typically the browser, when it requests an HTML page. The hypertext mark-up language page contains the basic structure the browser needs to render the web page. When the browser processes the html response it will fire a series of other requests, building the DOM tree and starting the critical rendering path.

### The DOM tree

The Domain Object Model aims to describe a web app as a tree of objects. Each of them holding properties and event listeners. The browser provides an API to work with these events, properties and the structure of the tree. The HTML document is the root node of the tree. An HTML document as described bellow, contains a head, with metadata about the app and a body with HTML elements. The browser parses these document to build a DOM tree and render the page.

Example 0:
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Basic HTML Page</title>
</head>
<body>
  <h1>Welcome to My Website</h1>
  <p>This is a basic HTML file.</p>
  <button class="click-me-button">Click-me</button>
</body>
</html>
```

### Javascript

In order to change and handle events of the page, the browser provides an API with a set of methods and objects. As shown below, html elements emits events based on user behavior and change the content of other dom nodes, the browser than reflect these change at the screen.

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Basic HTML Page</title>
</head>
<body>
  <h1>Welcome to My Website</h1>
  <p>This is a basic HTML file.</p>
  <p id="filled-content">
    <!-- Dinamic filled content -->
  </p>

  <button class="click-me-button">Toogle</button>

  <script>
    const initialText = "Hello, World!";
    const secondText = "Amazing!";
    let toggled = false;

    // Add an event listener to the button
    document.querySelector('.click-me-button').addEventListener('click', function() {
      toggled = !toggled;
      document.getElementById('filled-content').textContent = toggled? secondText : initialText;
    });

    window.addEventListener('load', function() {
      // Fill the paragraph with the global variable
      console.log("Page loaded, filling content...");
      document.getElementById('filled-content').textContent = initialText;
    });
  </script>
  
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f0f0f0;
      color: #333;
    }
    h1 {
      color: #4CAF50;
    }
    .click-me-button {
      font-weight: bold;
      padding: 10px 20px;
      background-color: #008CBA;
      color: white;
      border: none;
      cursor: pointer;
    }
    .click-me-button:hover {
      background-color: #005f73;
    }
  </style>
</body>
</html>
```

Example 1 also contains a <style> tag. The style tag contains CSS code, which is parsed by the browser to indicate how an HTML element is rendered.
