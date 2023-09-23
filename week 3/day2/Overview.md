# Day 2 (Week 3): Connecting MongoDB and Building a Project
[Go Back 👈](/readme.md)
### Table of Contents

- [Introduction](#introduction)
- [MongoDB](#mongodb)
  - [MongoDB Official Documentation](#mongodb-official-documentation)
- [Mongoose](#mongoose)
  - [Mongoose Official Documentation](#mongoose-official-documentation)
- [CRUD Operations](#crud-operations)
- [Connecting MongoDB to Node.js](#connecting-mongodb-to-nodejs)
- [Creating a Simple Login Page](#creating-a-simple-login-page)

## Introduction

Welcome to Day 2 of Week 3! Today, we will dive into connecting MongoDB and building a web project. MongoDB is a popular NoSQL database used in web development. We'll also start working on your project, applying the knowledge you've gained so far.

## MongoDB

MongoDB is a versatile NoSQL database that allows you to store, manage, and retrieve data in a flexible manner. Here are some resources to get you started:

### MongoDB Official Documentation

- [MongoDB Documentation](https://www.mongodb.com/docs/manual/introduction/): Explore comprehensive documentation for MongoDB, including installation, CRUD operations, and advanced features.

## Mongoose

Mongoose is an elegant MongoDB object modeling library for Node.js. It simplifies interactions with MongoDB and provides structure to your data models. Learn more about Mongoose:

### Mongoose Official Documentation

- [Mongoose Documentation](https://mongoosejs.com/docs/): Dive into the official documentation for Mongoose to understand how it works and how to use it effectively.



## Connecting MongoDB to Node.js

Connecting MongoDB to your Node.js application is a crucial step. We'll cover how to establish a connection and perform database operations.

```javascript
const mongoose = require('mongoose');

// Replace 'your_database_url' with your actual MongoDB connection string
const databaseUrl = 'mongodb://localhost:27017/your_database_name';

mongoose.connect(databaseUrl, { useNewUrlParser: true, useUnifiedTopology: true });

const db = mongoose.connection;

db.on('error', (error) => {
console.error('MongoDB Connection Error:', error);
});

db.once('open', () => {
console.log('Connected to MongoDB!');
});

```

## CRUD Operations

CRUD (Create, Read, Update, Delete) operations are fundamental to working with databases. You'll learn how to perform these operations with MongoDB and Mongoose.

## Create (C) - Inserting Data

To create new records in MongoDB, you can use the `create` method with Mongoose. Here's an example of adding a new user to a MongoDB collection:

```javascript
const mongoose = require('mongoose');

const userSchema = new mongoose.Schema({
  username: String,
  password: String,
});

const User = mongoose.model('User', userSchema);

const newUser = new User({
  username: 'john_doe',
  password: 'qwe123'
});

newUser.save()
```
## Read (R) - Querying Data

Reading data from MongoDB involves querying the database. With Mongoose, you can use methods like find and findOne to retrieve data. Here's an example of finding all users:

```javascript
User.find({}, (error, users) => {
    console.log('All Users:', users);
});
```
## Update (U) - Modifying Data

Updating data in MongoDB can be done using methods like updateOne or findOneAndUpdate in Mongoose. Below is an example of updating a user's email:

```javascript
User.updateOne({ username: 'john_doe' }, { password: 'abc123' },() => {
      console.log('User updated successfully!')
  }
)
```
## Delete (D) - Removing Data

To delete data, you can use methods like deleteOne or findOneAndDelete in Mongoose. Here's an example of removing a user by their username:

```javascript
User.findOneAndDelete({ username: 'john_doe' }, () => {
    console.log('User deleted successfully!');
});
```

## Creating a Simple Login Page

We'll start building a simple login page for your web project. This is an exciting step toward creating a functional web application.

```javascript
const express = require('express');
const mongoose = require('mongoose');

const app = express();

// Connect to MongoDB (replace 'your_database_url' with your MongoDB connection string)
mongoose.connect('mongodb://localhost/your_database_name', { useNewUrlParser: true, useUnifiedTopology: true });

// Define a User schema and create a model
const userSchema = new mongoose.Schema({
  username: {
    type: String,
    required: true,
    unique: true,
  },
  password: {
    type: String,
    required: true,
  },
});

const User = mongoose.model('User', userSchema);

app.use(express.json());

// Signup route
app.post('/signup', async (req, res) => {

    const { username, password } = req.body;

    // Create a new user
    const newUser = new User({
      username,
      password,
    });

    // Save the user to the database
    await newUser.save();
    console.log('User registered successfully')
});

// Login route
app.post('/login', async (req, res) => {

    const { username, password } = req.body;

    // Find the user by username
    const user = await User.findOne({ username });

    if (!user)
        console.log('Invalid username or password')

    // Compare the provided password with the stored password
    if (password !== user.password)
        console.log('Invalid username or password')

    console.log('Login successful')

});

app.listen(3000, () => {
  console.log('Server started');
});

```
