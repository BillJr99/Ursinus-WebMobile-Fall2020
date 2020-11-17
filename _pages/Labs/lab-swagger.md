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

In this lab, you will document a web service using [Swagger](https://swagger.io/docs/specification/2-0/basic-structure/).

You can add a Swagger renderer to your web service via:

```javascript
const swaggerUi = require("swagger-ui-express");
```

You can then document your data schema using a JSON structure:

```javascript
const swaggerDocument = {
   "swagger":"2.0",
   "info":{
      "title":"Example Item API",
      "description":"Insert and retrieve items from a datastore",
      "version":1.0
   },
   "host":"localhost",
   "basePath":"/api/v1",
   "schemes":[
      "http"
   ],
   "tags":[
      "Items"
   ],
   "components":{
      "schemas":{
         "ItemSchema":{
            "type":"object",
            "required":[
               "name",
               "price"
            ],
            "properties":{
               "name":{
                  "type":"string",
                  "example":"First Last"
               },
               "price":{
                  "type":"number",
                  "example":1.99
               },
               "status":{
                  "type":"string",
                  "example":"taxable"
               }
            }
         }
      }
   },
   "paths":{
      "/items":{
         "get":{
            "description":"Get all items from the datastore",
            "responses":{
               "200":{
                  "description":"A list of items",
                  "content":{
                     "application/json":{
                        "schema":{
                           "type":"array",
                           "items":{
                              "$ref":"#/components/schemas/ItemSchema"
                           }
                        }
                     }
                  }
               }
            }
         }"post":{
            "summary":"Create an item",
            "consumes":"application/json",
            "parameters":[
               {
                  "in":"body",
                  "name":"item",
                  "description":"item",
                  "schema":{
                     "type":"object",
                     "$ref":"#/components/schemas/ItemSchema"
                  }
               }
            ],
            "responses":{
               "200":{
                  "description":"Created Item",
                  "content":{
                     "application/json":{
                        "type":"object",
                        "item":{
                           "$ref":"#/components/schemas/ItemSchema"
                        }
                     }
                  }
               }
            }
         }
      }
   }
}
```

You can instantiate a path to your Swagger document as follows, which you can access at your usual URL with `/api/doc` appended to the end (as configured below):

```javascript
app.use('/api/doc', swaggerUi.serve, swaggerUi.setup(swaggerDocument));
```

You can even document your authentication paths, such as OAuth!  [See here for additional description of documentation structures supported by Swagger.](https://levelup.gitconnected.com/the-simplest-way-to-add-swagger-to-a-node-js-project-c2a4aa895a3c)

Here is a minimal working example:

<iframe height="800px" width="100%" src="https://repl.it/@BillJr99/SwaggerExample?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>  

## Part 1: Adding Swagger Documentation

Add Swagger documentation to one of your assignments or labs, and take a screenshot of the `/api/doc` page that is served when you run the project.