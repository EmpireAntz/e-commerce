# E-Commerce

## Description

This Node.js application provides a RESTful API for an e-commerce platform, utilizing Sequelize for database management and Express.js for handling HTTP requests. The application facilitates CRUD operations on categories, products, tags, and their relationships.

## Table of Contents
- [Setup and Configuration](#setup-and-configuration)
- [Walkthrough](#walkthrough)
- [Environment Variables](#environment-variables)
- [Database Connection](#database-connection)
- [Express.js Server](#expressjs-server)
- [Dependencies](#dependencies)
- [Installation](#installation)
- [Running the application](#running-the-application)
- [API Endpoints](#api-endpoints)
- [Categories](#categories)
- [Products](#products)
- [Tags](#tags)
- [Contributing](#contributing)

## Setup and Configuration

### Walkthrough
[Click here to view walkthrough link](https://drive.google.com/file/d/1C01R0HDU7BZFDoiDMzKiZRdSrrpeE-2R/view)

### Environment Variables

You need to set up the following environment variables:

- `DB_NAME`: Name of your database
- `DB_USER`: Database username
- `DB_PASSWORD`: Database password

### Database Connection

The application connects to a MySQL database using Sequelize. It supports both local and JawsDB MySQL connections, depending on your environment setup.

### Express.js Server

The server is set up to listen on a specified port and handles JSON and URL-encoded data. It imports and uses the defined routes for categories, products, and tags.

## Dependencies

- Node.js
- Express.js
- Sequelize
- MySQL

## Installation

- Clone the repository:
  ```bash
  git clone [repository URL]
- Install Dependencies:
  ```bash
  npm install
- Create an .env file in the root directory with the necessary environment variables.

## Running the application

- Open MySQL shell:
  ```bash
  mysql -u (user) -p (password)
  ```
- Run this in the shell to connect the schema:
  ```bash
  source /db/schema.sql
  ```
- Run this in the terminal to connect the seeds:
  ```bash
  node /seeds/index.js
  ```
- Run the server:
  ```bash
  node --watch server.js
  ```
  
## API Endpoints

### Categories

- GET /api/categories: Retrieve all categories with their associated products.
- GET /api/categories/:id: Retrieve a specific category by its ID.
- POST /api/categories: Create a new category.
- PUT /api/categories/:id: Update a category by its ID.
- DELETE /api/categories/:id: Delete a category by its ID.

### Products

- GET /api/products: Retrieve all products with their categories and tags.
- GET /api/products/:id: Retrieve a specific product by its ID.
- POST /api/products: Create a new product.
- PUT /api/products/:id: Update a product by its ID.
- DELETE /api/products/:id: Delete a product by its ID.

### Tags

- GET /api/tags: Retrieve all tags with their associated products.
- GET /api/tags/:id: Retrieve a specific tag by its ID.
- POST /api/tags: Create a new tag.
- PUT /api/tags/:id: Update a tag by its ID.
- DELETE /api/tags/:id: Delete a tag by its ID.

## Contributing

Contributions to the project are welcome. Please follow the standard fork-and-pull request workflow.