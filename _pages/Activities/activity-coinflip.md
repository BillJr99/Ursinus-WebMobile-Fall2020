---
layout: activity
permalink: /Activities/CoinFlip
title: "Web and Mobile Development - Peruvian Coin Flip"
excerpt: "Web and Mobile Development - Peruvian Coin Flip"

info:
  goals: 
    - To establish trust with unknown parties using a model algorithm (inspired by <a href=\"https://classic.csunplugged.org/wp-content/uploads/2014/12/unplugged-17-cryptographic_protocols_0.pdf\">CSUnplugged</a>)
  models:
    - model: |
        <button id="click" type="button">Coin Toss</button> <span id="result"></span>
        
        <script>
            // https://stackoverflow.com/questions/32302066/coin-toss-with-javascript-and-html
            document.getElementById('click').onclick = click;

            var heads = 0;
            var tails = 0;
            function click() {  
                x = (Math.floor(Math.random() * 2) == 0);
                if(x){
                    flip("heads");
                }else{
                    flip("tails");
                }
            };
            function flip(coin) {
                document.getElementById("result").innerHTML = coin;
            };
        </script>
      title: Flipping a Coin
      questions:
        - test

tags:
  - cryptographic
  
---

