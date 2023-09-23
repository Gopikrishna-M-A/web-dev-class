# Day 2 (Week 2): Advanced JavaScript
[Go Back 👈](/readme.md)

Welcome to Day 3 of Week 2 in our web development course! Today, we're diving deeper into the world of JavaScript, exploring more advanced concepts and techniques that will take your web development skills to the next level.

## Table of Contents

- [Introduction](#introduction)
- [Asynchronous JavaScript](#asynchronous-javascript)
  - [Promises](#promises)
  - [Async/Await](#asyncawait)
- [Working with APIs](#working-with-apis)
  - [Fetching Data](#fetching-data)
  - [JSON Parsing](#json-parsing)
- [Assignment](#assignment)

## Introduction

In the previous sessions, we covered the basics of JavaScript, including variables, functions, and DOM manipulation. Today, we'll explore more advanced topics that are crucial for building modern web applications.

## Asynchronous JavaScript

Modern web applications often need to handle asynchronous operations, such as fetching data from servers or dealing with user interactions. We'll delve into two essential concepts for managing asynchronous code.

```javascript
async function fetchData() {
  const data = await fetchDataFromAPI();
}
```

### Promises

Promises are a way to handle asynchronous operations more elegantly. Here's an example of using a promise to fetch data from a server:

```javascript
fetch('https://api.example.com/data')
  .then(response => response.json())
  .then(data => {
    console.log(data);
  })
  .catch(error => {
    console.error('Error:', error);
  });
```

# Working with APIs

Many modern web applications interact with external APIs to retrieve or send data. In this session, we'll explore how to work with APIs effectively.

## Fetching Data

We'll use the Fetch API to make HTTP requests to external services and retrieve data.
```javascript
async function fetchData() {
    const response = await fetch('https://api.example.com/data');
    const data = await response.json();
    console.log(data);
}
```

## JSON Parsing

Most APIs send and receive data in JSON format. We'll cover how to parse JSON data and work with it in JavaScript.

```javascript
const jsonData = '[{"id":1,"name":"John Doe","email":"john@example.com"},{"id":2,"name":"Jane Smith","email":"jane@example.com"}]';
  
const parsedData = JSON.parse(jsonData);
console.log(parsedData);
```

```javascript
[
  {
    "id": 1,
    "name": "John Doe",
    "email": "john@example.com"
  },
  {
    "id": 2,
    "name": "Jane Smith",
    "email": "jane@example.com"
  }
]
```

## Assignment

**Objective:** Build a web application that fetches data from an external API and displays it on your webpage. You can choose an API of your interest, such as weather data, news articles, or any other public API.

**Requirements:**

1. Fetch data from the chosen API using Fetch or async/await.
2. Parse the JSON response.
3. Display the relevant data on your webpage.

Feel free to get creative and add additional features or styling to make your application stand out.

## Resources

- [JavaScript Promises](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)
- [Async/Await](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/async_function)
- [Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API)

By the end of this session, you'll have a solid understanding of advanced JavaScript concepts, including asynchronous programming and working with external APIs. Have fun with your assignment, and explore the world of modern web development!

