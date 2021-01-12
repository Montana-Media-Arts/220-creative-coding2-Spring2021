---
title: Working with Variables
module: 2
jotted: false
---

# Working with Variables

So, how do we work with variables?  One of the ways we can do this by using the setup and draw to help update a variable.

```js
    var counter = 0;
    var x = 100;
    var y = 100;
    var diameter = 25;
    function setup()
    {
        createCanvas(800,600);
    }
    function draw()
    {
        background(0);
        fill(counter,200,29);
        circle(x,y,diameter);
        counter++;
    }

```

