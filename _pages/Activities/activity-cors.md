---
layout: activity
permalink: /Activities/CORS
title: "Web and Mobile Development - Cross-Origin Resource Sharing"
excerpt: "Web and Mobile Development - Cross-Origin Resource Sharing"

info:
  goals: 
    - To explain why CORS is necessary
    - To enable CORS on a per-domain basis
  models:
    - model: |
        <a title="Bluesmoon / CC BY-SA (https://creativecommons.org/licenses/by-sa/4.0)" href="https://commons.wikimedia.org/wiki/File:Flowchart_showing_Simple_and_Preflight_XHR.svg"><img width="512" alt="Flowchart showing Simple and Preflight XHR" src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/ca/Flowchart_showing_Simple_and_Preflight_XHR.svg/512px-Flowchart_showing_Simple_and_Preflight_XHR.svg.png"></a>
      title: CORS
      questions:
        - When accessing a resource from a web browser, like posting to a form on another server, you may receive a Cross-Domain error from your browser.  What header can you set to enable CORS?
        - How does the header change if you are enabling access to one or more specific hosts, rather than any?
    - model: |
        <div align="left">
        <pre>
        <code>
        // From: https://expressjs.com/en/resources/middleware/cors.html
        // Shared under a Creative Commons BY-SA license: http://creativecommons.org/licenses/by-sa/3.0/us/
        var express = require('express')
        var cors = require('cors')
        var app = express()

        var allowlist = ['http://example1.com', 'http://example2.com']
        var corsOptionsDelegate = function (req, callback) {
          var corsOptions;
          if (allowlist.indexOf(req.header('Origin')) !== -1) {
            corsOptions = { origin: true } // reflect (enable) the requested origin in the CORS response
          } else {
            corsOptions = { origin: false } // disable CORS for this request
          }
          callback(null, corsOptions) // callback expects two parameters: error and options
        }

        app.get('/products/:id', cors(corsOptionsDelegate), function (req, res, next) {
          res.json({msg: 'This is CORS-enabled for an allowed domain.'})
        })

        app.listen(80, function () {
          console.log('CORS-enabled web server listening on port 80')
        })
        </code>
        </pre>
        </div>
      title: CORS
      questions:
        - What functions are called when an endpoint is accessed to verify CORS for a particular host?
        - In what variable of the web request object can the accessing hostname be found?
        
tags:
  - cors
  
---

