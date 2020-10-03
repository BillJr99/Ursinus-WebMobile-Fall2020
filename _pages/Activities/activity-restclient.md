---
layout: activity
permalink: /Activities/ServiceClient
title: "Web and Mobile Development - RESTful Service Client"
excerpt: "Web and Mobile Development - RESTful Service Client"

info:
  goals: 
    - To explore Representational State Transfer (REST) as applied to HTTP web calls
    - To use OAuth to enable user authentication when interacting with a RESTful web service
  models:
    - model: |
        <iframe src="http://thecodebarbarian.com/github-oauth-login-with-node-js.html" width="100%" height="1068" scrolling="yes"></iframe>
      title: RESTful Service Clients
      questions:
        - "Using the <a href=\"http://thecodebarbarian.com/github-oauth-login-with-node-js.html\">tutorial above</a>, write a program to support OAuth login to GitHub, writing a web service using express to capture the callback with the user's token."
        - How could we use this token in place of a user account when developing our own web services?  How could we associate a user with a token, while ensuring that subsequent tokens for the same user are also associated with that same user?  In other words, how can we ensure that not just any valid GitHub user can masquerade as a user on our eventual service?
      embed: |
        <iframe height="400px" width="100%" src="https://repl.it/@BillJr99/WeatherClientExample?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>         
        
tags:
  - rest
  
---

