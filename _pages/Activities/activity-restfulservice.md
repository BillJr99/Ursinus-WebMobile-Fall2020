---
layout: activity
permalink: /Activities/RESTfulService
title: "Web and Mobile Development - RESTful Services"
excerpt: "Web and Mobile Development - RESTful Services"

info:
  goals: 
    - To explore Representational State Transfer (REST) service providers
    - To explain the mapping of RESTful verbs onto the HTTP verbs GET, PUT, POST, and DELETE
    - To explain how stateless HTTP calls can be used to establish state with a client
  models:
    - model: |
        <img src="../images/examples/restfulserviceexample/postman-restserviceexample.png" alt="Posting with form parameters">
        <br>
        <img src="../images/examples/restfulserviceexample/postman-restserviceexample-contenttype-applicationjson.png" alt="Posting with application/json Content-Type">
        <br>
        <img src="../images/examples/restfulserviceexample/postman-restserviceexample-get.png" alt="A GET request">
        <br>
        <img src="../images/examples/restfulserviceexample/mongodb-restserviceexample.png" alt="The data store after posting data">
        <br>
        <img src="../images/examples/restfulserviceexample/curl-restserviceexample.png" alt="Posting with cURL from the console">
        <br>
        <img src="../images/examples/restfulserviceexample/curl-restserviceexample-postputget.png" alt="Performing an update with cURL">
        <br>
      title: RESTful Service
      embed: <iframe height="400px" width="100%" src="https://repl.it/@BillJr99/RESTfulServiceExample?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>  
      questions:
        - "Launch the given web service and invoke it using your choice of web client.  To do this, you will want to set up a <a href=\"http://mongodb.com\">mongodb</a> database, add a test user with a password, and allow access from any IP address.  MongoDB will give you a connection string that you can paste into <code>index.js</code> over my default <code>test_user</code> connection string."
        - Invoke the service using a node.js application or a JavaScript browser client.
        - What HTTP verb is used to create a new item?  To retrieve an item?  To update an item?  To delete an item?
        - Why is POST used to create items while PUT is used to update them?  Aren't these interchangeable?
        - "What if you wanted to support other verbs on these items, like <code>putOnSale</code>?  Are service endpoints typically nouns or verbs, and how might you re-work a sale verb like this one into an appropriate CRUD endpoint?"
        - What is the advantage of separating your code into a model and a controller implementation?
        
tags:
  - rest
  
---

