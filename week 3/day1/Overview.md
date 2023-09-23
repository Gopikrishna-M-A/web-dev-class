# Week 3: Introduction to Node.js and Express
[Go Back 👈](/readme.md)

## Day 1 (Week 3): Introduction to Node.js

### Table of Contents

- [Introduction](#introduction)
- [Node.js Basics](#nodejs-basics)
  - [What is Node.js?](#what-is-nodejs)
  - [Setting up Node.js](#setting-up-nodejs)
- [Node.js Modules](#nodejs-modules)
  - [CommonJS Modules](#commonjs-modules)
  - [Built-in Modules](#built-in-modules)
- [Node.js HTTP Module](#nodejs-http-module)
  - [Creating a Simple Web Server](#creating-a-simple-web-server)
- [Assignment](#assignment)

## Introduction

In this session, we will dive into the world of server-side JavaScript development with Node.js. Node.js is a runtime environment that allows you to run JavaScript on the server, making it a powerful tool for building web applications, APIs, and more.

## Node.js Basics

### What is Node.js?

Node.js is an open-source, cross-platform JavaScript runtime environment that allows developers to run JavaScript code outside the web browser. It provides a vast ecosystem of libraries and modules that simplify server-side development.

### Setting up Node.js

Before we start, make sure you have Node.js installed on your computer. You can download it from the official website: [Node.js Download](https://nodejs.org/).

## Node.js Modules

### CommonJS Modules

Node.js uses the CommonJS module system for organizing code into reusable modules. We'll explore how to create and use modules in your Node.js applications.

### Built-in Modules

Node.js comes with a set of built-in modules that provide functionality for various tasks. We'll look at some commonly used built-in modules and their capabilities.

## Node.js HTTP Module

### Creating a Simple Web Server

We'll use Node.js's HTTP module to create a basic web server. You'll learn how to handle HTTP requests and serve web pages using Node.js.

**Using Inbuild HTTP module**
```javascript
// Import the http module
const http = require('http');

// Define the hostname and port for the server to listen on
const hostname = 'localhost';
const port = 3000;

// Create an HTTP server
const server = http.createServer((req, res) => {
  // Set the response status and headers
  res.statusCode = 200;
  res.setHeader('Content-Type', 'text/plain');

  // Send a response to the client
  res.end('Hello, World!\n');
});

// Start the server and listen on the specified hostname and port
server.listen(port, hostname, () => {
  console.log("server started");
});

```

**Using Express framework**
```javascript
const express = require('express');

const app = express();

app.get('/', (req, res) => {
  res.send('Hello, Express!');
});

app.listen(3000, () => {
  console.log("server started");
});

```

## Assignment

Your assignment for today is to create a simple web server using Node.js and the HTTP module. You should be able to respond to incoming HTTP requests with a "Hello, World!" message.

Feel free to explore and experiment with the capabilities of Node.js as you embark on your journey into server-side development.

Remember to refer to the resources provided for additional guidance and documentation.

Happy coding!

## Resources

- [Node.js Official Documentation](https://nodejs.org/en/docs/): The official documentation for Node.js, including guides, APIs, and best practices.

- [Express.js Official Documentation](https://expressjs.com/): The official documentation for the Express.js framework, covering routing, middleware, and more.

