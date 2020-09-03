---
layout: assignment
permalink: /Labs/Swagger
title: "Web and Mobile Development: Swagger"
excerpt: "Web and Mobile Development: Swagger"

info:
  coursenum: CS471
  githubclassroom:
    clonelink: https://classroom.github.com/a/OgaLKaBL
  points: 100
  goals:
    - To document web services in node.js using Swagger
  rubric:
    - weight: 90
      description: Code Quality and Documentation
      preemerging: Code commenting and structure are absent, or code structure departs significantly from best practice, and/or the code departs significantly from the style guide
      beginning: Code commenting and structure is limited in ways that reduce the readability of the program, and/or there are minor departures from the style guide
      progressing: Code documentation is present that re-states the explicit code definitions, and/or code is written that mostly adheres to the style guide
      proficient: Code is documented at non-trivial points in a manner that enhances the readability of the program, and code is written according to the style guide
    - weight: 10
      description: Writeup and Submission
      preemerging: An incomplete submission is provided
      beginning: The program is submitted, but not according to the directions in one or more ways (for example, because it is lacking a readme writeup)
      progressing: The program is submitted according to the directions with a minor omission or correction needed
      proficient: The program is submitted according to the directions, including a readme writeup describing the solution

tags:
  - documentation
  
---

In this lab, you will document a web service using [Swagger](https://levelup.gitconnected.com/swagger-time-to-document-that-express-api-you-built-9b8faaeae563).

You can add a Swagger router via:

```javascript
const swaggerJsdoc = require(“swagger-jsdoc”);
const swaggerUi = require(“swagger-ui-express”);
router.get("/docs", swaggerUi.setup(specs, { explorer: true }));
```

with basic options as defined [here](https://gist.githubusercontent.com/AlexanderKaran/bb1025d02190a917795a6942dcab92ac/raw/6500cef951dced2da0c4fe12a60a459162dba4b0/Time%20to%20document%20that%20Express%20API%20you%C2%A0built:%20Swagger%20set%20up).

You can then document your data schema using a Javadoc-like syntax:

```javascript
/**
 * @swagger
 *   components:
 *    <your object type>:
 *      type: object
 *      required:
 *        - list
 *        - of
 *        - elements
 *        - name
 *      properties:
 *        name:
 *          type: string
 *          description: Description here
 *        ...
 *      example:
 *        name: Alex
 *        ...
 */
```
which you can access at your usual URL with `/docs` appended to the end.

Similarly, you can document each of your routes (notice the references to the schema definitions above):

```javascript
/**
 * @swagger
 *   path:
 *    /<your path>/:
 *      post:
 *        summary: Create an element
 *        requestBody:
 *          required: true
 *          content:
 *            application/json:
 *          schema:
 *            $ref: '#/components/schemas/<YOUR OBJECT TYPE>'
 *        responses:
 *          "200":
 *            description: "A new item"
 *            content:
 *              application/json:
 *                schema:
 *                  $ref: '#/components/schemas/<YOUR OBJECT TYPE>'         
 */
```

## Part 1: Adding Swagger Documentation

Add Swagger documentation to one of your assignments or labs, and take a screenshot of the `/docs` page that is served when you run the project.