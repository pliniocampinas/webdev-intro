# webdev-intro
A Web development introduction repository

## Web Development Introduction

### Abstractions, protocols and key words.

Web apps work based on a client-server architecture. In such a model the communication is one sided, the client starts the communication with a request and receives a response from the server. Those two words are key to web development, being the base abstraction of the HyperText Transfer Protocol, HTTP for short.


HTTP is used to establish the communication between the client and the server through the internet. As its name says, the requests and responses are encoded as text or hypertext.
Hypertext contains links to other requests.

On the web the client is typically the browser, when it requests an HTML page. The hypertext mark-up language page contains the basic structure the browser needs to render the web page. When the browser processes the html response it will fire a series of other requests, building the DOM tree and starting the critical rendering path.

### The DOM tree

The Domain Object Model aims to describe a web app as a tree of objects or nodes. Each of them holding properties and event handlers, also called listeners. The browser provides an API to handle these events, change properties or the structure of the tree. The HTML document is the root node of the tree.

```

```
