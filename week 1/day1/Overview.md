# Day 1 (Week 1): Introduction to Web Development and HTML

[Go Back 👈](/readme.md)

Welcome to Day 1 of Week 1 in the "Basic HTML and CSS" section of our Web Development course. Today, we'll introduce you to the exciting field of web development and get started with the basics of HTML.

## Table of Contents

- [Introduction](#introduction)
- [Basic HTML Tags](#basic-html-tags)
  - [`<html>`](#html)
  - [`<head>`](#head)
  - [`<title>`](#title)
  - [`<meta>`](#meta)
  - [`<link>`](#link)
  - [`<script>`](#script)
  - [`<body>`](#body)
- [Headings and Paragraphs](#headings-and-paragraphs)
  - [`<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>`, `<h6>`](#headings)
  - [`<p>`](#paragraphs)
- [Links and Images](#links-and-images)
  - [`<a>`](#links)
  - [`<img>`](#images)
- [Lists](#lists)
  - [`<ul>`](#unordered-lists)
  - [`<ol>`](#ordered-lists)
  - [`<li>`](#list-items)
- [Containers](#containers)
  - [`<div>`](#div)

## Introduction

HTML (Hypertext Markup Language) is a fundamental language used in web development. It defines the structure and content of web pages, allowing web browsers to display information correctly to users.


## Basic HTML Tags

### `<html>`

- Description: Defines the root of an HTML document.
- Example:
  ```html
  <!DOCTYPE html>
  <html lang="en">
    <head>
      <meta charset="UTF-8">
      <title>My Website</title>
    </head>
    <body>
      <!-- Your content here -->
    </body>
  </html>
  ```
  - Attributes: `lang` (language code) for specifying the document's language.

### `<head>`

- Description: Contains meta-information about the document.
- Example:
  ```html
    <head>
      <title>Page Title</title>
    </head>
  ```

### `<title>`

- Description: Sets the title of the document (displayed in the browser tab).
- Example:
  ```html
  <title>My Website</title>
  ```

### `<meta>`

- Description: Provides metadata about the document.
- Example:
  ```html
  <meta charset="UTF-8">
  <meta name="description" content="A web page about something">
  ```
  - Attributes: `charset` (character encoding), `name`, `content`, `http-equiv`, and more.

### `<link>`

- Description: Links external resources, typically stylesheets.
- Example:
  ```html
  <link rel="stylesheet" href="styles.css">
  ```
  - Attributes: `rel` (relationship), `href` (URL), `type`, and others.

### `<script>`

- Description: Embeds JavaScript code or references an external script.
- Example:
  ```html
  <script src="script.js"></script>
  ```
  - Attributes: `src` (source file), `type`, `async`, `defer`, and more.

### `<body>`

- Description: Contains the visible content of the webpage.
- Example:
  ```html
  <body>
    <h1>Hello, World!</h1>
    <p>This is a paragraph of text.</p>
    <!-- Other content here -->
  </body>
  ```

## Headings and Paragraphs

### `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>`, `<h6>`

- Description: Define headings with varying levels of importance.
- Example:
  ```html
  <h1>Heading Level 1</h1>
  <h2>Heading Level 2</h2>
  <h3>Heading Level 3</h3>
  <h4>Heading Level 4</h4>
  <h5>Heading Level 5</h5>
  <h6>Heading Level 6-</h6>
  ```
  - Attributes: None.

### `<p>`

- Description: Represents a paragraph of text.
- Example:
  ```html
  <p>This is a paragraph tag.</p>
  ```

## Links and Images

### `<a>`

- Description: Creates hyperlinks to other web pages or resources.
- Example:
  ```html
  <a href="https://www.example.com">Visit Example Website</a>
  ```
  - Attributes: `href` (URL), `target`, `rel`, and more.

### `<img>`

- Description: Embeds images in the document.
- Example:
  ```html
  <img src="image.jpg" alt="A beautiful image">
  ```
  - Attributes: `src` (image source), `alt` (alternative text), `width`, `height`, and others.

## Lists

### `<ul>`

- Description: Defines an unordered (bulleted) list.
- Example:
  ```html
  <ul>
    <li>Item 1</li>
    <li>Item 2</li>
  </ul>

### `<ol>`

- Description: Defines an ordered list.
- Example:
  ```html
  <ol>
    <li>Item 1</li>
    <li>Item 2</li>
  </ol>

## Containers

### `<div>`

- Description: HTML `<div>` tags are versatile and commonly used for layout structuring and applying CSS styles to groups of elements.
- Example:
  ```html
  <div>
    <p>This is some content inside a div.</p>
  </div>
  ```