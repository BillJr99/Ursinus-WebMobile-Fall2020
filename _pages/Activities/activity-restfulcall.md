---
layout: activity
permalink: /Activities/RESTfulCalls
title: "Web and Mobile Development - RESTful Calls"
excerpt: "Web and Mobile Development - RESTful Calls"

info:
  goals: 
    - To explore Representational State Transfer (REST) as applied to HTTP web calls
    - To articulate the basic RESTful operations and map those to HTTP standard verbs
    - To identify arrays of objects, and elements within objects, of JSON structures
  models:
    - model: |
        <a href="https://twitter.com/NSF/status/1299367852374450185">https://twitter.com/NSF/status/1299367852374450185</a>
      title: RESTful Resources
      questions:
        - What part of the URL represents the tweet ID?
        - How do we know which user made that tweet?
        - What CRUD verb do you think is executed on this URL (Create, Read, Update, Delete)?
        - What HTTP verb do you think is executed (POST, PUT, DELETE)?
        - What is the noun in this transaction?
        - What changes in the URL if we want to get a different tweet from the same user?
    - model: | 
        <img src="../images/restfulexchange.png" alt="A RESTful Exchange Diagram">
      title: RESTful Exchanges
      questions:
        - Modify the program to print out the length of daylight (between sunrise and sunset) in hours, minutes, and seconds.  Note that the sunrise and sunset times are given in Unix epoch time, which is the number of seconds that have elapsed since January 1, 1970.
      embed: |
        <iframe height="400px" width="100%" src="https://repl.it/@BillJr99/WeatherClientExample?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>  
    - model: |
        <iframe src="https://api.weatherusa.net/v1/forecast?q=40.1915,-75.4559&daily=0&units=e&maxtime=7d" width="100%"></iframe>
        <br>
        <code>
        jsonobj.forEach(function(obj) {
            console.log(obj.field_name);
        });
        </code>
      title: JSON Objects
      questions:
        - "This JSON result was returned from a web request to <a href=\"https://api.weatherusa.net/v1/forecast?q=40.1915,-75.4559&daily=0&units=e&maxtime=7d\">https://api.weatherusa.net/v1/forecast?q=40.1915,-75.4559&daily=0&units=e&maxtime=7d</a>, which obtains the 7-day forecast at Ursinus College given the College's latitude and longitude GPS coordinates.  Use a <a href=\"https://jsonformatter.org/json-pretty-print\">JSON Pretty Printer</a> to better format the JSON for reading."
        - What do the curly braces represent?
        - What does the square bracket represent?
        - Modify the program above to access this RESTful endpoint and, in a loop, print out each day's date (using <code>validt</code>) and temperature. An example <code>for</code> loop in <a href=\"https://www.w3schools.com/js/js_json_arrays.asp\">JavaScript</a> is given above.
    - model: |
        <code>
        {
            "response": {
                "version": "0.1",
                "termsofService": "http://www.wunderground.com/weather/api/d/terms.html",
                "features": {
                    "conditions": 1
                }
            },
            "current_observation": {
                "image": {
                    "url": "http://icons-ak.wxug.com/graphics/wu2/logo_130x80.png",
                    "title": "Weather Underground",
                    "link": "http://www.wunderground.com"
                },
                "display_location": {
                    "city": "Philadelphia",
                    "state": "PA",
                    "zip": "19104",
                    "latitude": "39.96150970",
                    "longitude": "-75.19716644",
                    "elevation": "41.00000000"
                },
                "observation_location": {
                    "full": "University City - West Philadelphia, Philadelphia, Pennsylvania",
                    "city": "University City - West Philadelphia, Philadelphia",
                    "state": "Pennsylvania",
                    "latitude": "39.950554",
                    "longitude": "-75.211868",
                    "elevation": "70 ft"
                },
              "temp_f": 76.5,      
            }
        }
        </code>
      title: A Sample JSON Response
      questions:
        - "What is the path to <code>longitude</code>?"
        - "What is the path to <code>temp_f</code>?"
    - model: |
        <code>
        "forecast": {
            "txt_forecast": {
                "date": "5:00 PM EDT",
                "forecastday": [
                    {
                        "period": 0,
                        "icon": "tstorms",
                        "icon_url": "http://icons-ak.wxug.com/i/c/k/tstorms.gif",
                        "title": "Sunday",
                        "fcttext": "Mostly cloudy with thunderstorms and rain showers. High of 88F. Winds from the SSW at 5 to 15 mph. Chance of rain 30%.",
                        "fcttext_metric": "Mostly cloudy with thunderstorms and rain showers. High of 31C. Breezy. Winds from the SSW at 10 to 20 km/h. Chance of rain 30%.",
                        "pop": "30"
                    }
                 ]
        }
        </code>
      title: A Sample JSON Array Response
      questions:
        - "What is the path to the first <code>fcttext</code> element?"
        
tags:
  - rest
  
---

