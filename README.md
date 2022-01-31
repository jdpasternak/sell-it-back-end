# SellIt Back End

## Table of Contents

## Description

SellIt Back End is an e-commerce API server written on Express.js that uses Sequelize as an ORM to connected to a MySQL database.

## Installation

### Prerequisites

- MySQL server if installed locally, or JawsDB if deploying to Heroku

### Steps

1. Download the source code or clone it to an empty directory.
2. In the root of the downloaded code, open a console, type `npm install`, then press `Enter` to install dependecies.
3. In a MySQL console, type `source db/schema.sql`, then press `Enter`. (backslash `\` if on Windows)
4. In the original console window, type `npm run seed`, and press `Enter` to seed the database.
5. Type `npm run start` and press `Enter` to start the server.

## Usage

## Walkthrough

The video below demonstrates how to use this application.

[![walkthrough first frame](assets/images/walkthrough/walkthrough.png)](https://jdpasternak.github.io/sell-it-back-end)

### API Endpoints

The following describes available API endpoints.

#### /api/categories

`GET /api/categories` -> returns all categories
`GET /api/categories/<id>` -> returns a category with the given ID
`POST /api/categories` -> creates a new category. Expects `category_name`, a string, in the body.
`PUT /api/categories/<id>` -> updates a category with the given ID. Expects `category_name`, a string, in the body.
`DELETE /api/categories/<id>` -> deletes a category with the given ID

#### /api/products

`GET /api/products` -> returns all products
`GET /api/products/<id>` -> returns a product with the given ID
`POST /api/products` -> creates a new product. Expects the following in the body:

- `product_name`, a string
- `price`, a decimal
- `stock`, an integer
- `category_id`, an integer
- `tagIds`, an array of integers

`PUT /api/products/<id>` -> updates a product with the given ID. Expects the following in the body:

- `product_name`, a string
- `price`, a decimal
- `stock`, an integer
- `category_id`, an integer
- `tagIds`, an array of integers

`DELETE /api/products/<id>` -> deletes a product with the given ID

#### /api/tags

`GET /api/tags` -> returns all tags
`GET /api/tags/<id>` -> returns a tag with the given ID
`POST /api/tags` -> creates a new tag. Expects `tag_name`, a string, in the body.
`PUT /api/tags/<id>` -> updates a tag with the given ID. Expects `tag_name`, a string, in the body.
`DELETE /api/tags/<id>` -> deletes a tag with the given ID
