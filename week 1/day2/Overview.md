# Day 2 (Week 2): Basic CSS Concepts and Use Cases
[Go Back 👈](/readme.md)

Welcome to Day 2 of Week 2 in the "Intermediate HTML, CSS, and JavaScript" section of our Web Development course. Today, we'll explore basic CSS concepts and demonstrate their use cases with examples.

## Table of Contents
- [Introduction to CSS](#introduction-to-css)
- [CSS Selectors](#css-selectors)
- [Styling Text and Fonts](#styling-text-and-fonts)
- [Box Model and Layout](#box-model-and-layout)
- [Assignment](#assignment)

---

## Introduction to CSS

CSS (Cascading Style Sheets) is a crucial technology in web development that allows us to style and layout web pages. It provides the means to control the visual presentation of HTML elements. Today, we'll start with the basics.

---

## CSS Selectors

CSS selectors are used to target specific HTML elements for styling. Understanding selectors is fundamental to applying styles effectively.

**Use Case**: Selecting HTML elements by tag name, class, and ID.

**Example**:
```css
/* Selecting by tag name */
p {
  color: blue;
}

/* Selecting by class */
.title {
  font-size: 24px;
}

/* Selecting by ID */
#header {
  background-color: gray;
}
```

## Styling Text and fonts
CSS allows us to control the appearance of text and fonts on our web pages.

**Use Case**: Changing text color, font size, and family.

**Example**:
```css
/* Changing text color */
p {
  color: red;
}

/* Adjusting font size and family */
h1 {
  font-size: 36px;
  font-family: Arial, sans-serif;
}
```

## Box Model and Layout

Understanding the CSS box model is essential for controlling the layout and spacing of elements.

**Use Case**: Setting margins, borders, padding, and widths.

**Example**:
```css
/* Creating spacing around an element */
.container {
  margin: 20px;
  padding: 10px;
  border: 1px solid #ccc;
  width: 300px;
}

```