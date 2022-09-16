
# Object-Relational-Mapping-ORM-E-Commerce-Back-End

![GitHub License Badge](https://shields.io/badge/license-MIT-green)

## Description

Internet retail, also known as e-commerce, is the largest sector of the electronics industry, generating an estimated $29 trillion in 2019. E-commerce platforms like Shopify and WooCommerce provide a suite of services to businesses of all sizes. Due to their prevalence, understanding the fundamental architecture of these platforms will benefit a full-stack web developer.

### User Story

As a manager at an internet retail company
I want a back end for my e-commerce website that uses the latest technologies
so that my company can compete with other e-commerce companies

### Task

Build the back end for an e-commerce site by modifying starter code. You’ll configure a working Express.js API to use Sequelize to interact with a MySQL database.


## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Credits](#credits)
- [Features](#features)
- [Test](#test)
- [License](#license)

## Installation

The appropriate packages consists of

- npm i
- npm init
- npm install mysql2
- npm install doetenv
- npm install express

## Dependencies

```
"dependencies": {
    "dotenv": "^8.2.0",
    "express": "^4.17.1",
    "mysql2": "^2.2.1",
    "sequelize": "^6.3.5"
  }
```



### Database Models

database should contain the following four models, including the requirements listed for each model:

- `Category`

  - `id`

    - Integer.

    - Doesn't allow null values.

    - Set as primary key.

    - Uses auto increment.

  - `category_name`

    - String.

    - Doesn't allow null values.

- `Product`

  - `id`

    - Integer.

    - Doesn't allow null values.

    - Set as primary key.

    - Uses auto increment.

  - `product_name`

    - String.

    - Doesn't allow null values.

  - `price`

    - Decimal.

    - Doesn't allow null values.

    - Validates that the value is a decimal.

  - `stock`

    - Integer.

    - Doesn't allow null values.

    - Set a default value of `10`.

    - Validates that the value is numeric.

  - `category_id`

    - Integer.

    - References the `Category` model's `id`.

- `Tag`

  - `id`

    - Integer.

    - Doesn't allow null values.

    - Set as primary key.

    - Uses auto increment.

  - `tag_name`

    - String.

- `ProductTag`

  - `id`

    - Integer.

    - Doesn't allow null values.

    - Set as primary key.

    - Uses auto increment.

  - `product_id`

    - Integer.

    - References the `Product` model's `id`.

  - `tag_id`

    - Integer.

    - References the `Tag` model's `id`.

 ### Classes

In Product.js initialize Product model (table) by extending off Sequelize's Model class

```
class Product extends Model {}
```

In Category.js initialize Category model (table) by extending off Sequelize's Model class

```
class Category extends Model {}
```

In ProductTag.js initialize ProductTag. model (table) by extending off Sequelize's Model class

```
class ProductTag extends Model {}

```

In Tag.js initialize Tag. model (table) by extending off Sequelize's Model class

```
class Tag extends Model {}
```

The seeds directory contains a seed for category, product, product-tag, tag, and index.js.

-- After running the

```
 npm run seeds

```

command the ecommerce_db in mysql workbench was seeded and verified on mysql workbench.


## Associations

In the index.js file of models directory the associations were created with these methods `belongsTo`, `hasMany`, `belongsToMany` were used to associate the appropriate tables

## Video

Insomnia Walk Through


[![Insomnia Back End Walk Through ](http://img.youtube.com/vi/xQemFWT0NO8/0.jpg)](https://youtu.be/7jeuOJdRFZE "Ecommerce Code Walk through")

---




## Credits

https://sqlbolt.com/lesson/select_queries_introduction

https://guides.github.com/features/mastering-markdown/

https://sequelize.org/master/manual/model-querying-finders.html




## Acceptance Criteria

- A functional Express.js API will add my database name, MySQL username, and MySQL password to an environment variable file.

- I am able to connect to a database using Sequelize

- I enter schema and seed commands

- A development database is created and is seeded with test data

- I enter the command to invoke the application and my server is started and the Sequelize models are synced to the MySQL database

- Open API GET routes in Insomnia Core for categories, products, or tags and the data for each of these routes is displayed in a formatted JSON

- Test API POST, PUT, and DELETE routes in Insomnia Core and successfully create, update, and delete data in my database


## Tests

No testing on this app



## Attribution

[homepage]: https://www.contributor-covenant.org
[v2.0]: https://www.contributor-covenant.org/version/2/0/code_of_conduct.html
[mozilla coc]: https://github.com/mozilla/diversity
[faq]: https://www.contributor-covenant.org/faq
[translations]: https://www.contributor-covenant.org/translations

## License

![GitHub License Badge](https://shields.io/badge/license-MIT-green)

Copyright (c) [2022] [Duc Dang]


## Questions

### Contact:

Github: [https://github.com/simpmind](https://github.com/simpmind)

Email: <tengfai97@gmail.com>
