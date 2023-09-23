# CSS Flexbox Guide

## Table of Contents

1. [Introduction](#introduction)
2. [What is Flexbox?](#what-is-flexbox)
3. [Why Use Flexbox?](#why-use-flexbox)
4. [Basic Flexbox Concepts](#basic-flexbox-concepts)
   - [Flex Container](#flex-container)
   - [Flex Items](#flex-items)
   - [Main Axis and Cross Axis](#main-axis-and-cross-axis)
5. [Flex Container Properties](#flex-container-properties)
   - [`display`](#display)
   - [`flex-direction`](#flex-direction)
   - [`flex-wrap`](#flex-wrap)
   - [`justify-content`](#justify-content)
   - [`align-items`](#align-items)
   - [`align-content`](#align-content)
6. [Flex Item Properties](#flex-item-properties)
   - [`order`](#order)
   - [`flex-grow`](#flex-grow)
   - [`flex-shrink`](#flex-shrink)
   - [`flex-basis`](#flex-basis)
   - [`flex`](#flex)
   - [`align-self`](#align-self)
7. [Examples](#examples)
   - [Basic Flexbox Layout](#basic-flexbox-layout)
   - [Centering Elements](#centering-elements)
   - [Equal Width Columns](#equal-width-columns)
   - [Responsive Card Layout](#responsive-card-layout)
8. [Resources](#resources)

## Introduction

CSS Flexbox, or Flexible Box Layout, is a layout model designed to make it easier to design and distribute space within a container and align items when the size of your items is unknown or dynamic. It provides an efficient and predictable way to layout, align, and distribute space among elements, even when their sizes vary.


## What is Flexbox?

Flexbox is a one-dimensional layout model, meaning it deals with layout in one direction at a time, either in a row or a column. It enables you to create complex layouts with a simpler and more predictable structure compared to traditional CSS layout methods.

## Why Use Flexbox?

- **Simplified Layouts**: Flexbox simplifies the creation of complex layouts, such as navigation bars, grids, and card layouts.

- **Dynamic Sizing**: It's excellent for accommodating varying content sizes, ensuring your design remains flexible.

- **Alignment Control**: Easily control alignment and distribution of elements within a container.

- **Responsive Design**: Flexbox plays a crucial role in creating responsive and adaptive layouts.

## Basic Flexbox Concepts

### Flex Container

A flex container is an element that contains flex items. To create a flex container, you need to set its `display` property to `flex` or `inline-flex`. This property turns its children into flex items.

```css
.container {
  display: flex; /* or inline-flex */
}
```

### Flex Items
Flex items are the children of a flex container. They automatically become flexible, allowing them to grow or shrink as needed.

```css
.item {
  /* This element becomes a flex item */
}
```

# Main Axis and Cross Axis

In a flex container, there are two axes:

- **Main Axis**: The primary axis along which flex items are laid out. It's determined by the `flex-direction` property (e.g., row or column).

- **Cross Axis**: The perpendicular axis to the main axis.

## Flex Container Properties

### `display`

- **Values**: `flex` | `inline-flex`
- **Description**: Defines a flex container.

### `flex-direction`

- **Values**: `row` | `row-reverse` | `column` | `column-reverse`
- **Description**: Specifies the direction of the main axis.

### `flex-wrap`

- **Values**: `nowrap` | `wrap` | `wrap-reverse`
- **Description**: Controls whether flex items should wrap onto multiple lines when the container overflows.

### `justify-content`

- **Values**: `flex-start` | `flex-end` | `center` | `space-between` | `space-around`
- **Description**: Aligns flex items along the main axis.

### `align-items`

- **Values**: `flex-start` | `flex-end` | `center` | `baseline` | `stretch`
- **Description**: Aligns flex items along the cross axis.

### `align-content`

- **Values**: `flex-start` | `flex-end` | `center` | `space-between` | `space-around` | `stretch`
- **Description**: Aligns flex lines (when there are multiple lines) along the cross axis.

## Flex Item Properties

### `order`

- **Values**: `<number>`
- **Description**: Specifies the order in which flex items appear.

### `flex-grow`

- **Values**: `<number>`
- **Description**: Determines how much a flex item should grow relative to other items when there's available space along the main axis.
